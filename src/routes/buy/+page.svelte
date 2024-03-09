<script>
    let showWalletAddress = false;

    function toggleWalletAddress() {
        showWalletAddress = !showWalletAddress;
    }
</script>

<div class="navbar">
    <a href="#services">Services</a>
    <a href="#about">About Us</a>
    <a href="#contact">Contact</a>
</div>

<div class="contact" id="contact">
    <h2>Contact</h2>
    <p>
        Interested in our services? Fill out the form below or send us an email
        at contact@validatornode.management.
    </p>

    <div class="payment-section">
        <h2>Payments</h2>
        <p>
            If you would like to make a payment, please use the cryptocurrency
            wallet address below.
        </p>
        <button on:click={toggleWalletAddress}>
            {showWalletAddress ? "Hide Wallet Address" : "Show Wallet Address"}
        </button>
        <div class="wallet-address" class:show={showWalletAddress}>
            <p>
                <strong>Wallet Address:</strong> 0x123456789ABCDEF123456789ABCDEF1234567890
            </p>
        </div>
    </div>
</div>


<footer>
    <p>Nodecraft &copy; 2023</p>
</footer>

<style>
    /* Base and mobile styles */
    body {
        font-family: Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue";
        line-height: 1.6;
        margin-left: 0px;
        padding: 0;
        width: 100%;
    }
    .navbar {
        background-color: #1b1f2b;
        color: white;
        padding: 1rem;
        text-align: center;
    }
    .navbar a {
        color: white;
        padding: 0 15px;
        text-decoration: none;
    }
    button {
      box-shadow: var(--shadow-elevation-medium);
    }
    .card {
      box-shadow: var(--shadow-elevation-low);
    }
    .card-body {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 1rem;
        background-color: #e7e7e7;
        padding: 1rem;
        margin-bottom: 1rem;
    }
    .logo {
        width: 100%;
    }
    .card-img-top {
        margin-top: 1rem;
        max-width: 160px;
        max-height: 160px;
    }
    .about,
    .contact {
        padding: 2rem;
        text-align: center;
        color: white;
        background-color: #1b1f2b;
    }
    footer {
        background-color: #1b1f2b;
        color: white;
        text-align: center;
        padding: 1rem;
    }
    .payment-section {
        background-color: #f8f8f8;
        padding: 2rem;
        text-align: center;
    }
    .wallet-address {
        margin-top: 1rem;
        padding: 1rem;
        background-color: #e7e7e7;
        display: none;
    }
    .show {
        display: block;
    }
    button {
        padding: 0.5rem 1rem;
        margin-top: 1.4rem;
        font-size: 1rem;
        color: #fff;
        background-color: #007bff;
        border: none;
        border-radius: 0.3rem;
        cursor: pointer;
        outline: none;
    }
    button:hover {
        background-color: #0056b3;
    }

    /* Styles for tablets and desktop */
    @media (min-width: 768px) {
        .services {
            flex-direction: row;
            justify-content: space-between;
        }
        .service {
            width: 30%;
            margin-bottom: 0;
        }
    }
    :root {
      --shadow-color: 0deg 0% 0%;
      --shadow-elevation-low:
        0.9px 0.7px 1.3px hsl(var(--shadow-color) / 0.13),
        1.6px 1.2px 2.2px -1.3px hsl(var(--shadow-color) / 0.12),
        4.1px 3px 5.6px -2.7px hsl(var(--shadow-color) / 0.12);
      --shadow-elevation-medium:
        0.9px 0.7px 1.3px hsl(var(--shadow-color) / 0.13),
        3.2px 2.3px 4.3px -0.9px hsl(var(--shadow-color) / 0.13),
        8.2px 6px 11.2px -1.8px hsl(var(--shadow-color) / 0.13),
        20.3px 14.8px 27.7px -2.7px hsl(var(--shadow-color) / 0.12);
      --shadow-elevation-high:
        0.9px 0.7px 1.3px hsl(var(--shadow-color) / 0.11),
        5.3px 3.9px 7.3px -0.3px hsl(var(--shadow-color) / 0.11),
        9.8px 7.1px 13.3px -0.7px hsl(var(--shadow-color) / 0.11),
        15.6px 11.4px 21.3px -1px hsl(var(--shadow-color) / 0.11),
        24px 17.5px 32.7px -1.3px hsl(var(--shadow-color) / 0.11),
        36.3px 26.5px 49.6px -1.7px hsl(var(--shadow-color) / 0.1),
        53.8px 39.3px 73.5px -2px hsl(var(--shadow-color) / 0.1),
        77.6px 56.7px 106px -2.3px hsl(var(--shadow-color) / 0.1),
        109.2px 79.7px 149px -2.7px hsl(var(--shadow-color) / 0.1);
    }
</style>
