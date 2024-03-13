<script>
  let walletAddress = '0x48907b323130a9056b9b5B88F889AAaAB7E7Dcc1';

  function copyToClipboard() {
    const textarea = document.createElement('textarea');
    textarea.value = walletAddress;
    document.body.appendChild(textarea);
    textarea.select();
    document.execCommand('copy');
    document.body.removeChild(textarea);
  }

  let showWalletAddress = false;

  function toggleWalletAddress() {
    showWalletAddress = !showWalletAddress;
  }
</script>

<div class="payment-section">
    <h2>Make a Payment</h2>
    <p>
        To proceed with a payment, kindly use the cryptocurrency wallet address provided below.
    </p>
    <button on:click={toggleWalletAddress} class="toggle-button">
        {showWalletAddress ? "Hide Wallet Address" : "Show Payment Address"}
    </button>
    {#if showWalletAddress}
    <div class="wallet-address-container">
        <img class="wallet-qr" src="/walletQR.png" alt="Wallet QR Code" />
        <p class="wallet-label"><strong>Wallet Address:</strong></p>
        <div class="wallet-and-copy">
          <textarea class="wallet-address" readonly>{walletAddress}</textarea>
          <button on:click={copyToClipboard} class="copy-button">Copy</button>
        </div>
    </div>
    {/if}
</div>

<style>
    .payment-section {
        background-color: #f8f9fa;
        padding: 2rem;
        text-align: center;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        color: #333;
        max-width: 500px;
        margin: auto;
    }
    h2 {
        color: #007bff;
        margin-bottom: 1rem;
    }
    .toggle-button {
        padding: 0.5rem 1rem;
        margin-top: 1rem;
        font-size: 1rem;
        color: #fff;
        background-color: #007bff;
        border: none;
        border-radius: 0.3rem;
        cursor: pointer;
        outline: none;
        transition: background-color 0.3s ease;
    }
    .toggle-button:hover {
        background-color: #0056b3;
    }
    .wallet-address-container {
        margin-top: 1rem;
        padding: 1rem;
        background-color: #fff;
        border-radius: 8px;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }
    .wallet-qr {
        max-width: 100px;
        margin-bottom: 1rem;
    }
    .wallet-label {
        margin-bottom: 0.5rem;
    }
    .wallet-and-copy {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .wallet-address {
        flex-grow: 1;
        margin-right: 0.5rem;
        padding: 0.5rem;
        border: 1px solid #ccc;
        border-radius: 4px;
        font-family: monospace;
        background-color: #e9ecef;
        resize: none;
    }
    .copy-button {
        padding: 0.5rem 1rem;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        background-color: #28a745;
        color: white;
        transition: background-color 0.3s ease;
    }
    .copy-button:hover {
        background-color: #218838;
    }
    @media (max-width: 768px) {
        .wallet-and-copy {
            flex-direction: column;
            align-items: stretch;
        }
        .wallet-address {
            margin-right: 0;
            margin-bottom: 0.5rem;
        }
        .copy-button {
            width: 100%; /* Hace que el botón de copia se ajuste al contenedor */
        }
        .wallet-qr {
            margin: auto; /* Centra la imagen del QR en dispositivos móviles */
            margin-bottom: 1rem;
        }
    }
</style>