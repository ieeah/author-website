<template>
	<div class="head">
		<div class="container md">
			<div class="left">
				<h2 class="primary">{{title}}</h2>
				<h3 class="third subtitle">{{subTitle}}</h3>
			</div>
			<div class="right">
				<div class="btn accent_bg"> Read all testimonials</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'SectionHead',
	props: {
		title: String,
		subTitle: String,
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
.container.md {
	@include flexAlignCenter;
	justify-content: space-between;
	padding-block: 40px 20px;
	.left {
		h2 {
			font-size: 2.5rem;
		}
		h3 {
			font-size: 1rem;
		}
	}
}

</style>