<template>
	<div class="card critic">
		<div class="body">
			<h4 class="title primary">{{title}}</h4>
			<p class="subheading">{{text}}</p>
		</div>
		<div class="author">
			<img :src="img" alt="">
			<span class="author secondary">{{author}}</span>
		</div>
	</div>
</template>

<script>
export default {
	name: 'CritiCard',
	props: {
		title: String,
		text: String,
		img: String,
		author: String,
		magazine: String,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

</style>