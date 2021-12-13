<template>
	<div id="blog">
		<SectionHead 
			class="container md"
			:title="heading.title"
			:subTitle="heading.subTitle"
			:btnText="heading.btnText"
		/>
		<div class="container md">
			<div class="articles">
				<div class="left">
					
				</div>
				<div class="right">
					<Article
						v-for="(article, i) in articles" :key="`article_${i}`"
						:img="articles[i].img"
						:title="articles[i].title"
						:date="articles[i].date"
						:comments="articles[i].comments"
					/>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import SectionHead from '@/components/SectionHead.vue';
import Article from '@/components/Article.vue';
export default {
	name: 'Blog',
	components: {
		SectionHead,
		Article,
	},
	data() {
		return {
			heading: {
				title: 'Recent Articles',
				subTitle: 'read the latest entries',
				btnText: 'All Articles',
			},
			focusArticle: {	
					img: require('@/assets/blog/blog_1.jpg'),
					title: '20 Creativity Tips',
					author: 'admin',
					date: 'October 24th, 2019',
					cats: ['Event', 'Tips & Tricks'],
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin dignissim, mi at viverra bibendum, lacus erat vulputate quam, non lobortis ex erat quis nibh. Mauris.',
					comments: 0,
			},
			articles: [
				{	
					img: require('@/assets/blog/blog_2.jpg'),
					title: 'What\'s On Your Booklist?',
					author: 'admin',
					date: 'October 19th, 2019',
					cats: ['Reading'],
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin dignissim, mi at viverra bibendum, lacus erat vulputate quam, non lobortis ex erat quis nibh. Mauris.',
					comments: 0,
				},
				{	
					img: require('@/assets/blog/blog_3.jpg'),
					title: 'Istanbul Travel guide',
					author: 'admin',
					date: 'October 16th, 2019',
					cats: ['Travel', 'Guides'],
					text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin dignissim, mi at viverra bibendum, lacus erat vulputate quam, non lobortis ex erat quis nibh. Mauris.',
					comments: 0,
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
		width: 65%;
		Article {
			padding: 50px;
			height: 100%;
		}
	}

	.right {
		width: 35%;
		padding-left: 50px;
		Article {
			padding: 35px;
			img {
				margin-bottom: 35px;
			}
		}
	}
}
</style>