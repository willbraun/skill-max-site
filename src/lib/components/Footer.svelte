<script lang="ts">
	import DownloadButton from '$lib/components/DownloadButton.svelte'
	import { Separator } from '$lib/components/ui/separator'

	const navLinks = [
		{ href: '/support', label: 'Support' },
		{ href: '/privacy-policy', label: 'Privacy Policy' },
	]
</script>

<footer class="mt-auto">
	<Separator />
	<div
		class="mx-auto flex max-w-5xl flex-col items-center gap-4 px-4 py-8 text-sm text-muted-foreground sm:flex-row sm:justify-between"
	>
		<DownloadButton class="md:hidden" />
		<p>&copy; {new Date().getFullYear()} Will Braun. All rights reserved.</p>
		<nav class="flex items-center gap-4">
			{#each navLinks as link (link.href)}
				<a href={link.href} class="hover:text-foreground">{link.label}</a>
			{/each}
		</nav>
	</div>
</footer>
