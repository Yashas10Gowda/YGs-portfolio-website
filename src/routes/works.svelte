<script>
  const projects = [
    {
      name: "BookUrBooks.in",
      client: true,
      description: `I Built an E-Commerce website for a Client who had a business idea of selling used/read books online. Many industry standard functionalities like <b>OTP verification, Online Payment Gateway, Cart, Admin Interface</b> and so on are baked in into this project. Buy-Read-Exchange-Repeat!`,
      ts: "*** Confidential ***",
      link: "https://www.bookurbooks.in/",
    },
    {
      name: "Flash Chat",
      client: false,
      description: `A simple Real-time Chat App (indeed it's a PWA which means it can be installed on a smartphone just like a Native App), that mimics the basic functionality of a WhatsApp Group Chat(a clone to de precise) where chatrooms can be created by one and joined by others.`,
      ts: "Svelte.JS, Ionic, Firebase's Firestore",
      link: "https://flashchat-f7942.web.app/",
    },
    {
      name: "Portfoio Website",
      client: false,
      description: `Developed my portfolio website using W3.CSS which then turned out to be simple and minimal, exactly how I wanted it. This site is also SEO friendly, if try searching for "Yashas Gowda Postfolio Website" it'll be ranked 1st on google. Just trying to flex my SEO skills.`,
      ts: "Sapper.JS, W3.CSS",
      link: "https://yashasgowda.web.app/",
    },
    {
      name: "Flash Video Call",
      client: false,
      description: `An "End-to-End" Encrypted <b>"Real-Time Video Calling"</b> feature was built as an extension to the previous project(Flash Chat). So Two peers across the globe can "Video-Call" each other without giving out any of their personal info instead they share a uniquely generated number with each other.`,
      ts: "WebRTC, Svelte.JS, Firebase's Firestore, Ionic",
      link: "https://flashchat-f7942.web.app/",
    },
    {
      name: "Code Connector",
      client: false,
      description: `A Social Media App for developers, (available as PWA). It connects Coders, Developers, Programmers across the world to collaborate, invent and develop. I Handled everything from creation of accounts, posts to their permissions in the backend (This is a well separated frontend and backend project.)`,
      ts: "Django, Django Rest Framework, Sapper.JS, Bootstrap",
      link: "https://codeconnector.web.app/",
    },
    {
      name: "UI Templates",
      client: false,
      description: `Templates which drew inspiration from top websites like heroku.com, airbnb.com etc (do feel free to star this repo on Github). These templates are live right now so click on any one of the following names that you find attractive :<a
      style="text-decoration: underline;font-style: italic;"
      target="_blank"
      href="https://yashas.pythonanywhere.com/travelville">
      TravelVille
    </a>
    ,
    <a
      style="text-decoration: underline;font-style: italic;"
      target="_blank"
      href="https://yashas.pythonanywhere.com/quazzu">
      Quazzu
    </a>
    ,
    <a
      style="text-decoration: underline;font-style: italic;"
      target="_blank"
      href="https://yashas.pythonanywhere.com/madmin">
      M-Admin
    </a>
    ,
    <a
      style="text-decoration: underline;font-style: italic;"
      target="_blank"
      href="https://yashas.pythonanywhere.com/bizland">
      BizLand
    </a>`,
      ts: "MaterializeCSS, JQuery",
      link: "https://github.com/Yashas10Gowda/MaterializeCSSCourse",
    },
    {
      name: "UPI'ly Link'ed",
      client: false,
      description: `This Webpage is exclusively built for a mobile devices with anyone UPI App (PSP App) installed in it. And visitors can just enter an amount and pay me via UPI (thereby saving myself from happening to share that cryptic UPI-ID or QR-Code EACH AND EVERYTIME).`,
      ts: "Vanilla.JS, Google's Material Components",
      link: "https://yashas.pythonanywhere.com/",
    },
    {
      name: "Desktop Apps",
      client: false,
      description: `First one being CPUStats which monitors your CPU usage and warns you
    whenever the CPU is overload beyond the threshold value which you're gonna
    set. Second one is ImageShrinker. Third one is Logger which saves the log(or
    message) in a csv file programmatically.
    <a
      style="text-decoration: underline;font-style: italic;"
      target="_blank"
      href="https://github.com/Yashas10Gowda/3_PyQt5_GUIApps/raw/master/cpustats.exe">
      CPUStats
    </a>
    ,
    <a
      style="text-decoration: underline;font-style: italic;"
      target="_blank"
      href="https://github.com/Yashas10Gowda/3_PyQt5_GUIApps/raw/master/imageshrinker.exe">
      ImageShrinker
    </a>
    ,
    <a
      style="text-decoration: underline;font-style: italic;"
      target="_blank"
      href="https://github.com/Yashas10Gowda/3_PyQt5_GUIApps/raw/master/logger.exe">
      Logger
    </a>`,
      ts: "Python, PyQt5",
      link: "https://github.com/Yashas10Gowda/3_PyQt5_GUIApps",
    },
    {
      name: "AI-Projects",
      client: false,
      description: `Projects are :- 1)CommentSense &nbsp;2)StoQueAns &nbsp;3)WhatIsIt. Names are
    a little quirky so are these projects, do check it out. When the webpage is
    loaded for the first time it would take a minute or less to collect all the
    pre-trained models from the server, so please be patient.`,
      ts: "Tensorflow.JS, UI-Kit, Vanilla.JS",
      link: "https://yashas.pythonanywhere.com/ai-projects/",
    },
  ];
