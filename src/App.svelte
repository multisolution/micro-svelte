<script>
  let count = 0;
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

<button on:click={increment}>INCREMENTAR</button>
<p class={count > 0 ? 'positiVo' : 'negaAtiva'}>{count}</p>
<button on:click={decrement}>DECREMENTAR</button>
