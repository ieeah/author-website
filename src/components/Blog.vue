<template>
	<div id="blog">
		<SectionHead 
			:title="heading.title"
			:subTitle="heading.subTitle"
			:btnText="heading.btnText"
		/>
		<div class="container md">
			<div class="articles">
				<div class="left">
					
				</div>
				<div class="right">
					
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import SectionHead from '@/components/SectionHead.vue';
export default {
	name: 'Blog',
	components: {
		SectionHead,
	},
	data() {
		return {
			heading: {
				title: 'Recent Articles',
				subTitle: 'read the latest entries',
				btnText: 'All Articles',
			},
			articles: [
				{	
					img: require('@/assets/blog/blog_1.jpg'),
					title: '20 Creativity Tips',
					author: 'admin',
					date: 'October 24th, 2019',
					cats: ['Event', 'Tips & Tricks'],
				},
				{	
					img: require('@/assets/blog/blog_1.jpg'),
					title: 'Whats\'s On Your Booklist?',
					author: 'admin',
					date: 'October 19th, 2019',
					cats: ['Reading'],
				},
				{	
					img: require('@/assets/blog/blog_1.jpg'),
					title: 'Istanbul Travel guide',
					author: 'admin',
					date: 'October 16th, 2019',
					cats: ['Travel', 'Guides'],
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

#blog {
	padding-block: 60px;
	background-color: $bg-2;
	.articles {
	@include flexNoWrap;
	margin-bottom: 100px;
	}
	.left {
		width: 58%;
		height: 100%;
	}

	.right {
		width: 42%;
		padding-left: 80px;
	}
}
</style>