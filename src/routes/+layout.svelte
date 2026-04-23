<script>
	import favicon from "$lib/assets/favicon.svg";

	import "$lib/styles/reset.css";
	import "$lib/styles/tokens/tokens.css";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />

	<link rel="preconnect" href="https://use.typekit.net" />
	<link rel="stylesheet" href="https://use.typekit.net/ukz2bfk.css" />
</svelte:head>

{@render children()}
