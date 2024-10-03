<script>
	export let placeholder = "Placeholder";
	export let type = "light"; // light, dark
</script>

{#if type=="light"}
<input class="hover:bg-gray-50 bg-white border px-3 py-2 m-2 rounded-lg text-gray-500" type="text" value={placeholder}>
{/if}

{#if type=="dark"}
<input class="hover:bg-zinc-800 file:w-65 border bg-black px-3 py-2 m-2 rounded-lg text-gray-500" type="text" value={placeholder}>
{/if}