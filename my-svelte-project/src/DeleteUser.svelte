<script>
    import {users} from "./stores";
    let name;
    let age;

    const deleteUser = () => {
        users.update((_users) => _users.slice(0, -1));
    }
</script>
<button on:click={deleteUser}>Delete User</button>