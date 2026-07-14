# Abdelrahman Gamal 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abdelrahman Gamal — Sales &amp; Retention Specialist</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500;600&family=Zilla+Slab:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#10161F;
    --ink-deep:#0A0F16;
    --paper:#F6EFDC;
    --paper-dim:#E8DDC0;
    --brass:#D6A324;
    --brass-bright:#F4C64E;
    --signal:#E2604F;
    --ink-light:#8CA0B3;
    --text-on-ink:#F0EAD8;
    --text-on-paper:#1C2027;
    --teal:#2E8368;
    --radius:3px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--ink);
    color:var(--text-on-ink);
    font-family:'Inter',sans-serif;
    line-height:1.5;
  }
  a{color:inherit;}
  .wrap{max-width:960px;margin:0 auto;padding:0 28px;}

  /* ================= NAV ================= */
  nav{
    position:sticky;
    top:0;
    z-index:50;
    background:rgba(20,31,42,0.92);
    backdrop-filter:blur(6px);
    border-bottom:1px solid rgba(214,163,36,0.25);
  }
  nav .wrap{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding-top:14px;
    padding-bottom:14px;
  }
  nav .brand{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;
    letter-spacing:1.5px;
    color:var(--brass-bright);
    text-decoration:none;
  }
  nav .links{
    display:flex;
    gap:22px;
    list-style:none;
    margin:0;
    padding:0;
  }
  nav .links a{
    font-family:'IBM Plex Mono',monospace;
    font-size:11.5px;
    letter-spacing:0.8px;
    text-transform:uppercase;
    color:var(--ink-light);
    text-decoration:none;
    transition:color 0.15s ease;
  }
  nav .links a:hover{color:var(--brass-bright);}
  nav .resume-btn{
    font-family:'IBM Plex Mono',monospace;
    font-size:11px;
    letter-spacing:0.6px;
    color:var(--ink-deep);
    background:var(--brass);
    padding:8px 14px;
    border-radius:2px;
    text-decoration:none;
    white-space:nowrap;
  }
  nav .resume-btn:hover{background:var(--brass-bright);}
  @media (max-width:700px){
    nav .links{display:none;}
  }

  /* ================= HEADER / HERO ================= */
  header{
    padding:64px 0 40px;
    border-bottom:1px solid rgba(214,163,36,0.25);
    position:relative;
    overflow:hidden;
  }
  header::before{
    content:"";
    position:absolute;
    top:-220px;
    right:-160px;
    width:520px;
    height:520px;
    background:radial-gradient(circle, rgba(214,163,36,0.16), transparent 70%);
    pointer-events:none;
  }
  header .wrap{position:relative;z-index:1;}
  .eyebrow{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;
    letter-spacing:2.5px;
    text-transform:uppercase;
    color:var(--brass-bright);
    margin:0 0 18px;
  }
  h1.name{
    font-family:'Zilla Slab',serif;
    font-weight:700;
    font-size:clamp(38px,6vw,64px);
    line-height:1.02;
    margin:0 0 14px;
    background:linear-gradient(120deg, var(--text-on-ink) 40%, var(--brass-bright) 100%);
    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;
  }
  .role-line{
    font-family:'Inter',sans-serif;
    font-size:clamp(15px,2vw,18px);
    color:var(--ink-light);
    margin:0 0 36px;
    max-width:560px;
  }
  .role-line b{color:var(--paper);font-weight:600;}

  /* Flip-board stat strip */
  .stats{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:1px;
    background:rgba(214,163,36,0.25);
    border:1px solid rgba(214,163,36,0.25);
    margin-top:8px;
  }
  .stat{
    background:var(--ink-deep);
    padding:22px 18px;
    text-align:left;
    transition:background 0.2s ease;
  }
  .stat:hover{background:#131C27;}
  .stat .num{
    font-family:'IBM Plex Mono',monospace;
    font-variant-numeric:tabular-nums;
    font-size:clamp(26px,4vw,38px);
    font-weight:600;
    color:var(--brass-bright);
    display:block;
    letter-spacing:-0.5px;
  }
  .stat .label{
    font-size:11px;
    letter-spacing:1.2px;
    text-transform:uppercase;
    color:var(--ink-light);
    margin-top:6px;
    display:block;
  }

  /* ================= SECTION HEADINGS ================= */
  section{padding:56px 0;}
  .sec-head{
    display:flex;
    align-items:baseline;
    gap:14px;
    margin-bottom:30px;
  }
  .sec-head .tag{
    font-family:'IBM Plex Mono',monospace;
    font-size:11px;
    letter-spacing:2px;
    color:var(--ink-deep);
    background:var(--brass);
    padding:3px 8px;
    border-radius:2px;
  }
  .sec-head h2{
    font-family:'Zilla Slab',serif;
    font-size:26px;
    font-weight:600;
    margin:0;
    color:var(--text-on-ink);
  }

  /* ================= CALL LOG TICKETS ================= */
  #callboard{border-top:1px solid rgba(214,163,36,0.25);}
  .tickets{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
  }
  .ticket{
    position:relative;
    background:var(--paper);
    color:var(--text-on-paper);
    padding:26px 20px 22px;
    border-radius:var(--radius);
    box-shadow:0 10px 24px rgba(0,0,0,0.32);
    transition:transform 0.2s ease, box-shadow 0.2s ease;
  }
  .ticket:hover{
    transform:translateY(-4px);
    box-shadow:0 16px 32px rgba(0,0,0,0.4);
  }
  .ticket::before{
    content:"";
    position:absolute;
    top:0;left:0;right:0;
    height:10px;
    background-image:radial-gradient(circle 4px, var(--ink) 4px, transparent 4.5px);
    background-size:18px 10px;
    background-position:6px 0;
    background-repeat:repeat-x;
    transform:translateY(-5px);
  }
  .ticket .meta{
    font-family:'IBM Plex Mono',monospace;
    font-size:10.5px;
    letter-spacing:1px;
    text-transform:uppercase;
    color:var(--signal);
    margin:10px 0 14px;
    display:flex;
    justify-content:space-between;
    border-bottom:1px dashed rgba(32,36,42,0.25);
    padding-bottom:10px;
  }
  .ticket h3{
    font-family:'Zilla Slab',serif;
    font-size:17px;
    font-weight:600;
    margin:0 0 12px;
  }
  .ticket .row{margin-bottom:10px;font-size:13.5px;}
  .ticket .row b{
    display:block;
    font-family:'IBM Plex Mono',monospace;
    font-size:10px;
    letter-spacing:1px;
    text-transform:uppercase;
    color:#6b5a1f;
    margin-bottom:2px;
  }
  .ticket .outcome{
    margin-top:14px;
    font-family:'IBM Plex Mono',monospace;
    font-size:11.5px;
    letter-spacing:0.5px;
    color:#1F6E52;
    background:rgba(46,131,104,0.12);
    display:inline-block;
    padding:4px 10px;
    border-radius:2px;
  }
  .disclaimer{
    font-size:12px;
    color:var(--ink-light);
    margin-top:18px;
    font-style:italic;
  }

  /* ================= ROLE FIT ================= */
  #fit{border-top:1px solid rgba(214,163,36,0.25);}
  .fit-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
  }
  .fit-card{
    border:1px solid rgba(214,163,36,0.3);
    padding:24px 20px;
    border-radius:3px;
    background:linear-gradient(180deg, rgba(214,163,36,0.07), transparent 60%);
    transition:border-color 0.2s ease, transform 0.2s ease;
  }
  .fit-card:hover{
    border-color:rgba(244,198,78,0.6);
    transform:translateY(-3px);
  }
  .fit-card .fit-tag{
    font-family:'IBM Plex Mono',monospace;
    font-size:10px;
    letter-spacing:1.5px;
    text-transform:uppercase;
    color:var(--brass);
    margin:0 0 10px;
  }
  .fit-card h3{
    font-family:'Zilla Slab',serif;
    font-size:19px;
    margin:0 0 12px;
    color:var(--text-on-ink);
  }
  .fit-card p{
    font-size:13.5px;
    color:#C7D2DA;
    margin:0;
  }
  .fit-card p b{color:var(--paper);font-weight:600;}

  /* ================= METHOD ================= */
  #method{border-top:1px solid rgba(214,163,36,0.25);}
  .method-list{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:26px 30px;
  }
  .method-step{
    display:flex;
    gap:16px;
  }
  .method-step .step-num{
    font-family:'IBM Plex Mono',monospace;
    font-size:22px;
    font-weight:600;
    color:var(--brass);
    line-height:1;
    flex-shrink:0;
    padding-top:2px;
  }
  .method-step h4{
    font-family:'Zilla Slab',serif;
    font-size:16px;
    margin:0 0 6px;
    color:var(--text-on-ink);
  }
  .method-step p{
    font-size:13.5px;
    color:#C7D2DA;
    margin:0;
  }
  @media (max-width:700px){
    .fit-grid{grid-template-columns:1fr;}
    .method-list{grid-template-columns:1fr;}
  }
  #experience{border-top:1px solid rgba(214,163,36,0.25);}
  .log-row{
    display:grid;
    grid-template-columns:130px 1fr 160px;
    gap:18px;
    padding:20px 0;
    border-bottom:1px solid rgba(214,163,36,0.15);
    align-items:start;
  }
  .log-row:last-child{border-bottom:none;}
  .log-row .dates{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;
    color:var(--brass);
    letter-spacing:0.5px;
    padding-top:3px;
  }
  .log-row h3{
    font-family:'Zilla Slab',serif;
    font-size:17px;
    margin:0 0 6px;
    color:var(--text-on-ink);
  }
  .log-row .place{
    font-size:13px;
    color:var(--ink-light);
    margin:0 0 10px;
  }
  .log-row ul{
    margin:0;
    padding-left:16px;
    font-size:13.5px;
    color:#C7D2DA;
  }
  .log-row li{margin-bottom:5px;}
  .log-row .stamp{
    justify-self:end;
    font-family:'IBM Plex Mono',monospace;
    font-size:10.5px;
    letter-spacing:1px;
    text-transform:uppercase;
    color:var(--signal);
    border:1.5px solid var(--signal);
    padding:5px 9px;
    border-radius:2px;
    transform:rotate(3deg);
    white-space:nowrap;
    height:fit-content;
  }

  /* ================= SKILLS ================= */
  #skills{border-top:1px solid rgba(214,163,36,0.25);}
  .stamps{
    display:flex;
    flex-wrap:wrap;
    gap:10px;
  }
  .stamp-badge{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;
    letter-spacing:0.5px;
    color:var(--brass-bright);
    border:1px solid rgba(214,163,36,0.5);
    padding:8px 14px;
    border-radius:2px;
  }

  /* ================= EDUCATION / CERTS ================= */
  #creds{border-top:1px solid rgba(214,163,36,0.25);}
  .creds-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:30px;
  }
  .creds-grid h4{
    font-family:'IBM Plex Mono',monospace;
    font-size:11px;
    letter-spacing:1.5px;
    text-transform:uppercase;
    color:var(--brass);
    margin:0 0 12px;
  }
  .creds-grid p{margin:0 0 14px;font-size:13.5px;color:#C7D2DA;}
  .creds-grid p b{color:var(--text-on-ink);display:block;font-size:14.5px;margin-bottom:2px;}

  /* ================= FOOTER / CONTACT ================= */
  footer{
    border-top:1px solid rgba(214,163,36,0.25);
    padding:50px 0 60px;
    text-align:center;
  }
  footer h2{
    font-family:'Zilla Slab',serif;
    font-size:28px;
    margin:0 0 12px;
  }
  footer p{color:var(--ink-light);margin:0 0 24px;font-size:14px;}
  .contact-links{
    display:flex;
    justify-content:center;
    gap:16px;
    flex-wrap:wrap;
  }
  .contact-links a{
    font-family:'IBM Plex Mono',monospace;
    font-size:12.5px;
    letter-spacing:0.5px;
    color:var(--ink-deep);
    background:var(--brass);
    padding:11px 20px;
    border-radius:2px;
    text-decoration:none;
    transition:background 0.15s ease;
  }
  .contact-links a:hover{background:var(--brass-bright);}
  .contact-links a.outline{
    background:transparent;
    color:var(--brass);
    border:1px solid var(--brass);
  }

  /* ================= RESPONSIVE ================= */
  @media (max-width:760px){
    .stats{grid-template-columns:1fr;}
    .tickets{grid-template-columns:1fr;}
    .log-row{grid-template-columns:1fr;}
    .log-row .stamp{justify-self:start;}
    .creds-grid{grid-template-columns:1fr;}
  }

  :focus-visible{outline:2px solid var(--brass-bright);outline-offset:2px;}
  @media (prefers-reduced-motion: reduce){
    html{scroll-behavior:auto;}
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <a class="brand" href="#top">A. GAMAL — FILE NO. 2026</a>
    <ul class="links">
      <li><a href="#fit">Where I Fit</a></li>
      <li><a href="#callboard">Case Files</a></li>
      <li><a href="#method">Method</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <a class="resume-btn" href="Abdelrahman_Gamal_Resume_2026.pdf">Download Résumé ↓</a>
  </div>
</nav>

<header id="top">
  <div class="wrap">
    <p class="eyebrow">Sales · Business Development · Retention</p>
    <h1 class="name">Abdelrahman Gamal</h1>
    <p class="role-line">I work the calls nobody wants to take — the ones that start on <b>"no."</b> Two-plus years turning cancellations into closed sales, cold conversations into booked interest, and skeptical customers into retained accounts for the U.S. market.</p>

    <div class="stats">
      <div class="stat">
        <span class="num">+15%</span>
        <span class="label">Close rate vs. target</span>
      </div>
      <div class="stat">
        <span class="num">120%</span>
        <span class="label">Avg. monthly quota</span>
      </div>
      <div class="stat">
        <span class="num">2+ YRS</span>
        <span class="label">U.S.-market phone sales</span>
      </div>
    </div>
  </div>
</header>

<section id="fit">
  <div class="wrap">
    <div class="sec-head">
      <span class="tag">ROLE</span>
      <h2>Where I Fit</h2>
    </div>
    <div class="fit-grid">
      <div class="fit-card">
        <p class="fit-tag">01 — Sales Specialist</p>
        <h3>Full-cycle closer</h3>
        <p>I run the whole conversation — qualify the need, pitch the offer, handle the pushback, close on the call. <b>15% above target close rate</b> and <b>120% average quota attainment</b> came from owning outcomes, not just activity.</p>
      </div>
      <div class="fit-card">
        <p class="fit-tag">02 — Business Development</p>
        <h3>High-volume opener</h3>
        <p>Two years of daily outbound and inbound call volume, every dial logged in CRM. I'm built for the grind of prospecting — qualifying fast, earning attention in seconds, and moving a stranger to a next step.</p>
      </div>
      <div class="fit-card">
        <p class="fit-tag">03 — Retention Specialist</p>
        <h3>Save-the-account specialist</h3>
        <p>My core rep at Concentrix and INTELCIA: customers already trying to leave. Diagnosing the real reason, rebuilding value fast, and turning a cancellation into a renewed, expanded account.</p>
      </div>
    </div>
  </div>
</section>

<section id="callboard">
  <div class="wrap">
    <div class="sec-head">
      <span class="tag">LOG</span>
      <h2>Case Files</h2>
    </div>

    <div class="tickets">

      <div class="ticket">
        <div class="meta"><span>Dish · Concentrix</span><span>Case 01 — Retention</span></div>
        <h3>"I'm cancelling — I don't need this anymore."</h3>
        <div class="row"><b>Situation</b>Customer called to disconnect, saw no ongoing value in the service, decision already made in their mind.</div>
        <div class="row"><b>Action</b>Diagnosed the real reason behind the cancellation instead of arguing with it, then reframed Starlink as an upgrade that solved the underlying problem — not a bolt-on offer.</div>
        <div class="row"><b>Result</b>Account retained and expanded into a multi-service subscriber on the same call.</div>
        <span class="outcome">✓ Retained + cross-sold</span>
      </div>

      <div class="ticket">
        <div class="meta"><span>Optimum · INTELCIA</span><span>Case 02 — Cross-Sell</span></div>
        <h3>"I already have a phone plan elsewhere."</h3>
        <div class="row"><b>Situation</b>Single-play customer, no stated interest in bundling, guarded against "another sales pitch."</div>
        <div class="row"><b>Action</b>Skipped the generic script — built the pitch around their actual account history and usage pattern so it felt like a fit, not a pitch.</div>
        <div class="row"><b>Result</b>Converted into a multi-product account, directly growing revenue per customer.</div>
        <span class="outcome">✓ Multi-product close</span>
      </div>

      <div class="ticket">
        <div class="meta"><span>ASAP Tickets</span><span>Case 03 — High-Pressure Close</span></div>
        <h3>"I need this booked in the next 10 minutes."</h3>
        <div class="row"><b>Situation</b>Time-critical, high-ticket, multi-passenger booking with zero room for error.</div>
        <div class="row"><b>Action</b>Verified every detail at speed without cutting corners, then layered in insurance and seating upgrades without slowing the close down.</div>
        <div class="row"><b>Result</b>Booking closed on time, with add-ons attached — no re-work, no follow-up call needed.</div>
        <span class="outcome">✓ Booked + upsold</span>
      </div>

    </div>
    <p class="disclaimer">Representative case files drawn from real account types and outcomes — not verbatim transcripts.</p>
  </div>
</section>

<section id="method">
  <div class="wrap">
    <div class="sec-head">
      <span class="tag">SOP</span>
      <h2>How I Run a Call</h2>
    </div>
    <div class="method-list">
      <div class="method-step">
        <span class="step-num">01</span>
        <div>
          <h4>Open with purpose</h4>
          <p>No warm-up small talk that wastes their time or mine — state why I'm calling and earn the next ten seconds immediately.</p>
        </div>
      </div>
      <div class="method-step">
        <span class="step-num">02</span>
        <div>
          <h4>Diagnose the real objection</h4>
          <p>The stated reason and the real reason are often different. I ask before I pitch, so the offer actually answers the objection.</p>
        </div>
      </div>
      <div class="method-step">
        <span class="step-num">03</span>
        <div>
          <h4>Reframe the value</h4>
          <p>Not a script recital — a specific answer to what this exact customer just told me, using their account history when I have it.</p>
        </div>
      </div>
      <div class="method-step">
        <span class="step-num">04</span>
        <div>
          <h4>Close or set the next step</h4>
          <p>Ask directly for the close. If it's not a close today, I don't let the call end vague — I lock in a specific next step.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="wrap">
    <div class="sec-head">
      <span class="tag">FILE</span>
      <h2>Experience</h2>
    </div>

    <div class="log-row">
      <div class="dates">02/2026 –<br>06/2026</div>
      <div>
        <h3>Sales &amp; Retention Specialist</h3>
        <p class="place">Concentrix — Dish Network Account · Cairo, Egypt</p>
        <ul>
          <li>Sold and closed Starlink internet to existing customers on live retention calls.</li>
          <li>Handled real-time objections — price, distrust, competitor offers — to keep every call moving toward a close.</li>
          <li>Logged every call and outcome in Salesforce CRM.</li>
        </ul>
      </div>
      <div class="stamp">Top performer</div>
    </div>

    <div class="log-row">
      <div class="dates">02/2024 –<br>02/2026</div>
      <div>
        <h3>Sales &amp; Retention Specialist</h3>
        <p class="place">INTELCIA — Optimum Account · Alexandria, Egypt</p>
        <ul>
          <li>Sold Optimum Mobile to existing customers, converting single-play accounts to multi-product sales.</li>
          <li>Ran full-cycle sales conversations — qualify, pitch, negotiate, close — on every call.</li>
          <li>Tracked every pitch and outcome in a cloud-based CRM.</li>
        </ul>
      </div>
      <div class="stamp">120% quota</div>
    </div>

    <div class="log-row">
      <div class="dates">12/2022 –<br>01/2024</div>
      <div>
        <h3>Travel Sales Agent</h3>
        <p class="place">ASAP Tickets</p>
        <ul>
          <li>Closed time-sensitive, high-ticket travel sales from global inbound inquiries.</li>
          <li>Upsold insurance, seating tiers, and logistics add-ons on the majority of sales.</li>
        </ul>
      </div>
      <div class="stamp">Fast close</div>
    </div>

  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="sec-head">
      <span class="tag">KIT</span>
      <h2>What I Work With</h2>
    </div>
    <div class="stamps">
      <span class="stamp-badge">High-Volume Outbound Calling</span>
      <span class="stamp-badge">Objection Handling</span>
      <span class="stamp-badge">Consultative Selling</span>
      <span class="stamp-badge">Salesforce CRM</span>
      <span class="stamp-badge">Quota &amp; KPI Attainment</span>
      <span class="stamp-badge">Cross-Selling &amp; Upselling</span>
      <span class="stamp-badge">Resilience Under Rejection</span>
      <span class="stamp-badge">Fluent English (C1)</span>
    </div>
  </div>
</section>

<section id="creds">
  <div class="wrap">
    <div class="sec-head">
      <span class="tag">REF</span>
      <h2>Education &amp; Certifications</h2>
    </div>
    <div class="creds-grid">
      <div>
        <h4>Education</h4>
        <p><b>Alexandria University</b>Faculty of Law — Student</p>
        <p><b>Forward Learning</b>Certificate of Technical Studies: Digital Marketing (12/2022)</p>
      </div>
      <div>
        <h4>Certifications</h4>
        <p><b>Independent Travel Manager Certification</b>DreamPort, Jan 2024</p>
        <p><b>Customer Satisfaction Certification</b>Issued 11/2024</p>
      </div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="wrap">
    <h2>Let's talk numbers.</h2>
    <p>Cairo, Egypt · Available for U.S. business hours</p>
    <div class="contact-links">
      <a href="mailto:abdelrahmangamal.sh@hotmail.com">Email Me</a>
      <a class="outline" href="tel:+201555644225">+20 15 5564 4225</a>
      <a class="outline" href="Abdelrahman_Gamal_Resume_2026.pdf">Download Résumé</a>
    </div>
  </div>
</footer>

</body>
</html>

