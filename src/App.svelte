<script>
  import ContactCard from "./ContactCart.svelte";

  let name = "sahil";
  let age = 30;

  $: uppercaseName = name.toUpperCase();

  $: console.log(name);

  $: if (name !== "sahil") {
    age = 31;
  }

  function incAge() {
    age += 1;
  }

  // function changeName(event) {
  //   name = event.target.value;
  // }
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>Hello {uppercaseName}!, I'm {age} years old</h1>
<button on:click={incAge}>Change Age</button>
<!-- <button on:click={changeName}>Change Name</button> -->
<!-- <input type="text" value={name} on:input={changeName} /> -->
<input type="text" bind:value={name} />
<ContactCard userName={name} />
