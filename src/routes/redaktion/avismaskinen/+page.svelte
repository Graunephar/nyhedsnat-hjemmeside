<script lang="ts">
	import JoinButton from '$lib/components/JoinButton.svelte';
</script>

<svelte:head>
	<title>Avismaskinen – NyhedsNat</title>
</svelte:head>

<div>
	<p class="mb-6 text-star-white/70">Brug Avismaskinen til at samle jeres sider og gøre avisen klar til aflevering.</p>

	<JoinButton href="https://www.avismaskinen.dk" target="_blank" rel="noopener noreferrer" className="mb-6">
		Åbn Avismaskinen
	</JoinButton>

	<ul class="space-y-2 text-star-white/75">
		<li>• Lav jeres forside</li>
		<li>• Tilføj artikler</li>
		<li>• Færdiggør avisen</li>
	</ul>
</div>