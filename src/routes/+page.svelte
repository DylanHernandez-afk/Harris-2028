<script>
  import { writable } from 'svelte/store';
  
  const logoSrc = "https://www.figma.com/api/mcp/asset/080d5f66-212a-4f91-8290-a8e87a01410a";
  const footerLogoSrc = "https://www.figma.com/api/mcp/asset/7fc0e96f-1cf7-4f62-adb3-f19e5853551b";
  const btnJoinBgDefault = "https://www.figma.com/api/mcp/asset/4655d701-7f01-40a3-b34c-589a282b0802";
  const btnJoinBgHover = "https://www.figma.com/api/mcp/asset/70a53341-933e-4179-b919-261b4be98cf6";
  const btnJoinBgPressed = "https://www.figma.com/api/mcp/asset/3f671ead-58cc-4948-91db-506208a437ac";
  const btnJoinInnerDefault = "https://www.figma.com/api/mcp/asset/c9f58314-5795-4b8e-811a-78ea17e91dba";
  const btnJoinInnerHover = "https://www.figma.com/api/mcp/asset/35cab2c3-ba92-4a5a-9046-45edf4ae1324";
  const btnJoinInnerPressed = "https://www.figma.com/api/mcp/asset/3e5a21ea-e1ef-44be-b7b8-fde769141a2e";
  const btnChoiceBgDefault = "https://www.figma.com/api/mcp/asset/6453163f-cd60-432a-a6e2-176048f77316";
  const btnChoiceBgHover = "https://www.figma.com/api/mcp/asset/c188fb26-c7bb-48ce-90b4-1e7849fd833f";
  const btnChoiceBgPressed = "https://www.figma.com/api/mcp/asset/3f244a8f-87f1-48bc-a341-b9520e9399d3";
  const btnChoiceInnerDefault = "https://www.figma.com/api/mcp/asset/c591efb5-addc-4a84-b7d4-8e0d06cf82b0";
  const btnChoiceInnerHover = "https://www.figma.com/api/mcp/asset/01e5ee40-729d-486e-acc4-8cf65629d1f2";
  const btnChoiceInnerPressed = "https://www.figma.com/api/mcp/asset/6fc7b7ac-05ba-42bb-a316-13a53026c8ea";

  // TODO: sostituisci con la tua immagine hero finale (testo + foto già inclusi)
  const heroPlaceholder =
    "data:image/svg+xml;utf8," +
    encodeURIComponent(
      `<svg xmlns="http://www.w3.org/2000/svg" width="1600" height="900" viewBox="0 0 1600 900"><rect width="1600" height="900" fill="#f7f2e7"/><rect x="20" y="20" width="1560" height="860" rx="20" fill="none" stroke="#637c94" stroke-width="4" stroke-dasharray="18 12"/><text x="80" y="170" fill="#31496a" font-family="Arial, sans-serif" font-size="56" font-weight="700">HERO PLACEHOLDER</text><text x="80" y="250" fill="#31496a" font-family="Arial, sans-serif" font-size="32">Sostituisci questo blocco con la tua immagine finale.</text></svg>`
    );

  const sidePhotoSrc = "https://www.figma.com/api/mcp/asset/41acd5c2-c28f-4573-8314-c0acc9631ff2";
  const galleryLeftSrc = "https://www.figma.com/api/mcp/asset/3f39706a-a6dc-4635-863f-af3a20913103";
  const galleryCenterSrc = "https://www.figma.com/api/mcp/asset/18a31394-a03e-4937-8a14-be20c51d0df9";
  const galleryRightSrc = "https://www.figma.com/api/mcp/asset/7737048f-6d92-403d-9585-980c0c4a4724";
  const videoSrc = "/videos/Kam-video.mp4";
  
  // Gallery images - Story tab
  const storyLeftSrc = "https://www.figma.com/api/mcp/asset/4a8e436b-f335-4f4c-aa16-842fc9b78a2e"; // kamd2 1
  const storyRightSrc = "https://www.figma.com/api/mcp/asset/fdd3904f-bb67-4e0e-aec2-cd06a9da4fce"; // FUTURE 1
  
  // Gallery images - Now tab
  const nowLeftSrc = "https://www.figma.com/api/mcp/asset/578b4370-ef7d-411d-8870-d8360b4d5928"; // kam3a 1
  const nowCenterSrc = "https://www.figma.com/api/mcp/asset/633f1f22-d5ec-4d83-8d79-7804e8e2f346"; // victo 1
  const nowRightSrc = "https://www.figma.com/api/mcp/asset/4c217699-643e-4cde-b090-1e808dc8ef87"; // kam3c 1
  
  // Gallery images - Soon tab
  const soonLeftSrc = "https://www.figma.com/api/mcp/asset/82e6802e-c86f-411d-a2f1-b9506e41e2cb"; // kam3b 1
  
  // Gallery state
  let activeGallery = 'story';
  
  const galleryImages = {
    story: { left: storyLeftSrc, center: galleryCenterSrc, right: storyRightSrc },
    now: { left: nowLeftSrc, center: nowCenterSrc, right: nowRightSrc },
    soon: { left: soonLeftSrc, center: galleryCenterSrc, right: galleryRightSrc }
  };
  
  $: currentImages = galleryImages[activeGallery];
  
  function setGallery(tab) {
    activeGallery = tab;
  }
