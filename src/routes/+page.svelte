<script>
	import Coloumns from '$lib/Coloumns.svelte';
	//dfdf
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Coloumns />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	/*h1 {*/
	/*	width: 100%;*/
	/*}*/

	/*.welcome img {*/
	/*	position: absolute;*/
	/*	width: 100%;*/
	/*	height: 100%;*/
	/*	top: 0;*/
	/*	display: block;*/
	/*}*/
</style>
