<template>
	<div id="app">
		<header>
			<Head />
		</header>
	</div>
</template>

<script>
import Head from '@/components/Head.vue';
export default {
	name: 'App',
	components: {
		Head,

	}
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
</style>
