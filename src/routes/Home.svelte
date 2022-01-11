<script>
	function prev() {
		console.log("Previous");
	}
	function next() {
		console.log("Next");
	}
</script>

<main id="home">
	<h1>IKEA bridge</h1>
	<img
		id="main_img"
		src="/img/landscape_img.jpg"
		alt="Horizontal view of the bridge"
	/>
	<div id="select_img">
		<button id="prev_btn" on:click={prev}>Previous</button>
		<button id="next_btn" on:click={next}>Next</button>
	</div>
	<p>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In the year 301 BSE,
		tragedy struck. Yuts island declared war on Stuyvesant High School. In
		the midst of conflict, fighting ensued and deaths were common. For years
		they attacked one another, while their people lived in constant fear of
		death just looking over their shoulders. Finally, 96 years into the war,
		there was finally a winner. Yuts island had many troops and were
		especially fierce in battle, so they charged head-first without
		hesitation. The favor seemed to be on their side for a while, however,
		Stuyvesant came out on top in the end due to their brilliant battle
		strategies and rigorous training. Under the new rule, there were many
		changes made to the city.
	</p>
	<p>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This is a model of the
		famed IKEA bridge that was built in the year 5 ASE, just a couple years
		after Stuyvesant had won the war. Their ultimate goal, aside from world
		domination, was to cultivate an environmentally friendly city and to
		eliminate the pollution that had arisen from the many years of
		inefficient bridge use. This bridge represents an advanced and
		environmentally motivated civilization. Although the bridge may look a
		little disfigured, it was built that way to represent the historically
		accurate revolts and damage caused by certain individuals who refused to
		accept their new civilization. Building a bridge for trains provides a
		quick, safe, and efficient choice for passengers.
	</p>
</main>

<style>
	#home {
		padding: 3px;
		text-align: center;
		margin: auto;
		width: 95vw;
	}

	#home p {
		font-size: 1.2rem;
		text-align: left;
		margin-top: 5px;
	}

	#main_img,
	#select_img {
		width: 100%;
		max-width: 700px;
	}

	#select_img {
		margin: auto;
		display: flex;
		justify-content: space-around;
		align-items: center;
		height: 40px;
	}

	#select_img button {
		width: 100px;
		height: 40px;
		border: 1px solid black;
		background-color: white;
		border-radius: 5%;
		padding: 10px;
	}
</style>
