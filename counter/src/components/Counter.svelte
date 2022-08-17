<script>
  export let counterID;
  let counter = 0;

  const increaseCounter = () => counter++;
  const decreaseCounter = () => {
    counter--;
    if (counter < 0) {
      counter =0;
    }
  }
</script>

<div class="box">
  <slot>
    <h3>Counter {counterID}</h3>
    <h1 class='counter'>{counter}</h1>
    <button class="counter-btn" on:click={increaseCounter}>Increase</button>
    <button class="counter-btn" on:click={decreaseCounter}>Decrease</button>
  </slot>
</div>

<style>
  .counter {
    color: #FFD700;
  }

  .counter-btn {
    background-color: #7799ee;
  }

	.box {
		width: 300px;
		border: 1px solid #aaa;
		border-radius: 25px;
		box-shadow: 2px 2px 8px rgba(0,0,0,0.1);
		padding: 1em;
		margin: 0 0 1em 0;
	}
</style>