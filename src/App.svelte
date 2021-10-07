<script>
	let people = [
		{name:'Athira',color:'yellow',age:23, id:1},
		{name:'Femi',color:'blue',age:19, id:2},
		{name:'Felix',color:'red',age:19, id:3},
	];
	const handleClick = (id) => {
		// console.log(id);
		people = people.filter((person) => person.id!=id);
	}
</script>

<main>
	<!-- manually -->
	<!-- <div>
		{people[1].name} <p>{people[1].color}</p>
	</div> -->

	<!-- for each loop -->
	{#each people as person}
	<div>
		<p>Hi I'm {person.name}, {person.age} years old, favourite colour is {person.color}</p>
		<button on:click={() => handleClick(person.id)}>Delete</button>
	</div>
	{:else}
	<p>There are no people to show..</p>
	{/each}
</main>


<style>
	main{
		text-align: center;
	}
	button{
		background-color: blue;
		color: white;
	}
	/* @media (min-width: 640px) {} */
</style>