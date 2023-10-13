<style>
	@import 'bootstrap/dist/css/bootstrap.min.css';
	.listitem {
		list-style: none;
		color: blue;
	}
	.para {
		font-size: 14px;
		font-weight: 400;
		font-style: normal;
	}
	footer {
		background-color: black;
		height: auto;
		margin-top: 20px;
	}
	.head {
		font-size: 24px;
		font-style: normal;
		font-weight: 500;
	}
	.sidehead {
		font-style: normal;
		font-size: 30px;
		font-weight: 400;
	}
</style>

<script>
	import { onMount, onDestroy } from 'svelte';

	let screenWidth = 0;

	let check = 'empty';
	onMount(() => {
		screenWidth = window.innerWidth;
		window.addEventListener('resize', updateScreenSize);

		// Cleanup event listener when the component is destroyed
		return () => {
			window.removeEventListener('resize', updateScreenSize);
		};
	});

	function updateScreenSize() {
		screenWidth = window.innerWidth;
	}
	function firstclick() {
		check = 'firstdiv';
		console.log(check);
	}
	function secondclick() {
		check = 'seconddiv';
		console.log(check);
	}

	function thirdclick() {
		check = 'thirddiv';
		console.log(check);
	}

	let selectedOption = ''; // Initialize a variable to store the selected option.
	let options = [
		'Lifetime System',
		'Advanced Mode',
		'Loans',
		'Custom Position Sizing/Custom Shares',
		'Stop Limit Orders',
		'Technical Indicators',
		'FAQ'
	];

	import Fa from 'svelte-fa';
	import {
		faFlag,
		faHamburger,
		faHome,
		faList,
		faMessage
	} from '@fortawesome/free-solid-svg-icons';
</script>

