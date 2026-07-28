<script lang="ts">
	import { APP_NAME, SITE_URL } from '$lib/constants'

	const description = `Find answers to common questions about ${APP_NAME}, or get in touch with support.`
</script>

<svelte:head>
	<title>Support | {APP_NAME}</title>
	<meta name="description" content={description} />
	<link rel="canonical" href="{SITE_URL}/support" />
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Support | {APP_NAME}" />
	<meta property="og:description" content={description} />
	<meta property="og:url" content="{SITE_URL}/support" />
</svelte:head>

<section class="mx-auto max-w-3xl px-4 py-16">
	<h1 class="text-3xl font-bold tracking-tight">Support</h1>
	<p class="mt-4 text-muted-foreground">
		Need help with {APP_NAME}? Find answers to common questions below, or reach out to us directly.
	</p>

	<h2 class="mt-10 text-xl font-semibold">Frequently Asked Questions</h2>

	<div class="mt-4 space-y-6">
		<div>
			<h3 class="font-medium">What skills can I add?</h3>
			<p class="mt-1 text-muted-foreground">
				Anything! {APP_NAME} is designed to work with any skill, including music, languages, sports, games, and more. You
				can add as many skills as you want.
			</p>
		</div>

		<div>
			<h3 class="font-medium">How do I add a skill?</h3>
			<p class="mt-1 text-muted-foreground">
				The first time you load the app, you'll see an "Add Skill" button. Tap it to create your first skill. You must
				choose at least one category with a weekly goal of practice time.
			</p>
			<p class="mt-4 text-muted-foreground">
				You can also add, edit, and reorder skills later from the home screen by tapping the "Manage" button.
			</p>
		</div>

		<div>
			<h3 class="font-medium">What are categories?</h3>
			<p class="mt-1 text-muted-foreground">
				Categories let you split a skill into the individual areas you want to improve. For example, a "Guitar" skill
				might have categories like "Chords", "Scales", and "Songs". Time is tracked separately for each category.
			</p>
		</div>

		<div>
			<h3 class="font-medium">How does time tracking work?</h3>
			<p class="mt-1 text-muted-foreground">
				Start a timer for any category when you begin practicing, and stop it when you're done. You may track live
				sessions or manually enter past sessions. {APP_NAME} keeps a history of your sessions and uses it to recommend what
				to work on next.
			</p>
		</div>

		<div>
			<h3 class="font-medium">How are recommendations chosen?</h3>
			<p class="mt-1 text-muted-foreground">
				{APP_NAME} looks at your tracked time across all categories and chooses the one that has the lowest percentage of
				your weekly goal completed. This helps you focus on the areas that need the most attention.
			</p>
		</div>

		<div>
			<h3 class="font-medium">Can I edit or delete a skill or category?</h3>
			<p class="mt-1 text-muted-foreground">
				Yes. Tap "Manage" to edit the list of skills or "Edit" on the skill directly to edit or delete it. When editing
				a skill, tap a category to edit or delete it. Session history will remain intact even if you delete a skill or
				category.
			</p>
		</div>

		<div>
			<h3 class="font-medium">Can I edit a session?</h3>
			<p class="mt-1 text-muted-foreground">
				No. However, you may delete and re-add a session if you need to make changes. Sessions added retroactively will
				be counted toward your weekly goal for the week they are dated, not necessarily the current week.
			</p>
			<ol class="mt-1 ml-6 text-muted-foreground list-decimal">
				<li>To delete a session, tap the session in the history list and select "Delete".</li>
				<li>
					To add a session, tap the category, select "Log a previous session", select the time, and tap "Log Session".
				</li>
			</ol>
		</div>

		<div>
			<h3 class="font-medium">Is my data backed up?</h3>
			<p class="mt-1 text-muted-foreground">
				No. All data is stored locally on your device. If you delete the app or lose your device, your tracked time will
				be lost.
			</p>
		</div>

		<div>
			<h3 class="font-medium">Is this available for Android?</h3>
			<p class="mt-1 text-muted-foreground">
				Not yet. {APP_NAME} is currently only available for iOS devices. I may release an Android version in the future,
				but I don't have a timeline for that yet.
			</p>
		</div>
	</div>

	<h2 class="mt-10 text-xl font-semibold">Contact us</h2>
	<p class="mt-2 text-muted-foreground">
		Can't find what you're looking for, or run into a bug? Feel free to submit anonymous feedback via the Feedback form
		on the Settings page of the app, or reach out at
		<a href="mailto:support@skillmaxapp.com" class="underline">support@skillmaxapp.com</a>
		and I'll get back to you as soon as I can.
	</p>
</section>
