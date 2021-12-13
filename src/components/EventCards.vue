<template>
	<div class="eventCard">
		<div class="head">
			<img :src="cover" :alt="title">
		</div>
		<div class="body">
			<h4 class="primary event_heading fw500">{{title}}</h4>
			<p class="subheading secondary_dark container lg fw500">{{text}}</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'EventCard',
	props: {
		cover: String,
		title: String,
		text: String,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
.eventCard {
	width: calc(100% / 3);
	margin-inline: 25px;
	margin-bottom: 20px;
	background-color: $clear-color;
	cursor: pointer;
	&:hover .head img {
		filter: opacity(.9) contrast(70%);
	}
	.head {
		img {
			width: 100%;
			object-fit: cover;
			transition: all .1s ease-out;
		}
	}
	.body {
		text-align: center;
		h4 {
			font-family: $sans-serif;
			font-size: 1.5rem;
			margin-block: 40px 30px;
		}
		p {
			border-top: 1px solid rgba($color: $primary-color, $alpha: .2);
			padding-top: 20px;
		}
	}
}
</style>