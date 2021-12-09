<template>
	<div class="head">
		<img :src="require('@/assets/img/hero-07-2x.jpg')" alt="">
		<div class="head_content">
			<nav>
				<ul class="main_nav">
					<li v-for="link in mainNavLinks" :key="`${link.text}_link`">
						<a :href="`${link.url}`">
							{{link.text}}
						</a>
					</li>
					<li>
						<a href="">
							<i class="fas fa-shopping-cart"></i>
						</a>
					</li>
				</ul>
		</nav>
		<div class="hero"></div>
		<div class="more_about"></div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Head',
	data() {
		return {
			mainNavLinks: [
				{
					text: 'Home',
					url: '/',
				},
				{
					text: 'About Me',
					url: '#about',
				},
				{
					text: 'Testimonials',
					url: '#testimonials',
				},
				{
					text: 'My Blog',
					url: '#blog',
				},
				{
					text: 'Meetups',
					url: '#meetups',
				},
				{
					text: 'Shop',
					url: '/shop',
				},
				{
					text: 'Contact Me',
					url: '/contacts',
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

.head {
	position: relative;
	&::before {
		content: '';
		background: rgb(0,0,0);
		background: linear-gradient(0deg, rgba(0,0,0,.8) 20%, rgba(0,0,0,0) 100%);
		@include full100;
		@include absoluteTopLeft;
	}
	img {
	width: 100%;
	height: 800px;
	object-position: center;
	object-fit: cover;
	}
	.head_content {
		@include absoluteTopLeft;
		@include full100;
		.main_nav {
			@include absoluteTopRight;
			padding-right: 150px;
			li {
			margin-inline: 20px;
			padding-top: 40px;
			border-top: 4px solid transparent;
				&:hover {
					border-color: $accent;
					a,
					a i {
						color: $accent;
					}
				}
				a {
				font-weight: bold;
				font-size: .9rem;
				}
			}
		}
	}
}


</style>