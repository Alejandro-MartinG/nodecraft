<script>
  let name = '';
  let email = '';
  let txid = '';
  let message = '';

  async function handleSubmit(event) {
    event.preventDefault();

    const response = await fetch('/api/contact', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify({ name, email, txid, message }),
    });

    if (response.ok) {
      // Manejar la respuesta exitosa
      console.log('Formulario enviado con éxito');
    } else {
      // Manejar errores
      console.error('Error al enviar el formulario');
    }
  }
</script>


<form on:submit={handleSubmit}>
  <label for="name">
    Name:
    <input id="name" type="text" bind:value={name} required>
  </label>

  <label for="email">
    Email:
    <input id="email" type="email" bind:value={email} required>
  </label>

  <label for="email">
    Transaction id:
    <input id="txid" type="txid" bind:value={txid} required>
  </label>

  <label for="message">
    Message:
    <textarea id="message" bind:value={message} rows="4" required></textarea>
  </label>

  <button type="submit">Send</button>
</form>

<style>
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
</style>
