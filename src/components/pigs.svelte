<script lang="ts">
	import { phoneNumber } from '../data/contact';
</script>

<div class="container">
	<div class="title">Time to Clean Up? We Can Help</div>
	<img class="pigs" src="/pigs.png" alt="dirty-pigs" />
	<p class="number">{$phoneNumber}</p>
</div>

<style>
	.number {
		color: yellow;
		position: absolute;
		left: 50%;
		bottom: 0.5rem;
		font-size: 2rem;
		transform: translateX(-50%);
	}
	.container {
		position: relative;
	}
	.pigs {
		width: 100%;
	}
	.title {
		color: yellow;
		position: absolute;
		left: 50%;
		top: 0.2rem;
		transform: translateX(-50%);
		font-size: 2rem;
		white-space: nowrap;
	}
</style>
