/* ============================================================
   ELITE EVENT MANAGEMENT & DECOR
   Premium CSS — Gold, Ivory & Deep Charcoal Aesthetic
   ============================================================ */

/* ---- RESET & VARIABLES ---- */
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

:root {
  --gold: #C9A84C;
  --gold-light: #E8C96B;
  --gold-dark: #9E7A2A;
  --ivory: #FAF7F2;
  --cream: #F4EFE5;
  --charcoal: #1A1714;
  --charcoal-mid: #2D2924;
  --warm-white: #FFFEF9;
  --text-dark: #1A1714;
  --text-mid: #4A4540;
  --text-light: #7A736C;
  --text-inv: #FAF7F2;
  --radius: 12px;
  --radius-lg: 20px;
  --shadow: 0 4px 24px rgba(26,23,20,0.10);
  --shadow-lg: 0 12px 48px rgba(26,23,20,0.16);
  --transition: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  --font-display: 'Cormorant Garamond', Georgia, serif;
  --font-body: 'Jost', system-ui, sans-serif;
}

html { scroll-behavior: smooth; font-size: 16px; }

body {
  font-family: var(--font-body);
  color: var(--text-dark);
  background: var(--warm-white);
  line-height: 1.7;
  overflow-x: hidden;
}

img { max-width: 100%; height: auto; display: block; }
a { color: inherit; text-decoration: none; }
ul { list-style: none; }
button { cursor: pointer; border: none; background: none; font-family: var(--font-body); }

/* ---- UTILITIES ---- */
.container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }
.section-pad { padding: 96px 0; }
.bg-cream { background: var(--cream); }
.bg-dark { background: var(--charcoal); }
.center-btn { text-align: center; margin-top: 48px; }

.section-tag {
  font-family: var(--font-body);
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 12px;
  display: block;
}

.section-title {
  font-family: var(--font-display);
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 400;
  line-height: 1.15;
  color: var(--text-dark);
  margin-bottom: 20px;
}

.section-title em {
  font-style: italic;
  color: var(--gold-dark);
}

.section-sub {
  font-size: 1.05rem;
  color: var(--text-mid);
  max-width: 600px;
}

.section-header {
  text-align: center;
  margin-bottom: 56px;
}

.section-header .section-sub { margin: 0 auto; }

.body-text {
  font-size: 1rem;
  color: var(--text-mid);
  margin-bottom: 20px;
  line-height: 1.8;
}

/* ---- BUTTONS ---- */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 14px 32px;
  border-radius: 4px;
  font-family: var(--font-body);
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  transition: var(--transition);
  cursor: pointer;
}

.btn-primary {
  background: var(--gold);
  color: var(--charcoal);
  border: 2px solid var(--gold);
}
.btn-primary:hover {
  background: var(--gold-dark);
  border-color: var(--gold-dark);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(201,168,76,0.35);
}

.btn-outline {
  background: transparent;
  color: var(--gold);
  border: 2px solid var(--gold);
}
.btn-outline:hover {
  background: var(--gold);
  color: var(--charcoal);
  transform: translateY(-2px);
}

.btn-ghost {
  background: transparent;
  color: var(--ivory);
  border: 2px solid rgba(250,247,242,0.4);
}
.btn-ghost:hover {
  background: rgba(250,247,242,0.1);
  border-color: var(--ivory);
}

.btn-lg { padding: 18px 40px; font-size: 0.9rem; }
.btn-full { width: 100%; justify-content: center; }

/* ---- ANIMATIONS ---- */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(32px); }
  to   { opacity: 1; transform: translateY(0); }
}
@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}
@keyframes scrollPulse {
  0%, 100% { transform: scaleY(1); opacity: 1; }
  50%       { transform: scaleY(0.4); opacity: 0.4; }
}
@keyframes stripScroll {
  from { transform: translateX(0); }
  to   { transform: translateX(-50%); }
}

.animate-up { opacity: 0; animation: fadeUp 0.7s ease forwards; }
.delay-1 { animation-delay: 0.1s; }
.delay-2 { animation-delay: 0.25s; }
.delay-3 { animation-delay: 0.4s; }
.delay-4 { animation-delay: 0.55s; }
.delay-5 { animation-delay: 0.7s; }

