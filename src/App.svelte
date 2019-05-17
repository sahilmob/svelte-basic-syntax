<script>
  let name = "sahil";
  let age = 30;

  function incAge() {
    age += 1;
  }
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>Hello {name}!, I'm {age} years old</h1>
<button on:click={incAge}>Change Age</button>
