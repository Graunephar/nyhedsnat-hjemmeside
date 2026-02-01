<script lang="ts">
	import './layout.css';
	import Navigation from '$lib/components/Navigation.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Drone from '$lib/components/Drone.svelte';
	import Ufo from '$lib/components/Ufo.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/svg/logo.svg" type="image/svg+xml" />
	<meta name="theme-color" content="#030712" />
</svelte:head>

<!-- Animated starfield background -->
<div class="starfield">
	<div class="shooting-star"></div>
</div>

<!-- Flying drone -->
<Drone />

<!-- UFO with search pattern -->
<Ufo />

<!-- Main app structure -->
<div class="min-h-screen flex flex-col main-content">
	<Navigation />

	<!-- Main content with padding for fixed header -->
	<main class="page-content flex-1 pt-24 sm:pt-28 md:pt-36 lg:pt-40">
		{@render children()}
	</main>

	<!-- Houses silhouette at the bottom -->
	<div class="houses-container">
		<img src="/svg/huse.svg" alt="" class="houses-silhouette" aria-hidden="true" />
	</div>

	<Footer />
</div>

<style>
	.main-content {
		position: relative;
		z-index: 2;
	}

	.houses-container {
		width: 100%;
		overflow: hidden;
		margin-top: auto;
		position: relative;
		z-index: 1;
	}

	.houses-silhouette {
		width: 100%;
		height: auto;
		display: block;
		min-width: 1200px;
		margin-left: 50%;
		transform: translateX(-50%);
	}
</style>
