<script lang="ts">
	import ACard from './ACard.svelte';
	import { animals, type Animal } from './animals';
	let searchAnimal: string = '';
</script>

<h1 class="font-bold uppercase text-5xl text-center m-5">ŽIVALI</h1>
<div class="flex flex-col justify-items-stretch">
	<input
		class="rounded-xl p-2 m-2 border border-2 border-gray-500"
		placeholder="Search animal by name"
		type="text"
		bind:value={searchAnimal}
	/>
</div>

<div class="grid grid-cols-3">
	{#each animals as animal}
		<ACard {animal}></ACard>
	{/each}
</div>
