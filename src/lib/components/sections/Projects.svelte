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
					'A website for the band Lonely Together. I built this website using SvelteKit and SASS. I also used Sendgrid for the email contact form.'
			},
			{
				name: 'Post Definitions Podcast',
				link: 'https://postdefinitionpodcast.com',
				git: 'https://github.com/TTeuber/post-definitions-website',
				img: '/projects/postdefinitions.png',
				description:
					"A website for the Post Definitions Podcast. I built this website using React, Next.js, and TailwindCSS. I also used the YouTube API to get the podcast's videos and display them on the website."
			},
			{
				name: 'Tyler Teuber',
				link: 'https://tylerteuber.com',
				git: '',
				img: '/projects/portfolio.png',
				description:
					'The portfolio website that you are currently viewing. I built this website using SvelteKit and TailwindCSS.'
			}
		];

	const projects: {
		name: string;
		link: string | undefined;
		description: string;
		git: string;
		img: string;
	}[] = [
		{
			name: 'Chat Controlled Todo App',
			git: 'https://github.com/TTeuber/chat_controlled_todo',
			description:
				'A todo app controlled completely using a chat interface. This project uses the function calling functionality from the ChaptGPT api. This app was built using Python, Flask, and HTMX',
			img: '/projects/chatcontrol.png',
			link: undefined
		},
		{
			name: 'Web Developer Assistant',
			description:
				'An AI chat assistant for answering questions about web development. This project was built using Angular and SASS on the frontend, .NET Core and Entity Framework on the backend, and the ChatGPT API',
			git: 'https://github.com/TTeuber/web-dev-assistant',
			img: '/projects/webdevassistant.png',
			link: undefined
		},
		{
			name: 'Multi-Media Website',
			description:
				'A website for displaying my music and photography. This project was built using React, Next.js, and Tailwind',
			git: 'https://github.com/TTeuber/portfolio_website',
			img: '/projects/multimedia.png',
			link: 'portfolio-website-ljhe5ib8o-tteuber.vercel.app'
		}
	];
</script>

<Card.Root class="h-full">
	<Card.Header>
		<Card.Title class="text-center text-3xl">Projects and Websites</Card.Title>
	</Card.Header>
	<Card.Content class="flex flex-col gap-6">
		<div class="flex justify-evenly gap-4">
			{#each websites as website}
				<Project {...website} />
			{/each}
		</div>
		<div class="flex justify-evenly gap-4">
			{#each projects as project}
				<Project {...project} />
			{/each}
		</div>
	</Card.Content>
</Card.Root>
