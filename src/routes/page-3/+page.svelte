<script lang="ts">
</script>

<svelte:head>
	<title>Side 3 - NyhedsNat</title>
	<meta name="description" content="Side 3 - NyhedsNat" />
</svelte:head>

<div class="min-h-screen px-4 py-12">
	<div class="max-w-4xl mx-auto">
		<!-- Page Header -->
		<div class="text-center mb-16">
			<span class="inline-block px-4 py-2 bg-gold-500/10 text-gold-400 rounded-full text-sm font-medium mb-4">
				Side 3
			</span>
			<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-star-white mb-6">
				<span class="text-gradient-gold">Side 3</span>
			</h1>
			<p class="text-xl text-star-white/60 max-w-2xl mx-auto">
				Dette er indholdet for Side 3. Tilføj dit eget indhold her.
			</p>
		</div>

		<!-- Timeline Section -->
		<div class="space-y-8 mb-12">
			<h2 class="text-2xl font-bold text-star-white text-center">Program / Tidslinje</h2>

			<div class="relative">
				<!-- Timeline Line -->
				<div class="absolute left-4 md:left-1/2 top-0 bottom-0 w-0.5 bg-gold-500/30 transform md:-translate-x-1/2"></div>

				<!-- Timeline Items -->
				{#each [
					{ time: '18:00', title: 'Velkomst', desc: 'Dørene åbner' },
					{ time: '19:00', title: 'Første Session', desc: 'Nattens nyheder begynder' },
					{ time: '20:30', title: 'Pause', desc: 'Forfriskninger og networking' },
					{ time: '21:00', title: 'Anden Session', desc: 'Dybdegående diskussion' },
					{ time: '22:30', title: 'Afslutning', desc: 'Tak for i aften' }
				] as item, i}
					<div class="relative flex items-center gap-6 {i % 2 === 0 ? 'md:flex-row' : 'md:flex-row-reverse'}">
						<!-- Dot -->
						<div class="absolute left-4 md:left-1/2 w-4 h-4 bg-gold-500 rounded-full transform md:-translate-x-1/2 ring-4 ring-night-900"></div>

						<!-- Content -->
						<div class="ml-12 md:ml-0 md:w-1/2 {i % 2 === 0 ? 'md:pr-12 md:text-right' : 'md:pl-12'}">
							<div class="card-dark rounded-xl p-6 hover:scale-105 transition-transform">
								<span class="text-gold-400 font-mono font-bold">{item.time}</span>
								<h3 class="text-lg font-bold text-star-white mt-1">{item.title}</h3>
								<p class="text-star-white/50 text-sm mt-1">{item.desc}</p>
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>

		<!-- Additional Info -->
		<div class="card-dark rounded-2xl p-8 text-center">
			<h2 class="text-2xl font-bold text-star-white mb-4">Tilmelding</h2>
			<p class="text-star-white/60 mb-6">
				Tilmeld dig nu for at være en del af NyhedsNat.
			</p>
			<button
				class="px-8 py-4 bg-gradient-to-r from-gold-500 to-gold-600 text-night-900 font-bold rounded-full glow-gold hover:scale-105 transition-all"
			>
				Tilmeld dig
			</button>
		</div>

		<!-- Navigation -->
		<div class="mt-16 flex justify-between items-center">
			<a
				href="/page-2"
				class="text-gold-400 hover:text-gold-300 transition-colors flex items-center gap-2"
			>
				<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M15 19l-7-7 7-7"
					/>
				</svg>
				Forrige side
			</a>
			<a
				href="/page-4"
				class="text-gold-400 hover:text-gold-300 transition-colors flex items-center gap-2"
			>
				Næste side
				<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M9 5l7 7-7 7"
					/>
				</svg>
			</a>
		</div>
	</div>
</div>
