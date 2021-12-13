<template>
	<div id="app">
		<header id="top">
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
			<Footer />
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
import Footer from '@/components/Footer.vue';
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
		Footer,
	},
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
</style>
