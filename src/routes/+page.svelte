<script>
    import { goto } from '$app/navigation';

    const formUrl = './buy';

    function navigateForm() {
        goto(formUrl)
    }
</script>

<div class="navbar">
    <a href="#services">Services</a>
    <a href="#about">About Us</a>
    <a href="#contact">Contact</a>
</div>

<div class="hero">
</div>

<div class="services" id="services">
    <h2 class="services-title">Our Services</h2>
    <div class="card service" style="width: 18rem;">
        <img class="card-img-top" src="/myria.png?url" alt="Card image cap" />
        <div class="card-body">
            <h3 class="card-title">Myria</h3>
            <p class="card-text">
                Some quick example text to build on the card title and make up
                the bulk of the card's content.
            </p>
            <button on:click={navigateForm}>Buy service</button>
        </div>
    </div>
    <div class="card service" style="width: 18rem;">
        <img
            class="card-img-top"
            src="/celestia.svg?url"
            alt="Card image cap"
        />
        <div class="card-body">
            <h3 class="card-title">Celestia</h3>
            <p class="card-text">
                Some quick example text to build on the card title and make up
                the bulk of the card's content.
            </p>
            <button on:click={navigateForm}>Buy service</button>
        </div>
    </div>
    <div class="card service" style="width: 18rem;">
        <img class="card-img-top" src="/shardeum.svg?url" alt="Shardeum logo" />
        <div class="card-body">
            <h3 class="card-title">Shardeum</h3>
            <p class="card-text">
                Some quick example text to build on the card title and make up
                the bulk of the card's content.
            </p>
            <button on:click={navigateForm}>Buy service</button>
        </div>
    </div>
    <div class="card service" style="width: 18rem;">
        <img class="card-img-top" src="/xai.svg?url" alt="Card image cap" />
        <div class="card-body">
            <h3 class="card-title">Xai</h3>
            <p class="card-text">
                Some quick example text to build on the card title and make up
                the bulk of the card's content.
            </p>
            <button on:click={navigateForm}>Buy service</button>
        </div>
    </div>
</div>

<div class="about" id="about">
    <h2>About Us</h2>
    <p>
        We are a team of blockchain experts dedicated to providing high-quality
        solutions for validator node management.
    </p>
</div>

<div class="contact" id="contact">
    <h2>Contact</h2>
    <p>
        Interested in our services? Fill out the form below or send us an email
        at contact@validatornode.management.
    </p>
    <!-- You can add a contact form here -->
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
    .hero {
        background-image: url('/nodecraft.jpeg?url');
        padding-bottom: 1.5rem;
        text-align: center;
        background-size: cover; /* Esto asegura que la imagen cubra todo el div */
        background-position: center; /* Centra la imagen en el div */
        background-repeat: no-repeat; /* Evita que la imagen se repita */
        height: 530px; /* Establece una altura para tu div */
        max-height: 530px; /* Establece una altura para tu div */
        width: 100%;
    }
    .services {
        display: flex;
        flex-direction: column;
        padding: 1rem;
        background-color: #1b1f2b;
    }
    button {
      box-shadow: var(--shadow-elevation-medium);
    }
    .card {
      box-shadow: var(--shadow-elevation-low);
    }
    .service,
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
    .services-title,
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
