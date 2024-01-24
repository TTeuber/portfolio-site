<script lang="ts">
	import skills from '../../../skills.json';
	import { Button } from '$lib/components/ui/button';
	import * as Card from '$lib/components/ui/card';

	let selection: string = 'JavaScript/TypeScript';
</script>

<Card.Root class="flex h-full flex-col border border-black">
	<Card.Header>
		<Card.Title class="text-center text-3xl">Skills</Card.Title>
		<!--		<Card.Description class="text-center">{selection}</Card.Description>-->
	</Card.Header>
	<Card.Content class="flex grow flex-col">
		<span class="mb-6 border-t pt-6 text-center text-3xl">Languages</span>
		<div class="flex h-full grow items-center justify-evenly border-b">
			{#each skills.languages as skill}
				<button class="group relative h-48 w-48" on:click={() => (selection = skill.language)}>
					<div class="flex flex-col items-center justify-center gap-4">
						<img src="/logos/{skill.logo}" alt={skill.language} class="h-20 w-20" />
						<span class="text-xl {selection === skill.language ? 'underline' : ''}"
							>{skill.language}</span
						>
					</div>
				</button>
			{/each}
		</div>
		<div class="m-6 flex grow flex-col">
			<span class="mb-6 text-center text-3xl">{selection} Frameworks</span>
			<div class="flex flex justify-evenly">
				{#each skills.languages as skill}
					{#if skill.language === selection}
						{#each skill.frameworks as framework}
							<div class="flex flex-col items-center justify-center gap-4">
								<img src="/logos/{framework.logo}" alt={framework.framework} class="h-20 w-20" />
								<span class="text-xl">{framework.framework}</span>
							</div>
							{#if framework.tools}
								{#each framework.tools as tool}
									<div class="flex flex-col items-center justify-center gap-4">
										<img src="/logos/{tool.logo}" alt={tool.tool} class="h-20 w-20" />
										<span class="text-xl">{tool.tool}</span>
									</div>
								{/each}
							{/if}
						{/each}
					{/if}
				{/each}
			</div>
		</div>
	</Card.Content>
</Card.Root>
