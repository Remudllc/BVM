<script lang="ts">
	import List from '../components/list.svelte';
	import Pigs from '../components/pigs.svelte';
	import ValuePage from '../components/value_page.svelte';
	import { phoneNumber, email } from '../data/contact';

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
		'Trim, Plastic & Vinyl Restoration',
		'Odor Elimination',
		'Cupholders, Console, Dash and More',
		'Car Seats'
	];
</script>

<div class="app">
	<div class="title-bar">
		<img class="logo" src="/logo.png" alt="best value mobile detailing logo" />
		<div class="header-text">
			<div class="title">Best Value Mobile Detailing</div>
			<div>{$phoneNumber}</div>
			<div>{$email}</div>
		</div>
		<img class="logo" src="/logo.png" alt="best value mobile detailing logo" />
	</div>
	<div class="header-logo">
		<img src="/logo.png" alt="best value mobile detailing logo" />
	</div>
	<p class="description">Thanks for visiting our website. Below is a list of what we offer.</p>
	<div class="main-page">
		<div>
			<h1>Best Value</h1>
			<p>Exterior</p>
			<ol>
				<li>Tires and Rims</li>
				<li>Pre-Rinse</li>
				<li>Power Wash with Premium Soap</li>
				<li>Hand Wash and Dry</li>
				<li>Floor Mats Cleaned and Restored</li>
				<li class="bolded">Carnauba Wax Application</li>
				<li class="bolded">Front End Buffing</li>
				<li>Ceramic Sealant Application</li>
				<li>Exterior Glass</li>
				<li>Vacuum and Clean Trunk</li>
				<li>Trim, Plasic & Vinyl Restoration</li>
			</ol>
			<p>Interior</p>
			<ol>
				<li>BlowOut / Initial Vacuum</li>
				<li>Remove Gum and Sticky Things</li>
				<li class="bolded">Detail Solution Application,Brushing and Vacuuming of Crevices, etc.</li>
				<li class="bolded">Shampoo Carpets</li>
				<li class="bolded">Shampoo Fabric Seats</li>
				<li>Clean and Condition Leather Seats</li>
				<li>Scotch Guard Seats and Carpet</li>
				<li>Door Jambs</li>
				<li>Dash, Console, CupHolders, GloveBox, Etc.</li>
				<li>Trim, Vinyl and Plastic Restoration</li>
				<li>Final Vacuum</li>
				<li>Interior Glass</li>
			</ol>
		</div>
		<div>
			<h1>Good Value</h1>
			<p>Exterior</p>
			<ol>
				<li>Tires and Rims</li>
				<li>Pre-Rinse</li>
				<li>Power Wash with Premium Soap</li>
				<li>Hand Wash and Dry</li>
				<li>Floor Mats Cleaned and Restored</li>
				<li>Wet Wax Application</li>
				<li>Trim Restoration</li>
				<li>Plastic Restoration</li>
				<li>Exterior Glass</li>
			</ol>
			<p>Interior</p>
			<ol>
				<li>Blow Out / Initial Vacuum</li>
				<li>Remove Gum and Sticky Things</li>
				<li>Steam Clean Seats, Carpet, and Fabric</li>
				<li>Scotch Guard Seats and Carpet</li>
				<li>Door Jambs</li>
				<li>Dash, Console, Cup Holders, Glove Box, Etc.</li>
				<li>Trim, Plastic and Vinyl Restoration</li>
				<li>Plastic Restoration</li>
				<li>Final Vacuum</li>
				<li>Interior Glass</li>
			</ol>
		</div>
		<div>
			<h1>Add-Ons</h1>
			<ol>
				<li>Clay Bar</li>
				<li>Buffing</li>
				<li>Leather Clean &amp; Conditioning</li>
				<li>Pet Hair Removal</li>
				<li>Carpet Shampoo</li>
				<li>Seat Shampoo</li>
				<li>Child Car Seat</li>
				<li>Engine and Engine Bay</li>
				<li>Bug and Road Tar Removal</li>
				<li>Odor Elimination</li>
				<li>Rock Chip Repair</li>
				<li>Headlight Restoration</li>
				<li>Light Scratch Removal</li>
			</ol>
		</div>
		<div class="value">
			<ValuePage />
		</div>
		<div>
			<List header="Exterior" items={exterior} />
		</div>
		<Pigs />
		<div>
			<List header="Interior" items={interior} />
		</div>
	</div>
</div>

<style>
	.title-bar {
		display: grid;
		place-items: center;
		grid-template-columns: 1fr 1fr 1fr;
	}
	.main-page {
		display: grid;
		grid-template-columns: 1fr 2fr 1fr;
		place-items: center;
		align-items: start;
	}
	.logo {
		width: 10rem;
	}
	.header-text {
		text-align: center;
	}
	.header-logo {
		padding-top: 1rem;
		display: flex;
		justify-content: center;
		height: 45vh;
	}
	li.bolded {
		color: lightgreen;
	}
	.title {
		font-size: 2em;
		text-align: center;
		font-weight: normal;
	}
	.value {
		grid-column: 1 / -1;
		padding-top: 3rem;
		padding-bottom: 3rem;
	}
	.description {
		text-align: center;
	}
	h1 {
		color: var(--yellow);
	}
</style>
