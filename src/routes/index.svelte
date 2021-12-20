<script context="module" lang="ts">
	export const prerender = true
</script>

<script lang="ts">
	import Counter from '$lib/Counter.svelte'
</script>

<template lang=pug>
	svelte:head: title Home

	section
		h1
			.welcome
				picture
					source(srcset='svelte-welcome.webp' type='image/webp')
					img(src="svelte-welcome.png" alt="Welcome")
			to your new #[br] SvelteKit app
		h2 try editing #[strong src/routes/index.svelte]

		Counter
</template>

<style lang=stylus>
	section
		display: flex
		flex-direction: column
		justify-content: center
		align-items: center
		flex: 1

	h1
		user-select: none
		width: 100%

	.welcome
		position: relative
		width: 100%
		height: 0
		padding: 0 0 calc(100% * 495 / 2048) 0

		img
			position: absolute
			width: 100%
			height: 100%
			top: 0
			display: block
</style>
