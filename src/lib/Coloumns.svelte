<script>
	import Profile from './Profile.svelte';
	import Footer from './Footer.svelte';
	//
	const projects = [
		'Six months expe1rience of backend with spring-boot.',
		'Learning react for front end development.',
		'Looking for an internship for Micro services using spring boot.'
	];

	const skills = [
		'Wro participant for seven times.',
		'Learning react for front end development.',
		'Looking for an internship for Micro services using spring boot.'
	];

	// const jokeImage = './img/joke-image.jpg';
	// const title = 'Joke Title';
	// const date = 'July 10, 2023';
</script>

<div class="wrapper">
	<div class="cols00">
		<Profile profileImage="/img/photo_2023-03-25_16-41-20.jpg" {projects} {skills} />
	</div>
	<Footer />
</div>

<style>
	.wrapper {
		display: flex;
		align-items: center;
		width: 100%;
		height: 100vh;
		overflow: hidden;
		justify-content: center;
		/*padding-left: 10px ;*/
	}
	.cols00 {
		display: flex;
		width: 50%;
		height: 80vh;
		align-items: end;
		position: relative;
	}

	/*h1 {*/
	/*	display: block;*/
	/*	font-size: 1em;*/
	/*	font-weight: 900;*/
	/*	color: black;*/
	/*	font-family: 'Calibri Light';*/
	/*}*/

	/*.multi-text {*/
	/*	color: grey;*/
	/*	font-size: 1.5em;*/
	/*}*/
	/*p {*/
	/*	display: block;*/
	/*	width: 90%;*/
	/*	font-size: 0.9em;*/
	/*	color: red;*/
	/*}*/
	/*.btns {*/
	/*	width: 100%;*/
	/*	position: relative;*/
	/*	left: 80px;*/
	/*}*/
	/*button {*/
	/*	border-radius: 5px;*/
	/*	outline: none;*/
	/*	border: none;*/
	/*	cursor: pointer;*/
	/*	font-size: 18px;*/
	/*	font-weight: 600;*/
	/*	color: black;*/
	/*	background-color: wheat;*/
	/*	padding: 8px 14px;*/
	/*	margin: 40px 5px;*/
	/*	letter-spacing: 2px;*/
	/*	box-shadow: -5px 5px 6px rgba(0, 0, 0, 0.4);*/
	/*	transition: all 1s;*/
	/*}*/
	/*button:hover {*/
	/*	box-shadow: -10px 10px 10px rgba(0, 0, 0, 0.4);*/
	/*}*/
	/*.img-box {*/
	/*	position: relative;*/
	/*	width: 100%;*/
	/*	height: 100%;*/
	/*}*/
	/*.img-box #lol {*/
	/*	position: absolute;*/
	/*	top: 5%;*/
	/*	right: 40%;*/
	/*	height: 50%;*/
	/*	z-index: -1;*/
	/*	animation: animateBlush 4s ease infinite;*/
	/*}*/
	/*.img-box #mypicture {*/
	/*	position: relative;*/
	/*	height: 50%;*/
	/*	width: calc(100%- 80px);*/
	/*	top: 15%;*/
	/*	right: -10%;*/
	/*	animation: animateUser 5s linear infinite;*/
	/*}*/
	@keyframes animateUser {
		50% {
			/*transform: rotateY(180deg);*/
			right: 10%;
			top: 5%;
		}
	}
	@keyframes animateBlush {
		50% {
			top: 10%;
			right: 30%;
		}
	}
	/*.image-hello {*/
	/*	display: flex;*/
	/*	height: 9%;*/
	/*	width: 100%;*/
	/*	flex-direction: row;*/

	/*	position: relative;*/
	/*}*/
	/*.projects {*/
	/*	font-family: Arial;*/
	/*	font-size: 30px;*/
	/*}*/
</style>
