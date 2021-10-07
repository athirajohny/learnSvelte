<script>
	let num = 2;
</script>

<main>
	{#if num > 30}
	<p>greater than 30</p>

	{:else if num > 20}
	<p>greater than 20</p>

	{:else}
	<p>less than 12</p>
	
	{/if}
</main>


<style>
	
</style>