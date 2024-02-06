<script lang="ts">
	import * as Card from '$lib/components/ui/card/index.js';
	import * as HoverCard from '$lib/components/ui/hover-card/index.js';
	import { ArrowUpLeftFromSquare } from 'lucide-svelte';

	export let name: string;
	export let link: string | undefined;
	export let git: string;
	export let img: string;
	export let description: string;
</script>

<Card.Root class="grow basis-1">
	<a href={git} target="_blank" rel="noreferrer noopener">
		<Card.Header class="py-2">
			<Card.Title class="text-center text-xl">{name}</Card.Title>
		</Card.Header>
		<Card.Content class="px-0 pb-0">
			<!--			<h3 class="text-center text-xl">{name}</h3>-->
			<div class="relative">
				<img src={img} alt="lt" />
				<p
					class="absolute inset-0 h-full w-full overflow-scroll bg-background/80 p-3 text-xl opacity-0 transition-all duration-300 ease-in-out hover:opacity-100"
				>
					{description}
					<br />
					{#if link}
						<a href={link} target="_blank" rel="noreferrer noopener" class="hover:underline">
							{link}
							<ArrowUpLeftFromSquare class="ml-1 inline-block h-4 w-4" />
						</a>
					{/if}
				</p>
			</div>
		</Card.Content>
	</a>
</Card.Root>
