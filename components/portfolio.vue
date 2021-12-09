<template>
	<!-- Portfolio -->
	<div class="portfolio_content grid swiper-slide">
		<img :src="port.img" alt="" class="portfolio_img">
		<div class="portfolio_data">
			<h3 class="portfolio_title">{{port.title}}</h3>
			<p class="portfolio_description">{{port.description}}</p>

			<a :href="port.link" target="_blank" class="button button--flex button--small portfolio_button">
				{{port.button_name}}
				<i class="uil uil-arrow-right button_icon"></i>
			</a>
		</div>
	</div>
	
</template>

<script>
module.exports = {
	props: ['port'],
	mounted(){
		let swiper = new Swiper(".portfolio_container", {
			cssMode: true,
			navigation: {
				nextEl: ".swiper-button-next",
				prevEl: ".swiper-button-prev",
			},
			pagination: {
				el: ".swiper-pagination",
				clickable: true,
			},
			keyboard: true,
      });
	}
}
</script>

<style>

</style>