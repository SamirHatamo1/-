<script>
	let toDoOne = "";
	let toDoTwo = "";

	let turnOn ;

	function addTodo() {
		
		if(toDoOne === ""){
			toDoOne = input.value;
		}else if(toDoOne !== "") {
			toDoTwo = input.value;
		}
	}

	function checker() {
		if(toDoOne !== ""){
		toDoOne = "Done"
		}
		turnOn = true;
	}

	function checkerTwo() {
		if(toDoTwo !== ""){
		toDoTwo = "Done"
		}
	}

	function clear(){
		if(toDoTwo === "" && toDoOne !== ''){
		toDoOne = ""
		}else toDoTwo = ""
	}
	
</script>

<main>
	<h1>Svetle Todo app</h1>
	<input id="input" class="one">
	<button on:click={addTodo}>add</button>
	<button  on:click="{clear}" class="tex">Delete</button>
	<p><input type="checkbox" id="checkbox" on:click={checker} > My first todo:{toDoOne}</p>
	<p><input type="checkbox" id="checkboxTwo" on:click={checkerTwo}> My second todo:{toDoTwo}</p>
</main>

<style>
	.one{
		width: 300px;
	}
</style>