<script>
	let color = 'blue';
	let fname = 'Athira';
	let lname = 'Johny';

	//reactive value
    $: fullName = `${fname} ${lname}`;
	//reactive statments
	$: {
    console.log(color);
    console.log(fullName);
  }
	
	const changeColor = (e) =>{
		color = e.target.value
	};
</script>




<main>
	<p style="color: {color};"> {fullName} </p>
	<input type="text" bind:value={color}> 
	<input type="text" bind:value={fname}>
	<input type="text" bind:value={lname}>


</main>


<style>
	main{
		text-align: center;
	}
	/* @media (min-width: 640px) {} */
</style>