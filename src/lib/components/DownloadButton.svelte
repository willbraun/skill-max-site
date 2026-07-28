<script lang="ts">
	import { Button } from '$lib/components/ui/button'
	import { APP_NAME, APP_URL } from '$lib/constants'
	import { cn } from '$lib/utils'

	let { class: className }: { class?: string } = $props()
</script>

<Button
	href={APP_URL}
	target="_blank"
	rel="noopener noreferrer"
	class={cn(
		'group relative overflow-hidden shadow-lg hover:shadow-success/20 transition-transform hover:scale-105 flex items-center gap-2 p-4',
		className,
	)}
>
	<span
		class="absolute inset-0 origin-left scale-x-0 bg-success transition-transform duration-500 ease-out group-hover:scale-x-100 rounded-full"
	></span>
	<p class="relative text-sm">Download {APP_NAME}</p>
</Button>
