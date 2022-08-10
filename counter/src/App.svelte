<script>
  import CounterForm from './lib/CounterForm.svelte';
  import Counter from './lib/Counter.svelte';

  let nCounter = '';
  let isVisible = true;
  const hideForm = () => {
    isVisible = false;
  }
</script>

<main>
  {#if isVisible}
    <form on:submit={hideForm}>
      <label>
        <h1>How many counters do you need?</h1>
        <input bind:value={nCounter} type="text" placeholder="Number of counters :)">
      </label>
      <button type="submit">Create your counters!</button>
    </form>
  {/if}

  {#if !isVisible}
    {#each Array(parseInt(nCounter)) as _, i}
      <Counter counterID={i + 1}/>
    {/each}
  {/if}
</main>

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