<script>
    import Payments from "../components/payments.svelte";
    import { goto } from "$app/navigation";

    const formUrl = "./buy";

    function navigateForm() {
        goto(formUrl);
    }
</script>

<div class="services" id="services">
    <h2 class="services-title">Our Services</h2>
    <div class="services-container">
        <div class="card service">
            <img
                class="card-img-top"
                src="/myria.png?url"
                alt="Card image cap"
            />
            <div class="card-body">
                <h3 class="card-title">Myria</h3>
                <p class="card-text">
                    Ensure your Myria node operates at peak performance with our
                    comprehensive maintenance service. For just $15 per month,
                    we handle updates, monitoring, and troubleshooting to keep
                    your node running smoothly.
                </p>
                <p class="card-text">
                    <strong> Price: $15/month </strong>
                </p>
                <button on:click={navigateForm}>Get Started</button>
            </div>
        </div>
        <div class="card service">
            <img
                class="card-img-top"
                src="/celestia.svg?url"
                alt="Card image cap"
            />
            <div class="card-body">
                <h3 class="card-title">Celestia</h3>
                <p class="card-text">
                    Ensure your Celestia node operates at peak performance with
                    our comprehensive maintenance service. For just $20 per
                    month, we handle updates, monitoring, and troubleshooting to
                    keep your node running smoothly.
                </p>
                <p class="card-text">
                    <strong> Price: $20/month </strong>
                </p>
                <button on:click={navigateForm}>Get Started</button>
            </div>
        </div>
        <div class="card service">
            <img
                class="card-img-top"
                src="/aethir.png?url"
                alt="Shardeum logo"
            />
            <div class="card-body">
                <h3 class="card-title">Aethir</h3>
                <p class="card-text">
                    Ensure your Aethir node operates at peak performance with
                    our comprehensive maintenance service. For just $20 per
                    month, we handle updates, monitoring, and troubleshooting to
                    keep your node running smoothly.
                </p>
                <p class="card-text">
                    <strong> Price: $20/month </strong>
                </p>
                <button on:click={navigateForm}>Get Started</button>
            </div>
        </div>
        <div class="card service">
            <img class="rimg" src="/powerloom.jpg?url" alt="Shardeum logo" />
            <div class="card-body">
                <h3 class="card-title">Powerloom</h3>
                <p class="card-text">
                    Ensure your Powerloom node operates at peak performance with
                    our comprehensive maintenance service. For just $20 per
                    month, we handle updates, monitoring, and troubleshooting to
                    keep your node running smoothly.
                </p>
                <p class="card-text">
                    <strong> Price: $20/month </strong>
                </p>
                <button on:click={navigateForm}>Get Started</button>
            </div>
        </div>
        <div class="card service">
            <img
                class="card-img-top"
                src="/shardeum.svg?url"
                alt="Shardeum logo"
            />
            <div class="card-body">
                <h3 class="card-title">Shardeum</h3>
                <p class="card-text">
                    Ensure your Shardeum node operates at peak performance with
                    our comprehensive maintenance service. For just $12 per
                    month, we handle updates, monitoring, and troubleshooting to
                    keep your node running smoothly.
                </p>
                <p class="card-text">
                    <strong> Price: $12/month </strong>
                </p>
                <button on:click={navigateForm}>Get Started</button>
            </div>
        </div>
        <div class="card service">
            <img class="card-img-top" src="/xai.svg?url" alt="Card image cap" />
            <div class="card-body">
                <h3 class="card-title">Xai</h3>
                <p class="card-text">
                    Ensure your Xai node operates at peak performance with our
                    comprehensive maintenance service. For just $18 per month,
                    we handle updates, monitoring, and troubleshooting to keep
                    your node running smoothly.
                </p>
                <p class="card-text">
                    <strong> Price: $18/month </strong>
                </p>
                <button on:click={navigateForm}>Get Started</button>
            </div>
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

<div class="payments" id="payments">
    <Payments></Payments>
</div>

<div class="contact" id="contact">
    <h2>Contact</h2>
    <p>
        Interested in our services? Fill out the form below or send us an email
        at contact@validatornode.management.
    </p>
    <!-- You can add a contact form here -->
</div>

<style>
    /* Base and mobile styles */
    .rimg {
        border-radius: 50%;
        object-fit: cover;
        margin-top: 1rem;
        max-width: 160px;
        max-height: 160px;
    }
    .services {
        display: flex;
        flex-direction: column;
        padding: 1rem;
        background-color: #1b1f2b;
        align-items: center;
        justify-content: center;
    }
    .services-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 1rem;
    }
    button {
        box-shadow: var(--shadow-elevation-medium);
    }
    .card {
        box-shadow: var(--shadow-elevation-low);
        width: 18rem;
    }
    .card-text {
        font-size: 1rem;
        color: #333;
        margin-bottom: 15px;
    }
    .service,
    .card-body {
        flex: 1;
        min-width: 250px;
        max-width: 18rem;
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
    .payments,
    .about,
    .contact {
        padding: 2rem;
        text-align: center;
        color: white;
        background-color: #1b1f2b;
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
            flex-direction: column;
            align-items: center;
            padding: 7rem;
        }
        .services-title {
            margin-bottom: 2rem;
        }
        .services-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
        .service {
            margin: 0.5rem;
            width: calc(33.333% - 1rem); /* Adjust width for 3 columns */
        }
    }
    :root {
        --shadow-color: 0deg 0% 0%;
        --shadow-elevation-low: 0.9px 0.7px 1.3px
                hsl(var(--shadow-color) / 0.13),
            1.6px 1.2px 2.2px -1.3px hsl(var(--shadow-color) / 0.12),
            4.1px 3px 5.6px -2.7px hsl(var(--shadow-color) / 0.12);
        --shadow-elevation-medium: 0.9px 0.7px 1.3px
                hsl(var(--shadow-color) / 0.13),
            3.2px 2.3px 4.3px -0.9px hsl(var(--shadow-color) / 0.13),
            8.2px 6px 11.2px -1.8px hsl(var(--shadow-color) / 0.13),
            20.3px 14.8px 27.7px -2.7px hsl(var(--shadow-color) / 0.12);
        --shadow-elevation-high: 0.9px 0.7px 1.3px
                hsl(var(--shadow-color) / 0.11),
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
