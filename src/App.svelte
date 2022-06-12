<script>

	let numero1;
	let numero2;
	let resultado;

	function calcular(operacao){

		if(numero1!=null && numero2!=null){
			switch (operacao) {
				case "Somar":
					resultado = numero1 + numero2;
					break;
				case "Subtrair":
					resultado = numero1 - numero2;
					break;
				case "Multiplicar":
					resultado = numero1 * numero2;
					break;
				case "Dividir":
					resultado = numero1 / numero2;
				default:
					break;
			}

		}if(resultado==undefined){
			resultado=null;
		}
	}

	function limpar (){
		resultado = null;
		numero1 = null;
		numero2 = null;
	}

</script>


	<h1 class="center-align">Calculadora Super Simples</h1>


	<table>
		<tr>
			<td><input type="number" bind:value={numero1} placeholder="Número 1"></td>
			<td><input type="number" bind:value={numero2} placeholder="Número 2"></td>
		</tr>
	</table>	
	<table>
		<tr>
			<td><button on:click={() => calcular("Somar")} class="btn-calc">Somar</button></td>
			<td><button on:click={() => calcular("Subtrair")} class="btn-calc">Subtrair</button></td>
			<td><button on:click={() => calcular("Multiplicar")} class="btn-calc">Multiplicar</button></td>
			<td><button on:click={() => calcular("Dividir")} class="btn-calc">Dividir</button></td>
			<td><button on:click={() => limpar()} class="btn-limpar">Limpar</button></td>

		</tr>
	</table>

	

	


	{#if resultado!=null}
		<h2 class="result">Resultado:{resultado}</h2>
	{/if}
	
	
	
	
	
	
	



