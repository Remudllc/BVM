<script lang="ts">
	export let items: string[];
	export let header: string;
</script>

<div>
	<p><u>{header}</u></p>
</div>
<ul class="checkmark-list">
	{#each items as item (item)}
		<li>{item}</li>
	{/each}
</ul>

<style>
	ul.checkmark-list {
		list-style-type: none; /* Removes default list bullet points */
	}

	ul.checkmark-list li::before {
		content: '✔'; /* This is a Unicode checkmark character */
		color: green; /* Color of the checkmark */
		margin-right: 10px; /* Space between the checkmark and the list item text */
	}
</style>
