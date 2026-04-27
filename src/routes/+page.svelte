<script>
  // Asset immagini dalle URL localhost (dal design context Figma)
  const imgKamalaLogo = 'http://localhost:3845/assets/afb6a61f97b5f5b0be54976114c879bf6067bf62.png';
  const imgKam = 'http://localhost:3845/assets/72e1f9b982fbd28290e25f0b17c63e7897d7822b.png';
  const imgYoung = 'http://localhost:3845/assets/a3e82c807733060694019ef8f1f226608b63c561.png';
  const imgPast2 = 'http://localhost:3845/assets/b7eaef7603bf95c4a3d019bd214bb315147653cd.png';
  const imgKamyoung = 'http://localhost:3845/assets/83ccb406512e19799cf65dfb7fb5c2b4bcb00464.png';
  const imgKamkids = 'http://localhost:3845/assets/8a8d90ef230e804408bac097d5c355c00a627478.png';
  const imgPolitecnicoBianco = 'http://localhost:3845/assets/6b9b4cf31a02e2b91a6f95a24e22d7aa4e17a35f.png';
  const imgOfficeOfKamala = 'http://localhost:3845/assets/d1e0bb7f3f31eb3f729389a837a23311f252133f.svg';
  const imgVector3 = 'http://localhost:3845/assets/00ccfde73899b54e23cc249ed9a168151b36bc86.svg';
  const imgVector4 = 'http://localhost:3845/assets/6beaa98763a0df76c328eab09624c387b69d5363.svg';
  const imgVector5 = 'http://localhost:3845/assets/a7f1045418e9214e8e981f36a1489eae7f6bf5de.svg';

  let selectedImageSet = 0;
</script>

<main class="container">
  <!-- Header -->
  <div class="header">
    <img src={imgKamalaLogo} alt="Kamala Logo" class="logo" />
  </div>

  <!-- Hero Section with WE WIN -->
  <section class="hero">
    <div class="hero-grid">
      <div class="hero-left">
        <h1 class="title-we-win">WE WIN</h1>
      </div>
      <div class="hero-right">
        <img src={imgKam} alt="Kamala" class="hero-image" />
      </div>
    </div>
    <h2 class="title-when">When</h2>
    <h2 class="title-we-fight">WE FIGHT</h2>
  </section>

  <!-- Office of Kamala -->
  <div class="office-section">
    <img src={imgOfficeOfKamala} alt="Office of Kamala D. Harris" class="office-image" />
  </div>

  <!-- Dark Section with Text and Image -->
  <section class="dark-section">
    <div class="dark-content">
      <p class="text-kamala">Kamala's</p>
      <h3 class="text-legacy">LEGACY MAKING in the</h3>
      <p class="text-body">Fighting for the America We Love.</p>
      <p class="text-small">Freedom is not a state; it is an act.</p>
      <p class="text-body">We are a nation of joyful warriors, and in 2028, we choose hope over fear, unity over division, and the relentless pursuit of justice for all.</p>
    </div>
    <img src={imgKamkids} alt="Kamala with kids" class="dark-image" />
  </section>

  <!-- Gallery Section -->
  <section class="gallery-section">
    <div class="gallery-grid">
      <img src={imgKamyoung} alt="Kamala Young" class="gallery-img" />
      <img src={imgPast2} alt="Past" class="gallery-img" />
      <img src={imgYoung} alt="Young" class="gallery-img" />
    </div>

    <div class="buttons-section">
      <button class="btn btn-primary">
        <svg class="btn-svg" viewBox="0 0 224 128">
          <image href={imgVector3} width="224" height="128" />
        </svg>
        <svg class="btn-inner" viewBox="0 0 212 63">
          <image href={imgVector4} width="212" height="63" />
        </svg>
        <span class="btn-text">Join the Fight</span>
      </button>
      <button class="btn btn-secondary">
        <svg class="btn-svg" viewBox="0 0 216 128">
          <image href={imgVector5} width="216" height="128" />
        </svg>
        <svg class="btn-inner" viewBox="0 0 212 63">
          <image href={imgVector4} width="212" height="63" />
        </svg>
        <span class="btn-text">STORY</span>
      </button>
      <button class="btn btn-secondary">
        <svg class="btn-svg" viewBox="0 0 216 128">
          <image href={imgVector5} width="216" height="128" />
        </svg>
        <svg class="btn-inner" viewBox="0 0 212 63">
          <image href={imgVector4} width="212" height="63" />
        </svg>
        <span class="btn-text">SOON</span>
      </button>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <img src={imgPolitecnicoBianco} alt="Politecnico Bianco" class="footer-logo" />
  </footer>
