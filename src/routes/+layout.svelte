<script>
	import '../app.pcss';
	import { ModeWatcher } from 'mode-watcher';
	import Nav from '$lib/components/Nav.svelte';
</script>

<ModeWatcher />
<div class="flex">
	<Nav />
	<slot />
</div>

<style lang="postcss">
	:global(h1, h2) {
		font-family: 'Rubik Mono One', sans-serif;
		font-size: 1rem;
	}
</style>
