<template>
	<section class="audiobooks">
		<div class="platforms">
			<div class="container sm">
				<img :src="require('@/assets/audiobookHero/ebay-logotan-2x-200x66.png')" alt="">
				<img :src="require('@/assets/audiobookHero/audible-logotan-2x-200x66.png')" alt="">
				<img :src="require('@/assets/audiobookHero/kindlefire-logotan-2x-200x66.png')" alt="">
				<img :src="require('@/assets/audiobookHero/bb-logotan-2x-200x66.png')" alt="">
			</div>
		</div>
		<div class="hero">
			<div class="container sm">
				<img :src="require('@/assets/audiobookHero/audible-app-2x-600x628.png')" alt="">
				<div class="audiobook_banner_text">
					<h2>New Audiobook</h2>
					<h5 class="accent subtitle">no time to read? no problem. listen to it</h5>
					<p class="subheading secondary">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Neque doloremque ullam blanditiis at labore!</p>
					<div class="audiobook_banner_platforms">
						<img :src="require('@/assets/audiobookHero/audible-logo.png')" alt="">
						<img :src="require('@/assets/audiobookHero/bn-logo-tall.png')" alt="">
						<img :src="require('@/assets/audiobookHero/kindle-logo-tall.png')" alt="">
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Audiobook',
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
.audiobooks {
	.platforms {
		background-color: $bg-2;
		height: 200px;
		.container.sm {
			height: 100%;
			@include flexAlignCenter;
			justify-content: space-around;
		}
	}
	.hero {
		background-image: url('../assets/audiobookHero/banner.jpg');
		@include bgImage;
		.container.sm {
			@include flexAlignCenter;
			padding-top: 70px;
			img {
				width: 45%;
			}
			.audiobook_banner_text {
				width: 53%;
				margin-left: 2%;
			}
			.audiobook_banner_text {
				text-align: center;
				padding: 40px;
				h5 {
					font-size: 1rem;
					margin-bottom: 40px;
				}
				p {
					width: 85%;
					margin-inline: auto;
					margin-bottom: 40px;
				}
				.audiobook_banner_platforms {
					@include flexAlignCenter;
					justify-content: space-around;
					img {
						width: 130px;
					}
				}
			}
		}
	}
}
</style>