</script>

<svelte:head>
  <title>Works | Yashas Gowda</title>
</svelte:head>

<div class="w3-section">&nbsp;</div>
<div class="w3-section">&nbsp;</div>

<div class="w3-row">
  <div class="w3-col s1">&nbsp;</div>

  <div class="w3-col s10 w3-animate-bottom">
    <h1 style="font-weight:600;">My Works</h1>
  </div>
  <div class="w3-col s1">&nbsp;</div>
</div>
<div class="w3-section w3-hide-small w3-hide-medium w3-animate-opacity">
  <img
    class="worksimg w3-responsive"
    style="width:100%;max-width:300px;position: fixed;right: 100px;top: 30%;"
    src="works.svg"
    alt=""
  />
</div>

{#each projects as project}
  <div class="w3-row w3-section w3-animate-top">
    <div class="w3-col s1">&nbsp;</div>
    <div class="w3-col s10 m7 l6">
      <div class="w3-card-4">
        <header class="w3-container w3-text-white">
          {#if project.client}
            <div class="w3-row w3-border-bottom w3-border-white">
              <div class="w3-col s10 w3-margin-top">
                <h2>{project.name}</h2>
              </div>
              <div class="w3-col s2">
                <div class="w3-tag w3-white w3-text-blue w3-right">Client</div>
              </div>
            </div>
          {:else}
            <div class="w3-row w3-border-bottom w3-border-white">
              <h2>{project.name}</h2>
            </div>
          {/if}
        </header>
        <div class="w3-container">
          <p class="w3-large">
            {@html project.description}
          </p>
          <hr />
          <p class="w3-large">
            TECH-STACK:
            <br />
            {project.ts}
          </p>
        </div>
        <a
          target="_blank"
          class="w3-button w3-block w3-white w3-text-blue w3-ripple
          w3-hover-white w3-hover-text-blue"
          style="padding:0;padding-bottom:8px;"
          href={project.link}
        >
          View Project
          <i
            style="--ggs:0.75;display:inline-block;position:relative;top:6px;"
            class="gg-arrow-right"
          />
        </a>
      </div>
    </div>
    <div class="w3-col s1">&nbsp;</div>
  </div>
  <div class="w3-margin-bottom">&nbsp;</div>
{/each}

<style>
  h1,
  h2 {
    margin: 10px 0;
  }
  h2 {
    font-weight: 500;
  }
  .gg-arrow-right {
    box-sizing: border-box;
    position: relative;
    display: block;
    transform: scale(var(--ggs, 1));
    width: 22px;
    height: 22px;
  }
  .gg-arrow-right::after,
  .gg-arrow-right::before {
    content: "";
    display: block;
    box-sizing: border-box;
    position: absolute;
    right: 3px;
  }
  .gg-arrow-right::after {
    width: 8px;
    height: 8px;
    border-top: 2px solid;
    border-right: 2px solid;
    transform: rotate(45deg);
    bottom: 7px;
  }
  .gg-arrow-right::before {
    width: 16px;
    height: 2px;
    bottom: 10px;
    background: currentColor;
  }
</style>
