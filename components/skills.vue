<template>
			<section class="skills section" id="skills">
			<h2 class="section_title">Skills</h2>
			<span class="section_subtitle">My technical level</span>

			<div class="skills_container container grid">
				<div>
					<!-- Skills 1 -->
					<div class="skills_content skills_open">
						<div class="skills_header">
							<i class="uil uil-brackets-curly skills_icon"></i>

							<div>
								<h1 class="skills_title">Fronted developer</h1>
								<span class="skills_subtitle">More than 1 years</span>
							</div>

							<i class="uil uil-angle-down skills_arrow"></i>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">HTML</h3>
									<span class="skills_number">90%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_html"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">CSS</h3>
									<span class="skills_number">70%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_css"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">JavaScript</h3>
									<span class="skills_number">60%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_javascript"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">React</h3>
									<span class="skills_number">70%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_react"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">Vue JS</h3>
									<span class="skills_number">80%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_vuejs"></span>
								</div>
							</div>
						</div>


					</div>

					<!-- Skills 2 -->
					<div class="skills_content skills_close">
						<div class="skills_header">
							<i class="uil uil-server-network skills_icon"></i>

							<div>
								<h1 class="skills_title">Backend developer</h1>
								<span class="skills_subtitle">More than 1 years</span>
							</div>

							<i class="uil uil-angle-down skills_arrow"></i>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">PHP</h3>
									<span class="skills_number">80%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_php"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">Node JS</h3>
									<span class="skills_number">70%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_node"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">Firebase</h3>
									<span class="skills_number">90%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_firebase"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">Python</h3>
									<span class="skills_number">90%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_python"></span>
								</div>
							</div>
						</div>
					</div>

				</div>

				<div>
					<!-- Skills 3 -->
					<div class="skills_content skills_close">
						<div class="skills_header">
							<i class="uil uil-swatchbook skills_icon"></i>

							<div>
								<h1 class="skills_title">Data Science</h1>
								<span class="skills_subtitle">More than 1 years</span>
							</div>

							<i class="uil uil-angle-down skills_arrow"></i>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">Python</h3>
									<span class="skills_number">90%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_python"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">Pandas</h3>
									<span class="skills_number">80%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_pandas"></span>
								</div>
							</div>
						</div>

						<div class="skills_list grid">
							<div class="skills_data">
								<div class="skills_titles">
									<h3 class="skills_name">Machine Learning</h3>
									<span class="skills_number">80%</span>
								</div>
								<div class="skills_bar">
									<span class="skills_percentage skills_machine"></span>
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
	mounted() {
		// Accordion skills
		const skillsContent = document.getElementsByClassName('skills_content'),
		skillsHeader = document.querySelectorAll('.skills_header')

		function toggleSkills(){
			let itemClass = this.parentNode.className

			for(i = 0; i < skillsContent.length; i++){
				skillsContent[i].className = 'skills_content skills_close'
			}
			if(itemClass === 'skills_content skills_close'){
				this.parentNode.className = 'skills_content skills_open'
			}
		}

		skillsHeader.forEach((el) =>{
			el.addEventListener('click', toggleSkills)
		})
	}
};
</script>

<style>

</style>