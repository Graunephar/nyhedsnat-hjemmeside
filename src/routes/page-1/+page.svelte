<script lang="ts">
</script>

<svelte:head>
	<title>Side 1 - NyhedsNat</title>
	<meta name="description" content="Side 1 - NyhedsNat" />
</svelte:head>

<div class="min-h-screen px-4 py-12">
	<div class="max-w-4xl mx-auto">
		<!-- Page Header -->
		<div class="text-center mb-16">
			<span class="inline-block px-4 py-2 bg-gold-500/10 text-gold-400 rounded-full text-sm font-medium mb-4">
				Side 1
			</span>
			<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-star-white mb-6">
				<span class="text-gradient-gold">Side 1</span>
			</h1>
			<p class="text-xl text-star-white/60 max-w-2xl mx-auto">
				Dette er indholdet for Side 1. Tilføj dit eget indhold her.
			</p>
		</div>

		<!-- Content Section -->
		<div class="space-y-8">
			<div class="card-dark rounded-2xl p-8">
				<h2 class="text-2xl font-bold text-star-white mb-4">Sektion 1</h2>
				<p class="text-star-white/60 leading-relaxed">
					Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt
					ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
					ullamco laboris nisi ut aliquip ex ea commodo consequat.
				</p>
			</div>

			<div class="card-dark rounded-2xl p-8">
				<h2 class="text-2xl font-bold text-star-white mb-4">Sektion 2</h2>
				<p class="text-star-white/60 leading-relaxed">
					Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat
					nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
					deserunt mollit anim id est laborum.
				</p>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
				<div class="card-dark rounded-2xl p-6 hover:scale-105 transition-transform">
					<div class="w-12 h-12 rounded-full bg-gold-500/20 flex items-center justify-center mb-4">
						<svg class="w-6 h-6 text-gold-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
						</svg>
					</div>
					<h3 class="text-lg font-bold text-star-white mb-2">Feature A</h3>
					<p class="text-star-white/50 text-sm">En kort beskrivelse af denne feature.</p>
				</div>
				<div class="card-dark rounded-2xl p-6 hover:scale-105 transition-transform">
					<div class="w-12 h-12 rounded-full bg-gold-500/20 flex items-center justify-center mb-4">
						<svg class="w-6 h-6 text-gold-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
						</svg>
					</div>
					<h3 class="text-lg font-bold text-star-white mb-2">Feature B</h3>
					<p class="text-star-white/50 text-sm">En kort beskrivelse af denne feature.</p>
				</div>
			</div>
		</div>

		<!-- Navigation -->
		<div class="mt-16 flex justify-between items-center">
			<a href="/" class="text-gold-400 hover:text-gold-300 transition-colors flex items-center gap-2">
				<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
				</svg>
				Tilbage til forsiden
			</a>
			<a href="/page-2" class="text-gold-400 hover:text-gold-300 transition-colors flex items-center gap-2">
				Næste side
				<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
				</svg>
			</a>
		</div>
	</div>
</div>
