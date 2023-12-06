<script>
	export let name;
	export let lastName;
	let svelteLogo = "https://miro.medium.com/v2/resize:fit:1400/1*G9fzmaoymDGy7scbkgpC7A.png";
</script>

<style>

	:global(body){
		background-color: #f2eee2;
		color: #0084f6;
	}

	:global(:root){
		--theme-color: purple;
	}

	p {
		color: var(--theme-color);
		font-size: 30px;
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
	<p>Frontend developer!</p>
	<img class="logo" src={svelteLogo} alt="svelte-logo"/>
</main>