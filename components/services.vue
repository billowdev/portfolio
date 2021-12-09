<template>
<section class="services section" id="services">
	<h2 class="section_title">Services</h2>
	<span class="section_subtitle">What i offer</span>

	<div class="services_container container grid">
		<!-- Secvice 1 -->
		<div class="services_content">
			<div>
				<i class="uil uil-file-download-alt services_icon"></i>
				<h3 class="services_title">Web Scraping <br> Developer</h3>
			</div>

			<span class="button button--flex button--small button--link services_button">
				View More
				<i class="uil uil-arrow-right button_icon"></i>
			</span>
			<div class="services_modal">
				<div class="services_modal-content">
					<h4 class="services_modal-title">Web Scraping <br> Developer</h4>
					<i class="uil uil-times services_modal-close"></i>

					<ul class="services_modal-services grid">
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>ดึงข้อมูลเว็บไซต์ด้วย Python</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>บันทึกข้อมูลอยู่ในรูปแบบไฟล์ JSON, CSS, xlsx(Excel)</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>สคริปต์สำหรับดึงข้อมูลเว็บไซต์สำหรับใช้ดึงข้อมูลในครั้งต่อไปด้วยตนเอง</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>ทำงานไวในระยะเวลา 3-4 วันแล้วแต่ความยากง่ายของเว็บไซต์</p>
						</li>
						
					</ul>
				</div>
			</div>

		</div>
		<!-- Secvice 2 -->
		<div class="services_content">
			<div>
				<i class="uil uil-arrow services_icon"></i>
				<h3 class="services_title">Web <br> Developer</h3>
			</div>

			<span class="button button--flex button--small button--link services_button">
				View More
				<i class="uil uil-arrow-right button_icon"></i>
			</span>
			<div class="services_modal">
				<div class="services_modal-content">
					<h4 class="services_modal-title">Web <br> Developer</h4>
					<i class="uil uil-times services_modal-close"></i>

					<ul class="services_modal-services grid">
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>Single-page Application</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>Web Application</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>Responsive Design</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>ทำงานไวเสร็จในระยะเวลาที่กำหนดแล้วแต่ความยากง่ายของเว็บไซต์</p>
						</li>
						
					</ul>
				</div>
			</div>
		</div>
		<!-- Secvice 3 -->
		<div class="services_content">
			<div>
				<i class="uil uil-mobile-android services_icon"></i>
				<h3 class="services_title">Mobile <br> Application</h3>
			</div>

			<span class="button button--flex button--small button--link services_button">
				View More
				<i class="uil uil-arrow-right button_icon"></i>
			</span>
			<div class="services_modal">
				<div class="services_modal-content">
					<h4 class="services_modal-title">Mobile <br> Application</h4>
					<i class="uil uil-times services_modal-close"></i>

					<ul class="services_modal-services grid">
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>พัฒนาแอพพลิเคชันด้วย Flutter</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>รองรับทั้ง Android และ IOS</p>
						</li>
						<li class="services_modal-service">
							<i class="uil uil-check-circle services_modal-icon"></i>
							<p>ทำงานไวในระยะเวลาแล้วแต่ความยากง่ายของแอพพลิเตชัน</p>
						</li>
					</ul>
				</div>
			</div>
		</div>
		
	</div>
</section>
</template>

<script>
module.exports = {
	mounted(){
		// modal
		const modalViews = document.querySelectorAll('.services_modal'),
			modalBtns = document.querySelectorAll('.services_button'),
			modalCloses = document.querySelectorAll('.services_modal-close')
		let modal = function(modalClick){
			modalViews[modalClick].classList.add('active-modal')
		}

		modalBtns.forEach((modalBtn, i) => {
			modalBtn.addEventListener('click', () =>{
				modal(i)
			})
		})

		modalCloses.forEach((modalClose) => {
			modalClose.addEventListener('click', () =>{
				modalViews.forEach((modalView) =>{
					modalView.classList.remove('active-modal')
				})
			})
		})
	}
};
</script>

<style>

</style>