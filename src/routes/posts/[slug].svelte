<script context="module">
	export async function load({ page }) {
		try {
			const Post = await import(`../../posts/${page.params.slug}.md`);

			return {
				// Data passed into svelte component
				props: {
					Post: Post.default
				}
			};
		} catch (e) {
			return {
				status: 404,
				error: 'Post not found'
			};
		}
	}
</script>

<script>
	export let Post;
</script>

<svelte:component this={Post} />
