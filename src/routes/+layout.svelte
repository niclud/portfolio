<script>
	import Header from '../layouts/Header.svelte';
	import '../assets/tailwind.css';
	import Footer from '../layouts/Footer.svelte';
</script>

<Header />
<div class="min-h-screen bg-[#111111]">
	<slot />
</div>
<Footer />

<style>
	:gloobal(body) {
		font-family: 'Maven Pro', sans-serif;
		background-color: #111111;
		padding-bottom: 50px;
	}
</style>
