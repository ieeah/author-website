<template>
	<section id="dig_deeper" class="container md">
		<!-- the section heading -->
		<div class="three_cards_heading">
			<h2 class="section_heading primary">Dig A Little Deeper Into Damon Vaughn</h2>
			<h5 class="subtitle third">find out more about the author himself</h5>
		</div>
		<div class="deeper_articles">
			<!-- the three cards are displayed with a v for -->
			<DeeperCard
				class="card rounded_bt_right"
				v-for="(card, i) in deeperCards" :key="`card_${i}`"
				:img="deeperCards[i].img"
				:title="deeperCards[i].title"
				:text="deeperCards[i].text"
			/>
		</div>
	</section>
</template>

<script>
import DeeperCard from '@/components/DeeperCard.vue';
export default {
	name: 'DigDeeper',
	props: {
		cards: Object,
	},
	components: {
		DeeperCard,
	},
	data() {
		return {
			deeperCards: [
				{
					img: require('@/assets/digDeeper/box-1.jpg'),
					title: 'About Me',
					text: 'Vestibulum ante ipsum primis',
				},
				{
					img: require('@/assets/digDeeper/box-2.jpg'),
					title: 'My Latest Book',
					text: 'Vestibulum ante ipsum primis',
				},
				{
					img: require('@/assets/digDeeper/box-3.jpg'),
					title: 'Book Signing',
					text: 'Vestibulum ante ipsum primis',
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

#dig_deeper {
	padding-block: 60px 120px;
	.deeper_articles {
		@include flexBetween;
	}
}

</style>