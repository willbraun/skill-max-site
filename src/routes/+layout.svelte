<script lang="ts">
	import androidIcon144 from '$lib/assets/favicons/android-icon-144x144.png'
	import androidIcon192 from '$lib/assets/favicons/android-icon-192x192.png'
	import androidIcon36 from '$lib/assets/favicons/android-icon-36x36.png'
	import androidIcon48 from '$lib/assets/favicons/android-icon-48x48.png'
	import androidIcon72 from '$lib/assets/favicons/android-icon-72x72.png'
	import androidIcon96 from '$lib/assets/favicons/android-icon-96x96.png'
	import appleIcon114 from '$lib/assets/favicons/apple-icon-114x114.png'
	import appleIcon120 from '$lib/assets/favicons/apple-icon-120x120.png'
	import appleIcon144 from '$lib/assets/favicons/apple-icon-144x144.png'
	import appleIcon152 from '$lib/assets/favicons/apple-icon-152x152.png'
	import appleIcon180 from '$lib/assets/favicons/apple-icon-180x180.png'
	import appleIcon57 from '$lib/assets/favicons/apple-icon-57x57.png'
	import appleIcon60 from '$lib/assets/favicons/apple-icon-60x60.png'
	import appleIcon72 from '$lib/assets/favicons/apple-icon-72x72.png'
	import appleIcon76 from '$lib/assets/favicons/apple-icon-76x76.png'
	import appleIconPrecomposed from '$lib/assets/favicons/apple-icon-precomposed.png'
	import appleIcon from '$lib/assets/favicons/apple-icon.png'
	import favicon16 from '$lib/assets/favicons/favicon-16x16.png'
	import favicon32 from '$lib/assets/favicons/favicon-32x32.png'
	import favicon96 from '$lib/assets/favicons/favicon-96x96.png'
	import msIcon144 from '$lib/assets/favicons/ms-icon-144x144.png'
	import Footer from '$lib/components/Footer.svelte'
	import Header from '$lib/components/Header.svelte'
	import './layout.css'

	let { children } = $props()
</script>

<svelte:head>
	<link rel="apple-touch-icon" href={appleIcon} />
	<link rel="apple-touch-icon-precomposed" href={appleIconPrecomposed} />
	<link rel="apple-touch-icon" sizes="57x57" href={appleIcon57} />
	<link rel="apple-touch-icon" sizes="60x60" href={appleIcon60} />
	<link rel="apple-touch-icon" sizes="72x72" href={appleIcon72} />
	<link rel="apple-touch-icon" sizes="76x76" href={appleIcon76} />
	<link rel="apple-touch-icon" sizes="114x114" href={appleIcon114} />
	<link rel="apple-touch-icon" sizes="120x120" href={appleIcon120} />
	<link rel="apple-touch-icon" sizes="144x144" href={appleIcon144} />
	<link rel="apple-touch-icon" sizes="152x152" href={appleIcon152} />
	<link rel="apple-touch-icon" sizes="180x180" href={appleIcon180} />
	<link rel="icon" type="image/png" sizes="36x36" href={androidIcon36} />
	<link rel="icon" type="image/png" sizes="48x48" href={androidIcon48} />
	<link rel="icon" type="image/png" sizes="72x72" href={androidIcon72} />
	<link rel="icon" type="image/png" sizes="96x96" href={androidIcon96} />
	<link rel="icon" type="image/png" sizes="144x144" href={androidIcon144} />
	<link rel="icon" type="image/png" sizes="192x192" href={androidIcon192} />
	<link rel="icon" type="image/png" sizes="16x16" href={favicon16} />
	<link rel="icon" type="image/png" sizes="32x32" href={favicon32} />
	<link rel="icon" type="image/png" sizes="96x96" href={favicon96} />
	<meta name="msapplication-TileImage" content={msIcon144} />
	<meta name="msapplication-TileColor" content="#ffffff" />
	<meta name="theme-color" content="#ffffff" />
</svelte:head>
<div class="flex min-h-svh flex-col">
	<Header />
	<main class="flex-1">
		{@render children()}
	</main>
	<Footer />
</div>
