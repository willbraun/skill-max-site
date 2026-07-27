<script lang="ts">
	import AppleLogo from '$lib/assets/images/apple-logo.svg'
	import { Button } from '$lib/components/ui/button'
	import { APP_NAME } from '$lib/constants'
</script>

<svelte:head>
	<title>{APP_NAME}</title>
</svelte:head>

<section class="relative mx-auto max-w-5xl px-4 py-16 text-center">
	<div class="grow flex flex-col items-center justify-center gap-4">
		<h1 class="text-6xl font-bold tracking-tight text-primary">{APP_NAME}</h1>
		<p class="mt-4 max-w-xl text-lg text-muted-foreground">
			Placeholder tagline describing what {APP_NAME} helps you do, in one or two sentences.
		</p>
		<div class="mt-8 flex justify-center">
			<Button
				href="#"
				size="lg"
				class="group relative overflow-hidden shadow-lg hover:shadow-success/20 transition-transform hover:scale-105 flex items-center gap-2"
			>
				<span
					class="absolute inset-0 origin-left scale-x-0 bg-success transition-transform duration-500 ease-out group-hover:scale-x-100 rounded-full"
				></span>
				<div class="relative flex mb-0.5 items-center aspect-square w-4 invert">
					<img src={AppleLogo} alt="Apple logo" />
				</div>
				<p class="relative text-lg">Download on iOS</p>
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
