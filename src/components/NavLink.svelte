<script lang="ts">
	export let label: string;
	export let active: boolean;
	export let href: string = '/#';

	const handleClick = () => {
		active = !active;
	};
</script>

<a {href} on:click={handleClick}>
	<div class="px-4 grid place-content-center text-white">
		<h2 class=" text-lg text-center uppercase font-bold hover:opacity-70">
			{label}
		</h2>
	</div>
</a>
