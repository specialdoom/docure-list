<svelte:options tag="docure-list" />

<div class="docure-list">
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
    background-color: #4392f1;
    align-items: center;
  }
</style>
