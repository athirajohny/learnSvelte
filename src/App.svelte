<script>
	export let name;
	let org = 'Pearl Data Direct';
	let color = 'blue';
	

	const handleClick = () => {
		org = "Tablez";
	};

	const handleInput = (e) => {
		org = e.target.value
	};
	const changeColor = (e) =>{
		color = e.target.value
	};
</script>




<main>
	<h1>Hello {name}!</h1>
	<p>Welcome to {org}</p>
	<button on:click={handleClick}>Change Org</button>	
	<!-- <input type="text" on:input={handleInput} value={org}> -->
	<!-- data binding -->
	<input type="text" bind:value={org}>
	<p style="color: {color};">UI looks good in {color}</p>
	<input type="text" bind:value={color}>

</main>


<style>
	main{
		text-align: center;
	}
	h1{
		font-size: 20px;
	}
	button{
		background-color: rgb(31, 166, 219);
		color: white;
	}
	/* @media (min-width: 640px) {} */
</style>