<template>
	<section class="certificates section">
		<h2 class="section_title">Certificates</h2>
		<span class="section_subtitle">FutureSkill Linkedin Udemy etc.</span>
		<div class="certificates_container container swiper">
			<div class="swiper-wrapper">
				<!-- Certificates 1 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (1).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 2 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (2).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 3 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (3).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 4 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (4).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 5 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (5).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 6 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (6).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 7 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (7).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 8 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (8).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 9 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (9).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 10 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (10).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 11 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (11).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 12 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (12).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 13 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (13).jpg" alt="" class="certificates_img">
				</div>
				<!-- Certificates 14 -->
				<div class="certificates_content swiper-slide">
					<img src="../assets/images/cert_img/cer (14).jpg" alt="" class="certificates_img">
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
	let swiper = new Swiper(".certificates_container", {
        pagination: {
          el: ".swiper-pagination",
          type: "fraction",
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      });
	}
};
</script>

<style>

</style>