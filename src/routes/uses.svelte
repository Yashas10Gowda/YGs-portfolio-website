<script>
  const toolsData = {
    webTechnologies:[
      {name:'Svelte.JS',link:'https://svelte.dev/'},
      {name:'Lit',link:'https://lit.dev/'},
      {name:'Google Firebase',link:'https://firebase.google.com/'},
      {name:'PyQt5',link:'https://pypi.org/project/PyQt5/'},
      {name:'Ionic',link:'https://ionicframework.com/'},
      {name:'Sapper.JS (JAMSTACK)',link:'https://sapper.svelte.dev/'},
      {name:'Django & Django Rest Framework',link:'https://www.django-rest-framework.org/'},
      {name:'ShoeLace.style',link:'https://shoelace.style/'},
      {name:'MaterializeCSS',link:'https://materializecss.com/'},
      {name:'Bootstrap',link:'https://getbootstrap.com/'}
    ],
    skills:[
      'REST APIs','Single Page Applications (SPA)','Progressive Web Apps (PWA)',
      'Desktop Apps (GUI)'
    ],
    languages:['Python','Javascript','HTML and CSS','English'],
    devTools:[
      {name:'Lubuntu (LXQT)',link:'https://lubuntu.me/'},
      {name:'Visual Studio Code',link:'https://code.visualstudio.com'},
      {name:'Git Distributed VCS',link:'https://git-scm.com'},
      {name:'Jupyter Lab',link:'https://jupyter.org/'},
      {name:'Node.JS Runtime',link:'https://nodejs.org/'},
      {name:' Chrome Dev-Tools',link:'https://google.com/chrome'}
    ]
  }
</script>

<svelte:head>
  <title>Tools I Use | Yashas Gowda</title>
</svelte:head>

<div class="w3-section">&nbsp;</div>
<div class="w3-section">&nbsp;</div>

<div class="w3-row w3-margin-top w3-section">
  <div class="w3-col s1">&nbsp;</div>
  <div class="w3-col s10 w3-animate-bottom">
    <h1 style="font-weight:600">Tools I Use</h1>
  </div>
  <div class="w3-col s1">&nbsp;</div>
</div>
<div class="w3-section w3-hide-small w3-hide-medium w3-animate-fading">
  <img
    style="width: 400px; position: fixed; right: 60px; bottom: 20%;"
    src="tools.svg"
    alt="..." />
</div>

<div class="w3-row w3-animate-opacity">
  <div class="w3-col s1">&nbsp;</div>
  <div class="w3-col s10 m8 l6">

    <h3 style="font-weight:600">Web Technologies</h3>
    {#each toolsData.webTechnologies as webTech}
      <a
      target="_blank"
      rel="noopener noreferrer"
      class="w3-tag w3-white w3-text-blue w3-ripple"
      href={webTech.link}>
        {webTech.name}
    </a>
    {/each}
  
    <h3 style="font-weight:600" class="w3-margin-top">My Skills</h3>
    {#each toolsData.skills as skills}
      <div class="w3-tag w3-white w3-text-blue w3-ripple a">{skills}</div>
    {/each}
    
    <h3 style="font-weight:600" class="w3-margin-top">Languages</h3>
      <div
        style="padding-bottom: 3px; transform: scaleY(0.85)
        translateY(-2px); margin: 0; margin-bottom: 5px; font-size: 16px; font-weight: 600;"
        class="w3-tag w3-white w3-text-blue w3-ripple">
        ಕನ್ನಡ
      </div>
    {#each toolsData.languages as languages}
      <div class="w3-tag w3-white w3-text-blue w3-ripple a">{languages}</div>      
    {/each}
      

    <h3 style="font-weight:600" class="w3-margin-top">Development Tools</h3>
    {#each toolsData.devTools as devTools}
      <a
      target="_blank"
      rel="noopener noreferrer"
      href={devTools.link}
      class="w3-tag w3-white w3-text-blue w3-ripple">
        {devTools.name}
      </a>
    {/each}
    

  </div>
  <div class="w3-col s1">&nbsp;</div>
</div>
<div class="w3-section">&nbsp;</div>

<style>
  h3 {
    margin: 10px 0;
  }
  a,
  .a {
    margin-bottom: 5px;
    margin-right: 5px;
    font-size: 16px;
    font-weight: 600;
    text-decoration: none;
  }
  h1{
    margin: 0;
  }
</style>
