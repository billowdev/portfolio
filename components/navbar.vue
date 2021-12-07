<template>
	<nav class="nav container">
		<a href="#" class="nav_logo">Lacakp</a>

		<div class="nav_menu" id="nav-menu">
			<ul class="nav_list grid">
				<li class="nav_item">
					<a href="#home" class="nav_link nav_icon">
						<i class="uil uil-estate"></i> Home
					</a>
				</li>
				<li class="nav_item">
					<a href="#about" class="nav_link nav_icon">
						<i class="uil uil-user"></i> About
					</a>
				</li>
				<li class="nav_item">
					<a href="#skills" class="nav_link nav_icon">
						<i class="uil uil-file-alt"></i> Skills
					</a>
				</li>
				<li class="nav_item">
					<a href="#services" class="nav_link nav_icon">
						<i class="uil uil-briefcase-alt"></i> Services
					</a>
				</li>
				<li class="nav_item">
					<a href="#portfolio" class="nav_link nav_icon">
						<i class="uil uil-scenery"></i> Portfolio
					</a>
				</li>
				<li class="nav_item">
					<a href="#contact" class="nav_link nav_icon">
						<i class="uil uil-message"></i> Contact
					</a>
				</li>
			</ul>
			<i class="uil uil-times nav_close" id="nav-close"></i>
		</div>
		<div class="nav_btns">
			<div class="nav_toggle" id="nav-toggle">
				<i class="uil uil-apps"></i>
			</div>
		</div>
	</nav>
</template>

<script>
module.exports = {
	mounted() {
		// Menu Show Y Hidden
		const navMenu = document.getElementById('nav-menu'),
		navToggle = document.getElementById('nav-toggle'),
		navClose = document.getElementById('nav-close')

		// Menu Show
		// Validate if constant exists
		if(navToggle){
			navToggle.addEventListener('click', () =>{
				navMenu.classList.add('show-menu')
			})
		}

		// Menu Hidden
		// Validate if constant exists
		if(navClose){
			navClose.addEventListener('click', () =>{
				navMenu.classList.remove('show-menu')
			})
		}

		// Remove Menu Mobile
		const navLink = document.querySelectorAll('.nav_link')

		function linkAction(){
			const navMenu = document.getElementById('nav-menu')
			// When we click on each nav_link, we remove the show-menu class
			navMenu.classList.remove('show-menu')
		}
		navLink.forEach(n => n.addEventListener('click', linkAction))
	}
};



</script>

<style>

</style>