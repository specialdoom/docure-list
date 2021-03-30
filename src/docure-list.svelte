<svelte:options tag="docure-list" accessors={false} />

<script>
  import { onMount } from "svelte";

  const styleSheet = `
    ul {
      list-style-type: none;
      display: grid;
      grid-template-columns: auto auto auto;
      margin: 0;
      padding: 0;
      height: 440px;
      justify-self: center;
      background-color: #4392f1;
      align-items: center;
    }

    ul li {
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

    ul li h2 {
      height: 10%;
      margin: 0px;
      padding: 0px 0px 15px 0px;
      font-size: 30px;
      color: #282828;
      border-bottom: 3px solid #dc493a;
    }

    ul li p {
      height: 70%;
      margin: 15px 0px 0px 0px;
      font-weight: 300;
      font-size: 16px;
      word-break: break-all;
      word-wrap: pre-wrap;
    }

    ul li div {
      height: 20%;
      margin: 10px auto;
    }
  `;

  onMount(() => {
    const list = document.querySelector("docure-list");
    const children = list.children;
    const styleElement = document.createElement("style");
    styleElement.innerText = styleSheet;
    list.shadowRoot.appendChild(styleElement);
    list.shadowRoot.appendChild(children[0]);
  });
</script>