/* ---- NAVBAR ---- */
.navbar {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 1000;
  transition: background 0.4s, box-shadow 0.4s, padding 0.4s;
  padding: 20px 0;
}

.navbar.scrolled {
  background: rgba(26,23,20,0.97);
  backdrop-filter: blur(16px);
  box-shadow: 0 2px 24px rgba(0,0,0,0.3);
  padding: 12px 0;
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 12px;
  text-decoration: none;
}

.logo-e {
  width: 40px; height: 40px;
  background: var(--gold);
  color: var(--charcoal);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: var(--font-display);
  font-size: 1.4rem;
  font-weight: 600;
  border-radius: 50%;
  flex-shrink: 0;
}

.logo-text {
  display: flex;
  flex-direction: column;
  line-height: 1.2;
}

.logo-main {
  font-family: var(--font-display);
  font-size: 1.1rem;
  font-weight: 600;
  letter-spacing: 0.15em;
  color: var(--ivory);
}

.logo-sub {
  font-size: 0.62rem;
  letter-spacing: 0.08em;
  color: var(--gold);
  text-transform: uppercase;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 8px;
}

.nav-links a {
  font-size: 0.8rem;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: rgba(250,247,242,0.85);
  padding: 8px 16px;
  border-radius: 4px;
  transition: var(--transition);
}

.nav-links a:hover,
.nav-links a.active {
  color: var(--gold);
}

.nav-links .nav-cta {
  background: var(--gold);
  color: var(--charcoal) !important;
  padding: 10px 22px;
  border-radius: 4px;
  font-weight: 600;
}

.nav-links .nav-cta:hover {
  background: var(--gold-dark);
  color: var(--charcoal) !important;
}

.hamburger {
  display: none;
  flex-direction: column;
  gap: 5px;
  padding: 4px;
}

.hamburger span {
  display: block;
  width: 24px;
  height: 2px;
  background: var(--ivory);
  border-radius: 2px;
  transition: var(--transition);
}

.hamburger.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
.hamburger.open span:nth-child(2) { opacity: 0; }
.hamburger.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

/* ---- HERO ---- */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  overflow: hidden;
  background: var(--charcoal);
  padding: 120px 0 80px;
}

.hero-bg {
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.hero-orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px);
  opacity: 0.18;
}

.hero-orb-1 {
  width: 600px; height: 600px;
  background: var(--gold);
  top: -200px; right: -100px;
}

.hero-orb-2 {
  width: 400px; height: 400px;
  background: #8B4513;
  bottom: -100px; left: -100px;
}

.hero-orb-3 {
  width: 300px; height: 300px;
  background: var(--gold-light);
  top: 50%; left: 40%;
  transform: translate(-50%, -50%);
}

.hero-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
  position: relative;
  z-index: 1;
}

.hero-eyebrow {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.25em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 20px;
}

.hero-title {
  font-family: var(--font-display);
  font-size: clamp(2.8rem, 6vw, 5.5rem);
  font-weight: 300;
  line-height: 1.1;
  color: var(--ivory);
  margin-bottom: 28px;
  max-width: 780px;
}

.hero-title em {
  font-style: italic;
  color: var(--gold);
}

.hero-desc {
  font-size: clamp(1rem, 1.5vw, 1.15rem);
  color: rgba(250,247,242,0.75);
  max-width: 540px;
  margin-bottom: 44px;
  line-height: 1.8;
}

.hero-actions {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
  margin-bottom: 72px;
}

.hero-stats {
  display: flex;
  align-items: center;
  gap: 32px;
  flex-wrap: wrap;
}

.stat { text-align: center; }

.stat-num {
  display: block;
  font-family: var(--font-display);
  font-size: 2rem;
  font-weight: 600;
  color: var(--gold);
  line-height: 1;
}

.stat-label {
  font-size: 0.72rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: rgba(250,247,242,0.55);
}

.stat-divider {
  width: 1px;
  height: 40px;
  background: rgba(201,168,76,0.3);
}

.hero-scroll {
  position: absolute;
  bottom: 32px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  z-index: 1;
}

.hero-scroll span {
  font-size: 0.65rem;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: rgba(250,247,242,0.4);
}

.scroll-line {
  width: 1px;
  height: 48px;
  background: linear-gradient(to bottom, var(--gold), transparent);
  animation: scrollPulse 2s ease-in-out infinite;
}

