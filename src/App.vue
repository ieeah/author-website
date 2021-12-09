<template>
	<div id="app">
		<header>
			<Head />
			<main>
				<Audiobook />
				<Critics />
			</main>
		</header>
	</div>
</template>

<script>
import Head from '@/components/Head.vue';
import Audiobook from '@/components/Audiobook.vue';
import Critics from '@/components/Critics.vue';
export default {
	name: 'App',
	components: {
		Head,
		Audiobook,
		Critics,
	}
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
</style>
