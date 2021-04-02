<svelte:options tag="docure-list" />

<script>
  export let background = "#4392f1";

  const style = `background-color: ${background};`;
</script>

<div class="docure-list" {style}>
  <slot>
    <docure-list-item title="test" description="test">
      <button on:click={() => alert("test")}>Alert test</button>
    </docure-list-item>
  </slot>
</div>

<style>
  div {
    display: grid;
    grid-template-columns: auto auto auto;
    justify-content: space-around;
    margin: 0;
    padding: 0;
    height: 440px;
    justify-self: center;
    align-items: center;
  }
</style>
