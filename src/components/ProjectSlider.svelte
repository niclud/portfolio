<script>
	import { Swiper, SwiperSlide } from 'swiper/svelte';

	// Import Swiper styles
	import 'swiper/css';

	import 'swiper/css/effect-coverflow';
	import 'swiper/css/navigation';

	// import required modules
	import { EffectCoverflow, Navigation, Autoplay } from 'swiper';
	import ProjectCard from './ProjectCard.svelte';
	const projectObject = [
		{
			title: 'E-commerce para primer mate',
			description:
				'E-commerce realizado con el grupo de trabajo de Transformance Agency. Tecnologias: Svelte - JS - HTML - CSS - Tailwind - Shopify',
			href: 'https://primer-mate.clients.transformanceagency.com',
			image: 'images/primermate.jpeg'
		},
		{
			title: 'landing para Escuela de Surf',
			description:
				'Landing page para escuela de surf. Trabajo realizado en conjunto con Taps Developers. Tecnologias Svelte - JS - HTML - CSS - Tailwind',
			href: 'https://nalusurf.taps.digital/',
			image: 'images/nalusurf.jpeg'
		},
		{
			title: 'Proyecto personal TaskList',
			description:
				'Organizador de tareas diarias aplicando CRUD en cada tarea y poder agregarle una descripción y fecha limite a las tareas. Realizandolo con React',
			href: 'https://niclud.github.io/tasklist/',
			image: 'images/tasklist.jpeg'
		},
		{
			title: 'Escuela de Surf',
			description:
				'Landing page para escuela de surf. Trabajo realizado en conjunto con Taps Developers. Tecnologias Svelte - JS - HTML - CSS - Tailwind',
			href: 'https://nalusurf.taps.digital/',
			image: 'https://taps.digital/_app/immutable/assets/nalu-1b1c4eea.webp'
		},
		{
			title: 'Escuela de Surf',
			description:
				'Landing page para escuela de surf. Trabajo realizado en conjunto con Taps Developers. Tecnologias Svelte - JS - HTML - CSS - Tailwind',
			href: 'https://nalusurf.taps.digital/',
			image: 'https://taps.digital/_app/immutable/assets/nalu-1b1c4eea.webp'
		}
	];
</script>

<div class="m-6 h-[550px]">
	<Swiper
		effect={'coverflow'}
		grabCursor={false}
		centeredSlides={true}
		slidesPerView={3}
		coverflowEffect={{
			rotate: 50,
			stretch: 1,
			depth: 100,
			modifier: 1,
			slideShadows: false
		}}
		autoplay={true}
		navigation={true}
		modules={[EffectCoverflow, Navigation, Autoplay]}
		class="mySwiper"
	>
		{#each projectObject as project}
			<SwiperSlide
				><ProjectCard
					title={project.title}
					image={project.image}
					description={project.description}
					href={project.href}
				/></SwiperSlide
			>
		{/each}
	</Swiper>
</div>
