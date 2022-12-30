<script lang="ts">
	import { page } from '$app/stores';
	import NavLink from '../components/NavLink.svelte';

	$: url = $page.url.pathname;

	const navLinks = [
		{ label: 'Home', href: '/' },
		{
			label: 'Acerca de mí',
			href: '/#acercademi'
		},
		{
			label: 'Proyectos',
			href: '/#proyectos'
		},
		{
			label: 'Contactame',
			href: '/#contactame'
		}
	];
</script>

<header
	class="w-screen px-20 left-0 top-0 z-20 grid grid-flow-col fixed justify-between items-center h-20"
>
	<div class="">
		<h1 class=" text-white font-bold items-center text-lg">Portfolio</h1>
	</div>
	<nav class="grid grid-flow-col justify-center">
		{#each navLinks as { label, href }}
			<NavLink {label} {href} active={href === url} />
		{/each}
	</nav>
</header>
