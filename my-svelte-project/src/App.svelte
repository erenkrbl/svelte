<script>
  import { users } from "./stores";
  import AddUser from "./AddUser.svelte";
  import DeleteUser from "./DeleteUser.svelte";
  let _users;
  users.subscribe((usr) => {
    _users = usr;
  })

</script>

<main>

  
  <h1>{JSON.stringify(_users)}</h1>
  <AddUser />
| <DeleteUser/>
</main>