<template>
	<div class="focus critic rounded_bt_right">
		<img :src="img" :alt="`${title}`">
		<div class="content">
			<h3>{{title}}</h3>
			<h4>{{subTitle}}</h4>
			<p class="fw500">
				{{textOne}}
			</p>
			<p class="fw500">
				{{textTwo}}
			</p>
			<div class="critic_author">
				<img :src="logo" :alt="`${magazine} logo`">
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
.focus.critic {
	position: relative;
	&::before {
		content: '';
		width: 100%;
		height: 100%;
		object-fit: cover;
		@include absoluteTopLeft;
		background: rgb(0,0,0);
		background: linear-gradient(0deg, rgba(0,0,0,.6) 10%, rgba(0,0,0,0.2) 60%);
	}
}
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
		padding-bottom: 40px;
		margin-bottom: 30px;
		border-bottom: 1px solid rgba($color: $clear-color, $alpha: .4);
		transform: translateY(-20px);
	}
	h4 {
		font-family: $sans-serif;
		margin-bottom: 30px;
	}
	p {
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