/* ---- INTRO STRIP ---- */
.intro-strip {
  background: var(--gold);
  padding: 14px 0;
  overflow: hidden;
}

.strip-container {
  display: flex;
  gap: 32px;
  white-space: nowrap;
  animation: stripScroll 20s linear infinite;
  width: max-content;
}

.strip-container span {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--charcoal);
}

.strip-container .dot {
  font-size: 0.5rem;
  opacity: 0.6;
}

/* ---- ABOUT TEASER ---- */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}

.about-images {
  position: relative;
  height: 500px;
}

.img-frame {
  position: absolute;
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-lg);
}

.img-frame img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.6s ease;
}

.img-frame:hover img { transform: scale(1.04); }

.img-frame-1 {
  width: 68%;
  height: 380px;
  top: 0; left: 0;
}

.img-frame-2 {
  width: 52%;
  height: 280px;
  bottom: 0; right: 0;
  border: 4px solid var(--warm-white);
}

.about-badge {
  position: absolute;
  top: 50%;
  left: 60%;
  transform: translate(-50%, -50%);
  background: var(--gold);
  color: var(--charcoal);
  border-radius: 50%;
  width: 80px;
  height: 80px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 20px rgba(201,168,76,0.5);
  z-index: 2;
}

.badge-num {
  font-family: var(--font-display);
  font-size: 1.1rem;
  font-weight: 700;
  line-height: 1;
}

.badge-text {
  font-size: 0.55rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-align: center;
}

.about-copy { padding-left: 24px; }
.about-copy .btn { margin-top: 12px; }

/* ---- SERVICES GRID ---- */
.services-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.service-card {
  background: var(--warm-white);
  border: 1px solid rgba(201,168,76,0.15);
  border-radius: var(--radius-lg);
  padding: 36px 28px;
  position: relative;
  transition: var(--transition);
  overflow: hidden;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: linear-gradient(to right, var(--gold), var(--gold-light));
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.4s ease;
}

.service-card:hover::before { transform: scaleX(1); }

.service-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
}

.service-card.featured {
  background: var(--charcoal);
  border-color: var(--gold);
}

.service-card.featured h3,
.service-card.featured p,
.service-card.featured .service-price { color: var(--ivory); }

.service-card.featured .service-link { color: var(--gold); }

.featured-tag {
  position: absolute;
  top: 16px; right: 16px;
  background: var(--gold);
  color: var(--charcoal);
  font-size: 0.65rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 4px 10px;
  border-radius: 20px;
}

.service-icon {
  font-size: 2rem;
  margin-bottom: 16px;
}

.service-card h3 {
  font-family: var(--font-display);
  font-size: 1.35rem;
  font-weight: 500;
  margin-bottom: 12px;
  color: var(--text-dark);
}

.service-card p {
  font-size: 0.92rem;
  color: var(--text-mid);
  margin-bottom: 16px;
  line-height: 1.7;
}

.service-price {
  font-size: 0.85rem;
  color: var(--text-mid);
  margin-bottom: 20px;
}

.service-price strong {
  font-size: 1.1rem;
  color: var(--gold-dark);
  font-weight: 700;
}

.service-link {
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  color: var(--gold-dark);
  transition: color 0.2s;
}

.service-link:hover { color: var(--gold); }

/* ---- GALLERY MASONRY (Home) ---- */
.gallery-masonry {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: auto auto;
  gap: 16px;
}

.gal-item {
  position: relative;
  overflow: hidden;
  border-radius: var(--radius);
  background: var(--cream);
  cursor: pointer;
}

.gal-item img {
  width: 100%;
  height: 280px;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.gal-item.gal-tall img { height: 400px; }
.gal-item.gal-wide { grid-column: span 2; }
.gal-item.gal-wide img { height: 280px; }

.gal-item:hover img { transform: scale(1.06); }

.gal-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(26,23,20,0.85) 0%, transparent 60%);
  display: flex;
  align-items: flex-end;
  padding: 20px;
  opacity: 0;
  transition: opacity 0.3s;
}

.gal-item:hover .gal-overlay { opacity: 1; }

.gal-overlay span {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--gold);
  background: rgba(26,23,20,0.6);
  padding: 4px 12px;
  border-radius: 20px;
  border: 1px solid rgba(201,168,76,0.4);
}

