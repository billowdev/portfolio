<template>
  <section class="contact section" id="contact">
		<h2 class="section_title">Contact Me</h2>
		<span class="section_subtitle">Get in Touch</span>

		<div class="contact_container container grid">
			<div>
				<div class="contact_information">
					<i class="uil uil-user contact_icon"></i>
					<div>
						<h3 class="contact_title">Name</h3>
						<span class="contact_subtitle">Akkarapon Phikulsri</span>
					</div>
				</div>
					<div class="contact_information">
					<i class="uil uil-envelope contact_icon"></i>
					<div>
						<h3 class="contact_title">Message</h3>
						<span class="contact_subtitle">lacakp.contact@gmail.com</span>
					</div>
				</div>
					<div class="contact_information">
					<i class="uil uil-map-marker contact_icon"></i>
					<div>
						<h3 class="contact_title">Address</h3>
						<span class="contact_subtitle">Thailand</span>
					</div>
				</div>
			</div>

			<form action="https://formspree.io/f/xbjwjwlb" method="post" class="contact_form grid">
				<div class="contact_inputs grid">
					<div class="contact_content">
						<label for="" class="contact_label">Name</label>
						<input type="text" name="name" class="contact_input">
					</div>
					<div class="contact_content">
						<label for="" class="contact_label">Email</label>
						<input type="email" name="_replyto" class="contact_input">
					</div>
					<div class="contact_content">
						<label for="" class="contact_label">Title</label>
						<input type="text" name="title" class="contact_input">
					</div>
					<div class="contact_content">
						<label for="" class="contact_label">Message</label>
						<textarea name="message" cols="0" rows="7" class="contact_input"></textarea>
					</div>

					<div>
						<button href="#home" class="button button--flex button--contact" type="submit" value="Send">
							Send Message
							<i class="uil uil-message button_icon"></i>
						</button>
					</div>
				</div>
				
			</form>
		</div>
	</section>
</template>

<script>
module.exports = {

}
</script>

<style scope>

</style>