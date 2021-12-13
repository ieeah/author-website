<template>
	<article>
		<img :src="img" :alt="title">
		<div class="content">
			<h4 class="title primary event_heading fw500">{{title}}</h4>
			<div class="details">
				<span>{{date}} |</span>
				<span>
					{{comments}} Comments
				</span>
			</div>
		</div>
	</article>
</template>

<script>

export default {
	name: 'Article',
	props: {
		img: String,
		title: String,
		date: String,
		comments: Number,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

article {
	background-color: $clear-color;
	img {
		display: block;
		width: 100%;
	}
	.title,
	.content .details span {
		font-family: $sans-serif;
	}
	.title {
		font-size: 1.4rem;
		margin-block: 15px 10px;
	}
	.content .details span {
		font-size: .8rem;
		color: $primary-color;
	}
}

</style>