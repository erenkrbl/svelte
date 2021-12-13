<script>
  import { createEventDispatcher } from "svelte";
  let name;
  let surname;
  let age;
  let email;
  let languages = [];
  let send = createEventDispatcher();
  let hairColor;

  const sendData = () => {
    send("savePerson", {
      name, 
      surname, 
      age, 
      email, 
      languages, 
      hairColor
    });
  };
</script>

<main>
  <form on:submit|preventDefault={sendData}>
    <div><input type="text" placeholder="name" bind:value={name} /></div>
    <div><input type="text" placeholder="surname" bind:value={surname} /></div>
    <div><input type="number" placeholder="age" bind:value={age} /></div>
    <div><input type="email" placeholder="email" bind:value={email} /></div>
    <div><label>Languages</label></div>
    <div>
      <input type="checkbox" bind:group={languages} value="english" />English
    </div>
    <div>
      <input type="checkbox" bind:group={languages} value="turkish" />Turkish
    </div>
    <div>
      <input type="checkbox" bind:group={languages} value="russian" />Russian
    </div>
    <div>
      <select bind:value={hairColor}>
        <option value="black">Black</option>
        <option value="yellow">Yellow</option>
        <option value="brown">Brown</option>
      </select>
    </div>
    <button>Add a user</button>
  </form>
</main>

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
