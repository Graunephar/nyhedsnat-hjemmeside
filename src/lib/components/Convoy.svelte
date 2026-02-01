<script lang="ts">
	import { onMount } from 'svelte';
	import { triggerConvoy } from '$lib/stores/convoy';

	let visible = $state(false);
	let direction = $state<'ltr' | 'rtl'>('ltr');
	let duration = $state(20);

	const carCount = 10;
	const carWidth = 120;
	const gap = 60; // Half a car's width

	const startConvoy = () => {
		if (visible) return; // Don't start if already running

		direction = Math.random() > 0.5 ? 'ltr' : 'rtl';
		duration = Math.random() * 5 + 18; // 18-23 seconds

		visible = true;

		// Hide after animation completes
		setTimeout(() => {
			visible = false;
		}, duration * 1000 + 200);
	};

	onMount(() => {
		// Listen for manual trigger from car click
		const unsubscribe = triggerConvoy.subscribe((triggered) => {
			if (triggered) {
				startConvoy();
				triggerConvoy.set(false);
			}
		});

		// Very rare: initial delay between 3-8 minutes
		const initialDelay = Math.random() * 300000 + 180000;

		// First convoy after random delay
		setTimeout(() => {
			startConvoy();

			// Schedule next convoys every 5-10 minutes (very rare)
			const scheduleNext = () => {
				const nextInterval = Math.random() * 300000 + 300000;
				setTimeout(() => {
					startConvoy();
					scheduleNext();
				}, nextInterval);
			};
			scheduleNext();
		}, initialDelay);

		return unsubscribe;
	});
</script>

{#if visible}
	<div
		class="convoy-container {direction}"
		style="--duration: {duration}s;"
	>
		{#each Array(carCount) as _, i}
			<img
				src="/svg/car.svg"
				alt=""
				class="convoy-car"
				style="--offset: {i * (carWidth + gap)}px;"
				aria-hidden="true"
			/>
		{/each}
	</div>
{/if}

<style>
	.convoy-container {
		position: absolute;
		bottom: 10px;
		z-index: 2;
		pointer-events: none;
		display: flex;
		gap: 60px;
	}

	/* Left to right drive */
	.convoy-container.ltr {
		left: 0;
		animation: drive-ltr var(--duration, 20s) linear forwards;
	}

	/* Right to left drive */
	.convoy-container.rtl {
		right: 0;
		left: auto;
		flex-direction: row-reverse;
		animation: drive-rtl var(--duration, 20s) linear forwards;
	}

	.convoy-container.ltr .convoy-car {
		transform: scaleX(-1);
	}

	.convoy-car {
		width: 120px;
		height: auto;
		filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.5));
	}

	@keyframes drive-ltr {
		0% {
			transform: translateX(-1900px);
		}
		100% {
			transform: translateX(calc(100vw + 200px));
		}
	}

	@keyframes drive-rtl {
		0% {
			transform: translateX(1900px);
		}
		100% {
			transform: translateX(calc(-100vw - 200px));
		}
	}
</style>
