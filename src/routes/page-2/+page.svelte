<script lang="ts">
</script>

<svelte:head>
	<title>Side 2 - NyhedsNat</title>
	<meta name="description" content="Side 2 - NyhedsNat" />
</svelte:head>

<div class="min-h-screen px-4 py-12">
	<div class="max-w-4xl mx-auto">
		<!-- Page Header -->
		<div class="text-center mb-16">
			<span class="inline-block px-4 py-2 bg-gold-500/10 text-gold-400 rounded-full text-sm font-medium mb-4">
				Side 2
			</span>
			<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-star-white mb-6">
				<span class="text-gradient-gold">Side 2</span>
			</h1>
			<p class="text-xl text-star-white/60 max-w-2xl mx-auto">
				Dette er indholdet for Side 2. Tilføj dit eget indhold her.
			</p>
		</div>

		<!-- Content Section -->
		<div class="space-y-8">
			<!-- Image Gallery Placeholder -->
			<div class="grid grid-cols-2 md:grid-cols-3 gap-4">
				{#each [1, 2, 3, 4, 5, 6] as item}
					<div
						class="aspect-square card-dark rounded-xl flex items-center justify-center hover:scale-105 transition-transform cursor-pointer"
					>
						<div class="text-center">
							<svg
								class="w-12 h-12 text-gold-400/40 mx-auto mb-2"
								fill="none"
								stroke="currentColor"
								viewBox="0 0 24 24"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"
								/>
							</svg>
							<span class="text-star-white/30 text-sm">Billede {item}</span>
						</div>
					</div>
				{/each}
			</div>

			<div class="card-dark rounded-2xl p-8">
				<h2 class="text-2xl font-bold text-star-white mb-4">Om denne side</h2>
				<p class="text-star-white/60 leading-relaxed mb-6">
					Her kan du tilføje mere information om hvad denne side handler om. Du kan inkludere
					billeder, tekst, videoer og meget mere.
				</p>
				<a
					href="/page-3"
					class="inline-block px-6 py-3 bg-gradient-to-r from-gold-500 to-gold-600 text-night-900 font-bold rounded-full hover:scale-105 transition-all"
				>
					Fortsæt til Side 3
				</a>
			</div>
		</div>

		<!-- Navigation -->
		<div class="mt-16 flex justify-between items-center">
			<a
				href="/page-1"
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
				href="/page-3"
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
