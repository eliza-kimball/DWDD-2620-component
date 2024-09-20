<script>
	export let name = "Default";
	export let type = "regular"; // regular, disabled
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

{#if type=="disabled"}
 <button class={`rounded-full bg-gray-300 text-gray-500 m-7 ${(size in sizes) ? sizes[size] : sizes["md"]}`}>
  {name}
 </button> 
{/if}