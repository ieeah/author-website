<template>
	<div class="card critic">
		<div class="body">
			<h4 class="title primary">{{title}}</h4>
			<p class="subheading secondary_dark fw500">{{text}}</p>
		</div>
		<div class="author">
			<img :src="img" :alt="`${magazine} logo`">
			<span class="author secondary_dark">{{author}}</span>
			<span class="magazine primary fw500">{{magazine}}</span>
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
.card.critic {
	margin-bottom: 45px;
	&:last-of-type {
		margin-bottom: 0;
	}
	.body {
		background-color: $bg-2;
		text-align: center;
		padding: 45px;
		margin-bottom: 15px;
		position: relative;
		&::after {
			content: '';
			--size: 15px;
			width: var(--size);
			height: var(--size);
			background-color: $bg-2;
			position: absolute;
			bottom: calc(0px - (var(--size) / 2)) ;
			left: 40px;
			transform: rotate(45deg);
		}
		h4.title {
			font-size: 1.8rem;
			margin-bottom: 15px;
		}
	}
	.author {
		@include flexAlignCenter;
		img {
			margin-right: 30px;
		}
		span {
			font-family: $sans-serif;
		}
		span.author {
			font-size: 1.1rem;
			font-weight: 600;
			margin-right: 10px;
		}
	}
}

</style>