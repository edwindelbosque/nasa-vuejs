<template>
	<div class="newMain">
		<Nav v-on:getDate="onClick" />
		<div class="Main">
			<PhotoHolder v-bind:date="date" />
		</div>
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
.newMain {
	display: flex;
	flex-direction: column;
	align-content: center;
	color: black;
	justify-content: center;
	justify-items: center;
	width: 100vw;
}
.Main {
	display: block;
	margin-right: auto;
	margin-left: auto;
}
</style>
