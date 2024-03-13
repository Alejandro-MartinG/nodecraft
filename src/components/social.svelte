<script>
  const socialLinks = [
    // { icon: 'fab fa-facebook-f', url: 'https://www.facebook.com/tuUsuario' },
    { icon: 'fab fa-twitter', url: 'https://twitter.com/NodeCraft_Web3' },
    { icon: 'fab fa-instagram', url: 'https://www.instagram.com/tuUsuario' },
    // { icon: 'fab fa-linkedin-in', url: 'https://www.linkedin.com/in/tuUsuario' },
    { icon: 'fab fa-telegram-plane', url: 'https://t.me/tuUsuario' },
    // { icon: 'fab fa-whatsapp', url: 'https://wa.me/tuNumero' },
    { icon: 'fab fa-discord', url: 'https://discord.gg/tuInvitacion' },
  ];
</script>

<style>
  .social-bar {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
  }

  .social-icon {
    color: #d3fffa; /* Color de los iconos */
    font-size: 24px; /* Tamaño de los iconos */
    margin: 0 10px; /* Espaciado entre iconos */
    transition: color 0.3s ease;
  }

  .social-icon:hover {
    color: #007bff; /* Color de los iconos al pasar el mouse */
  }
</style>

<div class="social-bar">
  {#each socialLinks as link}
    <a href={link.url} class="social-icon" target="_blank" rel="noopener noreferrer">
      <i class={link.icon}></i>
    </a>
  {/each}
</div>