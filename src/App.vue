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
export default {
	name: 'App',
	components: {
		Head,
		Audiobook,
		Critics,
		Events,
		Newsletter,
	}
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
</style>
