HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 9.4 - Responsive Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <header class="site-header">
        <nav class="navbar container">
            <a href="#home" class="logo">Nova<span>.</span></a>

            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#about">About</a></li>
            </ul>

            <a href="#contact" class="nav-cta">Get Started</a>
        </nav>
    </header>

    <main>
        <!-- Hero Section -->
        <section class="hero container" id="home">
            <div class="hero-text">
                <span class="tagline">YOUR IDEAS, OUR INSPIRATION</span>

                <h1>Build Something <span>Amazing.</span></h1>

                <p>
                    Turn your ideas into reality with simple tools,
                    thoughtful design, and a better digital experience.
                    Start building something great today.
                </p>

                <div class="hero-buttons">
                    <a href="#features" class="btn btn-primary">
                        Explore Features →
                    </a>
                    <a href="#about" class="btn btn-secondary">
                        Learn More
                    </a>
                </div>

                <div class="hero-stats">
                    <div>
                        <strong>100+</strong>
                        <span>Creative Ideas</span>
                    </div>
                    <div>
                        <strong>24/7</strong>
                        <span>Always Available</span>
                    </div>
                </div>
            </div>

            <div class="hero-visual">
                <img
                    src="images/hero.jpg"
                    alt="Laptop on a modern creative workspace">
                <div class="image-label">
                    <span class="label-icon">✦</span>
                    <div>
                        <strong>Think. Create. Grow.</strong>
                        <p>Designed for your next big idea</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Features Section -->
        <section class="features section" id="features">
            <div class="container">
                <div class="section-heading">
                    <span class="tagline">WHAT WE OFFER</span>
                    <h2>Everything You Need to Get Started</h2>
                    <p>
                        Simple solutions to help you create, grow,
                        and achieve more.
                    </p>
                </div>

                <div class="feature-grid">
                    <article class="feature-card">
                        <div class="feature-icon">🎨</div>
                        <h3>Creative Design</h3>
                        <p>
                            Beautiful layouts and thoughtful details
                            for a memorable user experience.
                        </p>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon">⚡</div>
                        <h3>Fast Performance</h3>
                        <p>
                            Lightweight pages that load quickly
                            and keep your visitors engaged.
                        </p>
                    </article>

                    <article class="feature-card">
                        <div class="feature-icon">📱</div>
                        <h3>Responsive Layout</h3>
                        <p>
                            A flexible design that adapts to different
                            screen sizes and devices.
                        </p>
                    </article>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section class="about container" id="about">
            <div>
                <span class="tagline">OUR APPROACH</span>
                <h2>Simple Design. Powerful Results.</h2>
            </div>

            <p>
                We believe great websites combine clear content,
                attractive visuals, accessible navigation, and
                carefully organized layouts.
            </p>
        </section>

        <!-- Call to Action -->
        <section class="contact-section" id="contact">
            <div class="container contact-content">
                <div>
                    <h2>Ready to bring your ideas to life?</h2>
                    <p>Take the first step toward your next project.</p>
                </div>
                <a href="mailto:hello@example.com" class="btn btn-light">
                    Contact Us →
                </a>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <div class="container footer-content">
            <a href="#home" class="logo">Nova<span>.</span></a>
            <p>© 2026 Nova. Created for Assignment 9.4.</p>
        </div>
    </footer>

</body>
</html>

CSS
/* ===== 1. Global Styles ===== */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    color: #1f2937;
    background: #ffffff;
    line-height: 1.6;
}

a {
    text-decoration: none;
    color: inherit;
}

.container {
    width: min(1120px, 90%);
    margin: 0 auto;
}

:root {
    --primary: #6558e8;
    --primary-dark: #4f46c8;
    --heading: #172033;
    --text: #647084;
    --light-bg: #f7f8fc;
}

/* ===== 2. Navigation Bar ===== */
.site-header {
    background: #ffffff;
    border-bottom: 1px solid #edf0f5;
}

.navbar {
    min-height: 78px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 24px;
}

.logo {
    font-size: 29px;
    font-weight: 800;
    color: var(--heading);
    letter-spacing: -1px;
}

.logo span {
    color: var(--primary);
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 34px;
    list-style: none;
}

.nav-links a {
    color: #596477;
    font-size: 15px;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: var(--primary);
}

.nav-cta {
    background: var(--primary);
    color: #ffffff;
    padding: 11px 21px;
    border-radius: 7px;
    font-weight: 600;
    transition: background 0.3s;
}

.nav-cta:hover {
    background: var(--primary-dark);
}

/* ===== 3. Hero Section ===== */
.hero {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 65px;
    padding-top: 80px;
    padding-bottom: 85px;
}

.tagline {
    display: inline-block;
    color: var(--primary);
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 2px;
    margin-bottom: 18px;
}

.hero-text h1 {
    color: var(--heading);
    font-size: clamp(38px, 4.5vw, 57px);
    line-height: 1.12;
    letter-spacing: -2px;
    margin-bottom: 22px;
}

.hero-text h1 span {
    color: var(--primary);
}

.hero-text > p {
    color: var(--text);
    font-size: 16px;
    max-width: 490px;
    margin-bottom: 28px;
}

.hero-buttons {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 14px;
}

.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 12px 20px;
    border-radius: 7px;
    font-size: 14px;
    font-weight: 700;
    transition: background 0.3s, transform 0.3s;
}

.btn:hover {
    transform: translateY(-2px);
}

.btn-primary {
    background: var(--primary);
    color: #ffffff;
}

