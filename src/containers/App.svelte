<script>
	import Presión from './../pages/Presión.svelte';
  import Flotación from '../pages/Flotación.svelte';
  import X from '../pages/X.svelte';

    let currentPage ;
  function changePage(newPage) {
    currentPage = newPage;
  }
  function changePageVf() {
    changePage(Vf)
  }
</script>

<div>
  <div class="nav">
    <button on:click={() => changePage(Flotación)}>Flotación</button>
    <button on:click={() => changePage(Presión)}>Presión</button>
    <button on:click={() => changePage(X)}>X</button>
  </div>
  
  <div class="contend">
    <svelte:component this={currentPage} />
  </div>
</div>

<style>
  :global(body) {
    background-color: #676778;
    color: white;
  }
  
  .contend {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 1rem;

        padding-top: 0;

        font-size: 20px;

        position: relative;
    }
    .nav button {
        background-color: #676778;
        color: white;
        border: none;
        padding: 1rem;
        border-radius: 5px;
        font-size: 20px;
    }

    .nav button:hover {
        background-color: #ffffff;
        color: black;
        border: none;
        padding: 0.5rem;
        border-radius: 5px;
        font-size: 20px;
    }

    .nav button:active {
        background-color: black;
        color: white;
        border: none;
        padding: 0.5rem;
        border-radius: 5px;
        font-size: 20px;
    }
</style>
