<script lang="ts">
	import { page } from '$app/state';

	let mobileMenuOpen = $state(false);

	const navLinks = [
		{ href: '/', label: 'Hjem' },
		{ href: '/tilmelding', label: 'Tilmelding' },
		{ href: '/program', label: 'Program' },
		{ href: '/praktisk', label: 'Praktisk' },
		{ href: '/regler', label: 'Regler' },
		{ href: '/faq', label: 'FAQ' },
		{ href: '/kontakt', label: 'Kontakt' }
	];

	function toggleMobileMenu() {
		mobileMenuOpen = !mobileMenuOpen;
	}

	function closeMobileMenu() {
		mobileMenuOpen = false;
	}

	function isActive(href: string): boolean {
		if (href === '/') {
			return page.url.pathname === '/';
		}
		return page.url.pathname.startsWith(href);
	}

	function getDesktopLinkClass(href: string): string {
		const base = 'nav-link hover:text-gold-400 transition-colors font-medium text-lg';
		return isActive(href) ? `${base} text-gold-400 active` : `${base} text-star-white/80`;
	}

	function getMobileLinkClass(href: string): string {
		const base =
			'block px-4 py-3 rounded-lg hover:text-gold-400 hover:bg-night-700/50 transition-all font-medium text-lg';
		return isActive(href)
			? `${base} text-gold-400 bg-night-700/50`
			: `${base} text-star-white/80`;
	}
</script>

<header class="fixed top-0 left-0 right-0 z-50">
	<!-- Main header with large logo -->
	<div class="bg-night-900/90 backdrop-blur-md border-b border-gold-500/20">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="flex items-center justify-between py-4 md:py-6">
				<!-- Large Logo Area -->
				<a href="/" class="flex items-center gap-4 group" onclick={closeMobileMenu}>
					<img
						src="/images/logo.png"
						alt="NyhedsNat Logo"
						class="h-16 sm:h-20 md:h-24 lg:h-28 w-auto transition-transform duration-300 group-hover:scale-105 drop-shadow-lg"
					/>
				</a>

				<!-- Desktop Navigation -->
				<nav class="hidden md:flex items-center gap-6 lg:gap-10">
					{#each navLinks as link}
						<a href={link.href} class={getDesktopLinkClass(link.href)}>
							{link.label}
						</a>
					{/each}
				</nav>

				<!-- Mobile Menu Button -->
				<button
					onclick={toggleMobileMenu}
					class="md:hidden flex flex-col gap-1.5 p-3 rounded-lg hover:bg-night-700/50 transition-colors"
					aria-label="Toggle menu"
					aria-expanded={mobileMenuOpen}
				>
					<span
						class="block w-7 h-0.5 bg-gold-400 transition-all duration-300 origin-center {mobileMenuOpen
							? 'rotate-45 translate-y-2'
							: ''}"
					></span>
					<span
						class="block w-7 h-0.5 bg-gold-400 transition-all duration-300 {mobileMenuOpen
							? 'opacity-0'
							: ''}"
					></span>
					<span
						class="block w-7 h-0.5 bg-gold-400 transition-all duration-300 origin-center {mobileMenuOpen
							? '-rotate-45 -translate-y-2'
							: ''}"
					></span>
				</button>
			</div>
		</div>
	</div>

	<!-- Mobile Navigation Dropdown -->
	{#if mobileMenuOpen}
		<div
			class="md:hidden bg-night-800/95 backdrop-blur-md border-b border-gold-500/20 animate-slideDown"
		>
			<nav class="px-4 py-4 space-y-2">
				{#each navLinks as link}
					<a href={link.href} onclick={closeMobileMenu} class={getMobileLinkClass(link.href)}>
						{link.label}
					</a>
				{/each}
			</nav>
		</div>
	{/if}
</header>

<style>
	@keyframes slideDown {
		from {
			opacity: 0;
			transform: translateY(-10px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	.animate-slideDown {
		animation: slideDown 0.2s ease-out;
	}
</style>
