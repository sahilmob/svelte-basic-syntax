<script>
  let name = "sahil";
  let age = 30;

  $: uppercaseName = name.toUpperCase();

  function incAge() {
    age += 1;
  }

  function changeName() {
    name = "Not Sahil";
  }
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>Hello {uppercaseName}!, I'm {age} years old</h1>
<button on:click={incAge}>Change Age</button>
<button on:click={changeName}>Change Name</button>
