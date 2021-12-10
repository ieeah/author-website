<template>
	<div class="focus critic">
		<img :src="img" :alt="`${title}`">
		<!-- <img :src="require('@/assets/img/testimonial2-2x.jpg')" alt=""> -->
		<div class="content">
			<h3>{{title}}</h3>
			<h4>{{subTitle}}</h4>
			<p>
				{{textOne}}
			</p>
			<p>
				{{textTwo}}
			</p>
			<div class="critic_author">
				<img :src="logo" alt="">
				<h4>{{author}}</h4>
				<h4 class="third">{{magazine}}</h4>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'FocusCritic',
	props: {
		img: String,
		title: String,
		subTitle: String,
		textOne: String,
		textTwo: String,
		logo: String,
		author: String,
		magazine: String,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
img {
	width: 100%;
	height: 750px;
	display: block;
	object-fit: cover;
}
.content {
	@include absoluteTopLeft;
	padding: 120px 100px;
	h3 {
		padding-bottom: 30px;
		margin-bottom: 30px;
		border-bottom: 1px solid $clear-color;
	}
	h4 {
		font-family: $sans-serif;
		margin-bottom: 30px;
	}
	p {
		font-weight: 500;
		margin-bottom: 30px;
	}
	p:last-of-type {
		margin-top: 40px;
	}
}
.critic_author {
	display: flex;
	margin-top: 50px;
	img {
		width: 30px;
		margin-right: 15px;
		transform: translateY(-10px);
		object-fit: contain;
		object-position: top;
	}
	h4 {
		font-size: 1.1rem;
	}
	h4:first-of-type {
		margin-right: 4px;
	}
}
</style>