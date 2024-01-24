<script lang="ts">
	import { Sun, Moon } from 'lucide-svelte';
	import { Button } from '$lib/components/ui/button';
	import { toggleMode } from 'mode-watcher';
	import { onMount } from 'svelte';

	const links: { name: string; url: string }[] = [
		{ name: 'Tyler', url: '#home' },
		{ name: 'Projects', url: '#projects' },
		{ name: 'Skills', url: '#skills' }
	];

	let position = 0;
	let ul: HTMLElement;

	onMount(() => {
		window.addEventListener('scroll', () => {
			position = (window.scrollY / (window.innerHeight * 2)) * (ul.clientHeight - 32);
		});
	});
</script>

<nav
	class="sticky top-0 h-screen border-r border-black bg-slate-200 p-6 text-2xl dark:bg-background"
>
	<div class="fixed left-2 h-3 w-3 rounded-full bg-primary" style="top: {position + 33}px" />
	<ul bind:this={ul} class="flex flex-col gap-10">
		{#each links as link}
			<li
				class="uppercase underline-offset-2 shadow-amber-50 hover:text-green-900 dark:hover:text-green-200 dark:hover:[text-shadow:0_0_10px_white]"
			>
				<a href={link.url}>{link.name}</a>
			</li>
		{/each}
	</ul>
</nav>
<Button on:click={toggleMode} variant="outline" size="icon" class="fixed bottom-6 left-6">
	<Sun
		class="h-[1.2rem] w-[1.2rem] rotate-0 scale-100 transition-all dark:-rotate-90 dark:scale-0"
	/>
	<Moon
		class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
	/>
	<span class="sr-only">Toggle theme</span>
</Button>
