<script lang="ts">
	import { Button } from '$lib/components/ui/button'
</script>

<svelte:head>
	<title>Skill Max</title>
</svelte:head>

<section class="relative mx-auto max-w-5xl px-4 py-16 text-center">
	<div class="grow flex flex-col items-center justify-center gap-4">
		<h1 class="text-6xl font-bold tracking-tight text-primary">Skill Max</h1>
		<p class="mt-4 max-w-xl text-lg text-muted-foreground">
			Placeholder tagline describing what Skill Max helps you do, in one or two sentences.
		</p>
		<div class="mt-8 flex justify-center">
			<Button
				href="#"
				size="lg"
				class="group relative overflow-hidden shadow-lg hover:shadow-success/20 transition-transform hover:scale-105"
			>
				<span
					class="absolute inset-0 origin-left scale-x-0 bg-success transition-transform duration-500 ease-out group-hover:scale-x-100 rounded-full"
				></span>
				<span class="relative">Download on the App Store</span>
			</Button>
		</div>
	</div>
</section>

<section class="mx-auto max-w-5xl px-4 pb-16">
	<div class="mt-8 grid grid-cols-2 gap-4 sm:grid-cols-3 md:grid-cols-4">
		{#each Array(4) as _, i (i)}
			<div
				class="flex aspect-9/16 items-center justify-center rounded-lg border bg-muted text-sm text-muted-foreground transition-transform duration-200 hover:-translate-y-1 hover:rotate-1 hover:shadow-lg"
			>
				Screenshot {i + 1}
			</div>
		{/each}
	</div>
</section>
