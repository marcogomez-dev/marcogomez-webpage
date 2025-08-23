<script lang="ts">
	type Props = {
		title: string;
		subtitle?: string;
	};

	let { title, subtitle }: Props = $props();
</script>

<header class="emphasized">
	<h2>{title}</h2>
	{#if subtitle}
		<p>{subtitle}</p>
	{/if}
</header>
