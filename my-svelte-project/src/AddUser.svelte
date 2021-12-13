<script>
    import {users} from "./stores";
    let name;
    let age;

    const addUser = () => {
        users.update((_users) => [..._users, {name, age}])
    }
</script>
<input type="text" placeholder="name" bind:value = {name}>
<input type="number" placeholder="age" bind:value= {age}>
<button on:click={addUser}>Add User</button>