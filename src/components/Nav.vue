<template>
	<nav>
		<section>
			<div>
				<a href="https://www.nasa.gov/">
					<img alt="NASA logo" src="../assets/logo.png" class="logo" />
				</a>
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
	padding-top: 25px;
	display: flex;
	position: absolute;
	top: 0px;
	height: 70px;
	right: 0;
	left: 0;
	justify-content: center;
	border-bottom: 1px solid #043b92;
	background: rgb(17, 15, 15);
	padding-bottom: 20px;
}

section {
	justify-content: space-between;
	display: flex;
	width: 1000px;
}

div {
	display: flex;
	align-items: center;
}

a {
	display: flex;
	justify-content: center;
	align-items: center;
	height: 45px;
	width: 45px;
	border-radius: 30px;
	margin-bottom: 3px;
}

.logo {
	width: 60px;
	padding-bottom: 0px;
	height: auto;
}

h3 {
	color: rgb(223, 223, 223);
	margin-left: 10px;
	font-size: 20px;
	margin-bottom: 3px;
	cursor: default;
	font-weight: 400;
}
</style>
