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
  <section class="hero">
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
            <div class="info-card">
              <small>Branche</small>
              <h3>Automobilzulieferer</h3>
            </div>

            <div class="info-card">
              <small>Unternehmensgröße</small>
              <h3>Großkonzern</h3>
            </div>

            <div class="info-card">
              <small>Führungsstil</small>
              <h3 class="red">Autoritär</h3>
            </div>
          </div>
        </div>

        <div class="image-card">
          <img
            src="https://images.unsplash.com/photo-1503376780353-7e6692767b70?q=80&w=1400&auto=format&fit=crop"
            alt="Automobilindustrie"
          />
        </div>
      </div>
    </div>
  </section>

  <section class="section white">
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

  <section class="section gray">
    <div class="container">
      <p class="section-label">Analyse</p>

      <h2>Vorteile und Nachteile</h2>

      <div class="comparison-grid">
        <div class="comparison advantages">
          <h3>Vorteile</h3>

          {#each advantages as item}
            <div class="comparison-item">
              <h4>{item.title}</h4>
              <p>{item.text}</p>
            </div>
          {/each}
        </div>

        <div class="comparison disadvantages">
          <h3>Nachteile</h3>

          {#each disadvantages as item}
            <div class="comparison-item">
              <h4>{item.title}</h4>
              <p>{item.text}</p>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </section>
</div>

<style>
  :global(body) {
    margin: 0;
    font-family: Inter, Arial, sans-serif;
    background: #f4f7fb;
    color: #1e293b;
  }

  * {
    box-sizing: border-box;
  }

  .page {
    overflow-x: hidden;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 24px;
  }

  .hero {
    position: relative;
    background: linear-gradient(135deg, #edf5ff, #dbeafe);
    padding: 80px 0;
  }

  .hero-overlay {
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at top right, rgba(59, 130, 246, 0.2), transparent 40%);
  }

  .hero-content {
    position: relative;
    z-index: 2;
  }

  .badge {
    display: inline-block;
    padding: 10px 18px;
    border-radius: 999px;
    background: white;
    color: #2563eb;
    font-weight: 600;
    margin-bottom: 28px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.06);
  }

  .hero-grid,
  .two-columns,
  .comparison-grid {
    display: grid;
    gap: 40px;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  }

  h1 {
    font-size: clamp(3rem, 8vw, 5.5rem);
    line-height: 1;
    margin-bottom: 24px;
    color: #0f172a;
  }

  h1 span {
    color: #2563eb;
  }

  h2 {
    font-size: clamp(2rem, 4vw, 3.2rem);
    margin-bottom: 24px;
    color: #0f172a;
  }

  p {
    font-size: 1.1rem;
    line-height: 1.8;
  }

  .hero-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 20px;
    margin-top: 40px;
  }

  .info-card,
  .comparison-item {
    background: white;
    border-radius: 24px;
    box-shadow: 0 10px 35px rgba(15, 23, 42, 0.08);
    padding: 24px;
  }

  .red {
    color: #dc2626;
  }

  .image-card img,
  .image-stack img {
    width: 100%;
    border-radius: 28px;
    object-fit: cover;
    box-shadow: 0 15px 40px rgba(15, 23, 42, 0.15);
  }

  .image-stack {
    display: grid;
    gap: 24px;
  }

  .section {
    padding: 100px 0;
  }

  .gray {
    background: #eef2f7;
  }

  .section-label {
    text-transform: uppercase;
    letter-spacing: 0.2em;
    color: #2563eb;
    font-weight: 700;
    margin-bottom: 12px;
  }

  .comparison {
    border-radius: 32px;
    padding: 40px;
  }

  .advantages {
    background: #ecfdf5;
  }

  .disadvantages {
    background: #fef2f2;
  }

  @media (max-width: 768px) {
    .section {
      padding: 70px 0;
    }
  }
</style>
