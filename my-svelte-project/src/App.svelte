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
<!-- <script>
  import MyButtom from "./Button.svelte";
  import Content from "./Content.svelte";
  let appStatus = false;
  let appSuccess = false;
</script> -->

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


<!-- <main>
  <MyButtom show = {appStatus} success={appSuccess} />
  <Content>
    <p>Slot</p>
  </Content>
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
</main> -->

<script>
  let name;
  let surname;
  let age;
  let email;
  // let english;
  // let turkish;
  // let russian;

  let languages = []

  const sendData = () => {
    console.log(name, surname, age, email, languages)
  }
</script>

<style>
  main {
    text-align: center;
  }

  label {
    margin-top: 20px;
    margin-bottom: 5px;
  }

  button {
    margin-top: 20px;
  }
  </style>
  <main>
    <form on:submit|preventDefault={sendData}>
      <div><input type="text" placeholder="name" bind:value={name}></div>
      <div><input type="text" placeholder="surname" bind:value={surname}></div>
      <div><input type="number" placeholder="age" bind:value={age}></div>
      <div><input type="email" placeholder="email" bind:value={email}></div>
      <div><label>Languages</label></div>
      <!-- <div><input type="checkbox" bind:checked={english}>English</div>
      <div><input type="checkbox" bind:checked={turkish}>Turkish</div>
      <div><input type="checkbox" bind:checked={russian}>Russian</div> -->
      <div><input type="checkbox" bind:group={languages} value="english">English</div>
      <div><input type="checkbox" bind:group={languages} value="turkish">Turkish</div>
      <div><input type="checkbox" bind:group={languages} value="russian">Russian</div>
      <button>Add a user</button>
    </form>
    
  </main>
