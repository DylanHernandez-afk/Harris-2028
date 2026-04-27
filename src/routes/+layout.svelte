<script>
	import favicon from "$lib/assets/favicon.svg";

	import "$lib/styles/reset.css";
	import "$lib/styles/tokens/tokens.css";

	let { children } = $props();
</script>

<style global>
	:global(body) {
		background-color: var(--background-primary);
		margin: 0;
		padding: 0;
	}
	:global(main) {
		width: 100%;
		background-color: var(--background-primary);
	}
</style>

<svelte:head>
	<link rel="icon" href={favicon} />

	<link rel="preconnect" href="https://use.typekit.net" />
	<link rel="stylesheet" href="https://use.typekit.net/ukz2bfk.css" />
</svelte:head>

{@render children()}
