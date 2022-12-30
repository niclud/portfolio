<script lang="ts">
</script>

<div class="relative w-screen h-screen">
	<div class="absolute w-full h-full">
		<img src="images/digitization.jpg" alt="" class="w-full h-full object-cover" />
		<div class="absolute top-0 left-0 w-full h-full bg-black/50 " />
	</div>
	<div class="w-full h-full pt-16 grid place-content-center">
		<div class="text-center max-w-md z-10">
			<h3 class="text-white text-2xl">Bienvenido a mi sitio WEB</h3>
			<h1 class="text-white text-4xl">Front End Developer</h1>
		</div>
	</div>
</div>
<div class="w-screen h-screen flex flex-col sm:flex sm:flex-row relative " id="acercademi">
	<div class="sm:w-1/2 p-16 grid place-content-center mb-12">
		<img
			src="https://pps.whatsapp.net/v/t61.24694-24/309911406_152707060425191_7566008590557575580_n.jpg?ccb=11-4&oh=01_AdTIkmm4fAQLvikuUUFobLpa3rMy7hZfNRrxQDOGUNVm-A&oe=63BB312B"
			alt="Foto mia"
			class=""
		/>
	</div>
	<div class="sm:w-1/2 grid items-center p-16 text-white place-content-center gap-5 mb-12">
		<div>
			<h2 class="text-2xl font-bold">Nicolás Ludueña</h2>
			<h3 class="text-base font-semibold">Front End Developer</h3>
		</div>
		<p class="text-base">
			Actualmente me encuentro finalizando segundo año de Ing. en sistemas de información y
			trabajando de manera freelance para un emprendimiento que empezamos con compañeros de la
			facultad donde realizamos proyectos de desarrollo web. Estoy en la búsqueda de mi primera
			experiencia laboral en empresas de desarrollo de software, estoy abierto a aprender
			habilidades y conocimientos nuevos que aporten a mi crecimiento profesional y personal.
		</p>
		<h2 class="text-2xl font-semibold">Tecnologias <i class="fa-solid fa-code" /></h2>
		<div class="grid grid-flow-col">
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-html5 text-3xl" />
				<h2>HTML5</h2>
			</div>
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-css3-alt text-3xl" />
				<h2>CSS3</h2>
			</div>
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-square-js text-3xl" />
				<h2>JavaScript</h2>
			</div>
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-react text-3xl" />
				<h2>React</h2>
			</div>
		</div>

		<div class="grid grid-flow-col">
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-squarespace text-3xl" />
				<h2>Svelte</h2>
			</div>
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-python text-3xl" />
				<h2>Python</h2>
			</div>
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-java text-3xl" />
				<h2>Java</h2>
			</div>
			<div class="flex gap-2 items-center">
				<i class="fa-brands fa-git-alt text-3xl" />
				<h2>Git</h2>
			</div>
		</div>
	</div>
</div>

<style>
	h1 {
		display: block;
		white-space: nowrap;
		border-right: 4px solid;
		width: 18ch;

		animation: typing 2s steps(12), blink 0.5s infinite step-end alternate;
		overflow: hidden;
	}
	@keyframes typing {
		from {
			width: 0;
		}
	}
	@keyframes blink {
		50% {
			border-color: transparent;
		}
	}
</style>
