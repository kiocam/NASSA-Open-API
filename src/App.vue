<template>
	<div id="app">
		<Header class="header" />
		<Hero class="heroSec" />
		<Astronauts v-bind:astronauts="astronauts" class="astro" />
		<Footer class="footer" />
	</div>
</template>

<script>
import Header from './components/Header';
import Hero from './components/Hero';
import Footer from './components/Footer';
import Astronauts from './components/Astronauts';

import axios from 'axios';

export default {
	name: 'App',
	components: {
		Header,
		Hero,
		Astronauts,
		Footer,
	},

	data() {
		return {
			astronauts: [],
			issLocation: [],
		};
	},

	created() {
		axios
			.get('http://api.open-notify.org/astros.json')
			.then((res) => (this.astronauts = res.data))
			.catch((err) => console.log(err));
		/* Api for ISS Lat & Lang */
		axios
			.get('http://api.open-notify.org/iss-now.json')
			.then((res) => (this.issLocation = res.data))
			.catch((err) => console.log(err));
	},
};
</script>

<style>
#app {
	display: grid;
	grid-template-areas:
		'header header header header'
		'heroSec heroSec heroSec heroSec'
		'astro astro astro astro'
		'footer footer footer footer';

	font-family: Arial, Helvetica, sans-serif;
	background-color: #1a192a;
}

/* .header,
.heroSec,
.astro,
.footer {
	border: 1px #ccc solid;
	padding: 0.5rem;
} */

.header {
	grid-area: header;
	position: absolute;
	z-index: 5;
}

.heroSec {
	grid-area: heroSec;
}

.astro {
	grid-area: astro;
}

.footer {
	grid-area: footer;
	text-align: center;
}
</style>
