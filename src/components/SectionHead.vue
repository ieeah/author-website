<template>
	<div class="head">
		<div class="container md">
			<div class="left">
				<h2 class="primary section_heading">{{title}}</h2>
				<h3 class="third subtitle">{{subTitle}}</h3>
			</div>
			<div class="right">
				<div class="btn accent_bg">{{btnText}}</div>
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
		btnText: String,
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
		h3 {
			font-size: 1rem;
		}
	}
	.right .btn {
		width: 235px;
	}
}

</style>