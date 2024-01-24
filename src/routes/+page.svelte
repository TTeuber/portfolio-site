<script lang="ts">
	import Skills from '$lib/components/sections/Skills.svelte';
	import Projects from '$lib/components/sections/Projects.svelte';
	import Hero from '$lib/components/sections/Hero.svelte';
</script>

<div class="flex w-full flex-col">
	<div
		id="home"
		class="min-h-screen w-full bg-gradient-to-r from-green-800 via-teal-800 to-blue-800"
	>
		<Hero />
	</div>
	<div
		id="projects"
		class="min-h-screen w-full border-y border-black bg-gradient-to-r from-violet-800 via-purple-800 to-fuchsia-800 p-6"
	>
		<Projects />
	</div>
	<div
		id="skills"
		class="min-h-screen w-full bg-gradient-to-r from-sky-800 via-cyan-800 to-emerald-800 p-6"
	>
		<Skills />
	</div>
</div>
