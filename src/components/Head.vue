<template>
	<div class="head">
		<div class="hero">
			<img :src="require('@/assets/img/hero-07-2x.jpg')" alt="">
			<img class="brand" :src="require('@/assets/img/author-logo-round.png')" alt="">
			<div class="hero_content">
				<nav>
					<ul class="main_nav">
						<li v-for="link in mainNavLinks" :key="`${link.text}_link`">
							<a :href="`${link.url}`">
								{{link.text}}
							</a>
						</li>
						<li>
							<a href="/shop">
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
				<div class="buy_amz">
					<img :src="require('@/assets/img/book-widget.png')" alt="">
					<div class="buy_txt">
						<h4>Latest Book Release</h4>
						<h5 class="accent_subtitle">d. vaughn autobiography</h5>
						<p>
							Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatem quod, modi esse quos minima incidunt, quasi ad dolorem id reiciendis at?
						</p>
					</div>
					<div class="cta_amz">
						<div class="amz_btn">
							<i class="fab fa-amazon"></i>
							Buy On Amazon
						</div>
						<div class="amz_btn">
							<i class="fab fa-apple"></i>
							Buy On AppStore
						</div>
					</div>
					<div class="square_amz_btns">
						<a href="/demos" class="square_amz">
							<i class="fas fa-folder"></i>
							<div class="text">Demos</div>
						</a>
						<a href="/sales" class="square_amz">
							<div class="price">
								<sup>$</sup>
								39
							</div>
							<div class="text">On Sale</div>
						</a>
					</div>
				</div>
			</div>
		</div>
		<section id="about">
			<div class="container md">
				<h2 class="hand">
					More About Damon Vaughn
				</h2>
				<p>
					Damon Vaughn is a professor of psychology at the University of Toronto, a clinical Psychologist and the author of the multi-million copy bestseller "The story of my life."
				</p>
				<div class="btn third">
					Meet The Author
				</div>
			</div>
		</section>
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

.hero {
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
	.hero_content {
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
			padding-top: 80px;
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
					cursor: pointer;
					&:hover {
						background-color: rgba($color: $primary-color, $alpha: .2);
					}
				}
			}
		}
		.buy_amz {
			@include flexAlignCenter;
			background-color: $clear-color;
			flex-shrink: 0;
			width: 36%;
			padding: 75px;
			position: absolute;
			bottom: 0;
			right: 0;
			img {
				height: 220px;
				width: 50%;
				object-fit: cover;
			}
			.buy_txt {
				width: 50%;
				h4 {
					color: $primary-color;
					font-family: $serif;
					font-size: 1.6rem;
				}
				p {
					color: $primary-color;
					font-family: $sans-serif;
					font-size: .9rem;
				}
			}
			.cta_amz {
				@include flexAlignCenter;
				width: 100%;
				height: 50px;
				.amz_btn {
					@include flexCentered;
					width: 50%;
					height: 100%;
					border: 1px solid rgba($color: $third-color, $alpha: .5);
					font-family: $sans-serif;
					font-weight: bold;
					margin-top: 30px;
					background-color: $bg-3;
					box-shadow: 0 3px 5px rgba($color: $accent-2, $alpha: .2);
					cursor: pointer;
					transition: all .15s ease-in;
					&:hover {
						background-color: $clear-color;
						border-color: $accent-2-focus;
					}
				}
				.amz_btn,
				i {
					color: $primary-color;
					font-size: .9rem;
				}
				.amz_btn:first-of-type {
					border-top-left-radius: 6px;
					border-bottom-left-radius: 6px;
				}
				.amz_btn:last-of-type {
					border-top-right-radius: 6px;
					border-bottom-right-radius: 6px;
					border-left: none;
				}
				i {
					margin-right: 10px;
				}
			}
		}
		.square_amz_btns {
			@include flexCentered;
			flex-direction: column;
			font-size: 1rem;
			position: absolute;
			right: 15px;
			top: -50%;
			.square_amz {
				@include flexCentered;
				flex-direction: column;
				width: 60px;
				height: 60px;
				border-radius: 5px;
				background-color: $clear-color;
				margin-bottom: 5px;
				cursor: pointer;
				i {
					color: #33475b;
					font-size: 1.2rem;
				}
				.price {
					font-size: 1.4rem;
					font-family: $sans-serif;
				}
				.price sup {
					font-size: .8rem;
				}
				.price sup,
				.price {
					color: $accent-2;
					font-weight: bold;
				}
				.text {
					color: $primary-color;
					font-size: .8rem;
					font-family: $sans-serif;
					margin-top: 5px;
				}
			}
		}
	}
}
#about {
	padding-block: 80px;
	.container.md {
		display: flex;
		flex-direction: column;
		align-items: center;
		h2 {
			color: $accent; 
		}
		p {
			color: $primary-color;
			font-family: $sans-serif;
			text-align: center;
			font-size: 1.5rem;
			margin-block: 10px 40px;
		}
		.btn {
			font-weight: bold;
		}
	}
	
}


</style>