/* ---- REVIEWS ---- */
.reviews-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.review-card {
  background: rgba(250,247,242,0.06);
  border: 1px solid rgba(201,168,76,0.2);
  border-radius: var(--radius-lg);
  padding: 32px;
  transition: var(--transition);
}

.review-card:hover {
  background: rgba(201,168,76,0.06);
  border-color: rgba(201,168,76,0.4);
  transform: translateY(-4px);
}

.review-card.featured-review {
  background: rgba(201,168,76,0.08);
  border-color: var(--gold);
}

.review-stars {
  color: var(--gold);
  font-size: 1.1rem;
  letter-spacing: 2px;
  margin-bottom: 16px;
}

.review-text {
  font-family: var(--font-display);
  font-size: 1.05rem;
  font-style: italic;
  color: rgba(250,247,242,0.9);
  line-height: 1.7;
  margin-bottom: 24px;
}

.review-author {
  display: flex;
  align-items: center;
  gap: 12px;
}

.review-avatar {
  width: 40px; height: 40px;
  background: var(--gold);
  color: var(--charcoal);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.75rem;
  font-weight: 700;
  flex-shrink: 0;
}

.review-author strong {
  display: block;
  font-size: 0.9rem;
  color: var(--ivory);
  margin-bottom: 2px;
}

.review-author span {
  font-size: 0.75rem;
  color: rgba(250,247,242,0.5);
}

/* ---- CTA BAND ---- */
.cta-band {
  background: linear-gradient(135deg, var(--charcoal-mid) 0%, var(--charcoal) 100%);
  padding: 80px 0;
  border-top: 1px solid rgba(201,168,76,0.2);
  border-bottom: 1px solid rgba(201,168,76,0.2);
}

.cta-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 48px;
  flex-wrap: wrap;
}

.cta-text h2 {
  font-family: var(--font-display);
  font-size: clamp(1.6rem, 3vw, 2.4rem);
  font-weight: 400;
  color: var(--ivory);
  margin-bottom: 8px;
}

.cta-text p {
  font-size: 1rem;
  color: rgba(250,247,242,0.65);
}

.cta-actions {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
  flex-shrink: 0;
}

/* ---- PAGE HERO ---- */
.page-hero {
  padding: 160px 0 80px;
  position: relative;
  background: var(--charcoal);
  text-align: center;
  overflow: hidden;
}

.page-hero-bg {
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse at 50% 0%, rgba(201,168,76,0.12) 0%, transparent 70%);
}

.page-hero .container { position: relative; z-index: 1; }

.page-hero-title {
  font-family: var(--font-display);
  font-size: clamp(2.5rem, 5vw, 4rem);
  font-weight: 300;
  color: var(--ivory);
  margin-bottom: 16px;
}

.page-hero-title em {
  font-style: italic;
  color: var(--gold);
}

.page-hero-sub {
  font-size: 1.05rem;
  color: rgba(250,247,242,0.7);
  max-width: 540px;
  margin: 0 auto;
}

/* ---- ABOUT PAGE ---- */
.story-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}

.story-copy .section-title { margin-bottom: 28px; }

.story-img-main {
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow-lg);
}

.story-img-main img {
  width: 100%;
  object-fit: cover;
}

/* Values */
.values-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}

.value-card {
  background: var(--warm-white);
  border: 1px solid rgba(201,168,76,0.15);
  border-radius: var(--radius-lg);
  padding: 32px 24px;
  text-align: center;
  transition: var(--transition);
}

.value-card:hover {
  box-shadow: var(--shadow);
  transform: translateY(-4px);
  border-color: var(--gold);
}

.value-icon {
  font-size: 2.2rem;
  margin-bottom: 16px;
}

.value-card h3 {
  font-family: var(--font-display);
  font-size: 1.15rem;
  font-weight: 600;
  margin-bottom: 12px;
  color: var(--text-dark);
}

.value-card p {
  font-size: 0.88rem;
  color: var(--text-mid);
  line-height: 1.7;
}

/* Why Us */
.why-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}

.why-items { margin-top: 32px; }

.why-item {
  display: flex;
  gap: 16px;
  margin-bottom: 28px;
}

.why-check {
  width: 28px; height: 28px;
  background: var(--gold);
  color: var(--charcoal);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.85rem;
  font-weight: 700;
  flex-shrink: 0;
  margin-top: 2px;
}

