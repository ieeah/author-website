<template>
	<article>
		<img :src="img" :alt="title">
		<div class="content">
			<h3 class="title primary">
				{{title}}
			</h3>
			<div class="details">
				<span class="secondary_dark">
					By
					<span class="primary">
						{{author}}
					</span>
					|
				</span>
				<span class="primary">{{date}} | </span>
				<span class="secondary_dark">
					Categories: 
					<span class="primary"
						v-for="category in cats" :key="category"
					>
						{{category}}
					</span>
				</span>
			</div>
			<p class="text secondary_dark fw500">{{text}}</p>
		</div>
	</article>
</template>

<script>
export default {
	name: 'FocusArticle',
	props: {
		img: String,
		title: String,
		author: String,
		date: String,
		cats: Array,
		text: String,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

img {
	max-width: 100%;
	margin-bottom: 40px;
}
.content {
		padding-left: 35px;
		.title {
			font-family: $sans-serif;
			font-size: 1.6rem;
			font-weight: 500;
			margin-bottom: 10px;
		}
		.details span {
			font-family: $sans-serif;
			font-size: .75rem;
		}
		.text {
			margin-top: 15px;
			font-family: $sans-serif;
		}
}

</style>