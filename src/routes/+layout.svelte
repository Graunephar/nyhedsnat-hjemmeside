<script lang="ts">
	import './layout.css';
	import Navigation from '$lib/components/Navigation.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Drone from '$lib/components/Drone.svelte';
	import Ufo from '$lib/components/Ufo.svelte';
	import Car from '$lib/components/Car.svelte';
	import Bus from '$lib/components/Bus.svelte';
	import Convoy from '$lib/components/Convoy.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/svg/logo.svg" type="image/svg+xml" />
	<meta name="theme-color" content="#030712" />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
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
		<Car />
		<Bus />
		<Convoy />
		<img src="/svg/huse.svg" alt="" class="houses-silhouette" aria-hidden="true" />
	</div>

	<Footer />
</div>

<style>
	.moon-container {
		position: absolute;
		top: 110px;
		right: 25px;
		z-index: 1;
		pointer-events: none;
	}

	.moon {
		width: 60px;
		height: auto;
		position: relative;
		z-index: 1;
	}

	.moon-glow {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		width: 100px;
		height: 100px;
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

	@media (min-width: 768px) {
		.moon-container {
			top: 200px;
			right: 50px;
		}

		.moon {
			width: 120px;
		}

		.moon-glow {
			width: 200px;
			height: 200px;
		}
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
