<script>
	import TodoClear from "./TodoClear.svelte";
    export let toDoOne = "";
	export let toDoTwo = "";
function addTodo() {
    
		if(toDoOne === ""){
			toDoOne = input.value;
		}else if(toDoOne !== "") {
			toDoTwo = input.value;
		}
		input.value = ""
	}
</script>


<div>
    <input id="input" class="one">
	<button on:click={addTodo}>add</button>
    <p><input type="checkbox" id="checkbox" > My first todo:{toDoOne}</p>
	<p><input type="checkbox" id="checkboxTwo" > My second todo:{toDoTwo}</p>
</div>