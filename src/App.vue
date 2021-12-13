<template>
	<div id="app">
		<header>
			<Head />
		</header>
		<main>
			<Audiobook />
			<Critics />
			<Events />
			<Newsletter />
			<DigDeeper />
			<Blog />
		</main>
		<footer>
			
		</footer>
	</div>
</template>

<script>
import Head from '@/components/Head.vue';
import Audiobook from '@/components/Audiobook.vue';
import Critics from '@/components/Critics.vue';
import Events from '@/components/Events.vue';
import Newsletter from '@/components/Newsletter.vue';
import DigDeeper from '@/components/DigDeeper.vue';
import Blog from '@/components/Blog.vue';
export default {
	name: 'App',
	components: {
		Head,
		Audiobook,
		Critics,
		Events,
		Newsletter,
		DigDeeper,
		Blog,
	},
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
</style>
