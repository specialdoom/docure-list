<svelte:options tag="docure-list-item" />

<script>
  import { onMount } from "svelte";

  export let title = "";
  export let description = "";

  onMount(() => {
    if (title.length > 30) {
      title = `${title.slice(0, 29)}...`;
    }

    if (description.length > 330) {
      description = `${description.slice(0, 329)}...`;
    }
  });
</script>

<div class="docure-list-item">
  <h2>{title}</h2>
  <p>{description}</p>
  <div>
    <slot />
  </div>
</div>

<style>
  .docure-list-item {
    height: 350px;
    width: 250px;
    display: flex;
    flex-direction: column;
    justify-self: center;
    padding: 20px;
    border-radius: 10px;
    background-color: #fff;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  }

  .docure-list-item h2 {
    height: 20%;
    margin: 0px;
    padding: 0px 0px 15px 0px;
    word-break: break-all;
    font-size: 30px;
    color: #282828;
    border-bottom: 3px solid #dc493a;
  }

  .docure-list-item p {
    height: 70%;
    margin: 15px 0px 0px 0px;
    font-weight: 300;
    font-size: 16px;
    word-break: break-all;
    word-wrap: pre-wrap;
  }

  .docure-list-item div {
    height: 10%;
    margin: 10px auto;
  }
</style>