.why-item h4 {
  font-family: var(--font-display);
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 6px;
  color: var(--text-dark);
}

.why-item p {
  font-size: 0.9rem;
  color: var(--text-mid);
}

.why-img-stack {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}

.why-img-stack img {
  border-radius: var(--radius);
  height: 260px;
  object-fit: cover;
  box-shadow: var(--shadow);
}

.why-img-stack img:first-child { margin-top: 40px; }

/* ---- SERVICES PAGE ---- */
.pricing-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  align-items: stretch;
}

.pricing-card {
  background: var(--warm-white);
  border: 1px solid rgba(201,168,76,0.2);
  border-radius: var(--radius-lg);
  padding: 40px 32px;
  position: relative;
  display: flex;
  flex-direction: column;
  transition: var(--transition);
}

.pricing-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
}

.pricing-card.featured-pricing {
  background: var(--charcoal);
  border-color: var(--gold);
  box-shadow: 0 0 0 2px var(--gold), var(--shadow-lg);
}

.pricing-card.featured-pricing .pricing-header h3,
.pricing-card.featured-pricing .pricing-price,
.pricing-card.featured-pricing .pricing-features li,
.pricing-card.featured-pricing .pricing-desc {
  color: var(--ivory);
}

.featured-ribbon {
  position: absolute;
  top: -1px; right: 24px;
  background: var(--gold);
  color: var(--charcoal);
  font-size: 0.65rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 6px 16px;
  border-radius: 0 0 8px 8px;
}

.featured-tag-gold {
  display: inline-block;
  background: var(--gold);
  color: var(--charcoal);
  font-size: 0.65rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  padding: 4px 12px;
  border-radius: 20px;
  margin-bottom: 16px;
}

.pricing-header { margin-bottom: 24px; }

.pricing-icon {
  font-size: 2.2rem;
  margin-bottom: 12px;
}

.pricing-header h3 {
  font-family: var(--font-display);
  font-size: 1.5rem;
  font-weight: 500;
  margin-bottom: 8px;
  color: var(--text-dark);
}

.pricing-price {
  display: flex;
  flex-direction: column;
  color: var(--text-mid);
}

.price-from {
  font-size: 0.75rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--gold);
}

.price-amount {
  font-family: var(--font-display);
  font-size: 2.5rem;
  font-weight: 600;
  color: var(--text-dark);
  line-height: 1.2;
}

.pricing-features {
  list-style: none;
  margin-bottom: 24px;
}

.pricing-features li {
  font-size: 0.9rem;
  color: var(--text-mid);
  padding: 8px 0;
  border-bottom: 1px solid rgba(201,168,76,0.08);
}

.pricing-desc {
  font-size: 0.88rem;
  color: var(--text-mid);
  line-height: 1.7;
  margin-bottom: 28px;
  flex: 1;
}

.pricing-card .btn { margin-top: auto; }

/* Floral Section */
.floral-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
}

.floral-card {
  background: var(--warm-white);
  border-radius: var(--radius-lg);
  overflow: hidden;
  box-shadow: var(--shadow);
  transition: var(--transition);
}

.floral-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
}

.floral-img { overflow: hidden; height: 240px; }

.floral-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.floral-card:hover .floral-img img { transform: scale(1.06); }

.floral-content { padding: 28px; }

.floral-content h3 {
  font-family: var(--font-display);
  font-size: 1.3rem;
  font-weight: 600;
  margin-bottom: 12px;
  color: var(--text-dark);
}

.floral-content p {
  font-size: 0.9rem;
  color: var(--text-mid);
  margin-bottom: 16px;
  line-height: 1.7;
}

.floral-content ul {
  margin-bottom: 24px;
}

.floral-content ul li {
  font-size: 0.85rem;
  color: var(--text-mid);
  padding: 4px 0;
}

/* Included */
.included-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
  text-align: center;
}

.included-item {
  padding: 32px 20px;
  border: 1px solid rgba(201,168,76,0.15);
  border-radius: var(--radius-lg);
  transition: var(--transition);
}

.included-item:hover {
  border-color: var(--gold);
  box-shadow: var(--shadow);
}

.included-icon {
  font-size: 2.2rem;
  margin-bottom: 16px;
}

.included-item h4 {
  font-family: var(--font-display);
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 8px;
  color: var(--text-dark);
}

