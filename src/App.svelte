<script>
	let texto = "";
	let numero = 0;
	let rango = 5;
	let seleccion = true;
  
	let opciones = ["pizza", "sandia", "sushi"];
	let radio = "";
	let arraySeleccion = [];
  
	$: console.log(arraySeleccion);
  </script>
  
  <div>
	<h1>Bindings</h1>
  
	<input type="text" bind:value="{texto}" />
  
	<input type="number" bind:value="{numero}" />
  
	<input type="range" bind:value="{rango}" min="0" max="10" />
  
	<input type="checkbox" bind:checked="{seleccion}" />
  
	<h4>Texto: {texto}</h4>
	<h4>numero: {numero}</h4>
	<h4>rango: {rango}</h4>
	<h4>seleccion: {seleccion}</h4>
  
	{#each opciones as item}
	<input type="radio" bind:group="{radio}" value="{item}" />
	{item} {/each}
  
	<h4>radio: {radio}</h4>
  
	{#each opciones as item}
	<input type="checkbox" bind:group="{arraySeleccion}" value="{item}" />
	{item} {/each}
  
	<h4>arraySeleccion: {arraySeleccion}</h4>
  </div>
  