<template>
	<div class="head">
		<img :src="require('@/assets/img/hero-07-2x.jpg')" alt="">
		<img class="brand" :src="require('@/assets/img/author-logo-round.png')" alt="">
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
		<div class="hero_text">
			<h1 class="hand">Damon Vaughn</h1>
			<h2>Best-selling author and the most influential public intellectual in the western world right now.</h2>
			<p class="quote">- The New York times</p>
			<div class="slide_btns">
				<div class="arrow">
					<i class="fas fa-arrow-left"></i>
				</div>
				<div class="arrow">
					<i class="fas fa-arrow-right"></i>
				</div>
			</div>
		</div>
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
		background: linear-gradient(0deg, rgba(0,0,0,.8) 20%, rgba(0,0,0,0.2) 100%);
		@include full100;
		@include absoluteTopLeft;
	}
	img {
	width: 100%;
	height: 800px;
	object-position: center;
	object-fit: cover;
	}
	img.brand {
		width: 190px;
		height: 190px;
		position: absolute;
		left: 145px;
		top: 2px;
	}
	.head_content {
		@include absoluteTopLeft;
		@include full100;
		display: flex;
		align-items: center;
		.main_nav {
			@include absoluteTopRight;
			padding-right: 145px;
			li {
			margin-left: 40px;
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
		.hero_text {
			padding-left: 240px;
			padding-top: 50px;
			h1 {
				color: $accent;
			}
			h2 {
				font-size: 3em;
				width: 50%;
				line-height: 1.5;
			}
			.quote {
				font-size: 1.35em;
				margin-top: 30px;
			}
			.slide_btns {
				margin-top: 40px;
				display: flex;
				.arrow {
					padding: 18px;
					background-color: $primary-color;
					margin-left: 2px;
				}
			}
		}
	}
}


</style>