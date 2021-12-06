<script>
	let name = 'Steven';
	let surname = 'Svelte';
	$: fullname = `${name} ${surname}`;
	$: {
		console.log(name);
		console.log(surname);
		console.log(fullname);
	}
	let renk = '';
	

	// const firstFunction = (event) => {
	// 	renk = event.target.value;
	// }
</script>

<main>
	<!-- <p style="color:{renk}">{name}</p>
	<input type='text' on:input={firstFunction}>
	<input type="text" bind:value={renk}> -->

	<!-- <p> {name} {surname} </p> -->
	<p> {fullname} </p>
	<input type="text" bind:value={name}>
	<input type="text" bind:value={surname}>
	
</main>

<style>
	main {
		text-align: center;
	}
</style>

