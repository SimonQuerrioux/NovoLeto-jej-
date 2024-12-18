<script lang="ts">
	import { page } from '$app/stores';
	import '../app.css';

	/**
	 * NALOGA:
	 * 	- Dodaj linke do vseh treh strani (/prva, /druga, /tretja)
	 * 		(Nasvet: <div> bo potrebno zamenjati z <a>)
	 *
	 * DODATNA NALOGA:
	 * - Link do trenutne strani naj se odebeli (npr. Če se nahajamo na /druga, bo "Druga" odebeljeno, "Prva" in "Tretja" pa ne)
	 */
</script>

<nav class="w-full h-24 bg-sky-300 flex items-center justify-center gap-5">
	<div><a href="/" class={$page.url.pathname === '/' ? 'font-bold' : ''}>Domov</a></div>
	<div>
		<a href="/prva" class={$page.url.pathname === '/prva' ? 'font-bold' : ''}>Prva</a>
	</div>
	<div><a href="/druga" class={$page.url.pathname === '/druga' ? 'font-bold' : ''}>Druga</a></div>
	<div>
		<a href="/tretja" class={$page.url.pathname === '/tretja' ? 'font-bold' : ''}>Tretja</a>
	</div>
</nav>

<div class="p-5 h-full">
	<slot />
</div>
