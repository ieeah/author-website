<template>
	<div class="card critic">
		<div class="body">
			<h4 class="title primary">{{title}}</h4>
			<p class="subheading secondary_dark">{{text}}</p>
		</div>
		<div class="author">
			<img :src="img" alt="">
			<span class="author secondary_dark">{{author}}</span>
			<span class="magazine primary">{{magazine}}</span>
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
	.body {
		background-color: $bg-2;
		text-align: center;
		padding: 55px;
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
		p {
			font-weight: 500;
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
		span.magazine {
			font-weight: 500;
		}
	}
}

</style>