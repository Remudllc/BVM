<script lang="ts">
	import List from '../components/list.svelte';
	import Pigs from '../components/pigs.svelte';
	import ValuePage from '../components/value_page.svelte';

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
	<ValuePage />
	<div class="main-page">
		<div>
			<h1>best value</h1>
			<p>Exterior</p>
			<ol>
				<li>TiresandRims</li>
				<li>Pre-Rinse</li>
				<li>PowerWashwithPremiumSoap</li>
				<li>HandWashandDry</li>
				<li>FloorMatsCleanedandRestored</li>
				<li class="bolded">CarnaubaWaxApplication</li>
				<li class="bolded">FrontEndbuffing</li>
				<li>CeramicSealantApplication</li>
				<li>TrimRestoration</li>
				<li>PlasticRestoration</li>
				<li>ExteriorGlass</li>
				<li>VacuumandCleanTrunk</li>
			</ol>
			<p>Interior</p>
			<ol>
				<li>BlowOut/InitialVacuum</li>
				<li>RemoveGumandStickyThings</li>
				<li class="bolded">DetailSolutionApplication,BrushingandVacuumingofCrevices,etc.</li>
				<li class="bolded">ShampooCarpets</li>
				<li class="bolded">ShampooFabricSeats</li>
				<li>CleanandConditionLeatherSeats</li>
				<li>ScotchGuardSeatsandCarpet</li>
				<li>DoorJambs</li>
				<li>Dash,Console,CupHolders,GloveBox,Etc.</li>
				<li>Vinyl,RubberandPlasticRestoration</li>
				<li>FinalVacuum</li>
				<li>InteriorGlass</li>
			</ol>
		</div>
		<div>
			<h1>good value</h1>
			<p>Exterior</p>
			<ol>
				<li>Tires and Rims</li>
				<li>Pre-Rinse</li>
				<li>Power Wash with Premium Soap</li>
				<li>Hand Wash and Dry</li>
				<li>Floor Mats</li>
				<li>Wet Wax Application</li>
				<li>Trim Restoration</li>
				<li>Plastic Restoration</li>
				<li>Exterior Glass</li>
			</ol>
			<p>Interior</p>
			<ol>
				<li>Blow Out</li>
				<li>Initial Vacuum</li>
				<li>Remove Gum and Sticky Things</li>
				<li>Steam Clean Seats, Carpet, and Fabric</li>
				<li>Scotch Guard Seats and Carpet</li>
				<li>Door Jambs</li>
				<li>Dash, Console, Cup Holders, Glove Box, Etc.</li>
				<li>Vinyl, Rubber and Plastic Restoration</li>
				<li>Plastic Restoration</li>
				<li>Final Vacuum</li>
				<li>Interior Glass</li>
			</ol>
		</div>
		<div>
			<h1>add-ons</h1>
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
	li.bolded {
		color: lightgreen;
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
