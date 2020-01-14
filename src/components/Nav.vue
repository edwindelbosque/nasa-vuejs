<template>
	<nav>
		<section>
			<div>
				<img alt="NASA logo" src="../assets/logo.png" class="logo" />
				<h3>Photo of the day</h3>
			</div>
			<Date v-on="$listeners" />
		</section>
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
	margin-top: 0px;
	display: flex;
	position: absolute;
	top: 20px;
	height: 76px;
	right: 0;
	left: 0;
	justify-content: center;
	border-bottom: 1px solid #4f90ff;
	padding-bottom: 20px;
}

section {
	justify-content: space-between;
	padding: 0px 5px;
	display: flex;
	width: 1000px;
}

div {
	display: flex;
	align-items: center;
}

.logo {
	width: 90px;
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
