<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="relative z-10 bg-night-900/80 backdrop-blur-md border-t border-gold-500/20 mt-auto">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
		<div class="flex flex-col md:flex-row items-center justify-between gap-4">
			<!-- Logo and tagline -->
			<div class="flex items-center gap-3">
				<img src="/images/logo.png" alt="NyhedsNat" class="h-8 w-auto" />
				<span class="text-star-white/60 text-sm">Nattens nyheder</span>
			</div>

			<!-- Quick links -->
			<nav class="flex flex-wrap justify-center gap-6">
				<a href="/" class="text-star-white/60 hover:text-gold-400 transition-colors text-sm">
					Hjem
				</a>
				<a href="/page-1" class="text-star-white/60 hover:text-gold-400 transition-colors text-sm">
					Side 1
				</a>
				<a href="/page-2" class="text-star-white/60 hover:text-gold-400 transition-colors text-sm">
					Side 2
				</a>
				<a href="/page-3" class="text-star-white/60 hover:text-gold-400 transition-colors text-sm">
					Side 3
				</a>
				<a href="/page-4" class="text-star-white/60 hover:text-gold-400 transition-colors text-sm">
					Side 4
				</a>
			</nav>

			<!-- Copyright -->
			<p class="text-star-white/40 text-sm">&copy; {currentYear} NyhedsNat</p>
		</div>
	</div>
</footer>
