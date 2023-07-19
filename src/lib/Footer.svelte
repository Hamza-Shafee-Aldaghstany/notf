<script lang="ts">
	import { onMount } from 'svelte';
	//
	let titlepar = '';
	let datepar = '';
	let image: HTMLImageElement;

	interface Joke {
		img: string;
		alt: string;
		year: string;
		month: string;
		safe_title: string;
		day: string;
	}

	async function handleJoke(): Promise<string> {
		const params: URLSearchParams = new URLSearchParams();
		params.append('email', 'h.aldaghstany@innopolis.university');
		const response = await fetch('https://fwd.innopolis.app/api/hw2?' + params.toString());
		return await response.json();
	}

	async function idhandler(): Promise<Joke> {
		const params: URLSearchParams = new URLSearchParams();
		const firstFetch = await handleJoke();
		params.append('id', firstFetch);
		const response = await fetch('https://fwd.innopolis.university/api/comic?' + params.toString());
		return await response.json();
	}

	onMount(async () => {
		const data: Joke = await idhandler();

		console.log(data);
		console.log(data.safe_title);

		datepar = ' ';
		titlepar = 'Title: ' + data.safe_title;

		image = new Image();
		image.src = data.img;
	});
</script>

s
<div class="cols col1">
	<div class="img-box">
		<img src={image ? image.src : ''} alt="" id="jokeimage" />
	</div>
	<p id="titlepar">{titlepar}</p>
	<p id="datepar">{datepar}</p>
</div>

<style>
	.cols {
		width: 50%;
		height: 100vh;
		position: relative;
	}

	.img-box {
		position: relative;
		width: 100%;
		height: 100%;
	}

	/*.img-box img {*/
	/*  position: absolute;*/
	/*  top: 5%;*/
	/*  right: 40%;*/
	/*  height: 50%;*/
	/*  z-index: -1;*/
	/*  animation: animateBlush 4s ease infinite;*/
	/*}*/

	.img-box {
		position: relative;
		height: 50%;
		width: 90%;
		margin-left: 10px;
	}

	.img-box #jokeimage {
		position: absolute;
		width: 100%;
		max-height: 100%;
	}

	.col1 #titlepar {
		color: black;
		font-size: 30px;
		margin-left: 10px;
		font-weight: bold;
	}

	.col1 #datepar {
		font-weight: bold;
		margin-left: 10px;
		color: black;
		font-size: 23px;
	}

	#titlepar {
		color: black;
		font-size: 30px;
		margin-left: 10px;
		font-weight: bold;
	}

	#datepar {
		font-weight: bold;
		margin-left: 10px;
		color: black;
		font-size: 23px;
	}
</style>
