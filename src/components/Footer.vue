<template>
	<div class="footer">
		<!-- the footer is displayed as a flex-column parent -->
		<div class="top_footer">
			<!-- the author logo, absolute positioned -->
			<img :src="require('@/assets/img/author-logo-round.png')" alt="author logo" class="brand">
			<div class="container md">
				<!-- first of three columns displayed in a flex container -->
				<div class="column">
					<h3 class="col_title">{{col1[0]}}</h3>
					<!-- description -->
					<p class="clear demi_opac">{{col1[1]}}</p>
				</div>
				<!-- column 2 -->
				<div class="column">
					<h3 class="col_title">{{col2Title}}</h3>
					<!-- a v-for rendered list -->
					<ul class="list_two">
						<li v-for="(link, i) in col2" :key="`link_${i}`"
							class="fw500"
						>
							<i class="fas fa-chevron-right"></i>
							<a :href="link.url">{{link.text}}</a>
						</li>
					</ul>
				</div>
				<!-- column three -->
				<div class="column">
					<h3 class="col_title">{{col3Title}}</h3>
					<!-- contacts links -->
					<ul class="list_three">
						<li v-for="(link, i) in col3" :key="`link_${i}`">
							<p class="demi_opac">{{link}}</p>
							<span v-if="i == col3.length - 1">
								<a class="fw500" :href="`mailto:${col3Mail.mail}`">{{col3Mail.mail}}</a>
							</span>
						</li>
						<li>
							<a 
								v-for="(icon, i) in col3Socials"
								:key="`social_${i}`"
								:href="icon.url"
							>
								<i :class="icon.icon" class="demi_opac"></i>
							</a>
						</li>
					</ul>
				</div>
			</div>
		</div>
		<div class="sub_footer">
			<p>&copy; Copyright 2012 - 2020 | Avada Theme by <a href="#themefusion">ThemeFusion</a> | All rights Reserved | Powered by <a href="#wordpress">WordPress</a>
			</p>
		</div>
		<a class="div to_top" href="#top">
			<i class="fas fa-chevron-up"></i>
		</a>
	</div>
</template>

<script>
export default {
	name: 'Footer',
	data() {
		return {
			col1: [
				'ABOUT ME',
				'Vivamus suscipit tortor eget felis porttitor voluptat. Nulla quis lorem ut libero malesuada feugiat. Vivamus suscipit torto eget felis porttitor voluptat.'
			],
			col2Title: 'USEFUL LINKS',
			col2: [
				{
					text: 'Latest Books',
					url: '/latest_books',
				},
				{
					text: 'Upcoming Events',
					url: '#meetups',
				},
				{
					text: 'Recent Articles',
					url: '#blog',
				},
				{
					text: 'Business Enquiries',
					url: '/Enquiries',
				},
				{
					text: 'Visit My Foundation',
					url: '/foundation',
				},
			],
			col3Title: 'CONTACT INFO',
			col3: [
				'63 E. Studebaker Street BolingBrook, IL 60440',
				'Phone: (800) 000-0000',
				'Mobile: (800) 000-0000',
				'Email',
			],
			col3Mail: {
				text: 'Email',
				mail: 'info@your-company.com',
			},
			col3Socials: [
				{
					icon: 'fab fa-facebook-f',
					url: 'https://facebook.com',
				},
				{
					icon: 'fab fa-twitter',
					url: 'https://twitter.com',
				},
				{
					icon: 'fab fa-instagram',
					url: 'https://instagram.com',
				},
				{
					icon: 'fab fa-linkedin-in',
					url: 'https://linkedin.com',
				},
				{
					icon: 'fab fa-youtube',
					url: 'https://youtube.com',
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

.footer {
	background-image: url('../assets/Footer/footer-3.jpg');
	background-size: cover;
	background-position: top;
	height: 510px;
	position: relative;
	@include flexColumn;
	img.brand {
		width: 150px;
		height: 150px;
		position: absolute;
		left: 100px;
		top: 110px;
	}
	.top_footer {
		padding-top: 100px;
		position: relative;
		flex-grow: 1;
		.container {
		@include flexBetween;
		}
		.column {
			width: calc(100% / 3);
			padding-left: 90px;
			.col_title {
				font-size: 1.2rem;
				margin-bottom: 40px;
			}
			p.clear,
			p.demi_opac,
			i.demi_opac {
				font-size: .9rem;
				opacity: .7;
			}
			ul {
				li {
					display: block;
					margin-bottom: 15px;
					font-size: .9rem;
				}
			}

			.list_two li {
				padding-left: 10px;
				i {
					margin-right: 20px;
					font-size: .7em;
				}
			}

			.list_three p {
				display: inline;
				margin-right: 5px;
			}
			.list_three i {
				margin-right: 20px;
				font-size: 1.25em;
			}
		}
	}
	.sub_footer {
		@include flexCentered;
		height: 100px;
		p {
			font-size: .8rem;
			color: $secondary-clear;
			a {
				font-weight: 500;
			}
		}
	}
	.to_top {
		padding: 9px 18px 5px 18px;
		background-color: #303030;
		width: fit-content;
		border-radius: 3px;
		position: absolute;
		bottom: 0;
		right: 100px;
	}
}


</style>