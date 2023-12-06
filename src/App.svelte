<script>
	import About from "./components/About.svelte";
	import Text from "./components/Text.svelte";
	import Person from "./components/Person.svelte";
	export let name;
	export let lastName;
	let svelteLogo = "https://miro.medium.com/v2/resize:fit:1400/1*G9fzmaoymDGy7scbkgpC7A.png";

	const data = {
		name: 'jorge',
		lastName: 'Del Toro',
		age: 21
	};
</script>

<style>

	:global(body){
		background-color: #f2eee2;
		color: #0084f6;
	}

	:global(:root){
		--theme-color: purple;
	}

	:global(body.dark-mode){
		background-color: #1d3040;
		color: #bfc2c7;
	}
	.logo {
		height: 250px;
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>Hello {name} {lastName}!</h1>
	<About/>
	<Text anotherText="Hola mundo"/> <!--Using a value-->
	<Text /> <!--default value-->
	<Person {...data}/> <!--Propagation-->
	<img class="logo" src={svelteLogo} alt="svelte-logo"/>
</main>