<script>
	import H1Element from "./DraggableComponents/H1Element.svelte"; 
	import PElement from "./DraggableComponents/PElement.svelte"; 
	import ImgElement from "./DraggableComponents/ImgElement.svelte"; 
</script>

<div>
	<h1>HTML Elements</h1>
	
	<H1Element/>
	
	<ImgElement/>
	
	<PElement/>
	

</div>

<style>
	h1 {
		text-align: center; 
	}
	div {
		height: 50%; 
		width: 25%; 
		border: solid 1px gray; 
	}
</style>