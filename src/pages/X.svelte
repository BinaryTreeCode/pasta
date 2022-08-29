<script>
    let v2 = 0;
    let I = 0;
  
    let y = 0;
    let t = 0;
  
    let g = 0;

    let A1 = 0;
    let A2 = 0;

    let v1 = 0;

    </script>

    <div>
      <h2>hallar distancia en x</h2>

      <p>Primero hay que hallar t(tiempo)</p>
      <label>
        <samp>t =</samp>
        raiz( 2*<input type="number" bind:value={y} placeholder="y" />y /
        g<input type="number" bind:value={g} placeholder="g" />)
      </label>
      <p>t = {Math.sqrt((2*y)/g)}s</p> 

      <p>luego hay que hallar v2 que se despeja en: A1*v1 = A2*v2</p>
      <p>Sabiendo que Q=A1*v1 (Q = caudal)</p>
      <label>
        <samp>v2 =</samp>
        A1<input type="number" bind:value={A1} placeholder="A1" /> *
        v1<input type="number" bind:value={v1} placeholder="v1" /> /
        A2<input type="number" bind:value={A2} placeholder="A2" />
      </label>
      <p>v2 = {(A1 * v1) / A2}m/s</p> 

      <p>Finalmente X es igual v2*t</p>
      <h1>X = {(Math.sqrt((2*y)/g)) * ((A1 *v1) / A2)}m</h1>
    </div>

