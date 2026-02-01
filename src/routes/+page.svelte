<script lang="ts">
</script>

<svelte:head>
	<title>NyhedsNat - Velkommen til nattens nyheder</title>
	<meta name="description" content="NyhedsNat - Et arrangement om nattens nyheder" />
</svelte:head>

<!-- Hero Section -->
<section class="relative min-h-[80vh] flex items-center justify-center px-4 overflow-hidden">
	<!-- Decorative elements -->
	<div class="absolute inset-0 flex items-center justify-center opacity-10">
		<div
			class="w-[600px] h-[600px] rounded-full bg-gradient-to-br from-gold-500/30 to-transparent blur-3xl"
		></div>
	</div>

	<div class="relative z-10 text-center max-w-4xl mx-auto">
		<!-- Logo -->
		<div class="mb-8 animate-float">
			<img
				src="/images/logo.png"
				alt="NyhedsNat"
				class="w-48 md:w-64 lg:w-80 mx-auto drop-shadow-2xl"
			/>
		</div>

		<!-- Main heading -->
		<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-6">
			<span class="text-star-white">Velkommen til</span>
			<br />
			<span class="text-gradient-gold">NyhedsNat</span>
		</h1>

		<!-- Subtitle -->
		<p class="text-xl md:text-2xl text-star-white/70 mb-10 max-w-2xl mx-auto">
			Oplev nattens mest spændende nyheder under stjernehimlen
		</p>

		<!-- CTA Buttons -->
		<div class="flex flex-col sm:flex-row gap-4 justify-center">
			<a
				href="/page-1"
				class="px-8 py-4 bg-gradient-to-r from-gold-500 to-gold-600 text-night-900 font-bold rounded-full glow-gold hover:scale-105 transition-all duration-300"
			>
				Udforsk Nu
			</a>
			<a
				href="/page-2"
				class="px-8 py-4 border-2 border-gold-500/50 text-gold-400 font-bold rounded-full hover:bg-gold-500/10 hover:border-gold-400 transition-all duration-300"
			>
				Læs Mere
			</a>
		</div>
	</div>
</section>

<!-- Features Section -->
<section class="py-20 px-4">
	<div class="max-w-6xl mx-auto">
		<h2 class="text-3xl md:text-4xl font-bold text-center mb-16">
			<span class="text-gradient-gold">Hvad er NyhedsNat?</span>
		</h2>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
			<!-- Feature Card 1 -->
			<div
				class="card-dark rounded-2xl p-8 hover:scale-105 transition-all duration-300 group cursor-pointer"
			>
				<div
					class="w-16 h-16 rounded-full bg-gradient-to-br from-gold-400/20 to-gold-600/20 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
				>
					<svg
						class="w-8 h-8 text-gold-400"
						fill="none"
						stroke="currentColor"
						viewBox="0 0 24 24"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M11.049 2.927c.3-.921 1.603-.921 1.902 0l1.519 4.674a1 1 0 00.95.69h4.915c.969 0 1.371 1.24.588 1.81l-3.976 2.888a1 1 0 00-.363 1.118l1.518 4.674c.3.922-.755 1.688-1.538 1.118l-3.976-2.888a1 1 0 00-1.176 0l-3.976 2.888c-.783.57-1.838-.197-1.538-1.118l1.518-4.674a1 1 0 00-.363-1.118l-3.976-2.888c-.784-.57-.38-1.81.588-1.81h4.914a1 1 0 00.951-.69l1.519-4.674z"
						/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-star-white mb-3">Spændende Indhold</h3>
				<p class="text-star-white/60">
					Oplev unikke historier og nyheder præsenteret på en helt ny måde under nattehimlen.
				</p>
			</div>

			<!-- Feature Card 2 -->
			<div
				class="card-dark rounded-2xl p-8 hover:scale-105 transition-all duration-300 group cursor-pointer"
			>
				<div
					class="w-16 h-16 rounded-full bg-gradient-to-br from-gold-400/20 to-gold-600/20 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
				>
					<svg
						class="w-8 h-8 text-gold-400"
						fill="none"
						stroke="currentColor"
						viewBox="0 0 24 24"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"
						/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-star-white mb-3">Fællesskab</h3>
				<p class="text-star-white/60">
					Vær en del af et engageret fællesskab der samles om nattens fortællinger.
				</p>
			</div>

			<!-- Feature Card 3 -->
			<div
				class="card-dark rounded-2xl p-8 hover:scale-105 transition-all duration-300 group cursor-pointer"
			>
				<div
					class="w-16 h-16 rounded-full bg-gradient-to-br from-gold-400/20 to-gold-600/20 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
				>
					<svg
						class="w-8 h-8 text-gold-400"
						fill="none"
						stroke="currentColor"
						viewBox="0 0 24 24"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"
						/>
					</svg>
				</div>
				<h3 class="text-xl font-bold text-star-white mb-3">Atmosfære</h3>
				<p class="text-star-white/60">
					Nyd en helt særlig stemning med stjernehimmel og natlige oplevelser.
				</p>
			</div>
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="py-20 px-4">
	<div class="max-w-4xl mx-auto text-center">
		<div class="card-dark rounded-3xl p-10 md:p-16">
			<h2 class="text-3xl md:text-4xl font-bold text-star-white mb-6">
				Klar til at udforske natten?
			</h2>
			<p class="text-xl text-star-white/60 mb-10">
				Deltag i NyhedsNat og oplev nyheder på en helt ny måde.
			</p>
			<a
				href="/page-1"
				class="inline-block px-10 py-4 bg-gradient-to-r from-gold-500 to-gold-600 text-night-900 font-bold rounded-full glow-gold hover:scale-105 transition-all duration-300"
			>
				Kom i gang
			</a>
		</div>
	</div>
</section>

<style>
	@keyframes float {
		0%,
		100% {
			transform: translateY(0);
		}
		50% {
			transform: translateY(-10px);
		}
	}

	.animate-float {
		animation: float 4s ease-in-out infinite;
	}
</style>
