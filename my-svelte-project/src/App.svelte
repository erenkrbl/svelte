<script>
	let name = 'Eren';
	let renk = '';

	// const firstFunction = (event) => {
	// 	renk = event.target.value;
	// }
</script>

<main>
	<p style="color:{renk}">{name}</p>
	<!-- <input type='text' on:input={firstFunction}> -->
	<input type="text" bind:value={renk}>
</main>

<style>
	main {
		text-align: center;
	}
</style>

