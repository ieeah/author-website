<template>
	<section id="testimonials">
		<!-- section heading -->
		<SectionHead 
			class="container md"
			:title="critics.title"
			:subTitle="critics.subTitle"
			:btnText="critics.btnText"
		/>
		<div class="container md">
			<!-- the container is flex displayed and contain the two sections with main and secondary elements -->
			<div class="critics">
				<div class="left">
					<FocusCritic
						:img="focusCriticCard.img"
						:title="focusCriticCard.title"
						:subTitle="focusCriticCard.subTitle"
						:textOne="focusCriticCard.textOne"
						:textTwo="focusCriticCard.textTwo"
						:logo="focusCriticCard.logo"
						:author="focusCriticCard.author"
						:magazine="focusCriticCard.magazine"
					/>
					
				</div>
				<div class="right">
					<CritiCard v-for="(critics, i) in cards" :key="`critic_${i}`"
						:title="cards[i].title"
						:text="cards[i].text"
						:img="cards[i].img"
						:logo="cards[i].logo"
						:author="cards[i].author"
						:magazine="cards[i].magazine"
					/>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import SectionHead from '@/components/SectionHead.vue';
import CritiCard from '@/components/CritiCard.vue';
import FocusCritic from '@/components/FocusCritic.vue';
export default {
	name: 'Critics',
	components: {
		SectionHead,
		CritiCard,
		FocusCritic,
	},
	data() {
		return {
			critics: {
				title: 'What The Critics Say',
				subTitle: 'testimonials from around the world',
				btnText: 'Read All Testimonials',
			},
			focusCriticCard: 
				{
					img: require('@/assets/CriticCards/testimonial2-2x.jpg'),
					title: 'Best Author Of His Generation',
					subTitle: 'This book will change your perspective on life',
					textOne: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, vel autem impedit obcaecati eveniet commodi voluptate officia beatae blanditiis atque et tempora temporibus facere deleniti placeat laudantium laboriosam natus quae!',
					textTwo: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, vel autem impedit obcaecati eveniet commodi voluptate officia beatae blanditiis atque et tempora temporibus facere deleniti placeat laudantium laboriosam natus quae!',
					logo: require('@/assets/CriticCards/nytimes-logo-white-xsmall.png'),
					author: '`Justine Kilpatrick, `',
					magazine: 'The New York Times',
				},
			cards: [
				{
					title: 'A True Masterpiece, Bravo!',
					text: 'Nulla quis lorem ut libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellis. Vivamus suscipit tortor eget felis portitor voluptat. Nulla quis lorem ut libero malesuada feug at.',
					img: require('@/assets/CriticCards/theguardian-xsmall.png'),
					author: 'Gerald Hendley,',
					magazine: 'The Guardian',
				},
				{
					title: 'A Unique View On The World',
					text: 'Sed justo mauris, elementum vestibulum porta et, auctor vel metus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Quisque in felis quis urna tempor laoreet. Duis porta viverra urna, eget iaculis mi vehicula quis.',
					img: require('@/assets/CriticCards/globe-xsmall.png'),
					author: 'Mary Maxey,',
					magazine: 'The Globe And Mail',
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
.critics {
	@include flexNoWrap;
	margin-bottom: 100px;
}
.left {
	width: 58%;
	background-size: cover;
}

.right {
	width: 42%;
	padding-left: 80px;
}
</style>