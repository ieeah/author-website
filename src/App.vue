<template>
	<div id="app">
		<header>
			<Head />
		</header>
		<main>
			<Audiobook />
			<Critics />
			<Events />
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
export default {
	name: 'App',
	components: {
		Head,
		Audiobook,
		Critics,
		Events,

	}
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
</style>
