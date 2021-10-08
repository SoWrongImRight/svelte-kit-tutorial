<script>
	import Header from '$lib/header.svelte';
	import '../tailwind.css';
</script>

<Header />

<main>
	<slot><!-- optional fallback --></slot>
</main>

<footer>Copyright 2021</footer>