</main>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
    background-color: var(--background-primary);
  }

  .container {
    width: 100%;
    max-width: 1512px;
    margin: 0 auto;
    background-color: var(--background-primary);
  }

  /* Header */
  .header {
    padding: 1.5rem 4%;
  }

  .logo {
    height: 45px;
    width: auto;
  }

  /* Hero Section */
  .hero {
    padding: 2rem 4%;
    background-color: var(--background-primary);
  }

  .hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    align-items: center;
  }

  .hero-left {
    display: flex;
    align-items: center;
  }

  .title-we-win {
    font-family: var(--font-accent);
    font-size: 323px;
    font-weight: 900;
    color: var(--text-inverse);
    margin: 0;
    line-height: 1;
  }

  .hero-right {
    display: flex;
    justify-content: center;
  }

  .hero-image {
    max-width: 588px;
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 16px;
  }

  .title-when {
    font-family: var(--font-primary);
    font-size: 250px;
    font-style: italic;
    font-weight: 700;
    color: var(--brand-700);
    margin: 0;
    line-height: 1;
  }

  .title-we-fight {
    font-family: var(--font-accent);
    font-size: 128px;
    font-weight: 900;
    color: var(--text-inverse);
    margin: 0;
    line-height: 1;
  }

  /* Office Section */
  .office-section {
    padding: 2rem 4%;
    text-align: center;
  }

  .office-image {
    max-width: 1144px;
    width: 100%;
    height: auto;
  }

  /* Dark Section */
  .dark-section {
    background-color: var(--brand-700);
    padding: 3rem 4%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    align-items: center;
  }

  .dark-content {
    color: var(--text-inverse);
  }

  .text-kamala {
    font-family: var(--font-secondary);
    font-size: 64px;
    font-style: italic;
    color: var(--brand-500);
    margin: 0 0 1rem 0;
  }

  .text-legacy {
    font-family: var(--font-accent);
    font-size: 128px;
    font-style: italic;
    color: var(--brand-500);
    margin: 0 0 1rem 0;
    line-height: 1;
  }

  .text-body {
    font-family: var(--font-secondary);
    font-size: 32px;
    color: var(--text-inverse);
    margin: 1rem 0;
    line-height: 1.4;
  }

  .text-small {
    font-family: var(--font-secondary);
    font-size: 32px;
    color: var(--brand-500);
    margin: 1rem 0;
  }

  .dark-image {
    max-width: 692px;
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 16px;
  }

  /* Gallery Section */
  .gallery-section {
    padding: 3rem 4%;
    background-color: var(--background-primary);
    text-align: center;
  }

  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    margin-bottom: 3rem;
  }

  .gallery-img {
    width: 100%;
    height: 350px;
    object-fit: cover;
    border-radius: 16px;
  }

  /* Buttons */
  .buttons-section {
    display: flex;
    gap: 2rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .btn {
    position: relative;
    width: 224px;
    height: 128px;
    border: none;
    background: transparent;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0;
    overflow: hidden;
    transition: transform 0.2s;
  }

  .btn:hover {
    transform: scale(1.05);
  }

  .btn-svg {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
  }

  .btn-inner {
    position: absolute;
    width: 212px;
    height: 63px;
    top: 8px;
    left: 11px;
    z-index: 2;
  }

  .btn-text {
    position: relative;
    z-index: 3;
    font-family: var(--font-primary);
    font-size: 32px;
    font-style: italic;
    color: var(--text-inverse);
    font-weight: 700;
    text-align: center;
  }

  .btn-secondary {
    width: 216px;
  }

  /* Footer */
  .footer {
    background-color: var(--brand-700);
    padding: 3rem 4%;
    text-align: center;
  }

  .footer-logo {
    height: 78px;
    width: auto;
  }

  /* Responsive */
  @media (max-width: 1024px) {
    .hero-grid {
      grid-template-columns: 1fr;
    }

    .title-we-win {
      font-size: 200px;
    }

    .title-when {
      font-size: 150px;
    }

    .title-we-fight {
      font-size: 80px;
    }

    .dark-section {
      grid-template-columns: 1fr;
    }

    .gallery-grid {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 768px) {
    .buttons-section {
      gap: 1rem;
    }

    .btn,
    .btn-secondary {
      width: 180px;
      height: 100px;
    }

    .text-kamala {
      font-size: 48px;
    }

    .text-legacy {
      font-size: 80px;
    }

    .text-body,
    .text-small {
      font-size: 20px;
    }
  }
</style>
