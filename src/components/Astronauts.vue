<template>
	<div class="container">
		<h3 class="peopleInSpace">
			Number of people in space: {{ astronauts.number }}
		</h3>
		<div class="astronauts">
			<div v-bind:key="people" v-for="people in astronauts.people">
				<Astronaut v-bind:people="people" />
			</div>
		</div>
	</div>
</template>

<script>
import Astronaut from './Astronaut';
export default {
	name: 'Astronauts',
	components: {
		Astronaut,
	},
	props: ['astronauts'],
};
</script>

<style scoped>
.container {
	background-color: #1A192A;
	color: #fff;
	font-size: 2.5em;
	text-align: center;
	margin-bottom: 50px;
}

.peopleInSpace {
	margin: 100px 0;
}

.astronauts {
	display: grid;
	grid-column-start: 1;
	grid-template-columns: repeat(3, auto);
}
</style>
