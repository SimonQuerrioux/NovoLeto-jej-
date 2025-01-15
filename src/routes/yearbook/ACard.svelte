<script lang="ts">
	export let animal;
</script>

<div class="p-4 m-2 broder border-black border-2 rounded-xl hover:bg-gray-200">
	<p class="font-bold uppercase text-l">{animal.name}</p>
	<p class="italic text-s text-gray-500">{animal.latinName}, {animal.class}</p>

	<div class="p-2">
		<img class="rounded-xl" src={animal.photo} />
		<div class="p-2">
			<p>Weight: {animal.weight}</p>
			<p>Lifespan: {animal.lifespan}</p>
		</div>
	</div>
</div>
