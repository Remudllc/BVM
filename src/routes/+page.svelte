<script lang="ts">
	import List from '../components/list.svelte';
	import Pigs from '../components/pigs.svelte';

	let exterior: string[] = [
		'Tires & Rims',
		'Power Wash and Soap',
		'Hand Wash',
		'Wax',
		'Buffing',
		'Ceramic Sealant',
		'Trim Restoration',
		'Glass',
		'Bug and Tar Removal',
		'Rock Chip Repair',
		'Paint Correction',
		'Engine / Engine Bay',
		'Contamination Removal',
		'Headlight Restoration'
	];
	let interior: string[] = [
		'Blow Out',
		'Vacuum',
		'Deep Detail Cleaning',
		'Stain Removal',
		'Steam Cleaning',
		'Carpet Shampoo',
		'Fabric Shampoo',
		'Fabric & Carpet Protectant',
		'Leather Clean & Condition',
		'Vinyl, Rubber & Plastic Restoration',
		'Odor Elimination',
		'Cupholders, Console, Dash and More',
		'Car Seats'
	];
</script>

<div class="app">
	<div class="title-bar">
		<img class="logo" src="/logo.png" alt="best value mobile detailing logo" />
		<div class="title">Time to Clean Up? We Can Help</div>
		<img class="logo" src="/logo.png" alt="best value mobile detailing logo" />
	</div>
	<div class="main-page">
		<div>
			<List header="Exterior" items={exterior} />
		</div>
		<Pigs />
		<div>
			<List header="Interior" items={interior} />
		</div>
	</div>
	<div class="footer">info@bestvaluedetailing.com</div>
</div>

<style>
	.title-bar {
		display: grid;
		place-items: center;
		border-bottom: 1px solid yellow;
		grid-template-columns: 1fr 1fr 1fr;
	}
	.main-page {
		padding-top: 2rem;
		display: grid;
		grid-template-columns: 1fr 2fr 1fr;
		place-items: center;
	}
	.logo {
		width: 10rem;
	}
	.title {
		font-size: 2em;
		text-align: center;
		font-weight: normal;
	}
	.footer {
		display: grid;
		place-items: center;
		color: yellow;
		font-size: 1rem;
		padding-top: 1rem;
	}
</style>
