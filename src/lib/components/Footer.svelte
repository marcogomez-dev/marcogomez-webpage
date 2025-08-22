<script lang="ts">
  import Mail from '@lucide/svelte/icons/mail';
  import Linkedin from '@lucide/svelte/icons/linkedin';
</script>

<footer>
  <nav>
    <a href="mailto:marco.gomez@email.com">
      <Mail size={18} />
      marco.gomez@email.com
    </a>
    <a href="https://linkedin.com/in/marcogomez" target="_blank" rel="noopener noreferrer">
      <Linkedin size={18} />
      linkedin.com/in/marcogomez
    </a>
  </nav>
  <p>&copy; {new Date().getFullYear()} Marco Gómez. Todos los derechos reservados.</p>
</footer>
