<template>
	<section class="portfolio section" id="portfolio">
		<h2 class="section_title">Portfolio</h2>
		<span class="section_subtitle">Most recent work</span>

		<div class="portfolio_container container swiper">
			<div class="swiper-wrapper">
				<!-- Portfolio 1 -->
				<div class="portfolio_content grid swiper-slide">
					<img src="../assets/images/bg_project_1.png" alt="" class="portfolio_img">
					<div class="portfolio_data">
						<h3 class="portfolio_title">Demo Weblog</h3>
						<p class="portfolio_description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem, aliquam.</p>

						<a href="https://sanedevproj.web.app/" target="_blank" class="button button--flex button--small portfolio_button">
							Demo
							<i class="uil uil-arrow-right button_icon"></i>
						</a>
					</div>
				</div>
				<!-- Portfolio 2 -->
				<div class="portfolio_content grid swiper-slide">
					<img src="../assets/images/bg_project_2.png" alt="" class="portfolio_img">
					<div class="portfolio_data">
						<h3 class="portfolio_title">Timetables web</h3>
						<p class="portfolio_description">Learning vue js concept json fake rest api</p>

						<a href="https://cs63proj.web.app/" target="_blank" class="button button--flex button--small portfolio_button">
							Demo
							<i class="uil uil-arrow-right button_icon"></i>
						</a>
					</div>
				</div>
				<!-- Portfolio 3 -->
				<div class="portfolio_content grid swiper-slide">
					<img src="../assets/images/bg_project_3.png" alt="" class="portfolio_img">
					<div class="portfolio_data">
						<h3 class="portfolio_title">Window Form Application</h3>
						<p class="portfolio_description">Fruit Stock management, poit of sale C# .Net 4.7.2 </p>

						<a href="https://github.com/lacakp/Project-Fruit-Shop" target="_blank" class="button button--flex button--small portfolio_button">
							Repository
							<i class="uil uil-arrow-right button_icon"></i>
						</a>
					</div>
				</div>

				<!-- Portfolio 4 -->
				<div class="portfolio_content grid swiper-slide">
					<img src="../assets/images/bg_project_4.png" alt="" class="portfolio_img">
					<div class="portfolio_data">
						<h3 class="portfolio_title">Fruit Classification</h3>
						<p class="portfolio_description">Learning Digital Image Processing Fruit classification using python Deep learning ResNet50 Transfer learning</p>

						<a href="https://github.com/lacakp/Project-Fruit-Image-Classification" target="_blank" class="button button--flex button--small portfolio_button">
							Repository
							<i class="uil uil-arrow-right button_icon"></i>
						</a>
					</div>
				</div>

				<!-- Portfolio 5 -->
				<div class="portfolio_content grid swiper-slide">
					<img src="../assets/images/bg_project_5.png" alt="" class="portfolio_img">
					<div class="portfolio_data">
						<h3 class="portfolio_title">Youtube</h3>
						<p class="portfolio_description">Youtube Channel since i was collecge student this channel abot basic coding Matlab, Python etc.</p>
						<a href="https://www.youtube.com/channel/UC_rdRnVhKYYkD5d-3TsnvLA" target="_blank" class="button button--flex button--small portfolio_button">
							Demo
							<i class="uil uil-arrow-right button_icon"></i>
						</a>
					</div>
				</div>
			</div>
				<!-- Add Arrow -->
				 <div class="swiper-button-next">
					 <i class="uil uil-angle-right-b swiper-portfolio-icon"></i>
				 </div>
				<div class="swiper-button-prev">
					<i class="uil uil-angle-left-b swiper-portfolio-icon"></i>
				</div>
				<!-- Add Pagination -->
				<div class="swiper-pagination"></div>
		</div>
	</section>

</template>

<script>
module.exports = {
	mounted(){
		let swiper = new Swiper(".portfolio_container", {
			cssMode: true,
			loop: true,

			navigation: {
				nextEl: ".swiper-button-next",
				prevEl: ".swiper-button-prev",
			},
			pagination: {
				el: ".swiper-pagination",
				clickable: true,
			},
      });
	}
};
</script>

<style>

</style>