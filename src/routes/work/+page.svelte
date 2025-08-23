<script lang="ts">
	import Card from '$lib/components/ui/Card.svelte';
	import Icon from '$lib/components/ui/Icon.svelte';
	import { CircleAlert, Lightbulb, CircleCheck } from '@lucide/svelte';

	const caseStudy = [
		{
			title: 'Problema',
			description:
				'Una empresa cliente gestionaba su inventario a través de hojas de cálculo complejas y propensas a errores humanos. Este método no solo consumía una cantidad significativa de tiempo del equipo, sino que también generaba discrepancias en las auditorías, creando un riesgo financiero y operativo.',
			icon: CircleAlert
		},
		{
			title: 'Mi Enfoque',
			description:
				'Analicé el flujo de trabajo existente y diseñé una solución lógica basada en una aplicación web centralizada. El proceso incluyó el mapeo de los procesos clave (entradas, salidas, ajustes), el diseño de una base de datos relacional para garantizar la integridad de los datos y el desarrollo de una interfaz de usuario intuitiva y fácil de usar para el equipo.',
			icon: Lightbulb
		},
		{
			title: 'Solución y Resultados',
			description:
				'Desarrollé una página web a medida que automatiza el registro y seguimiento del inventario en tiempo real. La solución eliminó por completo el uso de hojas de cálculo, redujo los errores de registro en un 99% y disminuyó el tiempo dedicado a la gestión de stock en más de 15 horas semanales. Además, la empresa ahora cuenta con datos precisos y fiables para sus auditorías, fortaleciendo su control interno.',
			icon: CircleCheck
		}
	];
</script>

<hgroup class="emphatized">
	<h2>Caso de Estudio: Página Web de Control de Inventarios</h2>
	<h3>Cómo la tecnología a medida resuelve problemas de negocio.</h3>
</hgroup>

<section class="container grid">
	{#each caseStudy as step}
		<Card>
			<div class="stack">
				<Icon icon={step.icon} size={48} />
				<h3>{step.title}</h3>
				<p>{step.description}</p>
			</div>
		</Card>
	{/each}
</section>

<section class="container emphasized">
	<p>¿Tienes un desafío similar? <a href="/contact">Hablemos de cómo podemos crear una solución para ti.</a></p>
</section>
