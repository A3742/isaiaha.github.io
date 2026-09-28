<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta
    name="description"
    content="Isaiah is a Business Administration for Transfer student at Chaffey College, working toward transferring to UC Irvine to pursue a Business Information Management Major."
  />
  <title>Isaiah Aldas | Business Information Management</title>

  <style>
    /* ------------------------------
       Base / Theme
    ------------------------------ */
    :root {
      --navy: #091a2b;
      --navy-light: #102b46;
      --blue: #1769e0;
      --cyan: #48d5e7;
      --ink: #162334;
      --muted: #64748b;
      --surface: #ffffff;
      --surface-soft: #f5f8fc;
      --line: #dbe5f0;
      --shadow: 0 18px 45px rgba(9, 26, 43, 0.12);
      --radius-lg: 26px;
      --radius-md: 16px;
      --max-width: 1120px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      color: var(--ink);
      background: var(--surface);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont,
        "Segoe UI", sans-serif;
      line-height: 1.6;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      border: 0;
      cursor: pointer;
      font: inherit;
    }

    .container {
      width: min(var(--max-width), calc(100% - 2.5rem));
      margin: 0 auto;
    }

    .section {
      padding: 6.5rem 0;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 0.55rem;
      margin-bottom: 1rem;
      color: var(--blue);
      font-size: 0.8rem;
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .eyebrow::before {
      width: 26px;
      height: 2px;
      background: var(--cyan);
      content: "";
    }

    .section-heading {
      max-width: 710px;
      margin-bottom: 3rem;
    }

    .section-heading h2 {
      margin-bottom: 0.85rem;
      color: var(--navy);
      font-size: clamp(2rem, 4vw, 3rem);
      letter-spacing: -0.045em;
      line-height: 1.08;
    }

    .section-heading p {
      max-width: 620px;
      color: var(--muted);
      font-size: 1.05rem;
    }

    /* ------------------------------
       Navigation
    ------------------------------ */
    .site-header {
      position: fixed;
      z-index: 1000;
      top: 0;
      left: 0;
      width: 100%;
      border-bottom: 1px solid transparent;
      transition: background 0.3s ease, border-color 0.3s ease,
        box-shadow 0.3s ease;
    }

    .site-header.scrolled {
      border-color: rgba(219, 229, 240, 0.9);
      background: rgba(255, 255, 255, 0.92);
      box-shadow: 0 8px 30px rgba(9, 26, 43, 0.08);
      backdrop-filter: blur(14px);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      min-height: 78px;
    }

    .brand {
      color: var(--navy);
      font-size: 1.35rem;
      font-weight: 850;
      letter-spacing: -0.05em;
    }

    .brand span {
      color: var(--blue);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.8rem;
      list-style: none;
    }

    .nav-links a {
      position: relative;
      color: #405266;
      font-size: 0.92rem;
      font-weight: 700;
      transition: color 0.25s ease;
    }

    .nav-links a:not(.nav-button)::after {
      position: absolute;
      right: 0;
      bottom: -7px;
      left: 0;
      width: 0;
      height: 2px;
      margin: auto;
      background: var(--blue);
      content: "";
      transition: width 0.25s ease;
    }

    .nav-links a:hover {
      color: var(--blue);
    }

    .nav-links a:not(.nav-button):hover::after {
      width: 100%;
    }

    .nav-button {
      padding: 0.7rem 1rem;
      border-radius: 9px;
      color: #fff !important;
      background: var(--blue);
      transition: transform 0.25s ease, background 0.25s ease;
    }

    .nav-button:hover {
      background: #0e55bd;
      transform: translateY(-2px);
    }

    .menu-toggle {
      display: none;
      color: var(--navy);
      background: transparent;
      font-size: 1.5rem;
    }

    /* ------------------------------
       Hero
    ------------------------------ */
    .hero {
      position: relative;
      display: flex;
      align-items: center;
      min-height: 100vh;
      padding: 9.5rem 0 5rem;
      overflow: hidden;
      background:
        radial-gradient(circle at 88% 15%, rgba(72, 213, 231, 0.19), transparent 26rem),
        radial-gradient(circle at 8% 88%, rgba(23, 105, 224, 0.11), transparent 25rem),
        linear-gradient(135deg, #f8fbff 0%, #eef5fb 100%);
    }

    .hero::before {
      position: absolute;
      top: -280px;
      right: -250px;
      width: 600px;
      height: 600px;
      border: 1px solid rgba(23, 105, 224, 0.12);
      border-radius: 50%;
      content: "";
    }

    .hero-grid {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: 1.18fr 0.82fr;
      gap: 4rem;
      align-items: center;
    }

    .hero-copy h1 {
      max-width: 760px;
      margin-bottom: 1.4rem;
      color: var(--navy);
      font-size: clamp(3.1rem, 7vw, 5.8rem);
      font-weight: 850;
      letter-spacing: -0.075em;
      line-height: 0.98;
    }

    .hero-copy h1 span {
      color: var(--blue);
    }

    .hero-copy p {
      max-width: 625px;
      margin-bottom: 2rem;
      color: #4d6073;
      font-size: clamp(1.05rem, 2vw, 1.2rem);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      margin-bottom: 3rem;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.55rem;
      min-height: 50px;
      padding: 0.85rem 1.25rem;
      border-radius: 11px;
      font-size: 0.95rem;
      font-weight: 800;
      transition: transform 0.25s ease, box-shadow 0.25s ease,
        background 0.25s ease, color 0.25s ease;
    }

    .button-primary {
      color: #fff;
      background: var(--blue);
      box-shadow: 0 12px 24px rgba(23, 105, 224, 0.24);
    }

    .button-primary:hover {
      background: #0f57bf;
      box-shadow: 0 16px 28px rgba(23, 105, 224, 0.3);
      transform: translateY(-3px);
    }

    .button-secondary {
      border: 1px solid var(--line);
      color: var(--navy);
      background: rgba(255, 255, 255, 0.72);
    }

    .button-secon
