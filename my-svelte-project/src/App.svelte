<script>
  import AddPerson from "./AddPerson.svelte";
  let users = [
    {
      name: "x",
      surname: "y",
      age: "12",
      email: "x@y.com",
      languages: ["turkish"],
      hairColor: "black"

    },
    {
      name: "xx",
      surname: "yy",
      age: "18",
      email: "xx@yy.com",
      languages: ["english"],
      hairColor: "browv"

    },
  ];

  const savePerson = (event) => {
    //console.log(event.detail);
    users = [...users, {...event.detail}]
  };
</script>

<main>
  <AddPerson on:savePerson={savePerson} />
  {JSON.stringify(users)}
</main>
