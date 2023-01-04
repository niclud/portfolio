<script lang="ts">
	export let title: string;
	export let description: string;
	export let href: string = '/#';
	export let image: string;
</script>

<a {href} target="__blank">
	<div class="bg-[#161616] w-80 h-[400px] rounded-lg overflow-hidden">
		<img src={image} alt="Projetct ${title}" class="w-full h-300 object-cover" />
		<div class="p-4 text-white grid gap-2">
			<h1 class="uppercase text-lg font-bold">{title}</h1>
			<p class="text-base opacity-80">{description}</p>
		</div>
	</div>
</a>
