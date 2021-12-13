<template>
	<div class="footer">
		<div class="top_footer">
			<img :src="require('@/assets/img/author-logo-round.png')" alt="" class="brand">
			<div class="container md">
				<div class="column">
					<h3 class="col_title">{{col1[0]}}</h3>
					<p class="clear">{{col1[1]}}</p>
				</div>
				<div class="column">
					<h3 class="col_title">{{col2Title}}</h3>
					<ul>
						<li v-for="(link, i) in col2" :key="`link_${i}`">
							<i class="fas fa-chevron-right"></i>
							<a :href="link.url">{{link.text}}</a>
						</li>
					</ul>
				</div>
				<div class="column">
					<h3 class="col_title">{{col3Title}}</h3>
					<ul>
						<li v-for="(link, i) in col3" :key="`link_${i}`">
							<p>{{link}}</p>
						</li>
						<li>
							<a :href="`mailto:${col3Mail.mail}`">{{col3Mail.mail}}</a>
						</li>
					</ul>
				</div>
			</div>
		</div>
		<div class="sub_footer">

		</div>
	</div>
</template>

<script>
export default {
	name: 'Footer',
	data() {
		return {
			col1: [
				'ABOUT ME',
				'Vivamus suscipit tortor eget felis porttitor voluptat. Nulla quis lorem ut libero malesuada feugiat. Vivamus suscipit torto eget felis porttitor voluptat.'
			],
			col2Title: 'USEFUL LINKS',
			col2: [
				{
					text: 'Latest Books',
					url: '/latest_books',
				},
				{
					text: 'Upcoming Events',
					url: '#meetups',
				},
				{
					text: 'Recent Articles',
					url: '#blog',
				},
				{
					text: 'Business Enquiries',
					url: '/Enquiries',
				},
				{
					text: 'Visit My Foundation',
					url: '/foundation',
				},
			],
			col3Title: 'CONTACT INFO',
			col3: [
				'63 E. Studebaker Street BolingBrook, IL 60440',
				'Phone: (800) 000-0000',
				'Mobile: (800) 000-0000',
			],
			col3Mail: {
				text: 'Email',
				mail: 'info@your-company.com',
			},
		};
	},
}
</script>

<style scoped lang="scss">
@import '@/styles/globals.scss';

.footer {
	background-image: url('../assets/Footer/footer-3.jpg');
	background-size: cover;
	background-position: top;
	height: 510px;
	position: relative;
	img.brand {
		width: 150px;
		height: 150px;
		position: absolute;
		left: 100px;
		top: 110px;
	}
	.container {
		padding-left: 80px;
	}
}


</style>