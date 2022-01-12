<script>
	import { Router, Link, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import About from "./routes/About.svelte";
	import { onMount } from "svelte";

	export let url = "";

	import { initializeApp } from "firebase/app";
	import { getAnalytics } from "firebase/analytics";
	onMount(async () => {
		// Import the functions you need from the SDKs you need
		// TODO: Add SDKs for Firebase products that you want to use
		// https://firebase.google.com/docs/web/setup#available-libraries

		// Your web app's Firebase configuration
		// For Firebase JS SDK v7.20.0 and later, measurementId is optional
		const firebaseConfig = {
			apiKey: "AIzaSyDIi78kidzG_d2EsK9MgOftDTLsUQMkeDs",
			authDomain: "ikeabridge-analytics.firebaseapp.com",
			projectId: "ikeabridge-analytics",
			storageBucket: "ikeabridge-analytics.appspot.com",
			messagingSenderId: "617936178141",
			appId: "1:617936178141:web:8ec595045f9e3fa5f10434",
			measurementId: "G-J5SHLT16MK",
		};

		// Initialize Firebase
		const app = initializeApp(firebaseConfig);
		const analytics = getAnalytics(app);
	});
</script>

<Router {url}>
	<nav id="navbar">
		<Link class="link" to="/">Home</Link>
		|
		<Link class="link" to="about">About</Link>
	</nav>
	<div id="render">
		<Route path="about" component={About} />
		<Route path="/"><Home /></Route>
	</div>
</Router>

<style>
	#navbar {
		text-align: center;
		padding-top: 8px;
		color: black;
	}

	#render {
		width: 100%;
		height: 100%;
		margin: 0px;
		padding: 0px;
	}
</style>
