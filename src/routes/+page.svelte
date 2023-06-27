<div class="app">
	<div class="title-bar">
		<img class="logo" src="/logo.png" />
		<h1>Time to Clean Up? We Can Help</h1>
		<img class="logo" src="/logo.png" />
	</div>
	<div class="main-page">
		<div>
			<p>Exterior</p>
		</div>
		<img class="pigs" src="/pigs.png" alt="dirty-pigs" />
		<div>
			<p>Interior</p>
		</div>
	</div>
</div>

<style>
	.title-bar {
		display: grid;
		place-items: center;
		border-bottom: 1px solid yellow;
		grid-template-columns: 1fr 1fr 1fr;
	}
	.main-page {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		place-items: center;
	}
	.logo {
		width: 10rem;
	}
	.pigs {
		/* width: 70%; */
	}
	h1 {
		font-size: 2em;
		text-align: center;
		font-weight: normal;
	}
	.app {
		color: white;
	}
</style>
