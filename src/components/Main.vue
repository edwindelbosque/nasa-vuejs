<template>
	<div class="Main">
		<Nav v-on:getDate="onClick" />
		<PhotoHolder v-bind:date="date" />
		<Footer />
	</div>
</template>

<script>
import Nav from './Nav';
import PhotoHolder from './PhotoHolder';
import Footer from './Footer';

export default {
	name: 'Main',
	data() {
		return {
			date: null
		};
	},
	components: {
		Nav,
		PhotoHolder,
		Footer
	},
	methods: {
		onClick(newDate) {
			this.date = newDate;
		}
	}
};
</script>

<style scoped>
.Main {
	display: flex;
	flex-direction: column;
	align-content: center;
	width: 1000px;
	color: black;
}
</style>
