<script>

  let g = 0;
  let v = 0;
  
  let p = 0;
  let D = 0;


  
    let yes = false;
  </script>
  
  <label>
    <input type="checkbox" bind:checked={yes} />
    Quieres hallar el volumen sumergido (Vs)
  </label>
  
  {#if yes}
    <label>
      p(densidad Liqudio) <input type="number" bind:value={p} placeholder="p" /> /
      D(densidad material) <input type="number" bind:value={D} placeholder="D" />
    </label>
    <p>Vs = {D / p}</p>
  {:else}
    <label>
      p<input type="number" bind:value={p} placeholder="c" /> *
      v<input type="number" bind:value={v} placeholder="i" /> *
      g<input type="number" bind:value={g} placeholder="t" />
    </label>
    <p>B(Fuerza flotación) = {p * v * g}</p>
  {/if}