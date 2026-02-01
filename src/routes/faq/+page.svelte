<script lang="ts">
	const faqs = [
		{
			question: 'Er Nyhedsnat en rigtig journalistøvelse?',
			answer: `Nej. Journalistrollen er en legeramme. Nyhedsnat handler om leg, fantasi og fælles oplevelser – præcis som mange andre aktiviteter i FDF.

Seniorerne leger forskellige roller og laver sjove, dramatiske eller aktuelle hændelser. Væbnere og seniorvæbnere leger journalister, der oplever hændelserne, stiller spørgsmål og fortæller videre, hvad der er sket.

Der er ingen forventning om, at deltagerne arbejder journalistisk korrekt eller realistisk.`
		},
		{
			question: 'Skal man være god til at skrive for at deltage?',
			answer: `Nej. Aviserne kan bestå af mange forskellige typer indhold.

Det kan fx være:
• Billeder
• Korte tekster
• Kryds og tværs
• Tegninger
• Sjove indslag
• Video

Der gives også priser for bedste pressefoto og bedste reel, så der er mange måder at bidrage på.`
		},
		{
			question: 'Skal deltagerne være gode til IT?',
			answer: `Nej. De fleste væbnere og seniorvæbnere arbejder allerede med computer i skolen.

Derudover sørger udvalget for, at der er IT-kyndige frivillige til stede hele natten, som kan hjælpe, hvis der opstår tekniske problemer.`
		},
		{
			question: 'Kan mine væbnere finde ud af det her?',
			answer: `Ja. Erfaringen er, at væbnere hurtigt finder ind i legen.

Rammerne er tydelige, opgaverne er konkrete, og der er voksne og seniorer omkring dem hele tiden. Det er ikke en konkurrence i at være dygtigst – men i at være kreativ og have det sjovt sammen.`
		},
		{
			question: 'Skal lederne være "på" hele natten?',
			answer: `Nej. Arrangementet er tilrettelagt, så lederne ikke skal være aktive hele tiden.

Kortagekørsel og praktisk koordinering styres centralt. Som leder er der god tid til både at være en del af redaktionen, drikke kaffe og tage pauser.`
		},
		{
			question: 'Hvad laver seniorerne egentlig?',
			answer: `Seniorerne spiller de roller og laver de events, som redaktionerne skal dække.

Nogle seniorer er udvalgt på forhånd til at planlægge events. Andre seniorer får roller tildelt på dagen og indgår i eventafviklingen.

Seniorerne leger andre mennesker – og væbnere og seniorvæbnere leger journalister.`
		},
		{
			question: 'Er events virkelige?',
			answer: `Nej. Alle events er fiktive, men ofte inspireret af aktuelle begivenheder.

Det gør dem genkendelige og sjove at arbejde med, samtidig med at de er tydeligt adskilt fra virkeligheden.`
		},
		{
			question: 'Hvordan foregår transporten til events?',
			answer: `Transporten foregår via et fælles kortagekørselssystem.

• To redaktioner kører sammen
• Kun halvdelen af redaktionen kører ud ad gangen
• Arrangørerne står for koordineringen`
		},
		{
			question: 'Hvad hvis noget går galt teknisk?',
			answer: `Udvalget har sørget for, at der er IT-kyndige frivillige til stede hele natten, som kan hjælpe med:

• Computere
• Video
• Links
• Uploads`
		},
		{
			question: 'Hvem kontakter vi, hvis vi har spørgsmål?',
			answer: `I er altid velkomne til at skrive til:

info@nyhedsnat.dk`
		}
	];

	let openIndex = $state<number | null>(null);

	function toggle(index: number) {
		openIndex = openIndex === index ? null : index;
	}
</script>

<svelte:head>
	<title>FAQ - NyhedsNat i Landsdel 4</title>
	<meta name="description" content="Ofte stillede spørgsmål om Nyhedsnat i Landsdel 4" />
</svelte:head>

<div class="min-h-screen px-4 py-12">
	<div class="max-w-4xl mx-auto">
		<!-- Page Header -->
		<div class="text-center mb-16">
			<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-star-white mb-6">
				<span class="text-gradient-gold">Ofte stillede spørgsmål</span>
			</h1>
			<p class="text-xl text-star-white/60 max-w-2xl mx-auto">
				Find svar på de mest almindelige spørgsmål om Nyhedsnat
			</p>
		</div>

		<!-- FAQ Accordion -->
		<div class="space-y-4">
			{#each faqs as faq, index}
				<div class="card-dark rounded-2xl overflow-hidden">
					<button
						onclick={() => toggle(index)}
						class="w-full px-6 py-5 text-left flex items-center justify-between gap-4 hover:bg-night-700/30 transition-colors"
					>
						<h3 class="text-lg font-medium text-star-white pr-4">{faq.question}</h3>
						<div
							class="w-8 h-8 rounded-full bg-gold-500/20 flex items-center justify-center flex-shrink-0 transition-transform duration-300"
							class:rotate-180={openIndex === index}
						>
							<svg class="w-4 h-4 text-gold-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
								<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
							</svg>
						</div>
					</button>

					{#if openIndex === index}
						<div class="px-6 pb-6 animate-fadeIn">
							<div class="border-t border-gold-500/20 pt-4">
								<p class="text-star-white/70 whitespace-pre-line leading-relaxed">{faq.answer}</p>
							</div>
						</div>
					{/if}
				</div>
			{/each}
		</div>

		<!-- Contact CTA -->
		<div class="mt-16 card-dark rounded-2xl p-8 text-center">
			<h2 class="text-2xl font-bold text-star-white mb-4">Har du flere spørgsmål?</h2>
			<p class="text-star-white/60 mb-6">
				Vi er altid klar til at hjælpe.
			</p>
			<a
				href="/kontakt"
				class="inline-block px-8 py-4 bg-gradient-to-r from-gold-500 to-gold-600 text-night-900 font-bold rounded-full glow-gold hover:scale-105 transition-all"
			>
				Kontakt os
			</a>
		</div>

	</div>
</div>

<style>
	@keyframes fadeIn {
		from {
			opacity: 0;
			transform: translateY(-10px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	.animate-fadeIn {
		animation: fadeIn 0.2s ease-out;
	}
</style>
