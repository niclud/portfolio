<script lang="ts">
	import { bind } from 'svelte/internal';

	export let name: string;
	export let value: string = '';
	export let placeholder: string = '';
	export let error: string = '';
	export let multilpe: boolean = false;
	export let rows: number = 5;
	export let disabled: boolean = false;
</script>

<div class="grid gap-1">
	{#if !multilpe}
		<input
			{name}
			{disabled}
			type="text"
			bind:value
			{placeholder}
			class="bg-white/10 px-3 py-2 rounded-lg w-full"
		/>
	{:else}
		<textarea
			{name}
			{disabled}
			{rows}
			{placeholder}
			bind:value
			class="resize-none bg-white/10 rounded-lg px-3 py-2 w-full"
		/>
	{/if}
	{#if !error && error !== ''}
		<span class="font-medium text-red-600 text-sm">{error}</span>
	{/if}
</div>
