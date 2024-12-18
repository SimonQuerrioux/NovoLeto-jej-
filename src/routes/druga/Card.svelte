<script lang="ts">
	import type { Category } from './data';

	export let category: Category;
</script>

<div class="bg-slate-400 rounded-xl h-full border-2 border-slate-900 p-3">
	<h1>{category.name}</h1>
	<img src={category.image} />
	<p class="text-white bg-slate-500 rounded-xl p-2">{category.description}</p>
</div>
