<template>
	<nav>
		<div>
			<img alt="NASA logo" src="../assets/logo.png" class="logo" />
			<h3>Photo of the day</h3>
		</div>
		<Date />
	</nav>
</template>

<script>
import Date from './Date';

export default {
	name: 'Nav',
	components: {
		Date
	}
};
</script>

<style scoped>
nav {
	margin-top: 20px;
	display: flex;
	width: 1000px;
	justify-content: space-between;
}

div {
	display: flex;
	align-items: center;
}

.logo {
	width: 100px;
	height: auto;
}

h3 {
	color: white;
	margin-left: 10px;
	font-size: 20px;
	cursor: default;
	background: -webkit-linear-gradient(top right, #69a0ff, #468aff);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
}
</style>
