<template>
	<section id="dig_deeper" class="container lg ">
		<div class="three_cards_heading">
			<h2 class="section_heading primary">Dig A Little Deeper Into Damon Vaughn</h2>
			<h5 class="subtitle third">find out more about the author himself</h5>
		</div>
		<div class="deeper_articles">
			
		</div>
	</section>
</template>

<script>
export default {
	name: 'DigDeeper',
	props: {
		cards: Object,
	},
	data() {
		return {
			deeperCards: [
				{
					img: require('@/assets/digDeeper/box-1.jpg'),
					title: '',
					text: '',
				},
				{
					img: require('@/assets/digDeeper/box-2.jpg'),
					title: '',
					text: '',
				},
				{
					img: require('@/assets/digDeeper/box-3.jpg'),
					title: '',
					text: '',
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

#dig_deeper {
	padding-block: 60px;
	@include flexBetween;
}

</style>