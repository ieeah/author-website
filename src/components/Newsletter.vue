<template>
	<div class="newsletter">
		<h2>Subscribe To My Newsletter</h2>
		<h5 class="accent subtitle">be notified about book signing tour dates</h5>
		<div class="form">
			<input type="text" class="primary fw500" placeholder="Insert your email...*">
			<div class="btn third_bg">Subscribe</div>
		</div>
		<p class="subheading secondary fw500">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Neque doloremque ullam blanditiis at labore!
		</p>
	</div>
</template>

<script>
export default {
	name: 'Newsletter',
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
.newsletter {
	background-image: url('../assets/NewsletterHero/banner-2.jpg');
	@include bgImage;
	@include flexColumn;
	align-items: center;
	text-align: center;
	padding-block: 70px;
	h2 {
		width: 350px;
	}
	h5 {
		font-size: 1rem;
		margin-bottom: 40px;
	}
	.form {
		margin-bottom: 40px;
		@include flexAlignCenter;
		background-position: top;
		input,
		.btn {
			@include flexAlignCenter;
			height: 55px;
			font-size: 1.1rem;
		}
		input {
			padding-left: 15px;
			border-radius: 8px;
			margin-right: 20px;
			width: 300px;
			&:focus,

			&::placeholder {
				font-size: 1.1rem;
			}
		}
		.btn {
			width: 200px;
			justify-content: center;
			font-weight: 600;
		}
	}
	p {
		width: 30%;
	}
}
</style>