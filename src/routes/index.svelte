<script>
  let iteratingtexts =
    "Svelte.JS   |Django (inc. DRF)   |JAMStack (Sapper.JS)   |Desktop Apps (GUI)  |Ionic For PWAs  |";
  let iteratingtext = "";

  let i = 0;

  setInterval(() => {
    if (iteratingtexts[i] == "|") {
      iteratingtext = "";
      i = i + 1;
    }
    iteratingtext += iteratingtexts[i];
    i += 1;
    if (i > iteratingtexts.length) {
      i = 0;
      iteratingtext = "";
    }
  }, 200);
</script>

<style>
  .w3-padding-16y {
    padding-top: 32px;
  }
  @media (max-width: 700px) {
    .w3-padding-16y {
      padding-top: 0;
    }
    .intro {
      text-align: center !important;
    }
  }
</style>

<svelte:head>
  <title>Yashas Gowda | A Full-Stack Web Developer By Passion.</title>
</svelte:head>

<div class="w3-padding-48 w3-hide-small">&nbsp;</div>
<div class="w3-padding-32 w3-hide-large w3-hide-medium">&nbsp;</div>

<div class="w3-row">
  <div class="w3-col l1 m1 s1">&nbsp;</div>
  <div class="w3-col l3 m4 s10 w3-display-container w3-center">
    <img
      style="width:100%;max-width:375px;height:auto;"
      src="portfolio-pic.jpg"
      alt="Programming Vector"
      class="w3-card-4 w3-image w3-animate-opacity" />
    <div
      style="font-size: 20px;"
      class="w3-center w3-display-bottommiddle w3-animate-opacity w3-padding-32">
      Digital Nomad
    </div>
  </div>
  <div class="w3-col l1 m1 s1">&nbsp;</div>
  <div class="w3-row w3-hide-large w3-hide-medium">&nbsp;</div>
  <div class="w3-col s1 w3-hide-large w3-hide-medium">&nbsp;</div>
  <div
    class="w3-col l6 m5 s10 w3-animate-opacity w3-padding-16y w3-left-align
    intro">
    <div style="font-size:20px;">
      <br />
      Welcome to the portfolio website of YASHAS GOWDA, a Full-Stack Developer
      by passion, currently living and breathing in Bengaluru.
    </div>
    <br class="w3-hide-medium w3-hide-small" />
    <hr class="w3-hide-large w3-hide-medium" />
    <div style="font-weight:600;" class="w3-section w3-xxlarge">
      {iteratingtext}_
    </div>
    <hr class="w3-hide-large w3-hide-medium" />
    <br class="w3-hide-medium w3-hide-small" />
    <div style="font-size:20px;">
      Let's look at his
      <a
        href="/works"
        class="w3-button w3-hover-white w3-hover-text-blue w3-transparent
        w3-border w3-round-xxlarge w3-border-white">
        Works.
      </a>
    </div>
  </div>
  <div class="w3-col l1 m1 s1">&nbsp;</div>
</div>
<div class="w3-section">&nbsp;</div>
