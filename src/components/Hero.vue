<template>
	<div class="heroSec">
		<div class="overlay"></div>
		<div class="cta">
			<h2>Boldly Reaching for the Stars!</h2>
			<p class="quote">
				"Space offers extraordinary potential for commerce and adventure, for
				new innovations and new tests of will. As Human beings, we can't help
				but reach for the stars. It's our nature. It's our destiny."
			</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Hero',
};
</script>

<style scoped>
.heroSec {
	position: relative;
	background-image: url('../assets/hero-bg1.png');
	height: 135vh;
	background-position: center;
	background-repeat: no-repeat;
	background-size: cover;
}

.cta {
	/* border: 1px solid red; */
	display: flex;
	width: 65%;
	margin: 0 auto;
	margin-top: 12%;
	color: rgb(251, 251, 251);
	font-size: 1.7em;
	opacity: 0.8;
}

.cta h2 {
	font-size: 2.7em;
	/* margin-right: 70px; */
	padding-right: 10px;
	width: 262px;
}

.cta .quote {
	margin-left: 500px;
	line-height: 1.2;
	width: 400px;
}

.overlay {
	position: absolute;
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background-color: rgba(0, 0, 0, 0.2);
	z-index: 2;
}
</style>
