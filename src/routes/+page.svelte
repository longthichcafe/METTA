<script>
	import '$lib/styles.css';
	import Card from '$lib/Card.svelte';
	import Footer from '$lib/Footer.svelte';

	/** @type {import('./$types').PageData} */
	export let data;
</script>

<svelte:head>
	<title>METTA</title>
</svelte:head>

<Card />

<main>
	<h1><span>We are METTA</span></h1>

	<div class="info">
		<div class="block">
			<div class="contents">
				<span>Research & Develop</span>
				<strong>Virtual And Augmented Reality</strong>
			</div>
		</div>
		<div class="block">
			<div class="contents">
				<span>Work directly with</span>
				<strong>Professionals</strong>
			</div>
		</div>
	</div>
</main>

<Footer />

<style>
	main {
		position: relative;
		width: 100vw;
		height: 100%;
		padding: 2.5rem;
		box-sizing: border-box;
	}

	h1 {
		font-size: min(16vw, 4rem);
		font-weight: 600;
		margin: 0;
		text-align: center;
		position: absolute;
		top: 10vh;
		left: 0;
		width: 100%;
		padding: 0 2.5rem;
		box-sizing: border-box;
		line-height: 1;
	}

	h1 span {
		display: block;
		max-width: 6em;
		margin: 0 auto;
	}

	.info {
		--border-color: rgba(0, 0, 0, 0.08);
		position: absolute;
		bottom: 9rem;
		left: 0;
		width: 100%;
		display: grid;
		padding: 0 2.5rem;
		font-size: min(5vw, 2rem);
		box-sizing: border-box;
	}

	.block {
		display: flex;
		margin: 0;
		padding: 1rem 0;
	}

	.block:nth-child(1) {
		border-bottom: 1px solid var(--border-color);
	}

	.block span {
		display: block;
		margin: 0 0 0.2em 0;
		text-transform: uppercase;
		font-size: 0.6em;
	}

	.block strong {
		display: block;
		font-size: 1.4em;
		margin: 0;
		font-weight: 600;
	}

	@media (min-width: 640px) {
		h1 {
			font-size: min(8vw, 4rem);
		}

		h1 span {
			max-width: none;
		}

		.info {
			display: flex;
			justify-content: center;
			position: relative;
			top: 60vh;
			gap: 4rem;
			grid-template-columns: 1fr 1fr;
		}

		.block:nth-child(1) {
			border-bottom: none;
			justify-content: end;
		}

		.block:nth-child(2) {
			justify-content: start;
		}
	}

	@media (prefers-color-scheme: dark) {
		.block:nth-child(1) {
			--border-color: rgba(255, 255, 255, 0.35);
		}
	}
</style>
