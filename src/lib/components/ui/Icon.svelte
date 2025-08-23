<script lang="ts">
	import type { Icon } from '@lucide/svelte';

	type Props = {
		icon: typeof Icon;
		size?: number;
		class?: string;
	};

	let { icon: IconComponent, size = 24, class: className = '' }: Props = $props();
</script>

<IconComponent {size} class={`icon ${className}`} />
