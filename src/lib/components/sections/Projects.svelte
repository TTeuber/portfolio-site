<script lang="ts">
	import * as Card from '$lib/components/ui/card';
	import Project from '$lib/components/Project.svelte';

	const websites: { name: string; link: string; git: string; img: string; description: string }[] =
		[
			{
				name: 'Lonely Together',
				link: 'https://lonelytogethermusic.com',
				git: 'https://github.com/TTeuber/lonely_together_website',
				img: '/projects/lonelytogether.png',
				description:
					"A website for the band Lonely Together. I built this website using SvelteKit and TailwindCSS. I also used the Spotify API to get the band's music and display it on the website."
			},
			{
				name: 'Post Definitions Podcast',
				link: 'https://postdefinitionpodcast.com',
				git: 'https://github.com/TTeuber/post-definitions-website',
				img: '/projects/postdefinitions.png',
				description:
					"A website for the Post Definitions Podcast. I built this website using SvelteKit and TailwindCSS. I also used the Spotify API to get the band's music and display it on the website."
			},
			{
				name: 'Tyler Teuber',
				link: 'https://tylerteuber.com',
				git: '',
				img: '/projects/portfolio.png',
				description:
					"A website for myself. I built this website using SvelteKit and TailwindCSS. I also used the Spotify API to get the band's music and display it on the website."
			}
		];

	const projects: { name: string; git: string; img: string }[] = [
		{
			name: 'Chat Controlled Todo App',
			git: '',
			img: ''
		},
		{
			name: 'Web Developer Assistant',
			git: '',
			img: ''
		},
		{
			name: 'Habit Percentage Tracker',
			git: '',
			img: ''
		}
	];
</script>

<Card.Root class="h-full">
	<Card.Header>
		<Card.Title class="text-center text-3xl">Projects and Websites</Card.Title>
	</Card.Header>
	<Card.Content class="flex flex-col gap-6">
		<!--		<p class="border-t py-6 text-center text-3xl">Websites</p>-->
		<div class="flex justify-evenly gap-4">
			{#each websites as website}
				<Project {...website} />
			{/each}
		</div>
		<div class="flex justify-evenly gap-4">
			{#each websites as website}
				<Project {...website} />
			{/each}
		</div>
	</Card.Content>
</Card.Root>
