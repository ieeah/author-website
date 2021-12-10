<template>
	<section>
		<SectionHead :title="title" :subTitle="subTitle"/>
		<div class="container md">
			<div class="critics">
				<div class="left">
					<img :src="require('@/assets/img/testimonial2-2x.jpg')" alt="">
					<div class="content">
						<h3>Best Author Of His Generation</h3>
						<h4>This book will change your perspective on life</h4>
						<p>
							Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, vel autem impedit obcaecati eveniet commodi voluptate officia beatae blanditiis atque et tempora temporibus facere deleniti placeat laudantium laboriosam natus quae!
						</p>
						<p>
							Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores, vel autem impedit obcaecati eveniet commodi voluptate officia beatae blanditiis atque et tempora temporibus facere deleniti placeat laudantium laboriosam natus quae!
						</p>
						<div class="critic_author">
							<img :src="require('@/assets/img/nytimes-logo-white-xsmall.png')" alt="">
							<h4>Justine Kilpatrick,</h4>
							<h4 class="third">The New York Times</h4>
						</div>
					</div>
				</div>
				<div class="right"></div>
			</div>
		</div>
	</section>
</template>

<script>
import SectionHead from '@/components/SectionHead.vue';
export default {
	name: 'Critics',
	components: {
		SectionHead,
	},
	data() {
		return {
			title: 'What The Critics Say',
			subTitle: 'testimonials from around the world',
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
.left {
	width: 58%;
	background-size: cover;
	position: relative;
	margin-bottom: 200px;
	border-bottom-right-radius: 100px;
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
	img {
		width: 100%;
		height: 750px;
		display: block;
		object-fit: cover;
	}
	.content {
		@include absoluteTopLeft;
		padding: 120px 100px;
		h3 {
			padding-bottom: 30px;
			margin-bottom: 30px;
			border-bottom: 1px solid $clear-color;
		}
		h4 {
			font-family: $sans-serif;
			margin-bottom: 30px;
		}
		p {
			font-weight: 500;
			margin-bottom: 30px;
		}
	}
	.critic_author {
		display: flex;
		margin-top: 50px;
		img {
			width: 30px;
			margin-right: 15px;
			transform: translateY(-10px);
			object-fit: contain;
			object-position: top;
		}
		h4 {
			font-size: 1.1rem;
		}
		h4:first-of-type {
			margin-right: 4px;
		}
	}
	
}
</style>