<template>
	<nav class="nav container">
				<a href="#" class="nav_logo">
					<!-- <img class="logo" src="assets/images/lacakp_logo_t.png" width="100px" alt="lacakp_logo"> -->
					Lacakp
				</a>
				
				<div class="nav_menu" id="nav-menu">
					<ul class="nav_list grid">
						<li class="nav_item">
							<a href="#home" class="nav_link">
								<i class="uil uil-estate nav_icon"></i> Home
							</a>
						</li>
						<li class="nav_item">
							<a href="#about" class="nav_link">
								<i class="uil uil-user nav_icon"></i> About
							</a>
						</li>
						<li class="nav_item">
							<a href="#skills" class="nav_link">
								<i class="uil uil-file-alt nav_icon"></i> Skills
							</a>
						</li>
						<li class="nav_item">
							<a href="#services" class="nav_link">
								<i class="uil uil-briefcase-alt nav_icon"></i> Services
							</a>
						</li>
						<li class="nav_item">
							<a href="#portfolio" class="nav_link">
								<i class="uil uil-scenery nav_icon"></i> Portfolio
							</a>
						</li>
						<li class="nav_item">
							<a href="#contact" class="nav_link">
								<i class="uil uil-message nav_icon"></i> Contact
							</a>
						</li>
					</ul>
					<i class="uil uil-times nav_close" id="nav-close"></i>
				</div>
				<div class="nav_btns">
					<!-- btn change theme -->
					<i class="uil uil-moon change-theme" id="theme-button"></i>
		
					<div class="nav_toggle" id="nav-toggle">
						<i class="uil uil-apps"></i>
					</div>
				</div>

				<div class="progressContainer">
      			<div class="progressBar"></div>

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

		// ---------------------- Menu Hidden ---------------------- 
		// Validate if constant exists
		if(navClose){
			navClose.addEventListener('click', () =>{
				navMenu.classList.remove('show-menu')
			})
		}

		// ---------------------- Remove Menu Mobile ---------------------- 
		const navLink = document.querySelectorAll('.nav_link')

		function linkAction(){
			const navMenu = document.getElementById('nav-menu')
			// When we click on each nav_link, we remove the show-menu class
			navMenu.classList.remove('show-menu')
		}
		navLink.forEach(n => n.addEventListener('click', linkAction))

		// ---------------------- change backgroud header ----------------------
		function scrollHeader(){
			const nav = document.getElementById('header')
			// When the scroll is greater than 200 viewport height, add the scroll-header class to the header tag
			if(this.scrollY >= 200) nav.classList.add('scroll-header'); else nav.classList.remove('scroll-header')
		}
		window.addEventListener('scroll', scrollHeader)


	// ---------------------- show scroll up ---------------------- 
		function scrollUp(){
			const scrollUp = document.getElementById('scroll-up')
			// When the scroll is higher than 560 viewport height, add the show-scroll class to the a tag with the scroll-top class
			if(this.scrollY >= 560) scrollUp.classList.add('show-scroll'); 
			else scrollUp.classList.remove('show-scroll')
		}
		window.addEventListener('scroll', scrollUp)


	// ---------------------- dark theme ---------------------- 
		const themeButton = document.getElementById('theme-button')
		const darkTheme = 'dark-theme'
		const iconTheme = 'uil-sun'

		// Previously selected topic (if user selected)
		const selectedTheme = localStorage.getItem('selected-theme')
		const selectedIcon = localStorage.getItem('selected-icon')

		// We obtain the current theme that the interface has by validating the dark-theme class
		const getCurrentTheme = () => document.body.classList.contains(darkTheme) ? 'dark' : 'light'
		const getCurrentIcon = () => themeButton.classList.contains(iconTheme) ? 'uil-moon' : 'uil-sun'

		// We validate if the user previously chose a topic
		if (selectedTheme) {
		// If the validation is fulfilled, we ask what the issue was to know if we activated or deactivated the dark
		document.body.classList[selectedTheme === 'dark' ? 'add' : 'remove'](darkTheme)
		themeButton.classList[selectedIcon === 'uil-moon' ? 'add' : 'remove'](iconTheme)
		}

		// Activate / deactivate the theme manually with the button
		themeButton.addEventListener('click', () => {
			// Add or remove the dark / icon theme
			document.body.classList.toggle(darkTheme)
			themeButton.classList.toggle(iconTheme)
			// We save the theme and the current icon that the user chose
			localStorage.setItem('selected-theme', getCurrentTheme())
			localStorage.setItem('selected-icon', getCurrentIcon())
		})

		// ---------------------- progress bar ---------------------- 
		window.addEventListener('scroll', function(){
			let wintop = this.scrollY
			let navbar = document.querySelector(".navbar")

			let winheight = this.innerHeight
			let docheight = document.querySelector("body").offsetHeight
			let totalScroll = ( wintop / (docheight - winheight) ) * 100

			let bar = document.querySelector(".progressBar")
			bar.style.width = `${totalScroll}%`
    	})
	}
	
};

</script>

<style>

</style>