<script>
	import ContactCard from './ContactCard.svelte'
	let name = 'Richi';
	let age = 17;
	let job = '';
	let desc = '';
	let image = '';
	$: upperCaseName = name.toUpperCase()
	// $: console.log("it works?")
	$: if(upperCaseName === 'RICHI'){
		age +=1;
	}
	function incrementAge() {
		age += 1;
	}
	function changeName() {
		name = "Richi Ramadhan";
	}
	function nameInput() {
		const enteredValue = event.target.value;
		name = enteredValue;
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {upperCaseName}, my age is {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<!-- <button on:click="{changeName}">Change Name</button> -->
<!-- <input type="text" value="{name}" on:input="{nameInput}"> -->
<input type="text" bind:value={name}>
<input type="text" bind:value={job}>
<input type="text" bind:value={image}>
<textarea name="" id="" cols="30"  bind:value="{desc}"></textarea>

<ContactCard 
	userName={name} 
	jobTitle={job} 
	description={desc}
	imageName={image}/>