.included-item p {
  font-size: 0.88rem;
  color: var(--text-mid);
  line-height: 1.7;
}

/* ---- GALLERY PAGE ---- */
.gallery-filters {
  display: flex;
  gap: 12px;
  justify-content: center;
  margin-bottom: 48px;
  flex-wrap: wrap;
}

.filter-btn {
  padding: 10px 24px;
  border: 2px solid rgba(201,168,76,0.3);
  border-radius: 40px;
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--text-mid);
  background: transparent;
  transition: var(--transition);
}

.filter-btn:hover,
.filter-btn.active {
  background: var(--gold);
  border-color: var(--gold);
  color: var(--charcoal);
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.gallery-item {
  position: relative;
  overflow: hidden;
  border-radius: var(--radius);
  background: var(--cream);
  cursor: pointer;
  aspect-ratio: 3/4;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.gallery-item:hover img { transform: scale(1.07); }

.gallery-item-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(26,23,20,0.9) 0%, transparent 50%);
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-end;
  padding: 20px;
  opacity: 0;
  transition: opacity 0.3s;
}

.gallery-item:hover .gallery-item-overlay { opacity: 1; }

.gallery-tag {
  font-size: 0.65rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--gold);
  background: rgba(26,23,20,0.5);
  padding: 3px 10px;
  border-radius: 20px;
  border: 1px solid rgba(201,168,76,0.4);
  margin-bottom: 6px;
}

.gallery-item-overlay p {
  font-size: 0.9rem;
  color: var(--ivory);
  font-family: var(--font-display);
  font-style: italic;
}

.gallery-item.hidden {
  display: none;
}

/* Lightbox */
.lightbox {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.95);
  z-index: 9999;
  display: none;
  align-items: center;
  justify-content: center;
}

.lightbox.open { display: flex; }

.lightbox-content {
  max-width: 90vw;
  max-height: 90vh;
  text-align: center;
}

.lightbox-content img {
  max-width: 100%;
  max-height: 80vh;
  object-fit: contain;
  border-radius: var(--radius);
}

#lightboxCaption {
  color: rgba(250,247,242,0.7);
  font-size: 0.9rem;
  margin-top: 12px;
  font-family: var(--font-display);
  font-style: italic;
}

.lightbox-close,
.lightbox-prev,
.lightbox-next {
  position: absolute;
  background: rgba(201,168,76,0.2);
  border: 1px solid rgba(201,168,76,0.4);
  color: var(--ivory);
  font-size: 1.5rem;
  width: 48px; height: 48px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: var(--transition);
  cursor: pointer;
}

.lightbox-close:hover,
.lightbox-prev:hover,
.lightbox-next:hover {
  background: var(--gold);
  color: var(--charcoal);
}

.lightbox-close { top: 24px; right: 24px; }
.lightbox-prev { left: 24px; top: 50%; transform: translateY(-50%); }
.lightbox-next { right: 24px; top: 50%; transform: translateY(-50%); }

/* ---- CONTACT PAGE ---- */
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1.4fr;
  gap: 64px;
  align-items: start;
}

.contact-info .section-title { margin-bottom: 24px; }

.contact-items {
  margin: 32px 0;
}

.contact-item {
  display: flex;
  gap: 16px;
  margin-bottom: 24px;
  padding-bottom: 24px;
  border-bottom: 1px solid rgba(201,168,76,0.1);
}

.contact-item:last-child { border-bottom: none; }

.contact-item-icon {
  font-size: 1.4rem;
  flex-shrink: 0;
  width: 40px;
}

.contact-item h4 {
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--gold-dark);
  margin-bottom: 4px;
}

.contact-item p {
  font-size: 0.95rem;
  color: var(--text-mid);
  line-height: 1.5;
}

.contact-item a {
  color: var(--text-dark);
  font-weight: 600;
  transition: color 0.2s;
}
.contact-item a:hover { color: var(--gold-dark); }

.contact-social {
  margin: 24px 0 32px;
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

.social-btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 10px 16px;
  border: 1px solid rgba(201,168,76,0.3);
  border-radius: 8px;
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--text-mid);
  transition: var(--transition);
}

.social-btn:hover {
  background: var(--gold);
  border-color: var(--gold);
  color: var(--charcoal);
}

