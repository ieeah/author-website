<template>
	<div class="deeper_card">
		<img :src="img" :alt="title">
		<div class="content">
			<h4 class="clear event_heading fw500">{{title}}</h4>
			<div class="line"></div>
			<div class="text accent">{{text}}</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'DeeperCard',
	props: {
		img: String,
		title: String,
		text: String,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

.deeper_card {
	width: calc((100% - 150px) / 3);
	margin-inline: 25px;
	height: 512px;
	background-color: red;
	position: relative;
	img {
		@include full100;
		object-fit: cover;
		object-position: left;
	}
	.content {
		@include absoluteTopLeft;
		text-align: center;
		@include full100;
		padding-top: 80%;
		background: rgb(0,0,0);
		background: linear-gradient(0deg, rgba(0,0,0,.6) 10%, rgba(0,0,0,0.2) 60%);
	}
}
</style>