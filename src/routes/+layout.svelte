<script lang="ts">
	import './layout.css';
	import Navigation from '$lib/components/Navigation.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/images/logo.png" />
	<meta name="theme-color" content="#030712" />
</svelte:head>

<!-- Animated starfield background -->
<div class="starfield">
	<div class="shooting-star"></div>
	<div class="shooting-star"></div>
	<div class="shooting-star"></div>
</div>

<!-- Main app structure -->
<div class="min-h-screen flex flex-col">
	<Navigation />

	<!-- Main content with padding for fixed header -->
	<main class="page-content flex-1 pt-24 sm:pt-28 md:pt-36 lg:pt-40">
		{@render children()}
	</main>

	<Footer />
</div>
