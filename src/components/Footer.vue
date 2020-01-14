<template>
	<footer>
		<h4>Built by Edwin Del Bosque</h4>
	</footer>
</template>

<script>
export default {
	name: 'Footer'
};
</script>

<style scoped>
footer {
	position: relative;
	right: 0;
	left: 0;
	bottom: 0;
	height: 80px;
	display: flex;
	align-items: center;
	justify-content: center;
	border-top: 1px solid #4f90ff;
	margin-top: 100px;
	width: 100vw;
}

h4 {
	color: #4f90ff;
	font-size: 13px;
	font-weight: 400;
}
</style>
