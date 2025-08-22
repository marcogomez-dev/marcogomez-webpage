<script lang="ts">
  // Lógica para el manejo del formulario (envío, validación, etc.)
  let name: string = '';
  let email: string = '';
  let subject: string = '';
  let message: string = '';

  function handleSubmit() {
    console.log('Formulario enviado:', { name, email, subject, message });
    // Aquí iría la lógica para enviar el formulario, por ejemplo, a una API
    alert('Mensaje enviado con éxito!');
    // Resetear campos
    name = '';
    email = '';
    subject = '';
    message = '';
  }
</script>

<form onsubmit={handleSubmit} class="form-contact">
  <div class="form-group">
    <label for="name" class="form-label">Nombre:</label>
    <input type="text" id="name" bind:value={name} required class="form-input" />
  </div>
  <div class="form-group">
    <label for="email" class="form-label">Correo:</label>
    <input type="email" id="email" bind:value={email} required class="form-input" />
  </div>
  <div class="form-group">
    <label for="subject" class="form-label">Asunto:</label>
    <input type="text" id="subject" bind:value={subject} required class="form-input" />
  </div>
  <div class="form-group">
    <label for="message" class="form-label">Mensaje:</label>
    <textarea id="message" bind:value={message} required class="form-textarea"></textarea>
  </div>
  <button type="submit" class="button button-primary">Enviar Mensaje</button>
</form>
