<script>
    let name = "";
    let email = "";
    let txid = "";
    let message = "";

    async function handleSubmit(event) {
        event.preventDefault();

        const response = await fetch("/api/contact", {
            method: "POST",
            headers: {
                "Content-Type": "application/json",
            },
            body: JSON.stringify({ name, email, txid, message }),
        });

        if (response.ok) {
            // Handle successful response
            console.log("Form submitted successfully");
        } else {
            // Handle errors
            console.error("Error submitting form");
        }
    }
</script>

<form on:submit={handleSubmit} class="corporate-form">
    <div class="contact-info">
        <h2>Get in Touch</h2>
        <p>
            For more details, contact us on 👉 <a
                href="https://t.me/josenarant"
                target="_blank"
                rel="noopener noreferrer">Telegram</a
            >
        </p>
    </div>
    <div class="form-group">
        <label for="name">
            Name:
            <input id="name" type="text" bind:value={name} required />
        </label>
    </div>

    <div class="form-group">
        <label for="email">
            Email:
            <input id="email" type="email" bind:value={email} required />
        </label>
    </div>

    <div class="form-group">
        <label for="txid">
            Transaction ID:
            <input id="txid" type="text" bind:value={txid} required />
        </label>
    </div>

    <div class="form-group">
        <div class="node-selection">
            <h4>Select Your Nodes</h4>
            <p>
                Please indicate the number and types of nodes you wish to
                contract.
            </p>
        </div>

        <div class="transaction-verification">
            <h4>Transaction Verification</h4>
            <p>
                Submit your transaction ID and the service name for payment
                confirmation.
            </p>
        </div>

        <label for="message">
            Message:
            <textarea id="message" bind:value={message} rows="4" required
            ></textarea>
        </label>
    </div>

    <button type="submit" class="submit-button">Send</button>
</form>

<style>
    body {
        background-color: #1b1f2b;

    }
    .node-selection,
    .transaction-verification,
    .contact-info {
        margin-bottom: 20px;
    }

    h2 {
        margin-bottom: 10px;
        color: #333;
        font-size: 1.5rem;
    }

    p {
        color: #555;
        font-size: 1rem;
        margin-bottom: 10px;
    }

    a {
        color: #007bff;
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }
    .corporate-form {
        max-width: 600px;
        margin: 2rem auto;
        padding: 1rem;
        background-color: #f8f9fa;
        border-radius: 8px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
        box-sizing: border-box; /* Ensure padding is included in width */
    }

    .form-group {
        margin-bottom: 1rem;
    }

    label {
        display: block;
        margin-bottom: 0.5rem;
        color: #333;
        font-weight: bold;
    }

    input,
    textarea {
        width: 500px; /* Subtract padding/margin from width */
        margin: 0 0.5rem; /* Add margin to prevent fields from touching edges */
        padding: 0.5rem;
        border: 1px solid #ced4da;
        border-radius: 4px;
        font-size: 1rem;
        color: #495057;
    }

    input:focus,
    textarea:focus {
        border-color: #80bdff;
        outline: 0;
        box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
    }

    .submit-button {
        width: calc(100% - 1rem); /* Subtract padding/margin from width */
        margin: 0.5rem; /* Add margin to match input fields */
        padding: 0.6rem;
        font-size: 1rem;
        color: #fff;
        background-color: #007bff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        transition: background-color 0.2s ease-in-out;
    }

    .submit-button:hover {
        background-color: #0056b3;
    }

    /* Responsive styles */
    @media (min-width: 576px) {
        .corporate-form {
            padding: 2rem;
        }

        input,
        textarea,
        .submit-button {
            width: 100%; /* Subtract padding/margin from width */
            margin: 0.5rem 0.5rem 0.5rem 0; /* Add margin to prevent fields from touching edges */
            padding: 0.5rem;
            border: 1px solid #ced4da;
            border-radius: 4px;
            font-size: 1rem;
            color: #ffffff;
        }
    }
</style>