</script>

<main class="page">
  <header class="header">
    <img class="logo" src={logoSrc} alt="Logo" />
  </header>

  <section class="hero">
    <!-- Sostituisci questa immagine placeholder con la tua hero finale -->
    <img class="hero-image" src={heroPlaceholder} alt="Hero placeholder" />
  </section>

  <section class="split-band">
    <div class="split-section">
      <div class="split-text">
        <h2>Fighting for the America We Love.</h2>
        <p class="split-quote">Freedom is not a state; it is an act.</p>
        <p class="split-para-spacer">
          We are a nation of joyful warriors, and in 2028, we choose hope over fear, unity over
          division, and the relentless pursuit of justice for all.
        </p>
        <button class="figma-btn figma-btn--join" type="button" aria-label="Join the Fight">
          <img class="figma-btn-bg state-default" src={btnJoinBgDefault} alt="" />
          <img class="figma-btn-bg state-hover" src={btnJoinBgHover} alt="" />
          <img class="figma-btn-bg state-pressed" src={btnJoinBgPressed} alt="" />
          <img class="figma-btn-inner state-default" src={btnJoinInnerDefault} alt="" />
          <img class="figma-btn-inner state-hover" src={btnJoinInnerHover} alt="" />
          <img class="figma-btn-inner state-pressed" src={btnJoinInnerPressed} alt="" />
          <span>Join the Fight</span>
        </button>
      </div>
      <div class="split-photo-wrap">
        <img class="split-photo" src={sidePhotoSrc} alt="Foto sezione" />
      </div>
    </div>
  </section>

  <section class="gallery-section">
    <div class="gallery-title">
      <span class="gallery-title-part gallery-title-kamalas">Kamala's</span>
      <span class="gallery-title-part gallery-title-legacy">LEGACY</span>
      <span class="gallery-title-part gallery-title-inthe">in the</span>
      <span class="gallery-title-part gallery-title-making">MAKING</span>
    </div>
    <div class="gallery-grid">
      <figure class="gallery-item gallery-item--side">
        <img src={currentImages.left} alt="Galleria sinistra" />
      </figure>
      <figure class="gallery-item gallery-item--center">
        <img src={currentImages.center} alt="Galleria centrale" />
      </figure>
      <figure class="gallery-item gallery-item--side">
        <img src={currentImages.right} alt="Galleria destra" />
      </figure>
    </div>
    <div class="gallery-buttons">
      <button class="figma-btn figma-btn--choice {activeGallery === 'story' ? 'active' : ''}" type="button" aria-label="Story" on:click={() => setGallery('story')}>
        <img class="figma-btn-bg state-default" src={btnChoiceBgDefault} alt="" />
        <img class="figma-btn-bg state-hover" src={btnChoiceBgHover} alt="" />
        <img class="figma-btn-bg state-pressed" src={btnChoiceBgPressed} alt="" />
        <img class="figma-btn-inner state-default" src={btnChoiceInnerDefault} alt="" />
        <img class="figma-btn-inner state-hover" src={btnChoiceInnerHover} alt="" />
        <img class="figma-btn-inner state-pressed" src={btnChoiceInnerPressed} alt="" />
        <span>STORY</span>
      </button>
      <button class="figma-btn figma-btn--choice {activeGallery === 'now' ? 'active' : ''}" type="button" aria-label="Now" on:click={() => setGallery('now')}>
        <img class="figma-btn-bg state-default" src={btnChoiceBgDefault} alt="" />
        <img class="figma-btn-bg state-hover" src={btnChoiceBgHover} alt="" />
        <img class="figma-btn-bg state-pressed" src={btnChoiceBgPressed} alt="" />
        <img class="figma-btn-inner state-default" src={btnChoiceInnerDefault} alt="" />
        <img class="figma-btn-inner state-hover" src={btnChoiceInnerHover} alt="" />
        <img class="figma-btn-inner state-pressed" src={btnChoiceInnerPressed} alt="" />
        <span>NOW</span>
      </button>
      <button class="figma-btn figma-btn--choice {activeGallery === 'soon' ? 'active' : ''}" type="button" aria-label="Soon" on:click={() => setGallery('soon')}>
        <img class="figma-btn-bg state-default" src={btnChoiceBgDefault} alt="" />
        <img class="figma-btn-bg state-hover" src={btnChoiceBgHover} alt="" />
        <img class="figma-btn-bg state-pressed" src={btnChoiceBgPressed} alt="" />
        <img class="figma-btn-inner state-default" src={btnChoiceInnerDefault} alt="" />
        <img class="figma-btn-inner state-hover" src={btnChoiceInnerHover} alt="" />
        <img class="figma-btn-inner state-pressed" src={btnChoiceInnerPressed} alt="" />
        <span>SOON</span>
      </button>
    </div>
  </section>

  <video autoplay muted loop class="video-section">
    {#if videoSrc}
      <source src={videoSrc} type="video/mp4" />
    {/if}
    Il tuo browser non supporta il tag video.
  </video>

  <footer class="footer">
    <img src={footerLogoSrc} alt="Politecnico Milano" />
  </footer>
</main>

<style>
  .page {
    width: 100%;
    max-width: 1512px;
    margin: 0 auto;
    padding: 40px 39px 96px;
    background: var(--background-primary);
    box-sizing: border-box;
  }
  .header { margin-bottom: 28px; }
  .logo { width: 145px; height: 45px; object-fit: contain; display: block; }
  .hero { margin-bottom: 56px; }
  .hero-image {
    width: 100%;
    height: auto;
    min-height: 420px;
    display: block;
    border-radius: 12px;
    object-fit: contain;
  }

  .split-band {
    width: 100vw;
    margin-left: calc(50% - 50vw);
    margin-right: calc(50% - 50vw);
    background: var(--brand-700);
    margin-bottom: 80px;
  }
  .split-section {
    max-width: 1512px;
    margin: 0 auto;
    padding: 56px 39px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 56px;
    align-items: center;
  }
  .split-text h2 {
    margin: 0 0 20px;
    color: #fff;
    font-family: "Mrs Eaves XL Serif OT", var(--font-primary), serif;
    font-size: 64px;
    font-style: italic;
    font-weight: 700;
    line-height: 1;
  }
  .split-quote {
    margin: 0 0 40px;
    color: #fff;
    font-family: "Mrs Eaves", var(--font-primary), serif;
    font-size: 40px;
    font-style: normal;
    font-variant: small-caps;
    letter-spacing: 0.02em;
    line-height: 1.2;
  }
  .split-text p {
    margin: 0;
    color: #fff;
    font-family: "Mrs Eaves XL Serif OT", var(--font-primary), serif;
    font-size: 32px;
    font-style: normal;
    font-weight: 400;
    line-height: 1.3;
  }
  .split-para-spacer {
    margin-bottom: 32px !important;
  }
  .split-photo-wrap { display: flex; justify-content: center; }
  .split-photo {
    width: 100%;
    max-width: 692px;
    height: auto;
    display: block;
    border-radius: 12px;
    object-fit: contain;
  }

  .figma-btn {
    position: relative;
    width: 216px;
    height: 65px;
    border: 0;
    background: transparent;
    padding: 0;
    cursor: pointer;
    transition: transform 0.12s ease;
  }
  .figma-btn-bg {
    position: absolute;
    inset: 0;
    width: 216px;
    height: 65px;
    pointer-events: none;
    opacity: 0;
    transition: opacity 0.12s ease;
  }
  .figma-btn-inner {
    position: absolute;
    left: 11px;
    top: 8px;
    width: 212px;
    height: 63px;
    pointer-events: none;
    opacity: 0;
    transition: opacity 0.12s ease;
  }
  .figma-btn .state-default {
    opacity: 1;
  }
  .figma-btn span {
    position: absolute;
    top: 17px;
    left: 0;
    right: 0;
    z-index: 1;
    font-family: "Mrs Eaves XL Serif OT", var(--font-primary), serif;
    font-size: 32px;
    font-style: italic;
    font-weight: 800;
    line-height: 1;
    color: #ffffff;
    text-align: center;
    transition: color 0.12s ease;
  }
  .figma-btn--join {
    margin-top: 28px;
  }
  .figma-btn--join span {
    color: var(--brand-500);
    left: 0;
    right: 0;
    text-align: center;
    font-size: 32px;
  }
  .figma-btn:hover {
    transform: translateY(-1px);
  }
  .figma-btn:active {
    transform: translateY(0);
  }
  .figma-btn:hover .state-default,
  .figma-btn:hover .state-pressed,
  .figma-btn:active .state-default,
  .figma-btn:active .state-hover {
    opacity: 0;
  }
  .figma-btn:hover .state-hover {
    opacity: 1;
  }
  .figma-btn:active .state-pressed {
    opacity: 1;
  }
  .figma-btn--join:hover span,
  .figma-btn--join:active span {
    color: #ffffff;
  }
  .figma-btn:focus-visible {
    outline: 2px solid #ffffff;
    outline-offset: 2px;
  }

  .gallery-grid {
    max-width: 1512px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 0.8fr 1.6fr 0.8fr;
    gap: 42px;
    align-items: end;
  }
  .gallery-item {
    margin: 0;
    width: 100%;
    border-radius: 12px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .gallery-item--side { aspect-ratio: 4 / 5; }
  .gallery-item--center { aspect-ratio: 3 / 2; }
  .gallery-item img {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: contain;
    transition: transform 0.3s ease;
  }
  .gallery-item:hover img {
    transform: scale(1.05);
  }

  .gallery-section {
    width: 100vw;
    margin-left: calc(50% - 50vw);
    margin-right: calc(50% - 50vw);
    background: var(--background-primary);
    padding: 80px 39px;
    margin-bottom: 0;
  }

  .gallery-title {
    max-width: 1512px;
    margin: 0 auto 56px;
    text-align: center;
    line-height: 1.1;
  }
  .gallery-title-part {
    font-style: italic;
    font-weight: 700;
  }
  .gallery-title-kamalas {
    font-family: "Mrs Eaves XL Serif OT", var(--font-primary), serif;
    font-size: 64px;
    color: var(--brand-500);
    display: block;
    margin-bottom: 0;
  }
  .gallery-title-legacy {
    font-family: "Mr Eaves XL San OT", var(--font-primary), sans-serif;
    font-size: 128px;
    color: var(--brand-900);
    font-weight: 800;
    display: inline-block;
    line-height: 1;
    margin-right: 12px;
  }
  .gallery-title-inthe {
    font-family: "Mrs Eaves XL Serif OT", var(--font-primary), serif;
    font-size: 64px;
    color: var(--brand-500);
    display: inline-block;
    margin: 0 12px 0 0;
  }
  .gallery-title-making {
    font-family: "Mr Eaves XL San OT", var(--font-primary), sans-serif;
    font-size: 128px;
    color: var(--brand-800);
    font-weight: 800;
    display: inline-block;
    line-height: 1;
  }

  .gallery-buttons {
    max-width: 1512px;
    margin: 80px auto 0;
    display: flex;
    justify-content: center;
    gap: 116px;
  }

  .video-section {
    width: 100vw;
    margin-left: calc(50% - 50vw);
    margin-right: calc(50% - 50vw);
    margin-bottom: 80px;
    display: block;
    border: 0;
    padding: 0;
    background: transparent;
  }

  .footer {
    width: 100vw;
    margin-left: calc(50% - 50vw);
    margin-right: calc(50% - 50vw);
    height: 158px;
    background: var(--brand-700);
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .footer img {
    width: 201px;
    height: 78px;
    object-fit: contain;
    display: block;
  }
</style>
