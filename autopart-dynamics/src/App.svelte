<script>
  const advantages = [
    {
      title: 'Klare Struktur',
      text: 'Alle Mitarbeiter kennen ihre Aufgaben und Verantwortlichkeiten. Dadurch entstehen weniger Fehler und Missverständnisse.'
    },
    {
      title: 'Schnelle Entscheidungen',
      text: 'Die Geschäftsleitung trifft Entscheidungen direkt, ohne lange Diskussionen.'
    },
    {
      title: 'Hohe Qualitätskontrolle',
      text: 'Besonders in der Automobilindustrie sind Sicherheit und Qualität sehr wichtig.'
    },
    {
      title: 'Effiziente Prozesse',
      text: 'Standardisierte Abläufe sorgen für Stabilität und Zuverlässigkeit.'
    }
  ]

  const disadvantages = [
    {
      title: 'Wenig Kreativität',
      text: 'Mitarbeiter haben oft wenig Möglichkeiten, eigene Ideen einzubringen.'
    },
    {
      title: 'Geringe Motivation',
      text: 'Zu viel Kontrolle kann die Motivation und Zufriedenheit reduzieren.'
    },
    {
      title: 'Langsame Innovation',
      text: 'Neue Marketingstrategien oder IT-Lösungen werden langsamer umgesetzt.'
    },
    {
      title: 'Wenig Flexibilität',
      text: 'Das Unternehmen reagiert langsamer auf neue Trends und Marktveränderungen.'
    }
  ]
</script>

<svelte:head>
  <title>AutoPart Dynamics</title>
  <meta
    name="description"
    content="Marketing Präsentation über AutoPart Dynamics"
  />
</svelte:head>

