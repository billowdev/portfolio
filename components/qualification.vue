<template>
	<section class="qualification section">
		<h2 class="section_title">Qualification</h2>
		<span class="section_subtitle">My personal journey</span>

		<div class="qualification_container container">
			<div class="qualification_tabs">
				<div class="qualification_button buttton--flex qualification_active" data-target="#education">
					<i class="uil uil-graduation-cap qualification_icon"></i>
					Education
				</div>
				<div class="qualification_button buttton--flex" data-target="#work">
					<i class="uil uil-briefcase-alt qualification_icon"></i>
					Work
				</div>
			</div>
			<div class="qualification_sections">
				<!-- Qualification Content 1 -->
				<div class="qualification_content" data-content id="education">
					<!-- qualification 1 -->
					<div class="qualification_data">
						<div>
							
							<h3 class="qualification_title">Mathayom</h3>
							<span class="qualification_subtitle">Phosaiwittaya School</span>
							<div class="qualification_calendar">
								<i class="uil uil-calendar-alt"></i> 2013 - 2019
							</div>
						</div>
						<div>
								<span class="qualification_rounder"></span>
								<span class="qualification_line"></span>
							</div>
					</div>
					<!-- qualification 2 -->
					<div class="qualification_data">
						<div></div>
						<div>
							<span class="qualification_rounder"></span>
							<!-- <span class="qualification_line"></span> -->
						</div>
						<div>
							<h3 class="qualification_title">Computer Science</h3>
							<span class="qualification_subtitle">Rajabhat Sakon Nakhon University</span>
							<div class="qualification_calendar">
								<i class="uil uil-calendar-alt"></i> 2022 - 2024
							</div>
						</div>
					</div>

				</div>
				<!-- Qualification Content 2 -->
				<div class="qualification_content qualification_active" data-content id="work">
										<!-- qualification 1 -->
					<div class="qualification_data">
						<div>
							
							<h3 class="qualification_title">Freelance Websraping</h3>
							<span class="qualification_subtitle">Fastwork</span>
							<div class="qualification_calendar">
								<i class="uil uil-calendar-alt"></i> 2022 - Present
							</div>
						</div>
						<div>
								<span class="qualification_rounder"></span>
								<span class="qualification_line"></span>
							</div>
					</div>
					<!-- qualification 2 -->
					<div class="qualification_data">
						<div></div>
						<div>
							<span class="qualification_rounder"></span>
							<!-- <span class="qualification_line"></span> -->
						</div>
						<div>
							<h3 class="qualification_title">Developer</h3>
							<span class="qualification_subtitle">ALPHA COMPANY</span>
							<div class="qualification_calendar">
								<i class="uil uil-calendar-alt"></i> 2024 - 2025
							</div>
						</div>
					</div>
				
				</div>
			</div>
		</div>
	</section>
</template>

<script>
module.exports = {
	mounted(){
		const tabs = document.querySelectorAll('[data-target]'),
			tabsContents = document.querySelectorAll('[data-content]')

		tabs.forEach(tab =>{
			tab.addEventListener('click', () => {
				const target = document.querySelector(tab.dataset.target)

				tabsContents.forEach(tabsContent =>{
					tabsContent.classList.remove('qualification_active')
				})

				target.classList.add('qualification_active')

				tabs.forEach(tab =>{
					tab.classList.remove('qualification_active')
				})
				tab.classList.add('qualification_active')
			})
		})
	}
};
</script>

<style>

</style>