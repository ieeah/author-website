<template>
	<article>
		<img :src="img" :alt="title">
		<div class="content">
			<h4 class="primary event_heading fw500">{{title}}</h4>
			<div class="details">
				<span>By 
					<span class="primary">{{author}}</span>
					 |
				</span>
				<span class="primary">{{date}}</span>
				<span>
					Categories: 
					<span 	class="primary"
							v-for="(cat, i) in cats" :key="`${cats[i]}`"
					>
						{{cats[i]}}
					</span>
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
		author: String,
		date: String,
		cats: Array,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

article {
	background-color: $clear-color;
	padding: 30px;
	img {
		display: block;
	}
}
</style>