{#if screenWidth < 768}
	<!-- Mobile layout -->
	<div class="column">
		<nav class="navbar navbar-expand-lg navbar-light bg-dark">
			<div class="container-fluid">
				<a class="navbar-brand text-white" href="#">ChartGame</a>
				<button
					class="navbar-toggler bg-white"
					type="button"
					data-bs-toggle="collapse"
					data-bs-target="#navbarNavDropdown"
					aria-controls="navbarNavDropdown"
					aria-expanded="false"
					aria-label="Toggle navigation"
				>
					<span class="navbar-toggler-icon"></span>
				</button>
				<div class="collapse navbar-collapse" id="navbarNavDropdown">
					<ul class="navbar-nav">
						<li class="nav-item">
							<a class="nav-link active" aria-current="page" href="#">Home</a>
						</li>
						<li class="nav-item">
							<a class="nav-link" href="#">Features</a>
						</li>
						<li class="nav-item">
							<a class="nav-link" href="#">Pricing</a>
						</li>
						<li class="nav-item dropdown">
							<a
								class="nav-link dropdown-toggle"
								href="#"
								id="navbarDropdownMenuLink"
								role="button"
								data-bs-toggle="dropdown"
								aria-expanded="false"
							>
								Dropdown link
							</a>
							<ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
								<li><a class="dropdown-item" href="#">Action</a></li>
								<li><a class="dropdown-item" href="#">Another action</a></li>
								<li>
									<a class="dropdown-item" href="#">Something else here</a>
								</li>
							</ul>
						</li>
					</ul>
				</div>
			</div>
		</nav>
		<h2 class="mx-4 mt-5 sidehead">Help Center</h2>

		<div class="col-11 rounded border border-2 m-2 mt-5 mx-auto">
			<p class="mx-3 my-2">How to play-Coming soon</p>
			{#each options as option (option)}
				<li class="listitem my-3 mx-3">{option}</li>
			{/each}
		</div>
		<div class="col-11 rounded border border-2 mt-4 m-2 mx-auto">
			<h2 class="m-3 head">Lifetime System</h2>
			<p class="text-left mt-5 para m-3">
				The lifetime system challenges users to perform the best they can during 50 years, or 18,250
				trading days. 1 swing trading game counts as 90 trading days, whereas 1 day trading game
				counts as 1 trading day. The count is added to your lifetime total regardless of trades. If
				you decide not to play a chart, and skip to the next chart, the full count of trading days
				will still be added to your total, so skip wisely.
			</p>
			<p class="text-left para m-3">
				Users who have played the full 50 years worth of games will notice discrepancies in cash
				when playing new games. Once you play the full 50 years worth of games, the first game
				played in this time frame is removed to make room for the last game you have played. For an
				example, if the first game recorded in your lifetime has returns of 20%, and the last game
				you played has a return of 0%, then the 20% game is removed from your stats, and the 0% game
				is added. Therefore, your total cash amount will reflect the missing 20% returns.
			</p>
		</div>
		<footer>
			<p class="text-center text-white py-5">User Agreement | privacy policy</p>
		</footer>
	</div>
{:else if screenWidth < 1024}
	<!-- Tablet layout -->
	<div class="column">
		<nav class="navbar navbar-expand-lg navbar-light bg-dark">
			<div class="container-fluid">
				<a class="navbar-brand text-white" href="#">ChartGame</a>
				<button
					class="navbar-toggler bg-white"
					type="button"
					data-bs-toggle="collapse"
					data-bs-target="#navbarNavDropdown"
					aria-controls="navbarNavDropdown"
					aria-expanded="false"
					aria-label="Toggle navigation"
				>
					<span class="navbar-toggler-icon"></span>
				</button>
				<div class="collapse navbar-collapse" id="navbarNavDropdown">
					<ul class="navbar-nav">
						<li class="nav-item">
							<a class="nav-link active" aria-current="page" href="#">Home</a>
						</li>
						<li class="nav-item">
							<a class="nav-link" href="#">Features</a>
						</li>
						<li class="nav-item">
							<a class="nav-link" href="#">Pricing</a>
						</li>
						<li class="nav-item dropdown">
							<a
								class="nav-link dropdown-toggle"
								href="#"
								id="navbarDropdownMenuLink"
								role="button"
								data-bs-toggle="dropdown"
								aria-expanded="false"
							>
								Dropdown link
							</a>
							<ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
								<li><a class="dropdown-item" href="#">Action</a></li>
								<li><a class="dropdown-item" href="#">Another action</a></li>
								<li>
									<a class="dropdown-item" href="#">Something else here</a>
								</li>
							</ul>
						</li>
					</ul>
				</div>
			</div>
		</nav>
		<h2 class="mx-4 mt-5 sidehead">Help Center</h2>
		<div class="d-flex flex-row">
			<div class="col-4 rounded border border-2 m-2">
				<p class="mx-3 my-2">How to play-Coming soon</p>
				{#each options as option (option)}
					<li class="listitem my-3 mx-3">{option}</li>
				{/each}
			</div>
			<div class="col-8 rounded border border-2 m-2">
				<h2 class="m-3 head">Lifetime System</h2>
				<p class="text-left mt-5 para m-3">
					The lifetime system challenges users to perform the best they can during 50 years, or
					18,250 trading days. 1 swing trading game counts as 90 trading days, whereas 1 day trading
					game counts as 1 trading day. The count is added to your lifetime total regardless of
					trades. If you decide not to play a chart, and skip to the next chart, the full count of
					trading days will still be added to your total, so skip wisely.
				</p>
				<p class="text-left para m-3">
					Users who have played the full 50 years worth of games will notice discrepancies in cash
					when playing new games. Once you play the full 50 years worth of games, the first game
					played in this time frame is removed to make room for the last game you have played. For
					an example, if the first game recorded in your lifetime has returns of 20%, and the last
					game you played has a return of 0%, then the 20% game is removed from your stats, and the
					0% game is added. Therefore, your total cash amount will reflect the missing 20% returns.
				</p>
			</div>
		</div>
	</div>
	<footer>
		<p class="text-center text-white py-5">User Agreement | privacy policy</p>
	</footer>
{:else}
	<!-- Laptop/desktop layout -->
	<div class="column">
		<nav class="navbar navbar-expand-lg navbar-light bg-dark p-4 relative">
			<div class="container-fluid">
				<a class="navbar-brand text-white" href="#">ChartGame</a>
				<button
					class="navbar-toggler bg-white"
					type="button"
					data-bs-toggle="collapse"
					data-bs-target="#navbarNav"
					aria-controls="navbarNav"
					aria-expanded="false"
					aria-label="Toggle navigation"
				>
					<span class="navbar-toggler-icon"></span>
				</button>
			</div>

			<div class="absolute right-2 d-md-none d-lg-block">
				<div class="d-flex flex-row mx-3 px-5 py-3">
					<!-- First icon (e.g., a home icon) -->
					<Fa icon="{faHome}" class="mx-2 text-white " size="lg" />
					<Fa icon="{faList}" class="mx-2 text-white" size="lg" />
					<Fa icon="{faMessage}" class="mx-2 text-white" size="lg" />
				</div>
			</div>
		</nav>
		<h2 class="mx-4 mt-5 sidehead">Help Center</h2>

		<div class="d-flex flex-row col-12">
			<div class="col-4 rounded border border-2 mx-3 mt-3">
				<p class="mx-4 my-2 px-2">How to play -Coming soon</p>
				<ul>
					{#each options as option (option)}
						<li class="listitem my-3">{option}</li>
					{/each}
				</ul>
			</div>
			<div class="col-7 rounded border border-2 mx-3 mt-3">
				<h2 class="m-3 head">Lifetime System</h2>
				<p class="text-left mt-5 para m-1 mx-3">
					The lifetime system challenges users to perform the best they can during 50 years, or
					18,250 trading days. 1 swing trading game counts as 90 trading days, whereas 1 day trading
					game counts as 1 trading day. The count is added to your lifetime total regardless of
					trades. If you decide not to play a chart, and skip to the next chart, the full count of
					trading days will still be added to your total, so skip wisely.
				</p>
				<p class="text-left para m-1 mt-4 mx-3">
					Users who have played the full 50 years worth of games will notice discrepancies in cash
					when playing new games. Once you play the full 50 years worth of games, the first game
					played in this time frame is removed to make room for the last game you have played. For
					an example, if the first game recorded in your lifetime has returns of 20%, and the last
					game you played has a return of 0%, then the 20% game is removed from your stats, and the
					0% game is added. Therefore, your total cash amount will reflect the missing 20% returns.
				</p>
			</div>
		</div>
	</div>
	<footer>
		<p class="text-center text-white py-5">User Agreement | privacy policy</p>
	</footer>
{/if}
