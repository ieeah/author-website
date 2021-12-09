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
}
</style>