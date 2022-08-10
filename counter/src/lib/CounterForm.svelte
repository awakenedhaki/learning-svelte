<script>
  export let nCounter = '';
</script>

<form>
  <label>
    <h1>How many counters do you need?</h1>
    <input bind:value={nCounter} type="text" placeholder="Number of counters :)">
  </label>
  <button type="submit">Create your counters!</button>
</form>

<style>
  input {
    text-align: center;
  }

  button {
    width: 50%;
    margin: 0 auto;
    background-color: #7799ee;
  }
</style>