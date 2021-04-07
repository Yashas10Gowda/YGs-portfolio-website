<script>
  let name = "";
  let email = "";
  let message = "";
  let alert = false;
  let data = {};
  let sendfun = () => {
    if (
      name !== "" &&
      email !== "" &&
      message !== "" &&
      email.includes("@" && ".")
    ) {
      data = {
        fields: {
          name: {
            stringValue: name,
          },
          email: {
            stringValue: email,
          },
          message: {
            stringValue: message,
          },
        },
      };
      fetch(
        "https://firestore.googleapis.com/v1/projects/flashchat-f7942/databases/(default)/documents/PortfolioMessages/",
        {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify(data),
        }
      ).then(() => {
        alert = true;
        name = "";
        email = "";
        message = "";
        data = {};
      });
    }
  };
</script>

<svelte:head>
  <title>Contact | Yashas Gowda</title>
</svelte:head>

<div class="w3-section">&nbsp;</div>
<div class="w3-section">&nbsp;</div>

{#if alert}
  <div class="w3-panel w3-text-blue w3-white w3-display-container w3-center">
    <span
      on:click={() => (alert = false)}
      class="w3-button w3-padding-small w3-display-right w3-hover-white
      w3-hover-text-blue w3-ripple"
    >
      &times;
    </span>
    <p>Thank You!! {name} for contacting me. I will get back to you A.S.A.P.</p>
  </div>
{/if}

<div class="w3-section w3-hide-small">&nbsp;</div>
<div class="w3-section w3-hide-small">&nbsp;</div>

<div class="w3-row">
  <div class="w3-col s1">&nbsp;</div>
  <div class="w3-col m6 l6 s10">
    <div class="w3-card-4 w3-animate-left">
      <div class="w3-container w3-text-white">
        <h1 style="font-weight: 600;">Get In Touch</h1>
      </div>
      <div class="w3-container">
        <label for="name">Name:</label>
        <input
          bind:value={name}
          id="name"
          class="w3-input w3-margin-bottom w3-round-xxlarge w3-border-0"
          type="text"
        />
        <label for="email">Email:</label>
        <input
          bind:value={email}
          id="email"
          class="w3-input w3-margin-bottom w3-round-xxlarge w3-border-0"
          type="email"
        />
        <label for="message">Your Message:</label>
        <input
          bind:value={message}
          id="message"
          class="w3-input w3-margin-bottom w3-round-xxlarge w3-border-0"
          type="text"
        />
        <button
          style="outline:none;"
          class="w3-button w3-white w3-text-blue w3-round-xxlarge w3-hover-white
          w3-ripple w3-hover-text-blue"
          on:click={sendfun}
        >
          SEND
        </button>
        <span>&nbsp; -OR- &nbsp;</span>
        <a
          style="display:inline-block;--ggs:0.75;position:relative;top:5px;"
          target="_blank"
          href="https://www.instagram.com/ya_sha_sa/"
        >
          <i class="gg-instagram" />
        </a>
        &nbsp;
        <a
          style="display:inline-block;--ggs:0.95;"
          target="_blank"
          href="https://github.com/Yashas10Gowda/"
        >
          <i style="top:3px;margin-right:5px;" class="gg-git-fork" />
        </a>
        &nbsp;
        <a
          style="display:inline-block;--ggs:0.95;"
          target="_blank"
          href="mailto:yashasgowda270@outlook.com"
        >
          <i style="top:3px;" class="gg-mail" />
        </a>

        <br />
      </div>
      <br />
    </div>
  </div>
  <div class="w3-col m1">&nbsp;</div>
  <div class="w3-col w3-hide-large w3-hide-medium s1">&nbsp;</div>
  <div class="w3-col m3 l3 s10 w3-center w3-margin-top">
    <img
      style="width:100%;max-width:300px;"
      src="mail.svg"
      alt="..."
      class="w3-image w3-animate-left"
    />
  </div>
  <div class="w3-col s1">&nbsp;</div>
</div>

<style>
  input {
    outline: none;
    color: #02abfa;
  }
  .gg-instagram {
    box-sizing: border-box;
    position: relative;
    display: block;
    transform: scale(var(--ggs, 1));
    border: 2px solid transparent;
    box-shadow: 0 0 0 2px;
    border-radius: 4px;
    width: 20px;
    height: 20px;
  }

  .gg-instagram::after,
  .gg-instagram::before {
    content: "";
    display: block;
    box-sizing: border-box;
    position: absolute;
  }

  .gg-instagram::after {
    border: 2px solid;
    left: 3px;
    width: 10px;
    height: 10px;
    border-radius: 100%;
    top: 3px;
  }

  .gg-instagram::before {
    border-radius: 3px;
    width: 2px;
    height: 2px;
    background: currentColor;
    right: 1px;
    top: 1px;
  }

  .gg-mail,
  .gg-mail::after {
    display: block;
    box-sizing: border-box;
    height: 14px;
    border: 2px solid;
  }

  .gg-mail {
    overflow: hidden;
    transform: scale(var(--ggs, 1));
    position: relative;
    width: 18px;
    border-radius: 2px;
  }

  .gg-mail::after {
    content: "";
    position: absolute;
    border-radius: 3px;
    width: 14px;
    transform: rotate(-45deg);
    bottom: 3px;
    left: 0;
  }

  .gg-git-fork {
    box-sizing: border-box;
    position: relative;
    display: block;
    transform: scale(var(--ggs, 1));
    width: 2px;
    height: 14px;
    background: currentColor;
  }

  .gg-git-fork::after,
  .gg-git-fork::before {
    content: "";
    display: block;
    box-sizing: border-box;
    position: absolute;
  }

  .gg-git-fork::before {
    border-right: 2px solid;
    border-bottom: 2px solid;
    border-bottom-right-radius: 4px;
    bottom: 4px;
    width: 8px;
    height: 6px;
    left: 0;
  }

  .gg-git-fork::after {
    width: 4px;
    height: 4px;
    background: currentColor;
    box-shadow: 0 12px 0 0, 6px 2px 0 0;
    border-radius: 100%;
    left: -1px;
    top: -1px;
  }
</style>
