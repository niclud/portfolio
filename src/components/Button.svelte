<script lang="ts">
	export let type: 'button' | 'submit' = 'button';
	export let disabled: boolean = false;
</script>

<button
	{type}
	{disabled}
	class="bg-red-600 hover:bg-red-400 p-2 rounded-lg text-white shadow-lg m-5"
>
	<slot />
</button>