.map-embed {
  border-radius: var(--radius);
  overflow: hidden;
  border: 1px solid rgba(201,168,76,0.2);
  margin-top: 32px;
}

/* Form */
.form-card {
  background: var(--warm-white);
  border: 1px solid rgba(201,168,76,0.2);
  border-radius: var(--radius-lg);
  padding: 48px 40px;
  box-shadow: var(--shadow);
}

.form-card h3 {
  font-family: var(--font-display);
  font-size: 1.8rem;
  font-weight: 500;
  margin-bottom: 8px;
  color: var(--text-dark);
}

.form-card > p {
  font-size: 0.9rem;
  color: var(--text-mid);
  margin-bottom: 32px;
}

.form-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

.form-group {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

.form-group label {
  font-size: 0.78rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--text-mid);
  margin-bottom: 8px;
}

.form-group input,
.form-group select,
.form-group textarea {
  padding: 14px 16px;
  border: 1.5px solid rgba(201,168,76,0.25);
  border-radius: 8px;
  font-family: var(--font-body);
  font-size: 0.95rem;
  color: var(--text-dark);
  background: var(--warm-white);
  transition: border-color 0.2s, box-shadow 0.2s;
  outline: none;
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  border-color: var(--gold);
  box-shadow: 0 0 0 3px rgba(201,168,76,0.12);
}

.form-group input.error,
.form-group select.error,
.form-group textarea.error {
  border-color: #e53e3e;
}

.form-group textarea { resize: vertical; min-height: 120px; }

.form-error {
  font-size: 0.78rem;
  color: #e53e3e;
  margin-top: 4px;
  min-height: 18px;
}

.form-note {
  font-size: 0.78rem;
  color: var(--text-light);
  text-align: center;
  margin-top: 16px;
}

.form-success {
  text-align: center;
  padding: 40px;
  background: rgba(201,168,76,0.08);
  border: 1px solid rgba(201,168,76,0.3);
  border-radius: var(--radius);
  margin-bottom: 24px;
}

.success-icon {
  width: 60px; height: 60px;
  background: var(--gold);
  color: var(--charcoal);
  border-radius: 50%;
  font-size: 1.8rem;
  font-weight: 700;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 16px;
}

.form-success h4 {
  font-family: var(--font-display);
  font-size: 1.4rem;
  margin-bottom: 8px;
  color: var(--text-dark);
}

.form-success p {
  font-size: 0.9rem;
  color: var(--text-mid);
}

/* FAQ */
.faq-grid {
  max-width: 800px;
  margin: 0 auto;
}

.faq-item {
  border-bottom: 1px solid rgba(201,168,76,0.15);
}

.faq-question {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 22px 0;
  font-family: var(--font-body);
  font-size: 1rem;
  font-weight: 600;
  color: var(--text-dark);
  cursor: pointer;
  background: none;
  text-align: left;
  transition: color 0.2s;
}

.faq-question:hover { color: var(--gold-dark); }

.faq-question span {
  font-size: 1.4rem;
  color: var(--gold);
  transition: transform 0.3s;
  flex-shrink: 0;
  margin-left: 16px;
}

.faq-question.open span { transform: rotate(45deg); }

.faq-answer {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.4s ease, padding 0.3s;
}

.faq-answer.open { max-height: 200px; padding-bottom: 20px; }

.faq-answer p {
  font-size: 0.92rem;
  color: var(--text-mid);
  line-height: 1.8;
}

/* ---- SOCIAL LINKS (footer) ---- */
.social-links {
  display: flex;
  gap: 12px;
  margin-top: 20px;
}

.social-links a {
  width: 40px; height: 40px;
  background: rgba(201,168,76,0.1);
  border: 1px solid rgba(201,168,76,0.25);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--gold);
  transition: var(--transition);
}

.social-links a:hover {
  background: var(--gold);
  color: var(--charcoal);
  border-color: var(--gold);
}

/* ---- FOOTER ---- */
.footer {
  background: var(--charcoal);
  padding: 72px 0 0;
  border-top: 1px solid rgba(201,168,76,0.15);
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.8fr 1fr 1.2fr 1.2fr;
  gap: 48px;
  margin-bottom: 48px;
}

.footer-brand .footer-logo {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 16px;
}

.footer-brand p {
  font-size: 0.88rem;
  color: rgba(250,247,242,0.55);
  line-height: 1.7;
  max-width: 280px;
}

