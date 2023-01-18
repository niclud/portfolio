<script>
	import Button from './Button.svelte';
	import LabaledInput from './LabaledInput.svelte';
</script>

<div class=" text-white h-full m-6">
	<div class="grid grid-flow-row">
		<div class=" grid lg:grid-cols-2 grid-flow-row w-full px-10 gap-3 rounded-lg bg-[#262626]">
			<div class="grid grid-flow-row gap-3 my-3">
				<h2 class="text-white uppercase text-4xl font-bold">Contactame</h2>
				<form class="grid grid-cols-2 gap-3   h-full rounded-lg">
					<LabaledInput name="name" placeholder="Nombre..." />
					<LabaledInput name="lastName" placeholder="Apellido..." />
					<div class="col-span-2">
						<LabaledInput name="email" placeholder="Correo electronico..." />
					</div>
					<div class="col-span-2">
						<LabaledInput name="message" placeholder="Mensaje..." multilpe={true} />
					</div>
					<div class="col-span-2 text-center">
						<Button type="submit">Enviar</Button>
					</div>
				</form>
			</div>
			<div class="w-full h-full pb-6 sm:pb-0">
				<iframe
					src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3368.470052070259!2d-63.25032228497067!3d-32.406564852081964!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x95cc42df24d51be3%3A0x809b13fa837c5010!2sSalta%201075%2C%20Villa%20Mar%C3%ADa%2C%20C%C3%B3rdoba!5e0!3m2!1ses!2sar!4v1674004280043!5m2!1ses!2sar"
					class="w-full h-full rounded-lg"
					title=""
					style="border:0;"
					allowfullscreen={true}
					loading="lazy"
					referrerpolicy="no-referrer-when-downgrade"
				/>
			</div>
		</div>
	</div>
</div>
