<script context="module">
	export async function load({ page }) {
		const Hello = (await import(`../../posts/${page.params.slug}.md`)).default;

		/* 		const post = {
			title: page.params.slug,
			date: new Date(),
			body: 'lorem ispum'
		}; */

		return {
			props: {
				Hello
			}
		};
	}
</script>

<script>
	export let Hello;
</script>

<Hello />

