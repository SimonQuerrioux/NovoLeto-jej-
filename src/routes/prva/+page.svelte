<script lang="ts">
	let stevilo = 0;
	let sodo = true;

	function jeSodo(num: number) {
		return num % 2 == 0;
	}
	function RNumber() {
		stevilo = Math.floor(Math.random() * 100000000);
	}

	$: {
		sodo = jeSodo(stevilo);
	}

	/**
	 * NALOGA:
	 * 	- Dodaj <input> za vnos števila
	 *  - Definiraj spremenljivko "num" in jo "poveži" z <input> (Nasvet: uporabi bind:value)
	 *  - Če je num sodo, izpiši "Število je sodo", če je liho, izpiši "Število je liho"
	 *
	 * DODATNA NALOGA:
	 *  - Dodaj <button> s tekstom "Random"
	 *  - Po kliku na "Random" naj se num nastavi na naključno število med 1 in 100000000
	 */
</script>

<div class="flex flex-col gap-10 items-center justify-center pt-20 bg-slate-300 pb-10 rounded-2xl">
	<div class="flex">
		<input
			bind:value={stevilo}
			class="border-2 border-blue-500 m-3 p-2 rounded-3xl text-4xl text-center"
			type="number"
		/>
	</div>
	<div class="flex">
		<div>
			<p class="bg-white border-2 border-blue-500 m-3 p-2 rounded-3xl text-4xl text-center">
				{sodo ? 'SODO' : 'LIHO'}
			</p>
		</div>
		1
		<div>
			<button
				class="bg-white border-2 border-blue-500 m-3 p-2 rounded-3xl text-4xl text-center hover:bg-slate-200 duration-500 transition-colors"
				on:click={RNumber}>Naključno število</button
			>
		</div>
	</div>
</div>
