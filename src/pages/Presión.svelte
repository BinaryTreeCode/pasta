<script>
  let P = 0;

  let F = 0;
  let A = 0;

  let Po = 0;

  let h = 0;
  let g = 0;
  let p = 0;
  
  
  let yes = false;
</script>

<label>
  <input type="checkbox" bind:checked={yes} />
  Quieres hallar la presión del liquido (P= Po + phg);
</label>

{#if yes}
  <label>
    Po <input type="number" bind:value={Po} placeholder="Po" /> +
    p(densidad Liqudio) <input type="number" bind:value={p} placeholder="p" /> *
    h <input type="number" bind:value={h} placeholder="h" /> *
    g <input type="number" bind:value={g} placeholder="g" /> *

  </label>
  <p>p = {Po + (p * h * g)}</p>
{:else}
  <label>
    F <input type="number" bind:value={F} placeholder="i" /> /
    A <input type="number" bind:value={A} placeholder="t" />
  </label>
  <p>P = {F / A}</p>
{/if}

<style>
  label {
    display: flex;
  }
  input,
  p {
    margin: 6px;
  }
</style>
