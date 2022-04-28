<script>
  import Elements from './lib/Elements.svelte';
  import Canvas from './lib/Canvas.svelte'
  import Tree from './lib/Tree.svelte'
	import Codeblock from './Codeblock.svelte' ;

  let toggled = true

  function toggle() {
		toggled = !toggled;
   // console.log("test",checked)
	}
  $:console.log(toggled)
</script>

<main>
  <!-- <div id = "header">Svetch mock header</div> -->
  <!-- <button id = 'togBut' on:click = {toggle}> switch between canvas and tree </button> -->
  <Elements id = "el"/>
  {#if toggled}
  <Canvas bind:toggled = {toggled}/>
  {:else}
  <Tree bind:toggled = {toggled}/>
  {/if}
  <pre>
    <code>
      <Codeblock />
    </code>
  </pre>
</main>
<style>
main {
  padding-top: .5vh;
  display: flex;
  flex-direction: row;
  text-align: center;
  width: 100vw;
  height: 100vh;
  margin: 0 auto;
}
#togBut {
  float: right;
  margin-top: .5vh;
}

@media (min-width: 640px) {
  main {
    max-width: none;
  }
}
</style>