.footer h4 {
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 20px;
}

.footer ul li {
  margin-bottom: 10px;
}

.footer ul a {
  font-size: 0.9rem;
  color: rgba(250,247,242,0.6);
  transition: color 0.2s;
}

.footer ul a:hover { color: var(--gold); }

.footer-contact p {
  font-size: 0.88rem;
  color: rgba(250,247,242,0.6);
  margin-bottom: 10px;
  line-height: 1.6;
}

.footer-contact a {
  color: var(--gold);
}

.footer-contact a:hover { color: var(--gold-light); }

.footer-bottom {
  border-top: 1px solid rgba(201,168,76,0.12);
  padding: 24px 0;
  text-align: center;
}

.footer-bottom p {
  font-size: 0.8rem;
  color: rgba(250,247,242,0.35);
  letter-spacing: 0.05em;
}

/* ---- RESPONSIVE ---- */
@media (max-width: 1024px) {
  .services-grid { grid-template-columns: repeat(2, 1fr); }
  .pricing-grid { grid-template-columns: 1fr; max-width: 520px; margin: 0 auto; }
  .floral-grid { grid-template-columns: 1fr; max-width: 600px; margin: 0 auto; }
  .values-grid { grid-template-columns: repeat(2, 1fr); }
  .included-grid { grid-template-columns: repeat(2, 1fr); }
  .footer-grid { grid-template-columns: 1fr 1fr; }
  .gallery-grid { grid-template-columns: repeat(2, 1fr); }
}

@media (max-width: 768px) {
  .section-pad { padding: 64px 0; }

  .hamburger { display: flex; }

  .nav-links {
    position: fixed;
    top: 0; right: -100%;
    width: 280px;
    height: 100vh;
    background: var(--charcoal);
    flex-direction: column;
    align-items: flex-start;
    gap: 4px;
    padding: 80px 32px 40px;
    transition: right 0.4s ease;
    box-shadow: -8px 0 40px rgba(0,0,0,0.3);
    z-index: 999;
  }

  .nav-links.open { right: 0; }

  .nav-links li { width: 100%; }
  .nav-links a { display: block; padding: 12px 0; font-size: 0.9rem; }
  .nav-links .nav-cta { display: inline-flex; margin-top: 12px; }

  .hero { min-height: 100svh; padding: 100px 0 60px; }
  .hero-title { font-size: clamp(2.2rem, 8vw, 3.5rem); }
  .hero-actions { flex-direction: column; }
  .hero-actions .btn { width: fit-content; }
  .hero-stats { gap: 20px; }

  .about-grid,
  .story-grid,
  .why-grid { grid-template-columns: 1fr; gap: 40px; }

  .about-images { height: 400px; order: -1; }
  .img-frame-1 { width: 80%; height: 320px; }
  .img-frame-2 { width: 60%; height: 240px; }

  .story-images { order: -1; }
  .about-copy { padding-left: 0; }

  .services-grid { grid-template-columns: 1fr; }

  .gallery-masonry { grid-template-columns: repeat(2, 1fr); }
  .gal-item.gal-wide { grid-column: span 2; }

  .reviews-grid { grid-template-columns: 1fr; }

  .cta-inner { flex-direction: column; text-align: center; }
  .cta-actions { justify-content: center; }

  .contact-grid { grid-template-columns: 1fr; }
  .form-row { grid-template-columns: 1fr; }
  .form-card { padding: 32px 24px; }

  .values-grid { grid-template-columns: 1fr; }
  .included-grid { grid-template-columns: 1fr 1fr; }

  .footer-grid { grid-template-columns: 1fr; gap: 32px; }

  .gallery-grid { grid-template-columns: repeat(2, 1fr); }

  .why-img-stack { grid-template-columns: 1fr; }
  .why-img-stack img:first-child { margin-top: 0; }
}

@media (max-width: 480px) {
  .gallery-grid { grid-template-columns: 1fr; }
  .gallery-masonry { grid-template-columns: 1fr; }
  .gal-item.gal-wide { grid-column: span 1; }
  .hero-stats { flex-direction: column; gap: 16px; }
  .stat-divider { width: 40px; height: 1px; }
  .included-grid { grid-template-columns: 1fr; }
  .pricing-grid { max-width: 100%; }
  .floral-grid { max-width: 100%; }
}
