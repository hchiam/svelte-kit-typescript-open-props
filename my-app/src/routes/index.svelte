<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Counter from '$lib/Counter.svelte';

	// index.js loading JS object
	import OpenProps from 'open-props'; // module
	import OpenPropsSrc from 'open-props/src'; // unbundled ES module
	import Colors from 'open-props/src/colors';

	// object notation access is special to OpenProps
	console.info(OpenProps.size1);
	console.info(OpenProps['--size-1']);
	console.info(OpenPropsSrc.animationBlinkAt);
	console.info(OpenPropsSrc['--animation-blink-@']);

	console.info(Colors['--indigo-5']);

	// import just 1 color set object
	// import { indigo } from 'open-props/src/colors'; // TODO
	import { indigo } from 'open-props/src/props.colors';
	console.info(indigo)
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<h1>
		<div class="welcome">
			<picture>
				<source srcset="svelte-welcome.webp" type="image/webp" />
				<img src="svelte-welcome.png" alt="Welcome" />
			</picture>
		</div>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/index.svelte</strong>
	</h2>

	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
