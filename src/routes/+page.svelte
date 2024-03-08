<script>
    let showWalletAddress = false;

    function toggleWalletAddress() {
      showWalletAddress = !showWalletAddress;
    }
</script>

<style>
  /* Base and mobile styles */
  body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
  }
  .navbar {
    background-color: #333;
    color: white;
    padding: 1rem;
    text-align: center;
  }
  .navbar a {
    color: white;
    padding: 0 15px;
    text-decoration: none;
  }
  .hero {
    padding: 2rem;
    text-align: center;
  }
  .services {
    display: flex;
    flex-direction: column;
    padding: 2rem;
  }
  .service {
    background-color: #e7e7e7;
    padding: 1rem;
    margin-bottom: 1rem;
  }
  .about,
  .contact {
    padding: 2rem;
    text-align: center;
  }
  footer {
    background-color: #0088ff;
    color: white;
    text-align: center;
    padding: 1rem;
    border-radius: 0.3rem;
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
</style>

<div class="navbar">
  <a href="#services">Services</a>
  <a href="#about">About Us</a>
  <a href="#contact">Contact</a>
</div>

<div class="hero">
  <h1>Welcome to Validator Node Management</h1>
  <p>Professionals in blockchain validator node management and maintenance.</p>
</div>

<div class="services" id="services">
  <div class="card" style="width: 18rem;">
    <img class="card-img-top" src="/myria.png?url" alt="Card image cap">
    <div class="card-body">
      <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    </div>
  </div>
  <div class="service">
    <h2>Ethereum 2.0</h2>
    <p>Management and maintenance services for Ethereum 2.0 validator nodes.</p>
  </div>
  <div class="service">
    <h2>Polkadot</h2>
    <p>Full support for Polkadot network nodes, including updates and monitoring.</p>
  </div>
  <div class="service">
    <h2>Cosmos</h2>
    <p>Monitoring and management services to ensure the efficiency of your Cosmos nodes.</p>
  </div>
</div>

<div class="about" id="about">
  <h2>About Us</h2>
  <p>We are a team of blockchain experts dedicated to providing high-quality solutions for validator node management.</p>
</div>

<div class="contact" id="contact">
  <h2>Contact</h2>
  <p>Interested in our services? Fill out the form below or send us an email at contact@validatornode.management.</p>
  <!-- You can add a contact form here -->
</div>

<div class="payment-section">
  <h2>Payments</h2>
  <p>If you would like to make a payment, please use the cryptocurrency wallet address below.</p>
  <button on:click={toggleWalletAddress}>
    {showWalletAddress ? 'Hide Wallet Address' : 'Show Wallet Address'}
  </button>
  <div class="wallet-address" class:show={showWalletAddress}>
    <p><strong>Wallet Address:</strong> 0x123456789ABCDEF123456789ABCDEF1234567890</p>
  </div>
</div>

<footer>
  <p>Validator Node Management &copy; 2023</p>
</footer>