<template>
	<div class="deeper_card">
		<img :src="img" :alt="title">
		<div class="content">
			<h3 class="clear event_heading fw500">{{title}}</h3>
			<div class="line"></div>
			<p class="text accent fw500">{{text}}</p>
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
	--margin: 25px;
	width: calc((100% - 100px) / 3);
	height: 512px;
	background-color: red;
	position: relative;
	cursor: pointer;
	transition: all .2s ease-in-out;
	&:hover {
		transform: scale(1.03);
		box-shadow: 0 0 15px rgba($color: $primary-color, $alpha: .5)
	}
	img {
		@include full100;
		object-fit: cover;
		object-position: left;
	}
	.content {
		@include absoluteTopLeft;
		@include flexColumn;
		align-items: center;
		@include full100;
		padding-top: 90%;
		background: rgb(0,0,0);
		background: linear-gradient(0deg, rgba(0,0,0,.6) 10%, rgba(0,0,0,0.2) 60%);
		h3 {
			font-size: 1.6rem;
			font-family: $sans-serif;
		}
		.line {
			height: 2px;
			width: 50px;
			background-color: rgba($color: $clear-color, $alpha: .3);
			margin-block: 15px;
		}
	}
}
</style>