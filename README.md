index.html.<!DOCTYPE html>
<html lang="en-CA">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Montreal Radon | Radon Testing & Mitigation in Montreal</title>
  <meta
    name="description"
    content="Montreal Radon provides radon testing and mitigation services for homes, condos, and commercial properties across Montreal and surrounding areas."
  />
  <link rel="preconnect" href="[fonts.googleapis.com](https://fonts.googleapis.com)">
  <link rel="preconnect" href="[fonts.gstatic.com](https://fonts.gstatic.com)" crossorigin>
  <link
    href="[fonts.googleapis.com](https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap)"
    rel="stylesheet"
  />
  <style>
    :root {
      --bg: #f7fafc;
      --surface: #ffffff;
      --surface-2: #edf2f7;
      --text: #14213d;
      --muted: #4a5568;
      --primary: #0f766e;
      --primary-dark: #115e59;
      --accent: #14b8a6;
      --line: #d9e2ec;
      --danger: #b91c1c;
      --success: #166534;
      --shadow: 0 10px 30px rgba(15, 23, 42, 0.08);
      --radius: 18px;
      --max: 1180px;
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: "Inter", sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }

    img {
      max-width: 100%;
      display: block;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(100% - 2rem, var(--max));
      margin: 0 auto;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      padding: 0.95rem 1.35rem;
      border-radius: 999px;
      border: 1px solid transparent;
      font-weight: 700;
      transition: 0.25s ease;
      cursor: pointer;
    }

    .btn-primary {
      background: var(--primary);
      color: white;
      box-shadow: var(--shadow);
    }

    .btn-primary:hover {
      background: var(--primary-dark);
      transform: translateY(-1px);
    }

    .btn-secondary {
      background: transparent;
      border-color: rgba(255,255,255,0.25);
      color: white;
    }

    .btn-secondary:hover {
      background: rgba(255,255,255,0.08);
    }

    .btn-light {
      background: white;
      color: var(--text);
      border-color: var(--line);
    }

    .btn-light:hover {
      transform: translateY(-1px);
      box-shadow: var(--shadow);
    }

    .site-header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(14px);
      background: rgba(247, 250, 252, 0.85);
      border-bottom: 1px solid rgba(217, 226, 236, 0.7);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      min-height: 78px;
      gap: 1rem;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 0.85rem;
      font-weight: 800;
      font-size: 1.05rem;
    }

    .brand-mark {
      width: 42px;
      height: 42px;
      border-radius: 12px;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, var(--primary), var(--accent));
      color: white;
      box-shadow: var(--shadow);
      font-weight: 800;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.2rem;
      color: var(--muted);
      font-weight: 500;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    .hero {
      position: relative;
      overflow: hidden;
      background:
        radial-gradient(circle at top left, rgba(20, 184, 166, 0.18), transparent 30%),
        linear-gradient(135deg, #0f172a, #14213d 55%, #0f766e);
      color: white;
    }

    .hero-inner {
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 2rem;
      align-items: center;
      padding: 5.5rem 0 4.5rem;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.45rem 0.8rem;
      border-radius: 999px;
      background: rgba(255,255,255,0.1);
      border: 1px solid rgba(255,255,255,0.12);
      color: #d1fae5;
      font-size: 0.92rem;
      font-weight: 600;
      margin-bottom: 1rem;
    }

    h1 {
      font-size: clamp(2.4rem, 5vw, 4.4rem);
      line-height: 1.05;
      margin: 0 0 1rem;
      letter-spacing: -0.03em;
    }

    .hero p {
      font-size: 1.08rem;
      color: rgba(255,255,255,0.86);
      max-width: 60ch;
      margin: 0 0 1.6rem;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      margin-bottom: 1.7rem;
    }

    .hero-points {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem 1.5rem;
      padding: 0;
      margin: 0;
      list-style: none;
      color: rgba(255,255,255,0.86);
      font-weight: 500;
    }

    .hero-points li::before {
      content: "• ";
      color: #5eead4;
    }

    .hero-card {
      background: rgba(255,255,255,0.08);
      border: 1px solid rgba(255,255,255,0.14);
      border-radius: 24px;
      padding: 1.25rem;
      backdrop-filter: blur(18px);
      box-shadow: var(--shadow);
    }

    .stat-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
      margin-top: 1rem;
    }

    .stat {
      background: rgba(255,255,255,0.08);
      border-radius: 18px;
      padding: 1rem;
      border: 1px solid rgba(255,255,255,0.12);
    }

    .stat strong {
      display: block;
      font-size: 1.6rem;
      margin-bottom: 0.25rem;
    }

    section {
      padding: 5rem 0;
    }

    .section-head {
      max-width: 760px;
      margin-bottom: 2rem;
    }

    .section-head h2 {
      font-size: clamp(2rem, 4vw, 3rem);
      margin: 0 0 0.75rem;
      line-height: 1.1;
      letter-spacing: -0.03em;
    }

    .section-head p {
      margin: 0;
      color: var(--muted);
      font-size: 1.05rem;
    }

    .cards-3 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.25rem;
    }

    .card {
      background: var(--surface);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 1.4rem;
      box-shadow: var(--shadow);
    }

    .card-icon {
      width: 52px;
      height: 52px;
      border-radius: 14px;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, rgba(15,118,110,0.15), rgba(20,184,166,0.15));
      color: var(--primary);
      font-size: 1.35rem;
      margin-bottom: 1rem;
    }

    .card h3 {
      margin: 0 0 0.6rem;
      font-size: 1.18rem;
    }

    .card p {
      margin: 0;
      color: var(--muted);
    }

    .alt-bg {
      background: linear-gradient(180deg, #f8fbfd, #eef6f6);
    }

    .steps {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1rem;
    }

    .step {
      background: white;
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 1.35rem;
      box-shadow: var(--shadow);
    }

    .step-number {
      width: 36px;
      height: 36px;
      border-radius: 999px;
      background: var(--primary);
      color: white;
      display: grid;
      place-items: center;
      font-weight: 700;
      margin-bottom: 0.9rem;
    }

    .split {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.5rem;
      align-items: start;
    }

    .checklist {
      list-style: none;
      padding: 0;
      margin: 1rem 0 0;
    }

    .checklist li {
      position: relative;
      padding-left: 1.6rem;
      margin-bottom: 0.9rem;
      color: var(--muted);
    }

    .checklist li::before {
      content: "✓";
      position: absolute;
      left: 0;
      top: 0;
      color: var(--success);
      font-weight: 800;
    }

    .pricing {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.25rem;
    }

    .price-card {
      background: white;
      border: 1px solid var(--line);
      border-radius: 22px;
      padding: 1.6rem;
      box-shadow: var(--shadow);
      position: relative;
    }

    .price-card.featured {
      border: 2px solid var(--primary);
      transform: translateY(-6px);
    }

    .badge {
      display: inline-block;
      padding: 0.35rem 0.7rem;
      border-radius: 999px;
      background: rgba(15,118,110,0.12);
      color: var(--primary);
      font-size: 0.84rem;
      font-weight: 700;
      margin-bottom: 1rem;
    }

    .price {
      font-size: 2.2rem;
      font-weight: 800;
      line-height: 1;
      margin-bottom: 0.35rem;
    }

    .price-note {
      color: var(--muted);
      margin-bottom: 1rem;
    }

    .testimonial-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.25rem;
    }

    .testimonial {
      background: white;
      border: 1px solid var(--line);
      border-radius: 20px;
      padding: 1.4rem;
      box-shadow: var(--shadow);
    }

    .stars {
      color: #f59e0b;
      margin-bottom: 0.85rem;
      letter-spacing: 0.08em;
    }

    .testimonial p {
      color: var(--muted);
      margin: 0 0 1rem;
    }

    .testimonial strong {
      display: block;
    }

    .coverage {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      margin-top: 1.25rem;
    }

    .coverage span {
      padding: 0.7rem 1rem;
      background: white;
      border: 1px solid var(--line);
      border-radius: 999px;
      color: var(--muted);
      font-weight: 600;
    }

    .cta {
      background: linear-gradient(135deg, #0f766e, #0f172a);
      color: white;
      border-radius: 28px;
      padding: 2rem;
      box-shadow: var(--shadow);
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 1.5rem;
      align-items: center;
    }

    .cta p {
      color: rgba(255,255,255,0.84);
      margin-bottom: 0;
    }

    .contact-card {
      background: white;
      color: var(--text);
      border-radius: 22px;
      padding: 1.4rem;
    }

    form {
      display: grid;
      gap: 0.9rem;
    }

    .field-group {
      display: grid;
      gap: 0.4rem;
    }

    label {
      font-size: 0.92rem;
      font-weight: 600;
    }

    input,
    textarea,
    select {
      width: 100%;
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 0.95rem 1rem;
      font: inherit;
      color: var(--text);
      background: white;
    }

    textarea {
      min-height: 120px;
      resize: vertical;
    }

    .footer {
      padding: 2rem 0 3rem;
      color: var(--muted);
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 1rem;
      flex-wrap: wrap;
      border-top: 1px solid var(--line);
      padding-top: 1.5rem;
    }

    .small {
      font-size: 0.92rem;
      color: var(--muted);
    }

    @media (max-width: 1024px) {
      .hero-inner,
      .split,
      .cta,
      .cards-3,
      .steps,
      .pricing,
      .testimonial-grid {
        grid-template-columns: 1fr;
      }

      .price-card.featured {
        transform: none;
      }
    }

    @media (max-width: 760px) {
      .nav {
        flex-direction: column;
        align-items: flex-start;
        padding: 0.8rem 0;
      }

      .nav-links {
        flex-wrap: wrap;
      }

      .hero-inner {
        padding: 4rem 0;
      }

      h1 {
        font-size: 2.4rem;
      }
    }
  </style>
</head>
<body>
  <header class="site-header">
    <div class="container nav">
      <a href="#top" class="brand">
        <span class="brand-mark">MR</span>
        <span>Montreal Radon</span>
      </a>

      <nav class="nav-links">
        <a href="#services">Services</a>
        <a href="#process">Process</a>
        <a href="#pricing">Pricing</a>
        <a href="#areas">Areas</a>
        <a href="#contact">Contact</a>
      </nav>

      <a class="btn btn-primary" href="tel:+15145550199">Call Now</a>
    </div>
  </header>

  <main id="top">
    <section class="hero">
      <div class="container hero-inner">
        <div>
          <div class="eyebrow">Professional radon testing and mitigation in Montreal</div>
          <h1>Protect your home from radon with fast, certified local service.</h1>
          <p>
            Montreal Radon helps homeowners, landlords, and businesses detect and reduce
            radon safely. Get clear testing, honest recommendations, and effective mitigation
            systems designed for Quebec properties.
          </p>

          <div class="hero-actions">
            <a class="btn btn-primary" href="#contact">Get a Free Estimate</a>
            <a class="btn btn-secondary" href="#services">Explore Services</a>
          </div>

          <ul class="hero-points">
            <li>Residential and commercial service</li>
            <li>Clear reporting and expert guidance</li>
            <li>Serving Montreal and surrounding areas</li>
          </ul>
        </div>

        <aside class="hero-card">
          <h3>Why homeowners act now</h3>
          <p class="small">
            Radon is a naturally occurring gas that can build up indoors without smell,
            colour, or immediate warning signs. Testing is the only way to know your level.
          </p>

          <div class="stat-grid">
            <div class="stat">
              <strong>48 hrs</strong>
              <span>Fast response for quote requests</span>
            </div>
            <div class="stat">
              <strong>1 visit</strong>
              <span>Typical on-site assessment</span>
            </div>
            <div class="stat">
              <strong>Local</strong>
              <span>Montreal-focused service</span>
            </div>
            <div class="stat">
              <strong>Trusted</strong>
              <span>Clear, straightforward recommendations</span>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <section id="services">
      <div class="container">
        <div class="section-head">
          <h2>Radon services built for peace of mind</h2>
          <p>
            From first-time testing to full mitigation systems, Montreal Radon provides
            practical solutions that help reduce risk and improve indoor air quality.
          </p>
        </div>

        <div class="cards-3">
          <article class="card">
            <div class="card-icon">01</div>
            <h3>Radon Testing</h3>
            <p>
              Short-term and long-term radon measurement for homes, condos, rental
              properties, and commercial buildings.
            </p>
          </article>

          <article class="card">
            <div class="card-icon">02</div>
            <h3>Radon Mitigation</h3>
            <p>
              Custom mitigation systems designed to reduce indoor radon levels efficiently
              and with minimal disruption to your property.
            </p>
          </article>

          <article class="card">
            <div class="card-icon">03</div>
            <h3>Property Assessments</h3>
            <p>
              Pre-purchase, post-renovation, and real estate assessments to help buyers,
              sellers, and property managers make informed decisions.
            </p>
          </article>
        </div>
      </div>
    </section>

    <section id="process" class="alt-bg">
      <div class="container">
        <div class="section-head">
          <h2>A simple 4-step process</h2>
          <p>
            The goal is straightforward: identify the issue, explain the findings clearly,
            and install the right solution if mitigation is needed.
          </p>
        </div>

        <div class="steps">
          <div class="step">
            <div class="step-number">1</div>
            <h3>Book a consultation</h3>
            <p class="small">Tell us about your property, concerns, and timeline.</p>
          </div>

          <div class="step">
            <div class="step-number">2</div>
            <h3>Test the property</h3>
            <p class="small">We assess radon levels and identify likely entry points.</p>
          </div>

          <div class="step">
            <div class="step-number">3</div>
            <h3>Review your options</h3>
            <p class="small">You receive a clear explanation and practical recommendation.</p>
          </div>

          <div class="step">
            <div class="step-number">4</div>
            <h3>Mitigate with confidence</h3>
            <p class="small">If needed, we install a system designed for durable performance.</p>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="container split">
        <div class="card">
          <h2>Why choose Montreal Radon</h2>
          <p class="small">
            People want a contractor they can trust with something serious but invisible.
            The site messaging should feel calm, professional, and evidence-based.
          </p>
          <ul class="checklist">
            <li>Local expertise for Montreal homes, basements, and building types</li>
            <li>Plain-language explanations without pressure or scare tactics</li>
            <li>Clean installation practices and respectful service</li>
            <li>Detailed reporting for homeowners, landlords, and real estate transactions</li>
            <li>Helpful support before, during, and after mitigation</li>
          </ul>
        </div>

        <div class="card">
          <h2>Who we help</h2>
          <p class="small">
            This layout supports both residential and commercial lead generation while keeping
            the page focused and easy to scan.
          </p>
          <ul class="checklist">
            <li>Homeowners concerned about basement or ground-floor radon exposure</li>
            <li>Buyers and sellers needing testing during a transaction</li>
            <li>Landlords and property managers managing tenant safety</li>
            <li>Businesses requiring indoor air quality assessments</li>
            <li>Families wanting long-term peace of mind</li>
          </ul>
        </div>
      </div>
    </section>

    <section id="pricing" class="alt-bg">
      <div class="container">
        <div class="section-head">
          <h2>Simple pricing structure</h2>
          <p>
            These are placeholder packages you can adjust to match your real pricing,
            service scope, and call-to-action strategy.
          </p>
        </div>

        <div class="pricing">
          <div class="price-card">
            <span class="badge">Testing</span>
            <div class="price">\$199</div>
            <div class="price-note">Starting price</div>
            <ul class="checklist">
              <li>Initial property consultation</li>
              <li>Residential radon test setup</li>
              <li>Clear written results</li>
            </ul>
          </div>

          <div class="price-card featured">
            <span class="badge">Most Popular</span>
            <div class="price">\$1,895</div>
            <div class="price-note">Typical mitigation system</div>
            <ul class="checklist">
              <li>On-site assessment and system design</li>
              <li>Professional mitigation installation</li>
              <li>Post-installation guidance</li>
            </ul>
          </div>

          <div class="price-card">
            <span class="badge">Commercial</span>
            <div class="price">Custom</div>
            <div class="price-note">Quoted per project</div>
            <ul class="checklist">
              <li>Multi-unit and commercial assessments</li>
              <li>Site-specific recommendations</li>
              <li>Flexible scheduling and reporting</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="container">
        <div class="section-head">
          <h2>What clients say</h2>
          <p>
            Replace these with real testimonials, Google review excerpts, or verified client
            feedback once available.
          </p>
        </div>

        <div class="testimonial-grid">
          <article class="testimonial">
            <div class="stars">★★★★★</div>
            <p>
              Professional, punctual, and easy to understand. The whole process felt clear
              from the first call to the final installation.
            </p>
            <strong>Sarah L.</strong>
            <span class="small">Montreal homeowner</span>
          </article>

          <article class="testimonial">
            <div class="stars">★★★★★</div>
            <p>
              We needed radon testing quickly during a home purchase. They explained everything
              clearly and helped us move fast.
            </p>
            <strong>David R.</strong>
            <span class="small">Home buyer</span>
          </article>

          <article class="testimonial">
            <div class="stars">★★★★★</div>
            <p>
              Clean work, respectful team, and no hard sell. The mitigation system was installed
              neatly and works exactly as promised.
            </p>
            <strong>Nadia T.</strong>
            <span class="small">Property owner</span>
          </article>
        </div>
      </div>
    </section>

    <section id="areas">
      <div class="container">
        <div class="section-head">
          <h2>Proudly serving Montreal and nearby communities</h2>
          <p>
            Add or remove service areas depending on your business footprint and local SEO
            strategy.
          </p>
        </div>

        <div class="coverage">
          <span>Montreal</span>
          <span>Laval</span>
          <span>West Island</span>
          <span>Longueuil</span>
          <span>Brossard</span>
          <span>South Shore</span>
          <span>North Shore</span>
          <span>Greater Montreal</span>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="cta">
          <div>
            <h2>Book your radon consultation today</h2>
            <p>
              If you are concerned about radon in your home or building, the next step is
              simple: get in touch and request a quote or testing appointment.
            </p>
          </div>

          <div class="contact-card">
            <form>
              <div class="field-group">
                <label for="name">Full name</label>
                <input id="name" type="text" placeholder="Your name" />
              </div>

              <div class="field-group">
                <label for="email">Email</label>
                <input id="email" type="email" placeholder="you@example.com" />
              </div>

              <div class="field-group">
                <label for="service">Service needed</label>
                <select id="service">
                  <option>Radon testing</option>
                  <option>Radon mitigation</option>
                  <option>Property assessment</option>
                  <option>Commercial inquiry</option>
                </select>
              </div>

              <div class="field-group">
                <label for="message">Tell us about your property</label>
                <textarea id="message" placeholder="Home type, location, concerns, and timing"></textarea>
              </div>

              <button class="btn btn-primary" type="submit">Request Estimate</button>
            </form>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container footer-inner">
      <div>
        <strong>Montreal Radon</strong>
        <div class="small">Radon testing and mitigation services in Montreal</div>
      </div>

      <div class="small">
        <div>Phone: (514) 555-0199</div>
        <div>Email: info@montrealradon.ca</div>
      </div>
    </div>
  </footer>
</body>
</html>
# montreal-radon
