<script lang="ts">
	import AppleLogo from '$lib/assets/images/apple-logo.svg'
	import { APP_NAME } from '$lib/constants'

	type Screenshot = {
		image: string
		feature: string
	}

	const screenshots: Screenshot[] = [
		{
			image: '/screenshot1.png',
			feature: 'Feature 1',
		},
	]

	// TODO - View Recommendations, Customize Goals, Track Time, Manage From Lock Screen, View History, Use Widgets
</script>

<svelte:head>
	<title>{APP_NAME}</title>
</svelte:head>

{#snippet listItem(name: string)}
	<li class="flex items-center gap-2">
		<!-- check icon -->
		<svg
			fill="currentColor"
			version="1.1"
			id="Capa_1"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			width="14px"
			height="14px"
			viewBox="0 0 78.369 78.369"
			xml:space="preserve"
		>
			<g>
				<path
					d="M78.049,19.015L29.458,67.606c-0.428,0.428-1.121,0.428-1.548,0L0.32,40.015c-0.427-0.426-0.427-1.119,0-1.547l6.704-6.704
		c0.428-0.427,1.121-0.427,1.548,0l20.113,20.112l41.113-41.113c0.429-0.427,1.12-0.427,1.548,0l6.703,6.704
		C78.477,17.894,78.477,18.586,78.049,19.015z"
				/>
			</g>
		</svg>
		<p>{name}</p>
	</li>
{/snippet}

<section class="relative mx-auto max-w-5xl px-4 py-16 text-center grid grid-cols-2 items-center">
	<div class="grow flex flex-col items-center justify-center gap-4">
		<h1 class="text-6xl font-bold text-foreground">Know what to practice next</h1>
		<p class="mt-4 max-w-xl text-lg text-muted-foreground">
			Organize your goals, track your practice time, and get personalized recommendations to keep improving
		</p>
		<div class="mt-8 flex justify-center">
			<button
				class="group relative overflow-hidden shadow-lg hover:shadow-success/20 transition-transform hover:scale-105 flex items-center gap-2 rounded-full bg-primary px-6 py-3 text-lg font-semibold text-primary-foreground cursor-pointer"
			>
				<span
					class="absolute inset-0 origin-left scale-x-0 bg-success transition-transform duration-500 ease-out group-hover:scale-x-100 rounded-full"
				></span>
				<div class="relative flex mb-0.5 items-center aspect-square w-4 invert">
					<img src={AppleLogo} alt="Apple logo" />
				</div>
				<p class="relative text-lg">Download on iOS</p>
			</button>
		</div>
		<div class="text-sm text-start text-muted-foreground">
			<ul>
				{#each ['Free to use', 'No ads', 'No subscription', 'No account'] as item}
					{@render listItem(item)}
				{/each}
			</ul>
		</div>
	</div>
	<div class="flex aspect-9/16 items-center mx-auto justify-center rounded-2xl border bg-muted w-64">Screenshot</div>
</section>

<section class="mx-auto max-w-5xl px-4 pb-16">
	<h2 class="text-4xl font-bold">Your path to improvement</h2>
	<div class="mt-8 grid grid-cols-2 gap-4 sm:grid-cols-3 md:grid-cols-4">
		{#each screenshots as screenshot, i}
			<div>
				<div class="flex aspect-9/16 mb-2 items-center justify-center rounded-lg border bg-muted">
					<img src={screenshot.image} alt="Screenshot {i + 1}" />
				</div>
				<p class="text-center text-sm text-muted-foreground">{screenshot.feature}</p>
			</div>
		{/each}
	</div>
</section>
