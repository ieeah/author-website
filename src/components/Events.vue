<template>
	<div id="meetups">
		<div class="heading">
			<h2 class="section_heading primary">Upcoming Events</h2>
			<h5 class="subtitle accent">Meet the author in person</h5>
		</div>
		<div class="events container lg">
			<EventCards v-for="(event, i) in events" :key="`Event_0${i+1}`"
				:cover="events[i].cover"
				:title="events[i].title"
				:text="events[i].text"
			/>
		</div>
	</div>
</template>

<script>
import EventCards from '@/components/EventCards.vue';
export default {
	name: 'Events',
	components: {
		EventCards,
	},
	data() {
		return {
			events: [
				{
					cover: require('@/assets/Events/Events_01.jpg'),
					title: 'Chicago Book Signing',
					text: 'Proin mattis, nunc sed sagittis lacinia, ante lorem malesuada libero, et ornare ex erat nec orci. Nunc pretium laoreet arcu nec porttitor.',
				},
				{
					cover: require('@/assets/Events/Events_02.jpg'),
					title: 'Meet & Greet With Amanda',
					text: 'Aliquam eu nibh ut mauris lacinia vulputate vitae sed neque. Maecenas tincidunt elementum diam eu egestas.',
				},
				{
					cover: require('@/assets/Events/Events_03.jpg'),
					title: 'Open Book: Dialogues',
					text: 'In sodales orci aliquam quis. Donec feugiat lacus nulla. Mauris suscipit luctus erat, at scelerisque massa semper ut. Etiam id luctus ipsum. Nam ac tellus et turpis aliquet luctus et id ante.',
				},
			],
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';
#meetups {
	@include flexColumn;
	padding-block: 60px;
	background-color: $bg-2;
	.heading {
		text-align: center;
		width: 100%;
		margin-bottom: 50px;
		h5 {
			font-size: 1rem;
		}
	}
	.events {
		@include flexNoWrap;
	}
}

</style>