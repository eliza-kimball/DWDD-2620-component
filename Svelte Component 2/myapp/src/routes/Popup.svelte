<script>
	import MyButton from "./Button.svelte";
	import MyInput from "./Input.svelte";
	export let type = "light"; // light, dark
</script>


{#if type=="light"}
<div class="w-96 bg-white border p-5 rounded-3xl m-7">
	<h1 class="text-center font-bold text-2xl m-2">What's you team name</h1>
	<p class="text-center text-gray-500 m-4">The team name will be shown for all members.</p>
	<form action="/auth" class="flex flex-col space-y-4">
		<MyInput placeholder="Name" type="light"/>
	  <MyButton name="Confirm" type="regular" size="sm"/>
		<MyButton name="Cancel" type="flat" size="sm"/>
	</form>
</div>
{/if}

{#if type=="dark"}
<div class="w-96 bg-black border p-5 rounded-3xl m-7">
	<h1 class="text-white text-center font-bold text-2xl m-2">What's you team name</h1>
	<p class="text-center text-gray-500 m-4">The team name will be shown for all members.</p>
	<form action="/auth" class="flex flex-col space-y-4">
		<MyInput placeholder="Name" type="dark"/>
	  <MyButton name="Confirm" type="regular" size="sm"/>
		<MyButton name="Cancel" type="dark" size="sm"/>
	</form>
</div>
{/if}