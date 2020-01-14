<template>
	<section>
		<h2>{{ nasaData.title }}</h2>
		<a v-bind:href="nasaData.hdurl" target="_blank">
			<div class="image-holder">
				<img v-bind:alt="nasaData.title" v-bind:src="nasaData.url" />
			</div>
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
	margin-top: 60px;
	display: flex;
	flex-direction: column;
	align-items: flex-start;
	justify-content: flex-start;
}

h2 {
	color: #e4eaec;
	background: #1a212c;
	padding: 10px 20px;
	font-weight: 800;
	letter-spacing: 1px;
	text-align: left;
	cursor: default;
	margin-bottom: 12px;
}

.image-holder {
	width: 1000px;
	height: fit-content;
	display: flex;
	justify-content: center;
	align-content: flex-start;
	padding-bottom: 1px;
	background: #334055;
}

img {
	width: 998px;
	height: auto;
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
	background: #1a212c;
	padding: 30px 50px;
	text-align: left;
	cursor: default;
}
</style>
