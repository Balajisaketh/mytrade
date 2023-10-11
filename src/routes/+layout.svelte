<script>
	
	import './styles.css';
	
</script>

<div class="app">
	
<header>

</header>
	<main>
		<slot/>
	</main>


</div>

<style>
header{
	width:100vw;
	background-color: black;
}
	main {
		

		height: 100vh;
		overflow-x: hidden;
		width: 100vw;
		padding-top: 0rem;
		margin: 0 auto;
		box-sizing: border-box;
	}



	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
