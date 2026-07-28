<script lang="ts">
	import { APP_NAME } from '$lib/constants'
</script>

<svelte:head>
	<title>Privacy Policy | {APP_NAME}</title>
</svelte:head>

<section class="mx-auto max-w-3xl px-4 py-16">
	<h1 class="text-3xl font-bold tracking-tight">Privacy Policy</h1>
	<p class="mt-2 text-sm text-muted-foreground">Last updated: July 28, 2026</p>

	<p class="mt-6 text-muted-foreground">
		This Privacy Policy explains what information {APP_NAME} collects and how it is used. We built {APP_NAME} to respect
		your privacy and only collect the minimum information needed to understand how the app is used and improve it over time.
	</p>

	<h2 class="mt-10 text-xl font-semibold">Information We Collect</h2>

	<p class="mt-2 text-muted-foreground">
		{APP_NAME} uses <a href="https://posthog.com" class="underline">PostHog</a>, a third-party analytics service, to
		collect anonymous usage analytics. This may include information such as:
	</p>
	<ul class="mt-2 list-disc space-y-1 ml-6 text-muted-foreground">
		<li>Usage data and interactions within the app</li>
		<li>Device and app information, such as device type, operating system, and app version</li>
		<li>A randomly generated identifier used to recognize repeat usage, which is not tied to your name or email</li>
	</ul>
	<p class="mt-2 text-muted-foreground">
		We do not collect your name, email address, or any personally identifiable data. We do not use any of the data you
		create in the app for advertising or marketing purposes.
	</p>

	<h2 class="mt-10 text-xl font-semibold">How We Use It</h2>
	<p class="mt-2 text-muted-foreground">
		We use this analytics data solely to understand how people use {APP_NAME}, identify bugs, and determine which
		features to improve or build next. We do not sell your information, and we do not share it with third parties other
		than PostHog, which processes it on our behalf.
	</p>
	<h2 class="mt-10 text-xl font-semibold">Data Retention</h2>
	<p class="mt-2 text-muted-foreground">
		Analytics data is retained by PostHog in accordance with their data retention practices. You can learn more in <a
			href="https://posthog.com/privacy"
			class="underline">PostHog's privacy policy</a
		>.
	</p>

	<h2 class="mt-10 text-xl font-semibold">Your Choices</h2>
	<p class="mt-2 text-muted-foreground">
		Because our analytics data is anonymous, we may not be able to identify or delete analytics records for a specific
		individual. If you have questions about your data or would like to make a privacy-related request, please contact us
		at
		<a href="mailto:support@skillmaxapp.com" class="underline">support@skillmaxapp.com</a>, and we will review your
		request.
	</p>

	<h2 class="mt-10 text-xl font-semibold">Changes to This Policy</h2>
	<p class="mt-2 text-muted-foreground">
		We may update this Privacy Policy from time to time. Any changes will be posted on this page with an updated
		revision date.
	</p>

	<h2 class="mt-10 text-xl font-semibold">Contact</h2>
	<p class="mt-2 text-muted-foreground">
		Questions about this policy? Reach out at
		<a href="mailto:support@skillmaxapp.com" class="underline">support@skillmaxapp.com</a>.
	</p>
</section>
