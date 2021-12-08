<!-- <script>
  import { each } from "svelte/internal";

  let messages = [
    { id: 0, from: "x", to: "y", message: "Hello y" },
    { id: 1, from: "xx", to: "yy", message: "Hello yy" },
    { id: 2, from: "xxx", to: "yyy", message: "Hello yyy" },
    { id: 3, from: "xxx", to: "yyyy", message: "Hello yyyy" },
  ];

  const clicked = () => {
    messages = messages.splice(1);
  };
</script>

<main>
  <table>
    <thead>
      <tr>
        <td>ID</td>
        <td>FROM</td>
        <td>TO</td>
        <td>MESSAGE</td>
      </tr>
    </thead>
    <tbody>
      {#each messages as message (message.id)}
        {#if message.id === 1}
          <tr>
            <td>{message.id}</td>
            <td>{message.from}</td>
            <td>{message.to}</td>
            <td>{message.message}</td>
          </tr>
		  {:else if message.id === 3}
          <tr>
            <td>{message.id}</td>
            <td>{message.from}</td>
            <td>{message.to}</td>
            <td>{message.message}</td>
          </tr>
		  {:else}
          <tr>
            <td>............</td>
            <td>............</td>
            <td>............</td>
            <td>............</td>
          </tr>

        {/if}
      {:else}
        <tr>
          <td colspan="4">No data vas not found</td>
        </tr>
      {/each}
    </tbody>
  </table>
  <button on:click={clicked}>Delete</button>
</main>

<style>
  main {
    text-align: center;
  }
  table {
    width: 100%;
    padding: 20px;
  }
</style> -->
<script>
  import MyButtom from "./Button.svelte";
  let appStatus = false;
  let appSuccess = false;
</script>

<!-- <script>
	let name = 'Steven';
	let surname = 'Svelte';
	$: fullname = `${name} ${surname}`;
	$: {
		console.log(name);
		console.log(surname);
		console.log(fullname);
	}
	let renk = '';
	

	const firstFunction = (event) => {
		renk = event.target.value;
	}
</script>

<main>
	<p style="color:{renk}">{name}</p> 
	<input type='text' on:input={firstFunction}>
	<input type="text" bind:value={renk}>

	<p> {name} {surname} </p>
	<p> {fullname} </p>
	<input type="text" bind:value={name}>
	<input type="text" bind:value={surname}>
	
</main> -->

<main>
  <MyButtom show = {appStatus} success={appSuccess} />
  <button
    on:click={() => {
      appSuccess = !appSuccess;
    }}>Change Color</button
  >
  <button
    on:click={() => {
      appStatus = !appStatus;
    }}>{appStatus ? "Disable" : "active"}</button
  >
</main>

<style>
  main {
    text-align: center;
  }
</style>
