<script>
	import Navbar from "../components/Navbar.svelte"
</script>

<Navbar/>

<slot />

	<style>
		@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');

		:global(*) {
			font-family: 'Poppins', sans-serif;
			margin: 0;
			padding: 0;
			box-sizing: border-box;
			text-decoration: none;
			color: var(--light);
		}
		/* color variables */
		:global(:root){
			--primary: #033461;
			--secondary: #F3A712;
			--dark: #222222;
			--light: #ebebeb;


		}
		:global(body){
				background-color: #555555;

		}
		
		
	</style>

	
