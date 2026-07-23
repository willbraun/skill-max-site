<script lang="ts">
	import { Button } from '$lib/components/ui/button'
</script>

<svelte:head>
	<title>Skill Max</title>
</svelte:head>

<section class="mx-auto max-w-5xl px-4 py-16 text-center">
	<h1 class="text-4xl font-bold tracking-tight">Skill Max</h1>
	<p class="mx-auto mt-4 max-w-xl text-lg text-muted-foreground">
		Placeholder tagline describing what Skill Max helps you do, in one or two sentences.
	</p>
	<div class="mt-8 flex justify-center">
		<Button href="#" size="lg">Download on the App Store</Button>
	</div>
</section>

<section class="mx-auto max-w-5xl px-4 py-16">
	<h2 class="text-center text-2xl font-semibold">Screenshots</h2>
	<div class="mt-8 grid grid-cols-2 gap-4 sm:grid-cols-3 md:grid-cols-4">
		{#each Array(4) as _, i (i)}
			<div
				class="flex aspect-9/16 items-center justify-center rounded-lg border bg-muted text-sm text-muted-foreground"
			>
				Screenshot {i + 1}
			</div>
		{/each}
	</div>
</section>
