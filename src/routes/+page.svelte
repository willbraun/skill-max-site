<script lang="ts">
	import appleLogo from '$lib/assets/images/icons/apple-logo.svg'
	import editCategoryScreenshot from '$lib/assets/images/screenshots/edit-category.png'
	import historyScreenshot from '$lib/assets/images/screenshots/history.png'
	import homeScreenshot from '$lib/assets/images/screenshots/home.png'
	import liveActivityScreenshot from '$lib/assets/images/screenshots/live-activity.png'
	import startScreenshot from '$lib/assets/images/screenshots/start.png'
	import widgetsScreenshot from '$lib/assets/images/screenshots/widgets.png'
	import { APP_NAME, APP_URL } from '$lib/constants'

	type Screenshot = {
		image: string
		feature: string
	}

	const screenshots: Screenshot[] = [
		{
			image: editCategoryScreenshot,
			feature: 'Set Goals for Any Skill',
		},
		{
			image: homeScreenshot,
			feature: 'Get Recommendations',
		},
		{
			image: startScreenshot,
			feature: 'Log Practice Sessions',
		},
		{
			image: liveActivityScreenshot,
			feature: 'Monitor Your Sessions Easily',
		},
		{
			image: widgetsScreenshot,
			feature: 'Prepare With Widgets',
		},
		{
			image: historyScreenshot,
			feature: 'View History',
		},
	]
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

<section class="relative mx-auto max-w-5xl px-4 py-16 text-center grid sm:grid-cols-2 gap-16 sm:gap-2 items-center">
	<div class="grow flex flex-col items-center justify-center gap-4">
		<h1 class="text-6xl font-bold text-foreground">Know what to practice next</h1>
		<p class="mt-4 max-w-xl text-lg text-muted-foreground">
			Organize your goals, track your practice time, and get personalized recommendations to keep improving
		</p>
		<div class="mt-8 flex justify-center">
			<a href={APP_URL} target="_blank" rel="noopener noreferrer">
				<button
					class="group relative overflow-hidden shadow-lg hover:shadow-success/20 transition-transform hover:scale-105 flex items-center gap-2 rounded-full bg-primary px-6 py-3 text-lg font-semibold text-primary-foreground cursor-pointer"
				>
					<span
						class="absolute inset-0 origin-left scale-x-0 bg-success transition-transform duration-500 ease-out group-hover:scale-x-100 rounded-full"
					></span>
					<div class="relative flex mb-0.5 items-center aspect-square w-4 invert">
						<img src={appleLogo} alt="Apple logo" />
					</div>
					<p class="relative text-lg">Download on iOS</p>
				</button>
			</a>
		</div>
		<div class="text-sm text-start text-muted-foreground">
			<ul>
				{#each ['Free to use', 'No ads', 'No subscription', 'No account'] as item}
					{@render listItem(item)}
				{/each}
			</ul>
		</div>
	</div>
	<div
		class="flex items-center mx-auto overflow-hidden justify-center rounded-[32px] sm:rounded-[36px] border w-64 sm:w-72"
	>
		<img src={homeScreenshot} alt="Screenshot of the app" />
	</div>
</section>

<section class="mx-auto max-w-5xl px-4 py-16">
	<h2 class="text-4xl text-center sm:text-start font-bold mb-2">Your Path to Improvement</h2>
	<p class="text-lg text-muted-foreground text-center sm:text-start">Everything you need to get better</p>
	<div class="mt-8 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-12">
		{#each screenshots as screenshot, i}
			<div class="flex flex-col items-center gap-2">
				<div class="flex mb-2 w-64 mx-auto h-115 items-center justify-center rounded-[32px] border overflow-hidden">
					<img
						src={screenshot.image}
						alt={screenshot.feature}
						class="w-full h-[calc(100%+40px)] object-cover object-top -translate-y-5"
					/>
				</div>
				<p class="text-center text-lg text-foreground">{screenshot.feature}</p>
			</div>
		{/each}
	</div>
</section>

<section class="mx-auto max-w-5xl px-4 pt-16 md:pb-32 pb-16">
	<h2 class="text-4xl text-center sm:text-start font-bold mb-2">Why I Built Skill Max</h2>
	<p class="text-lg text-muted-foreground text-center sm:text-start">
		I originally built Skill Max for myself as a chess improvement tool. My goal was to eliminate the decision fatigue
		of figuring out what to practice next. As I used it, I realized the same approach could help with learning any
		skill, from music to coding to languages. I've already found it helpful, and I hope you will too.
	</p>
</section>
