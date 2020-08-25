<template>
	<div class="card">
		<img src="../assets/astronaut-profile.png" alt="astronaut image" />
		<h1>Name: {{ people.name }}</h1>
		<h2>Craft: {{ people.craft }}</h2>
	</div>
</template>

<script>
export default {
	name: 'Astronaut',
	props: ['people'],
};
</script>

<style scoped>
.card {
	background-color: #1a192a;
}

.card img {
	margin-bottom: 30px;
}

.card h1 {
	margin-bottom: 20px;
}
</style>
