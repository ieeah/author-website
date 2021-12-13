<template>
	<div class="blog">
		<SectionHead 
			:title="title"
			:subTitle="subTitle"
			:btnText="btnText"
		/>
	</div>
</template>

<script>
import SectionHead from '@/components/SectionHead.vue';
export default {
	name: 'Blog',
	components: {
		SectionHead,
	},
	data() {
		return {
			title: 'Recent Articles',
			subTitle: 'read the latest entries',
			btnText: 'All Articles',
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

</style>