<div class="page">
  <div class="background-decoration background-1"></div>
  <div class="background-decoration background-2"></div>

  <section class="hero full-width-section">
    <div class="hero-overlay"></div>

    <div class="container hero-content">
      <div class="badge">NGP-MUKB • Marketing Präsentation</div>

      <div class="hero-grid">
        <div>
          <h1>
            AutoPart
            <span>Dynamics</span>
          </h1>

          <p class="hero-text">
            AutoPart Dynamics ist ein großer Automobilzulieferer mit einem autoritären
            Führungsstil. Das Unternehmen produziert moderne Sensoren für die
            Automobilindustrie und arbeitet mit bekannten Fahrzeugherstellern zusammen.
          </p>

          <div class="hero-cards">
            <div class="info-card glass-card">
              <small>Branche</small>
              <h3>Automobilzulieferer</h3>
            </div>

            <div class="info-card glass-card">
              <small>Unternehmensgröße</small>
              <h3>Großkonzern</h3>
            </div>

            <div class="info-card glass-card">
              <small>Führungsstil</small>
              <h3 class="red">Autoritär</h3>
            </div>
          </div>
        </div>

        <div class="image-card floating-card">
          <img
            src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?q=80&w=1400&auto=format&fit=crop"
            alt="Automobilindustrie"
          />
        </div>
      </div>
    </div>
  </section>

  <section class="section white full-width-section">
    <div class="container two-columns">
      <div>
        <p class="section-label">Unternehmen</p>

        <h2>Was macht AutoPart Dynamics?</h2>

        <p>
          AutoPart Dynamics entwickelt und produziert Sensoren für moderne Fahrzeuge.
          Diese Sensoren werden zum Beispiel für Sicherheitssysteme,
          Parkassistenten oder intelligente Fahrfunktionen verwendet.
        </p>

        <p>
          Das Unternehmen arbeitet international und beliefert große
          Automobilhersteller. Deshalb sind Qualität, Zuverlässigkeit und klare
          Prozesse besonders wichtig.
        </p>

        <p>
          Durch moderne Produktionsmethoden und starke Qualitätskontrollen
          gehört AutoPart Dynamics zu den wichtigsten Partnern der Automobilindustrie.
        </p>
      </div>

      <div class="image-stack">
        <img
          src="https://images.unsplash.com/photo-1487754180451-c456f719a1fc?q=80&w=1200&auto=format&fit=crop"
          alt="Produktion"
        />

        <img
          src="https://images.unsplash.com/photo-1517048676732-d65bc937f952?q=80&w=1200&auto=format&fit=crop"
          alt="Management"
        />
      </div>
    </div>
  </section>

  <section class="section gray full-width-section">
    <div class="container">
      <p class="section-label">Analyse</p>

      <h2>Vorteile und Nachteile</h2>

      <div class="comparison-grid spaced-grid">
        <div class="comparison advantages glass-panel">
          <h3>Vorteile</h3>

          {#each advantages as item}
            <div class="comparison-item stylish-item">
              <h4>{item.title}</h4>
              <p>{item.text}</p>
            </div>
          {/each}
        </div>

        <div class="comparison disadvantages glass-panel">
          <h3>Nachteile</h3>

          {#each disadvantages as item}
            <div class="comparison-item stylish-item">
              <h4>{item.title}</h4>
              <p>{item.text}</p>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </section>

  <footer class="footer">
    <div class="footer-content">
      <div>
        <h3>AutoPart Dynamics</h3>
        <p>Marketing Präsentation • NGP-MUKB</p>
      </div>

      <div class="footer-authors">
        <p><strong>Authors:</strong></p>
        <p>Yehor Svyntsov</p>
        <p>Andrii Belaiev</p>
      </div>

      <div>
        <p><strong>School:</strong></p>
        <p>IBB</p>
      </div>
    </div>
  </footer>
</div>

<style>
  :global(body) {
    margin: 0;
    font-family: Inter, Arial, sans-serif;
    background: linear-gradient(to bottom, #f8fbff, #eef4ff);
    color: #1e293b;
  }

  * {
    box-sizing: border-box;
  }

  .page {
    width: 100%;
    overflow-x: hidden;
    position: relative;
  }

  .background-decoration {
    position: absolute;
    border-radius: 999px;
    filter: blur(80px);
    z-index: 0;
    opacity: 0.35;
  }

  .background-1 {
    width: 500px;
    height: 500px;
    background: #93c5fd;
    top: -120px;
    right: -120px;
  }

  .background-2 {
    width: 400px;
    height: 400px;
    background: #c4b5fd;
    bottom: 200px;
    left: -120px;
  }

  .full-width-section {
    width: 100%;
    position: relative;
    z-index: 2;
  }

  .container {
    width: 100%;
    max-width: 100%;
    margin: 0;
    padding: 0 6vw;
  }

  .hero {
    width: 100%;
    position: relative;
    /* background: linear-gradient(135deg, #edf5ff, #dbeafe); */
    padding: 140px 0;
  }

  .hero-overlay {
    position: absolute;
    inset: 0;
    background:
      radial-gradient(circle at top right, rgba(59, 130, 246, 0.25), transparent 35%),
      radial-gradient(circle at bottom left, rgba(168, 85, 247, 0.18), transparent 35%);
  }

  .hero-content {
    position: relative;
    z-index: 2;
  }

  .badge {
    display: inline-block;
    padding: 12px 22px;
    border-radius: 999px;
    background: rgba(255,255,255,0.75);
    backdrop-filter: blur(12px);
    color: #2563eb;
    font-weight: 700;
    margin-bottom: 32px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  }

  .hero-grid,
  .two-columns,
  .comparison-grid {
    display: grid;
    gap: 60px;
    grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
    align-items: center;
  }

  h1 {
    font-size: clamp(4rem, 8vw, 7rem);
    line-height: 0.95;
    margin-bottom: 30px;
    color: #0f172a;
    letter-spacing: -3px;
  }

  h1 span {
    color: #2563eb;
  }

  h2 {
    font-size: clamp(2.5rem, 5vw, 4rem);
    margin-bottom: 24px;
    color: #0f172a;
    line-height: 1.1;
  }

  h3 {
    font-size: 1.6rem;
  }

  p {
    font-size: 1.15rem;
    line-height: 1.9;
  }

  .hero-text {
    max-width: 750px;
  }

  .hero-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 24px;
    margin-top: 50px;
  }

  .glass-card,
  .glass-panel,
  .stylish-item {
    backdrop-filter: blur(20px);
  }

  .info-card,
  .comparison-item {
    background: rgba(255,255,255,0.75);
    border-radius: 28px;
    box-shadow: 0 20px 45px rgba(15, 23, 42, 0.08);
    padding: 28px;
    border: 1px solid rgba(255,255,255,0.5);
  }

  .info-card small {
    display: block;
    color: #64748b;
    margin-bottom: 12px;
    font-size: 0.9rem;
  }

  .red {
    color: #dc2626;
  }

  .floating-card {
    transform: rotate(2deg);
  }

  .image-card img,
  .image-stack img {
    width: 100%;
    border-radius: 32px;
    object-fit: cover;
    box-shadow: 0 25px 55px rgba(15, 23, 42, 0.18);
  }

  .image-stack {
    display: grid;
    gap: 30px;
  }

  .section {
    width: 100%;
    padding: 140px 0;
  }

  .gray {
    width: 100%;
    background: linear-gradient(to bottom, #eef4ff, #f8fbff);
  }

  .section-label {
    text-transform: uppercase;
    letter-spacing: 0.25em;
    color: #2563eb;
    font-weight: 800;
    margin-bottom: 16px;
    font-size: 0.85rem;
  }

  .comparison {
    border-radius: 40px;
    padding: 50px;
  }

  .spaced-grid {
    align-items: stretch;
    gap: 50px;
    margin-top: 40px;
  }

  .comparison-item {
    margin-top: 24px;
  }

  .comparison-item h4 {
    margin-top: 0;
    margin-bottom: 14px;
    font-size: 1.3rem;
  }

  .advantages {
    background: rgba(236, 253, 245, 0.85);
  }

  .disadvantages {
    background: rgba(254, 242, 242, 0.85);
  }

  .footer {
    width: 100%;
    background: #0f172a;
    color: white;
    padding: 60px 0;
    margin-top: 80px;
    position: relative;
    z-index: 2;
  }

  .footer-content {
    width: 100%;
    max-width: 100%;
    margin: 0;
    padding: 0 6vw;
    display: flex;
    justify-content: space-between;
    gap: 40px;
    flex-wrap: wrap;
  }

  .footer h3 {
    margin-top: 0;
    margin-bottom: 12px;
  }

  .footer p {
    margin: 6px 0;
    color: #cbd5e1;
  }

  @media (max-width: 900px) {
    .container,
    .footer-content {
      padding: 0 28px;
    }

    .hero-grid,
    .two-columns,
    .comparison-grid {
      grid-template-columns: 1fr;
    }

    .section {
      padding: 80px 0;
    }

    h1 {
      font-size: 4rem;
    }
  }
</style>
