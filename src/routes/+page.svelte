<script lang="ts">
	import Skills from '$lib/components/Skills.svelte';
</script>

<div class="flex w-full flex-col">
	<div id="home" class="min-h-screen w-full bg-blue-200 p-6 dark:bg-teal-900">
		<p>home</p>
	</div>
	<div
		id="projects"
		class="min-h-screen w-full border-y border-black bg-violet-200 p-6 dark:bg-violet-900"
	>
		<p>projects</p>
	</div>
	<div id="skills" class="bg min-h-screen w-full bg-sky-200 p-6 dark:bg-sky-900">
		<Skills />
	</div>
</div>
