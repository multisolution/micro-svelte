<script>
  let count = 0;

  addEventListener("increment", e => increment(), false);

  function dispatchIncrment() {
    window.dispatchEvent(new CustomEvent("svelte", { detail: "micro-svelte" }));
    // window.postMessage("increment", "*");
  }
  function increment() {
    count += 1;
  }
  function decrement() {
    count -= 1;
  }
</script>

<style>
  .positiVo {
    color: #000000;
  }
  .negaAtiva {
    color: #ff3e00;
  }
</style>

<svelte:options tag="svelte-micro" immutable={true} />
<button on:click={increment}>INCREMENTAR</button>
<p class={count > 0 ? 'positiVo' : 'negaAtiva'}>{count}</p>
<button on:click={decrement}>DECREMENTAR</button>
<button on:click={dispatchIncrment}>dispatchEvent</button>
