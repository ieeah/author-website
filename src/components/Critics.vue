<template>
	<section>
		<SectionHead :title="title" :subTitle="subTitle"/>
	</section>
</template>

<script>
import SectionHead from '@/components/SectionHead.vue';
export default {
	name: 'Critics',
	components: {
		SectionHead,
	},
	data() {
		return {
			title: 'What The Critics Say',
			subTitle: 'testimonial from around the world',
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

</style>