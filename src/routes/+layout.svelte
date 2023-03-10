<script>
	// import picocss
	import '@picocss/pico/css/pico.min.css';
	// customize pico
	import './global.css';
</script>

<main>
	<slot />
</main>

<style>
	main {
		max-width: 800px;
		margin: 0 auto;
		padding: 1rem;
	}
</style>
