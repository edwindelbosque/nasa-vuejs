<template>
	<section>
		<h2>{{ nasaData.title }}</h2>
		<div>
			<img alt="Photo of the day by NASA." v-bind:src="nasaData.url" />
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
	color: #d5dadd;
	background: #1a212c;
	padding: 0px 10px;
	padding-top: 3px;
	font-weight: 800;
	letter-spacing: 1px;
	text-align: left;
	cursor: default;
}

div {
	margin-top: 12px;
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
</style>
