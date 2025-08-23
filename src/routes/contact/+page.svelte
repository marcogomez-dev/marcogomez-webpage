<script lang="ts">
	import ContactForm from '$lib/components/ContactForm.svelte';
	import Icon from '$lib/components/ui/Icon.svelte';
	import { Mail, Linkedin } from '@lucide/svelte';
</script>

<hgroup class="emphatized">
	<h2>Contacto</h2>
	<h3>
		Si estás buscando un socio estratégico que entienda tanto de números como de código, estoy aquí
		para ayudarte. Hablemos sobre cómo podemos llevar tu negocio al siguiente nivel.
	</h3>
</hgroup>

<section class="container grid">
	<div class="stack">
		<h3>Información de Contacto</h3>
		<p class="blocks">
			<Icon icon={Mail} />
			<a href="mailto:marco.gomez@email.com">marco.gomez@email.com</a>
		</p>
		<p class="blocks">
			<Icon icon={Linkedin} />
			<a href="https://linkedin.com/in/marcogomez" target="_blank" rel="noopener noreferrer">
				linkedin.com/in/marcogomez
			</a>
		</p>
	</div>

	<ContactForm />
</section>
