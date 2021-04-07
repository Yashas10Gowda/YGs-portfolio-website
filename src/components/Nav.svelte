<script>
  import { onMount } from "svelte";

  let icon = 'gg-menu-round';

  onMount(async () => {
    let a = document.getElementsByClassName("icon");
    a[0].href = "javascript:void(0)";
  });

  function myFunction() {
    icon =
      icon == 'gg-menu-round'
        ? 'gg-close-o'
        : 'gg-menu-round';
    var x = document.getElementById("demo");
    if (x.className.indexOf("w3-show") == -1) {
      x.className += " w3-show";
    } else {
      x.className = x.className.replace(" w3-show", "");
    }
  }
</script>

<style>
  .w3-hide-small {
    padding-bottom: 7px;
    margin-top: 2px;
  }
  .icon {
    --ggs: 1.25;
    position: relative;
    top: 5px;
  }
  .gg-menu-round {
    box-sizing: border-box;
    position: relative;
    display: block;
    transform: scale(var(--ggs,1));
    width: 22px;
    height: 22px;
    border-radius: 24px;
    border: 2px solid;
  }
  .gg-menu-round::before {
    content: "";
   display: block;
   box-sizing: border-box;
   position: absolute;
   width: 10px;
   height: 2px;
   background: currentColor;
   border-radius: 3px;
   top: 4px;
   left: 4px;
   box-shadow: 0 4px 0, 0 8px 0
  }
  .gg-close-o {
    box-sizing: border-box;
    position: relative;
    display: block;
    transform: scale(var(--ggs,1));
    width: 22px;
    height: 22px;
    border: 2px solid;
    border-radius: 40px
  }
  .gg-close-o::after,
  .gg-close-o::before {
    content: "";
    display: block;
    box-sizing: border-box;
    position: absolute;
    width: 12px;
    height: 2px;
    background: currentColor;
    transform: rotate(45deg);
    border-radius: 5px;
    top: 8px;
    left: 3px
  }
  .gg-close-o::after {
    transform: rotate(-45deg)
  }
</style>

<div data-nosnippet class="w3-top">
  <div
    class="w3-bar w3-xlarge w3-white w3-text-blue w3-border w3-card-4
    w3-container">
    <a href="/" class="w3-bar-item w3-button w3-hover-white w3-hover-text-blue">
      <h1
        style="font-weight:600;font-size:27px;font-family: 'Montserrat',
        sans-serif;margin:0;">
        Yashas Gowda
      </h1>
    </a>
    <div class="w3-right w3-hide-medium">
      <a
        rel="prefetch"
        href="/"
        class="w3-bar-item w3-button w3-hover-blue w3-hide-small">
        Home
      </a>
      <a
        rel="prefetch"
        href="/about"
        class="w3-bar-item w3-button w3-hover-blue w3-hide-small">
        About
      </a>
      <a
        rel="prefetch"
        href="/works"
        class="w3-bar-item w3-button w3-hover-blue w3-hide-small">
        Works
      </a>
      <a
        rel="prefetch"
        href="/uses"
        class="w3-bar-item w3-button w3-hover-blue w3-hide-small">
        Uses
      </a>
      <a
        rel="prefetch"
        href="/contact"
        class="w3-bar-item w3-button w3-hover-blue w3-hide-small">
        Contact
      </a>
    </div>

    <a
      href="/"
      class="w3-bar-item w3-button w3-right w3-hide-large w3-hover-blue icon
      w3-ripple"
      on:click={myFunction}>
      <i class="{icon}"></i>
    </a>
  </div>

  <div
    id="demo"
    class="w3-bar-block w3-large w3-white w3-hide w3-hide-large w3-container
    w3-text-blue">
    <a
      href="/"
      rel="prefetch"
      on:click={myFunction}
      class="w3-bar-item w3-button w3-hover-blue">
      Home
    </a>
    <a
      href="/about"
      rel="prefetch"
      on:click={myFunction}
      class="w3-bar-item w3-button w3-hover-blue">
      About
    </a>
    <a
      href="/works"
      rel="prefetch"
      on:click={myFunction}
      class="w3-bar-item w3-button w3-hover-blue">
      Works
    </a>
    <a
      href="/uses"
      rel="prefetch"
      on:click={myFunction}
      class="w3-bar-item w3-button w3-hover-blue">
      Uses
    </a>
    <a
      href="/contact"
      rel="prefetch"
      on:click={myFunction}
      class="w3-bar-item w3-button w3-hover-blue">
      Contact
    </a>
  </div>
</div>
