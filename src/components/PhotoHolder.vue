<template>
	<section>
		<h2>{{ nasaData.title }}</h2>
		<a v-bind:href="nasaData.hdurl" target="_blank">
			<img v-bind:alt="nasaData.title" v-bind:src="nasaData.url" />
		</a>
		<div class="quote-block">
			<p>{{ nasaData.explanation }}</p>
			<h6>{{ displayCopyright() }}</h6>
		</div>
	</section>
</template>

<script>
export default {
	name: 'PhotoHolder',
	data() {
		return {
			nasaData: ''
		};
	},
	props: ['date'],
	created() {
		return fetch(
			'https://api.nasa.gov/planetary/apod?api_key=Ot4l5yvwK4E688azgJrDhttp46o2stPxLvfCfCQL'
		)
			.then(data => data.json())
			.then(data => (this.nasaData = data));
	},
	methods: {
		displayCopyright() {
			if (this.nasaData.copyright) {
				return `Copyright © ${this.nasaData.copyright}`;
			} else {
				return '';
			}
		}
	},
	watch: {
		date: {
			immediate: true,
			deep: true,
			handler() {
				return fetch(
					`https://api.nasa.gov/planetary/apod?date=${this.date}&api_key=Ot4l5yvwK4E688azgJrDhttp46o2stPxLvfCfCQL`
				)
					.then(data => data.json())
					.then(data => (this.nasaData = data));
			}
		}
	}
};
</script>

<style scoped>
section {
	margin-top: 100px;
	display: flex;
	flex-direction: column;
	align-items: flex-start;
	justify-content: flex-start;
	min-height: 70vh;
}

h2 {
	color: #e4eaec;
	background: #1f1f1f;
	padding: 10px 25px;
	font-weight: 800;
	letter-spacing: 1px;
	text-align: left;
	cursor: default;
	margin-bottom: 12px;
}

img {
	width: 998px;
	height: auto;
	border: 1px solid #1f1f1f;
	margin-top: 1px;
}

h6 {
	margin-top: 12px;
	color: rgb(146, 146, 146);
	font-weight: 300;
	text-align: right;
	cursor: default;
}

.quote-block {
	width: 100%;
	display: flex;
	flex-direction: column;
}

p {
	margin-top: 12px;
	width: 1000px;
	color: rgb(217, 223, 226);
	background: #1f1f1f;
	padding: 30px 50px;
	text-align: left;
	cursor: default;
}
</style>
