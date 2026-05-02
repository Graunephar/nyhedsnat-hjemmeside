<script lang="ts">
	export let href = '#';
	export let variant: 'cta' | 'secondary' = 'cta';
	export let className = '';

	const base = 'inline-flex items-center justify-center gap-3 rounded-full font-bold transition-all duration-300';
	const cta =
		'px-8 py-5 bg-gradient-to-r from-gold-500 to-gold-600 text-night-900 text-lg hover:from-gold-400 hover:to-gold-500';
	const secondary =
		'px-8 py-4 border-2 border-gold-500/50 text-gold-400 hover:bg-gold-500/10 hover:border-gold-400';
</script>

<a href={href} class={`${base} ${variant === 'cta' ? cta : secondary} ${className}`} {...$$restProps}>
	<slot />
</a>
