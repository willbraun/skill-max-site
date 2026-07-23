<script lang="ts">
	import { page } from '$app/state'
	import { Button } from '$lib/components/ui/button'
	import * as Sheet from '$lib/components/ui/sheet'
	import { cn } from '$lib/utils'
	import MenuIcon from '@lucide/svelte/icons/menu'

	const navLinks = [
		{ href: '/', label: 'Home' },
		{ href: '/support', label: 'Support' },
		{ href: '/privacy-policy', label: 'Privacy Policy' },
	]

	let open = $state(false)
</script>

<header class="border-b bg-background">
	<div class="mx-auto flex h-16 max-w-5xl items-center justify-between px-4">
		<a href="/" class="font-semibold">Skill Max</a>

		<nav class="hidden items-center gap-6 md:flex">
			{#each navLinks as link (link.href)}
				<a
					href={link.href}
					class={cn(
						'text-sm transition-colors hover:text-foreground',
						page.url.pathname === link.href ? 'text-foreground font-medium' : 'text-muted-foreground',
					)}
				>
					{link.label}
				</a>
			{/each}
		</nav>

		<Sheet.Root bind:open>
			<Sheet.Trigger class="md:hidden">
				{#snippet child({ props })}
					<Button {...props} variant="ghost" size="icon" aria-label="Open menu">
						<MenuIcon class="size-6" />
					</Button>
				{/snippet}
			</Sheet.Trigger>
			<Sheet.Content side="right">
				<nav class="flex flex-col gap-4 px-6 pt-6">
					{#each navLinks as link (link.href)}
						<a
							href={link.href}
							onclick={() => (open = false)}
							class={cn(
								'text-base',
								page.url.pathname === link.href ? 'text-foreground font-medium' : 'text-muted-foreground',
							)}
						>
							{link.label}
						</a>
					{/each}
				</nav>
			</Sheet.Content>
		</Sheet.Root>
	</div>
</header>
