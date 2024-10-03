<script>
	export let name = "Default";
	export let type = "regular"; // regular, flat, dark
	export let size = "md";
	export let color = "indigo";
	const sizes = {
		"md" : "px-28 py-2.5",
	}
</script>

{#if type=="regular"}
 <button class={`rounded-full bg-${color}-600 text-white m-7 hover:bg-indigo-700 focus:ring focus:ring-indigo-400 ${(size in sizes) ? sizes[size] : sizes["md"]}`}>
  {name}
 </button>
{/if}

{#if type=="flat"}
 <button class={`rounded-full text-indigo-600 hover:text-indigo-300 m-7 ${(size in sizes) ? sizes[size] : sizes["md"]}`}>
  {name}
 </button> 
{/if}

{#if type=="dark"}
 <button class={`rounded-full text-gray-500 hover:text-white m-7 ${(size in sizes) ? sizes[size] : sizes["md"]}`}>
  {name}
 </button> 
{/if}