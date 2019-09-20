<script>
	let name = 'Richi';
	let age = 17;
	$: upperCaseName = name.toUpperCase()
	$: console.log("it works?")
	$: if(upperCaseName === "RICHI"){
		age +=1;
	}
	function incrementAge() {
		age += 1;
	}
	function changeName() {
		name = "Richi Ramadhan";
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {upperCaseName}, my age is {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<button on:click="{changeName}">Change Name</button>