.btn-primary:hover {
    background: var(--primary-dark);
}

.btn-secondary {
    border: 1px solid #dce0e9;
    color: var(--heading);
}

.btn-secondary:hover {
    background: var(--light-bg);
}

/* Hero statistics using Flexbox */
.hero-stats {
    display: flex;
    gap: 45px;
    margin-top: 38px;
}

.hero-stats div {
    display: flex;
    flex-direction: column;
}

.hero-stats strong {
    font-size: 23px;
    color: var(--heading);
}

.hero-stats span {
    font-size: 13px;
    color: var(--text);
}

/* Hero Image */
.hero-visual {
    position: relative;
    min-width: 0;
}

.hero-visual > img {
    display: block;
    width: 100%;
    height: 400px;
    object-fit: cover;
    border-radius: 18px;
    background: var(--light-bg);
}

.image-label {
    position: absolute;
    bottom: 20px;
    left: 20px;
    right: 20px;
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 17px;
    background: rgba(255, 255, 255, 0.96);
    border-radius: 12px;
    box-shadow: 0 8px 25px rgba(23, 32, 51, 0.1);
}

.label-icon {
    width: 43px;
    height: 43px;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    background: #efedff;
    color: var(--primary);
    border-radius: 10px;
    font-size: 23px;
}

.image-label strong {
    color: var(--heading);
    font-size: 14px;
}

.image-label p {
    color: var(--text);
    font-size: 12px;
}

/* ===== 4. Features Section ===== */
.section {
    padding: 75px 0;
}

.features {
    background: var(--light-bg);
}

.section-heading {
    max-width: 650px;
    margin: 0 auto 42px;
    text-align: center;
}

.section-heading h2,
.about h2 {
    color: var(--heading);
    font-size: 34px;
    line-height: 1.25;
    letter-spacing: -0.7px;
    margin-bottom: 14px;
}

.section-heading > p,
.about > p {
    color: var(--text);
    font-size: 15px;
}

/* Feature Cards using CSS Grid */
.feature-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 24px;
}

.feature-card {
    background: #ffffff;
    padding: 30px;
    border: 1px solid #eceef4;
    border-radius: 13px;
    transition: transform 0.3s, box-shadow 0.3s;
}

.feature-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 30px rgba(23, 32, 51, 0.07);
}

.feature-icon {
    width: 52px;
    height: 52px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #efedff;
    border-radius: 12px;
    font-size: 25px;
    margin-bottom: 22px;
}

.feature-card h3 {
    color: var(--heading);
    font-size: 19px;
    margin-bottom: 10px;
}

.feature-card p {
    color: var(--text);
    font-size: 14px;
}

/* ===== 5. About Section ===== */
.about {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 60px;
    padding-top: 75px;
    padding-bottom: 75px;
}

.about .tagline {
    margin-bottom: 12px;
}

.about h2 {
    margin-bottom: 0;
}

.about > p {
    font-size: 16px;
}

/* ===== 6. Contact Section ===== */
.contact-section {
    background: var(--primary);
    color: #ffffff;
    padding: 45px 0;
}

.contact-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 25px;
}

.contact-content h2 {
    font-size: 27px;
    line-height: 1.3;
    margin-bottom: 8px;
}

.contact-content p {
    color: #eeecff;
    font-size: 15px;
}

.btn-light {
    flex-shrink: 0;
    background: #ffffff;
    color: var(--primary-dark);
}

.btn-light:hover {
    background: #efedff;
}

/* ===== 7. Footer ===== */
.footer {
    background: #ffffff;
    padding: 24px 0;
    border-top: 1px solid #edf0f5;
}

.footer-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
}

.footer-content .logo {
    font-size: 24px;
}

.footer-content p {
    color: var(--text);
    font-size: 13px;
}

/* ===== 8. Tablet Layout ===== */
@media (max-width: 900px) {
    .hero {
        gap: 35px;
        padding-top: 60px;
        padding-bottom: 65px;
    }

    .hero-visual > img {
        height: 340px;
    }

    .nav-links {
        gap: 18px;
    }

    .feature-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .about {
        gap: 30px;
    }
}

/* ===== 9. Mobile Layout ===== */
@media (max-width: 600px) {
    .navbar {
        padding: 16px 0;
        flex-wrap: wrap;
        justify-content: center;
        gap: 14px;
    }

    .logo {
        width: 100%;
        text-align: center;
    }

    .nav-links {
        justify-content: center;
        flex-wrap: wrap;
        gap: 10px 18px;
    }

    .nav-links a {
        font-size: 14px;
    }

    .nav-cta {
        padding: 9px 15px;
    }

    .hero {
        grid-template-columns: 1fr;
        gap: 35px;
        padding-top: 45px;
        padding-bottom: 55px;
    }

    .hero-text h1 {
        font-size: 40px;
    }

    .hero-visual > img {
        height: 290px;
    }

    .hero-stats {
        gap: 30px;
    }

    .section {
        padding: 55px 0;
    }

    .section-heading h2,
    .about h2 {
        font-size: 28px;
    }

    .feature-grid {
        grid-template-columns: 1fr;
        gap: 18px;
    }

    .about {
        grid-template-columns: 1fr;
        gap: 20px;
        padding-top: 55px;
        padding-bottom: 55px;
    }

    .contact-content {
        flex-direction: column;
        align-items: flex-start;
    }

    .contact-content h2 {
        font-size: 24px;
    }

    .footer-content {
        flex-direction: column;
        text-align: center;
        gap: 8px;
    }
}
