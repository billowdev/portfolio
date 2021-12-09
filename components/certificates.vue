<template>
	<div class="certificate_content swiper-slide">
		<div class="certificate_data">
			<div class="certificate_header">
				<img :src="cert.img" alt="" class="certificate_img">
			</div>
		</div>
		<div>
			<h3 class="certificate_name">{{cert.name}}</h3>
			<span class="certificate_platform">{{cert.platform}}</span>
		</div>
		<p class="certificate_description">{{cert.description}}</p>
		<a :href="cert.link" target="_blank" rel="noopener noreferrer">
			<span class="button button--flex button--small button--link services_button">
				View Certificate.
				<i class="uil uil-arrow-right button_icon"></i>
		</span>
		</a>
			
	</div>
</template>

<script>
module.exports = {
	props: ['cert'],
	mounted(){
		let swiper = new Swiper(".certificates_container", {
			loop: true,
			grapCursor: true,
			spaceBetween: 48,

			pagination: {
				el: ".swiper-pagination",
				clickable: true,
				dynamicBullets: true,
			},
			breakpoints:{
				568:{
					slidesPerView: 3,
				}
			},
			keyboard: true,
			mouse: true
		})
	}
}
</script>

<style>

</style>