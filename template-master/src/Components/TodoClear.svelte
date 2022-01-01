<script>
    import AddTodo from "./AddTodo.svelte";
    const props = {
            toDoOne:"",
            toDoTwo:""
		
	}
    export function clear(){
		if(props.toDoTwo === "" && props.toDoOne !== ''){
		props.toDoOne = ""
		}else props.toDoTwo = ""
	}
    
</script>

<div>
    <button on:click={clear}>Delete</button>
    <AddTodo {...props}/>
</div>