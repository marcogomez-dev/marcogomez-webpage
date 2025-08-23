<script lang="ts">
	import Card from '$lib/components/ui/Card.svelte';
	import Icon from '$lib/components/ui/Icon.svelte';
	import { Briefcase, Code } from '@lucide/svelte';

	const services = [
		{
			title: 'Optimización de Procesos y Estrategia Financiera',
			description:
				'Ofrezco un análisis profundo de tus procesos contables y financieros para identificar áreas de mejora, optimizar flujos de trabajo y asegurar que tu negocio opere con la máxima eficiencia. El objetivo es simple: transformar tus desafíos en oportunidades de crecimiento a través de una estrategia clara y bien estructurada.',
			benefit:
				'Obtendrás una hoja de ruta clara para fortalecer tu control financiero, reducir costos operativos y tomar decisiones más informadas.',
			icon: Briefcase
		},
		{
			title: 'Desarrollo de Soluciones Tecnológicas a Medida',
			description:
				'Lidero proyectos de implementación de software y desarrollo de herramientas digitales desde la concepción hasta la puesta en marcha. Mi enfoque combina la rigurosidad de la gestión de proyectos con un profundo entendimiento de las necesidades del negocio, asegurando que la tecnología trabaje para ti, y no al revés.',
			benefit:
				'Tendrás la certeza de que tu inversión tecnológica se traducirá en resultados tangibles, con soluciones robustas, seguras y perfectamente alineadas a tus objetivos.',
			icon: Code
		}
	];
</script>

<hgroup class="emphatized">
	<h2>Servicios</h2>
	<h3>Soluciones integrales que unen estrategia financiera y desarrollo tecnológico.</h3>
</hgroup>

<section class="container grid">
	{#each services as service}
		<Card>
			<div class="stack">
				<Icon icon={service.icon} size={48} />
				<h3>{service.title}</h3>
				<p>{service.description}</p>
				<p><strong>Beneficio Clave:</strong> {service.benefit}</p>
			</div>
		</Card>
	{/each}
</section>
