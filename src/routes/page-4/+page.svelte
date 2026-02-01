<script lang="ts">
</script>

<svelte:head>
	<title>Side 4 - NyhedsNat</title>
	<meta name="description" content="Side 4 - NyhedsNat" />
</svelte:head>

<div class="min-h-screen px-4 py-12">
	<div class="max-w-4xl mx-auto">
		<!-- Page Header -->
		<div class="text-center mb-16">
			<span class="inline-block px-4 py-2 bg-gold-500/10 text-gold-400 rounded-full text-sm font-medium mb-4">
				Side 4
			</span>
			<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-star-white mb-6">
				<span class="text-gradient-gold">Kontakt</span>
			</h1>
			<p class="text-xl text-star-white/60 max-w-2xl mx-auto">
				Har du spørgsmål? Kontakt os her.
			</p>
		</div>

		<!-- Contact Form -->
		<div class="card-dark rounded-2xl p-8 md:p-12 mb-12">
			<form class="space-y-6">
				<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
					<div>
						<label for="name" class="block text-star-white mb-2 font-medium">Navn</label>
						<input
							type="text"
							id="name"
							placeholder="Dit navn"
							class="w-full px-4 py-3 bg-night-700/50 border border-gold-500/20 rounded-lg text-star-white placeholder-star-white/30 focus:border-gold-400 focus:ring-1 focus:ring-gold-400 transition-colors"
						/>
					</div>
					<div>
						<label for="email" class="block text-star-white mb-2 font-medium">Email</label>
						<input
							type="email"
							id="email"
							placeholder="din@email.dk"
							class="w-full px-4 py-3 bg-night-700/50 border border-gold-500/20 rounded-lg text-star-white placeholder-star-white/30 focus:border-gold-400 focus:ring-1 focus:ring-gold-400 transition-colors"
						/>
					</div>
				</div>
				<div>
					<label for="subject" class="block text-star-white mb-2 font-medium">Emne</label>
					<input
						type="text"
						id="subject"
						placeholder="Hvad handler din henvendelse om?"
						class="w-full px-4 py-3 bg-night-700/50 border border-gold-500/20 rounded-lg text-star-white placeholder-star-white/30 focus:border-gold-400 focus:ring-1 focus:ring-gold-400 transition-colors"
					/>
				</div>
				<div>
					<label for="message" class="block text-star-white mb-2 font-medium">Besked</label>
					<textarea
						id="message"
						rows="5"
						placeholder="Skriv din besked her..."
						class="w-full px-4 py-3 bg-night-700/50 border border-gold-500/20 rounded-lg text-star-white placeholder-star-white/30 focus:border-gold-400 focus:ring-1 focus:ring-gold-400 transition-colors resize-none"
					></textarea>
				</div>
				<button
					type="submit"
					class="w-full md:w-auto px-8 py-4 bg-gradient-to-r from-gold-500 to-gold-600 text-night-900 font-bold rounded-full glow-gold hover:scale-105 transition-all"
				>
					Send besked
				</button>
			</form>
		</div>

		<!-- Contact Info Cards -->
		<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
			<div class="card-dark rounded-xl p-6 text-center hover:scale-105 transition-transform">
				<div class="w-12 h-12 rounded-full bg-gold-500/20 flex items-center justify-center mx-auto mb-4">
					<svg class="w-6 h-6 text-gold-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
						/>
					</svg>
				</div>
				<h3 class="font-bold text-star-white mb-2">Email</h3>
				<p class="text-star-white/50 text-sm">info@nyhedsnat.dk</p>
			</div>

			<div class="card-dark rounded-xl p-6 text-center hover:scale-105 transition-transform">
				<div class="w-12 h-12 rounded-full bg-gold-500/20 flex items-center justify-center mx-auto mb-4">
					<svg class="w-6 h-6 text-gold-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
						/>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
						/>
					</svg>
				</div>
				<h3 class="font-bold text-star-white mb-2">Lokation</h3>
				<p class="text-star-white/50 text-sm">København, Danmark</p>
			</div>

			<div class="card-dark rounded-xl p-6 text-center hover:scale-105 transition-transform">
				<div class="w-12 h-12 rounded-full bg-gold-500/20 flex items-center justify-center mx-auto mb-4">
					<svg class="w-6 h-6 text-gold-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
						/>
					</svg>
				</div>
				<h3 class="font-bold text-star-white mb-2">Åbningstider</h3>
				<p class="text-star-white/50 text-sm">Kun om natten</p>
			</div>
		</div>

		<!-- Navigation -->
		<div class="mt-16 flex justify-between items-center">
			<a
				href="/page-3"
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
				href="/"
				class="text-gold-400 hover:text-gold-300 transition-colors flex items-center gap-2"
			>
				Tilbage til forsiden
				<svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
					/>
				</svg>
			</a>
		</div>
	</div>
</div>
