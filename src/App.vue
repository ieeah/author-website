<template>
	<div id="app">
		<header>
			<Head />
			<main>
				<Audiobook />
			</main>
		</header>
	</div>
</template>

<script>
import Head from '@/components/Head.vue';
import Audiobook from '@/components/Audiobook.vue';
export default {
	name: 'App',
	components: {
		Head,
		Audiobook,
	}
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
</style>
