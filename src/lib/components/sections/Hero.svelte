<script lang="ts">
	import { Github, Linkedin } from 'lucide-svelte';
</script>

<section
	class="h-full w-full bg-gradient-to-r from-green-800 via-teal-800 to-blue-800 py-12"
	style=""
>
	<div class="container h-full px-4 md:px-6">
		<div class="grid h-full gap-6 lg:grid-cols-[1fr_400px] lg:gap-12 xl:grid-cols-[1fr_600px]">
			<div class="flex flex-col justify-center space-y-4">
				<div class="space-y-2">
					<h1 class="text-2xl font-bold tracking-tighter sm:text-3xl xl:text-4xl/none">
						Hi() {'{'}<br /><span class="pl-8">I'm Tyler Teuber</span><br />{'}'}
					</h1>
					<p class="max-w-[600px] text-gray-50 md:text-xl/relaxed">
						A passionate web developer specializing in front-end development.
					</p>
				</div>
				<div class="flex flex-col items-center gap-2 min-[400px]:flex-row">
					<a
						class="inline-flex h-10 items-center justify-center rounded-md bg-gray-900 px-8 text-sm font-medium text-gray-50 shadow transition-colors hover:bg-gray-900/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-gray-950 disabled:pointer-events-none disabled:opacity-50 dark:bg-gray-50 dark:text-gray-900 dark:hover:bg-gray-50/90 dark:focus-visible:ring-gray-300"
						href="#projects"
					>
						View Portfolio
					</a>
					<a href="https://github.com/TTeuber" target="_blank" rel="noreferrer noopener">
						<Github />
					</a>
					<a
						href="https://www.linkedin.com/in/tyler-teuber"
						target="_blank"
						rel="noreferrer noopener"
					>
						<Linkedin />
					</a>
				</div>
			</div>
			<img
				src="/hero/hero.png"
				width="1024"
				height="1024"
				alt="Web Developer"
				class="mx-auto h-full w-full overflow-hidden rounded-xl object-cover lg:order-last"
			/>
		</div>
	</div>
</section>
