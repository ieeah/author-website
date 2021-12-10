<template>
	<section>
		<SectionHead :title="critics.title" :subTitle="critics.subTitle"/>
		<div class="container md">
			<div class="critics">
				<div class="left">
					<FocusCritic
						:img="focusCriticCard[0].img"
						:title="focusCriticCard[0].title"
						:subTitle="focusCriticCard[0].subTitle"
						:textOne="focusCriticCard[0].textOne"
						:textTwo="focusCriticCard[0].textTwo"
						:logo="focusCriticCard[0].logo"
						:author="focusCriticCard[0].author"
						:magazine="focusCriticCard[0].magazine"
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
			},
			focusCriticCard: [
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
			],
			cards: [
				{
					title: 'A True Masterpiece, Bravo!',
					text: 'Nulla quis lorem ut libero malesuada feugiat. Vivamus magna justo, lacinia eget consectetur sed, convallis at tellis. Vivamus suscipit tortor eget felis portitor voluptat. Nulla quis lorem ut libero malesuada feug at.',
					img: require('@/assets/CriticCards/theguardian-xsmall.png'),
					author: 'Gerald Hendley,',
					magazine: '` The Guardian`',
				},
				{
					title: 'A Unique View On The World',
					text: 'Sed justo mauris, elementum vestibulum porta et, auctor vel metus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Quisque in felis quis urna tempor laoreet. Duis porta viverra urna, eget iaculis mi vehicula quis.',
					img: require('@/assets/CriticCards/globe-xsmall.png'),
					author: 'Mary Maxey,',
					magazine: '` The Globe And Mail`',
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
.critics {
	@include flexAlignCenter;
	margin-bottom: 200px;
}
.left {
	width: 58%;
	height: 100%;
	background-size: cover;
	position: relative;
	border-bottom-right-radius: 10%;
	overflow: hidden;
	&::before {
		content: '';
		width: 100%;
		height: 100%;
		object-fit: cover;
		@include absoluteTopLeft;
		background: rgb(0,0,0);
		background: linear-gradient(0deg, rgba(0,0,0,.6) 10%, rgba(0,0,0,0.2) 60%);
	}
}

.right {
	width: 42%;
}
</style>