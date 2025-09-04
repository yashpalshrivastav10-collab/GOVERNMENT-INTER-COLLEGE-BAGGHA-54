<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>GIC Baggha 54 School</title>
  <style>
    :root{--blue:#1e3a8a;--yellow:#facc15;--bg:#f9fafb}
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{margin:0;font-family:Inter, Arial, sans-serif;background:var(--bg);color:#111}
    header{background:var(--blue);color:white;padding:18px 24px;display:flex;justify-content:space-between;align-items:center;gap:16px}
    .header-left h1{margin:0;font-size:20px}
    .nav{display:flex;gap:10px;align-items:center}
    .nav-btn{background:var(--yellow);color:#000;border:none;padding:8px 14px;border-radius:999px;font-weight:600;cursor:pointer;display:inline-block}
    .nav-btn.secondary{background:transparent;color:white;border:1px solid rgba(255,255,255,0.18)}
    .nav-btn:hover{transform:translateY(-2px);box-shadow:0 6px 18px rgba(0,0,0,0.12)}
    .hero{background:linear-gradient(90deg,#1d4ed8,#3b82f6);color:white;text-align:center;padding:84px 20px}
    .hero h2{margin:0;font-size:36px}
    .hero p{max-width:720px;margin:12px auto 18px}
    .section{padding:56px 20px;max-width:1000px;margin:0 auto}
    .card{background:white;padding:20px;border-radius:10px;box-shadow:0 4px 12px rgba(0,0,0,0.06);text-align:left}
    .cards{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px}
    .stream-buttons{display:flex;gap:12px;flex-wrap:wrap;margin-top:14px}
    .stream-btn{background:#e8f1ff;border:none;padding:10px 16px;border-radius:999px;cursor:pointer;font-weight:600}
    .stream-btn.active{background:var(--yellow);color:#000;box-shadow:0 6px 18px rgba(0,0,0,0.08)}
    .stream-content{overflow:hidden;max-height:0;transition:max-height .4s ease,opacity .3s ease;padding:0;opacity:0}
    .stream-content.open{max-height:400px;padding:12px 0;opacity:1}
    .stream-content ul{margin:8px 0 0 20px;padding:0}
    footer{background:var(--blue);color:white;text-align:center;padding:20px;margin-top:36px}
    small.note{display:block;margin-top:8px;color:#dbeafe;font-size:13px}
    @media(max-width:600px){.hero h2{font-size:28px}}
  </style>
</head>
<body>

<header>
  <div class="header-left">
    <h1>GIC Baggha 54 School</h1>
  </div>
  <nav class="nav" aria-label="Main navigation">
    <button class="nav-btn" onclick="scrollToSection('about')" aria-controls="about">About</button>
    <button class="nav-btn" onclick="scrollToSection('academics')" aria-controls="academics">Academics</button>
    <button class="nav-btn" onclick="scrollToSection('contact')" aria-controls="contact">Contact</button>
  </nav>
</header>

<section class="hero" aria-labelledby="hero-heading">
  <h2 id="hero-heading">Welcome to GIC Baggha 54 School</h2>
  <p>Empowering students with knowledge, discipline, and values for a brighter future.</p>
  <button class="nav-btn" onclick="scrollToSection('about')">Learn More</button>
</section>

<section id="about" class="section" aria-labelledby="about-heading">
  <h2 id="about-heading">About Us</h2>
  <div class="card">
    <p><strong>Government Inter College Baggha 54</strong> is dedicated to academic excellence and holistic development of students. With experienced faculty and modern facilities, we aim to nurture future leaders.</p>
    <p class="note">We provide education from <strong>Class 1 to 12</strong>, with academic programs, extracurricular activities, and guidance to prepare students for higher education and responsible citizenship.</p>
  </div>
</section>

<section id="academics" class="section" aria-labelledby="academics-heading" style="background:#f3f4f6">
  <h2 id="academics-heading">Academics</h2>
  <div class="card">
    <p>Choose a stream to see subjects offered:</p>
    <div class="stream-buttons" role="tablist" aria-label="Streams">
      <button class="stream-btn" id="btn-science" onclick="toggleStream('science')" role="tab" aria-selected="false">Science (11–12)</button>
      <button class="stream-btn" id="btn-arts" onclick="toggleStream('arts')" role="tab" aria-selected="false">Arts (11–12)</button>
      <button class="stream-btn" id="btn-maths9" onclick="toggleStream('maths9')" role="tab" aria-selected="false">Maths (9–10)</button>
      <button class="stream-btn" id="btn-home9" onclick="toggleStream('home9')" role="tab" aria-selected="false">Home Science (9–10)</button>
    </div>

    <!-- Science Stream 11-12 -->
    <div id="science-content" class="stream-content" role="tabpanel" aria-labelledby="btn-science">
      <h3>Science (Class 11–12, PCMB)</h3>
      <ul>
        <li>Hindi</li>
        <li>English</li>
        <li>Physics</li>
        <li>Chemistry</li>
        <li>Mathematics</li>
        <li>Biology</li>
      </ul>
    </div>

    <!-- Arts Stream 11-12 -->
    <div id="arts-content" class="stream-content" role="tabpanel" aria-labelledby="btn-arts">
      <h3>Arts (Class 11–12)</h3>
      <ul>
        <li>Hindi</li>
        <li>English</li>
        <li>Economics</li>
        <li>Sociology</li>
        <li>Political Science</li>
      </ul>
    </div>

    <!-- Maths Stream 9-10 -->
    <div id="maths9-content" class="stream-content" role="tabpanel" aria-labelledby="btn-maths9">
      <h3>Maths Stream (Class 9–10)</h3>
      <ul>
        <li>Hindi</li>
        <li>English</li>
        <li>Science</li>
        <li>Social Science</li>
        <li>Mathematics</li>
      </ul>
    </div>

    <!-- Home Science Stream 9-10 -->
    <div id="home9-content" class="stream-content" role="tabpanel" aria-labelledby="btn-home9">
      <h3>Home Science Stream (Class 9–10)</h3>
      <ul>
        <li>Hindi</li>
        <li>English</li>
        <li>Science</li>
        <li>Social Science</li>
        <li>Home Science</li>
      </ul>
    </div>

    <div class="cards" style="margin-top:18px">
      <div class="card"><h3>Quality Education</h3><p>Providing strong academic foundation from Class 1 to 12 in Science, Arts, and Home Science streams.</p></div>
      <div class="card"><h3>Holistic Development</h3><p>Encouraging participation in sports, cultural activities, and leadership programs.</p></div>
      <div class="card"><h3>Modern Facilities</h3><p>Equipped with library, labs, and digital learning resources for students.</p></div>
    </div>
  </div>
</section>

<section id="contact" class="section" aria-labelledby="contact-heading">
  <h2 id="contact-heading">Contact Us</h2>
  <div class="card">
    <p>📍 Address: GIC Baggha 54, Khatima, US Nagar, Uttarakhand, India</p>
    <p>📞 Phone: <a href="tel:+91XXXXXXXXXX">+91-XXXXXXXXXX</a></p>
    <p>✉️ Email: <a href="mailto:info@gicbaggha54.ac.in">info@gicbaggha54.ac.in</a></p>
  </div>
</section>

<footer>
  <div style="display:flex;gap:8px;justify-content:center;margin-bottom:8px">
    <button class="nav-btn secondary" onclick="scrollToSection('about')">About</button>
    <button class="nav-btn secondary" onclick="scrollToSection('academics')">Academics</button>
    <button class="nav-btn secondary" onclick="scrollToSection('contact')">Contact</button>
  </div>
  <small class="note">&copy; <span id="yr"></span> GIC Baggha 54 School. All Rights Reserved.</small>
</footer>

<script>
// set year
document.getElementById('yr').textContent = new Date().getFullYear();

// Toggle streams
let active = null;
function toggleStream(name){
  const streams = {
    science: {content:'science-content', btn:'btn-science'},
    arts: {content:'arts-content', btn:'btn-arts'},
    maths9: {content:'maths9-content', btn:'btn-maths9'},
    home9: {content:'home9-content', btn:'btn-home9'}
  };

  // close all first
  for (const key in streams){
    document.getElementById(streams[key].content).classList.remove('open');
    document.getElementById(streams[key].btn).classList.remove('active');
    document.getElementById(streams[key].btn).setAttribute('aria-selected','false');
  }

  // if already active, just close
  if(active === name){active = null; return;}

  // open selected
  document.getElementById(streams[name].content).classList.add('open');
  document.getElementById(streams[name].btn).classList.add('active');
  document.getElementById(streams[name].btn).setAttribute('aria-selected','true');
  active = name;
}

// smooth scroll helper
function scrollToSection(id){
  const el = document.getElementById(id);
  if(el) el.scrollIntoView({behavior:'smooth',block:'start'});
}
</script>

</body>
</html>

    
