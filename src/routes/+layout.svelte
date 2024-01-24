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
