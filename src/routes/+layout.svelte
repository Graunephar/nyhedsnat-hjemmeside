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

<!-- Moon in top right corner -->
<div class="moon-container">
	<div class="moon-glow"></div>
	<img src="/svg/moon.svg" alt="" class="moon" aria-hidden="true" />
</div>

<!-- Flying drone -->
<Drone />

<!-- UFO with search pattern -->
<Ufo />

<!-- Main app structure -->
<div class="main-content flex min-h-screen flex-col">
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
	.moon-container {
		position: absolute;
		top: 200px;
		right: 50px;
		z-index: 1;
		pointer-events: none;
	}

	.moon {
		width: 120px;
		height: auto;
		position: relative;
		z-index: 1;
	}

	.moon-glow {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 200px;
		height: 200px;
		border-radius: 50%;
		background: radial-gradient(
			circle,
			rgba(255, 255, 235, 0.45) 0%,
			rgba(255, 255, 215, 0.28) 22%,
			rgba(255, 255, 190, 0.14) 45%,
			rgba(255, 255, 160, 0.05) 70%,
			transparent 100%
		);
		filter: blur(30px);
		animation: moon-pulse 8s ease-in-out infinite;
	}

	@keyframes moon-pulse {
		0%,
		100% {
			opacity: 0.8;
			transform: translate(-50%, -50%) scale(1);
		}
		50% {
			opacity: 1;
			transform: translate(-50%, -50%) scale(1.1);
		}
	}

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
