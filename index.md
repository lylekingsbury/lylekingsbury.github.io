---
layout: default
---

<!--
  Personal academic site for Lyle Kingsbury.
  Built on the Minima theme (see _config.yml), whose header and footer are
  hidden below so this page controls its own layout.

  Editing tips
  - Each section is marked with a  ===== SECTION =====  comment.
  - To use a photo instead of the "LK" monogram, upload e.g. assets/photo.jpg
    and replace the <div class="lk-avatar">LK</div> line with:
      <img class="lk-avatar" src="{{ '/assets/photo.jpg' | relative_url }}" alt="Lyle Kingsbury">
-->

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Source+Serif+4:opsz,wght@8..60,500;8..60,600&display=swap');

:root {
  --bg: #fbfaf8;
  --surface: #ffffff;
  --text: #1c1b1a;
  --muted: #6b6862;
  --rule: #e7e4df;
  --accent: #a41034;
  --accent-soft: #f7e9ec;
  --shadow: 0 1px 2px rgba(0,0,0,.04), 0 4px 16px rgba(0,0,0,.04);
}
@media (prefers-color-scheme: dark) {
  :root {
    --bg: #141312;
    --surface: #1c1b19;
    --text: #ecebe8;
    --muted: #a3a09a;
    --rule: #2e2c29;
    --accent: #f07489;
    --accent-soft: #3a1d23;
    --shadow: none;
  }
}

/* ---- Take over from Minima ---- */
body { background: var(--bg); color: var(--text); font-family: Inter, -apple-system, "Segoe UI", Helvetica, Arial, sans-serif; font-size: 16px; line-height: 1.6; }
.site-header, .site-footer { display: none; }
.page-content { padding: 0; }
.page-content .wrapper { max-width: 960px; padding: 0 24px; margin: 0 auto; }
.lk a { color: var(--accent); text-decoration: none; }
.lk a:hover { text-decoration: underline; }
.lk h1, .lk h2, .lk h3 { font-family: "Source Serif 4", Georgia, serif; font-weight: 600; color: var(--text); letter-spacing: -0.01em; }
.lk p, .lk ul { margin: 0; }
.lk ul { list-style: none; padding: 0; }

/* ---- Hero ---- */
.lk-hero { display: grid; grid-template-columns: 1fr auto; gap: 40px; align-items: center; padding: 72px 0 40px; }
.lk-eyebrow { font-size: 13px; font-weight: 600; letter-spacing: .12em; text-transform: uppercase; color: var(--accent); margin-bottom: 12px; }
.lk-hero h1 { font-size: 52px; line-height: 1.05; margin: 0 0 18px; }
.lk-lede { font-size: 20px; line-height: 1.5; max-width: 34em; margin-bottom: 14px !important; }
.lk-role { color: var(--muted); margin-bottom: 24px !important; }
.lk-avatar { width: 168px; height: 168px; border-radius: 50%; object-fit: cover; display: grid; place-items: center; background: var(--accent-soft); color: var(--accent); font-family: "Source Serif 4", Georgia, serif; font-size: 56px; font-weight: 600; }
.lk-buttons { display: flex; flex-wrap: wrap; gap: 10px; }
.lk .lk-btn { display: inline-block; padding: 9px 18px; border-radius: 999px; border: 1px solid var(--accent); font-size: 14px; font-weight: 500; }
.lk .lk-btn.primary { background: var(--accent); color: var(--bg); }
.lk .lk-btn:hover { text-decoration: none; background: var(--accent); color: var(--bg); }

/* ---- At-a-glance numbers ---- */
.lk-stats { display: grid; grid-template-columns: repeat(4, 1fr); border-top: 1px solid var(--rule); border-bottom: 1px solid var(--rule); margin-bottom: 8px; }
.lk-stats div { padding: 20px 16px; border-left: 1px solid var(--rule); }
.lk-stats div:first-child { border-left: 0; padding-left: 0; }
.lk-stats b { display: block; font-family: "Source Serif 4", Georgia, serif; font-size: 30px; font-weight: 600; line-height: 1.1; }
.lk-stats span { color: var(--muted); font-size: 14px; }

/* ---- Section nav ---- */
.lk-nav { position: sticky; top: 0; z-index: 10; background: var(--bg); border-bottom: 1px solid var(--rule); margin: 0 -24px; padding: 0 24px; display: flex; gap: 24px; overflow-x: auto; scrollbar-width: none; }
.lk-nav::-webkit-scrollbar { display: none; }
.lk .lk-nav a { color: var(--muted); font-size: 14px; font-weight: 500; padding: 14px 0; white-space: nowrap; border-bottom: 2px solid transparent; }
.lk .lk-nav a:hover { color: var(--text); text-decoration: none; border-bottom-color: var(--accent); }

/* ---- Sections ---- */
.lk-section { padding: 56px 0 8px; scroll-margin-top: 48px; }
.lk-section > h2 { font-size: 30px; margin: 0 0 6px; }
.lk-intro { color: var(--muted); max-width: 40em; margin-bottom: 28px !important; }
.lk-sub { font-size: 13px !important; font-weight: 600; letter-spacing: .1em; text-transform: uppercase; color: var(--muted) !important; font-family: Inter, sans-serif !important; margin: 32px 0 14px !important; }

/* ---- Research cards ---- */
.lk-cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 18px; }
.lk-card { background: var(--surface); border: 1px solid var(--rule); border-radius: 12px; padding: 22px; box-shadow: var(--shadow); display: flex; flex-direction: column; }
.lk-tag { align-self: flex-start; font-size: 12px; font-weight: 600; color: var(--accent); background: var(--accent-soft); border-radius: 999px; padding: 2px 10px; margin-bottom: 12px; }
.lk-card h3 { font-size: 20px; line-height: 1.25; margin: 0 0 10px; }
.lk-card p { font-size: 15px; color: var(--muted); }
.lk-card .lk-papers { margin-top: auto; padding-top: 16px; font-size: 14px; }

/* ---- Publications ---- */
.lk-pubs li { display: grid; grid-template-columns: 112px 1fr; gap: 20px; padding: 18px 0; border-top: 1px solid var(--rule); }
.lk-pubs li:first-child { border-top: 0; padding-top: 4px; }
.lk-venue { font-family: "Source Serif 4", Georgia, serif; font-style: italic; font-weight: 600; line-height: 1.3; }
.lk-year { display: block; color: var(--muted); font-size: 14px; }
.lk .lk-pub-title { display: block; color: var(--text); font-weight: 600; font-size: 17px; line-height: 1.4; margin-bottom: 4px; }
.lk .lk-pub-title:hover { color: var(--accent); }
.lk-authors { color: var(--muted); font-size: 14px; }
.lk-authors b { color: var(--text); font-weight: 600; }
.lk-extra { font-size: 14px; margin-top: 6px !important; }
.lk-pill { display: inline-block; font-size: 12px; font-weight: 600; border: 1px solid var(--rule); border-radius: 999px; padding: 1px 9px; margin-right: 6px; color: var(--muted); }
.lk-note { color: var(--muted); font-size: 13px; margin-top: 14px !important; }

/* ---- Talks ---- */
.lk-years > div { display: grid; grid-template-columns: 112px 1fr; gap: 20px; padding: 14px 0; border-top: 1px solid var(--rule); }
.lk-years > div:first-child { border-top: 0; }
.lk-years .yr { font-family: "Source Serif 4", Georgia, serif; font-size: 20px; font-weight: 600; }
.lk-years li { padding: 3px 0; }
.lk-years li span { color: var(--muted); }

/* ---- Awards ---- */
.lk-two { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; }
.lk-list li { display: flex; justify-content: space-between; gap: 16px; padding: 9px 0; border-top: 1px solid var(--rule); }
.lk-list li:first-child { border-top: 0; }
.lk-list .when { color: var(--muted); white-space: nowrap; font-variant-numeric: tabular-nums; font-size: 14px; }

/* ---- Teaching & mentoring ---- */
.lk-courses { display: grid; grid-template-columns: repeat(auto-fill, minmax(270px, 1fr)); gap: 14px; }
.lk-course { background: var(--surface); border: 1px solid var(--rule); border-radius: 10px; padding: 16px 18px; }
.lk-course b { display: block; font-weight: 600; }
.lk-course .meta { display: block; color: var(--muted); font-size: 13px; margin-bottom: 6px; }
.lk-course p { font-size: 14px; color: var(--muted); }
.lk-labs { display: grid; grid-template-columns: repeat(3, 1fr); gap: 28px; }
.lk-labs h3 { font-size: 17px; margin: 0 0 2px; }
.lk-labs .where { display: block; color: var(--muted); font-size: 13px; margin-bottom: 10px; }
.lk-labs li { padding: 4px 0; font-size: 15px; }
.lk-labs li span { display: block; color: var(--muted); font-size: 13px; line-height: 1.3; }
.lk-service { background: var(--surface); border: 1px solid var(--rule); border-radius: 10px; padding: 16px 18px; }

/* ---- Background timeline ---- */
.lk-timeline { position: relative; padding-left: 28px; }
.lk-timeline::before { content: ""; position: absolute; left: 6px; top: 8px; bottom: 8px; width: 2px; background: var(--rule); }
.lk-timeline li { position: relative; padding-bottom: 26px; }
.lk-timeline li::before { content: ""; position: absolute; left: -28px; top: 6px; width: 14px; height: 14px; border-radius: 50%; background: var(--bg); border: 2px solid var(--accent); box-sizing: border-box; }
.lk-timeline li.now::before { background: var(--accent); }
.lk-timeline .when { font-size: 13px; font-weight: 600; color: var(--accent); letter-spacing: .04em; }
.lk-timeline b { display: block; font-size: 17px; font-weight: 600; }
.lk-timeline span.where { display: block; color: var(--muted); }
.lk-timeline p { color: var(--muted); font-size: 15px; margin-top: 4px; max-width: 42em; }

/* ---- Contact footer ---- */
.lk-contact { margin: 64px 0 0; padding: 40px 0 56px; border-top: 1px solid var(--rule); display: flex; flex-wrap: wrap; justify-content: space-between; gap: 24px; align-items: flex-end; }
.lk-contact h2 { font-size: 26px; margin: 0 0 6px; }
.lk-contact p { color: var(--muted); }
.lk-updated { font-size: 13px; color: var(--muted); }

/* ---- Small screens ---- */
@media (max-width: 760px) {
  .page-content .wrapper { padding: 0 16px; }
  .lk-nav { margin: 0 -16px; padding: 0 16px; gap: 20px; }
  .lk-hero { grid-template-columns: 1fr; padding-top: 40px; gap: 24px; }
  .lk-hero .lk-avatar { order: -1; width: 96px; height: 96px; font-size: 34px; }
  .lk-hero h1 { font-size: 38px; }
  .lk-lede { font-size: 18px; }
  .lk-stats { grid-template-columns: 1fr 1fr; }
  .lk-stats div:nth-child(3) { border-left: 0; padding-left: 0; }
  .lk-stats div:nth-child(n+3) { border-top: 1px solid var(--rule); }
  .lk-cards, .lk-two, .lk-labs { grid-template-columns: 1fr; }
  .lk-two { gap: 8px; }
  .lk-pubs li, .lk-years > div { grid-template-columns: 1fr; gap: 6px; }
  .lk-venue .lk-year { display: inline; margin-left: 6px; }
}
</style>

<div class="lk">

<!-- ===== HERO ===== -->
<header class="lk-hero">
  <div>
    <p class="lk-eyebrow">Systems Neuroscience &middot; Harvard University</p>
    <h1>Lyle Kingsbury</h1>
    <p class="lk-lede">I study how the brain makes flexible decisions: how neural circuits weigh time, reward, and expectation to decide when to stay and when to move on.</p>
    <p class="lk-role">Postdoctoral Researcher and Helen Hay Whitney Fellow in the Uchida Lab, Department of Molecular and Cellular Biology.</p>
    <div class="lk-buttons">
      <a class="lk-btn primary" href="mailto:{{ site.email }}">Get in touch</a>
      <a class="lk-btn" href="{{ '/cv.pdf' | relative_url }}">Download CV</a>
      <a class="lk-btn" href="#publications">Publications</a>
    </div>
  </div>
  <div class="lk-avatar" aria-hidden="true">LK</div>
</header>

<div class="lk-stats">
  <div><b>10</b><span>publications &amp; preprints</span></div>
  <div><b>5</b><span>first-author papers</span></div>
  <div><b>9</b><span>invited talks</span></div>
  <div><b>12</b><span>trainees mentored</span></div>
</div>

<nav class="lk-nav" aria-label="Sections">
  <a href="#research">Research</a>
  <a href="#publications">Publications</a>
  <a href="#talks">Talks</a>
  <a href="#awards">Awards</a>
  <a href="#teaching">Teaching &amp; Mentoring</a>
  <a href="#background">Background</a>
</nav>

<!-- ===== RESEARCH ===== -->
<section class="lk-section" id="research">
  <h2>Research</h2>
  <p class="lk-intro">My work connects behavior, neural population dynamics, and computational models to understand how animals make decisions in changing environments, both on their own and with others.</p>
  <div class="lk-cards">
    <article class="lk-card">
      <span class="lk-tag">Current &middot; Harvard</span>
      <h3>Flexible foraging decisions</h3>
      <p>When should an animal leave a food patch that is running out? I study how mice make these stay-or-leave decisions, and how neural populations integrate time and reward to guide them. Our recent work shows that decisions adapt to new conditions by reconfiguring orthogonal integrator dynamics.</p>
      <div class="lk-papers"><a href="#pub-integrators">Kingsbury et al., 2026</a> &middot; <a href="#pub-bukwich">Bukwich et al., 2025</a></div>
    </article>
    <article class="lk-card">
      <span class="lk-tag">Current &middot; Harvard</span>
      <h3>Dopamine and learned value</h3>
      <p>Dopamine neurons signal how much better or worse a reward was than expected. I am testing how these signals teach animals what to expect from their environment, and how those learned value expectations shape foraging choices.</p>
      <div class="lk-papers"><a href="#pub-dopamine">Kingsbury, May et al., 2026</a></div>
    </article>
    <article class="lk-card">
      <span class="lk-tag">Ph.D. &middot; UCLA</span>
      <h3>The social brain, across brains</h3>
      <p>Using calcium imaging in freely behaving mice, I showed how the cortex represents the sex of other animals, and that neural activity becomes correlated across the brains of animals as they interact. This led to a multi-brain framework for studying social behavior.</p>
      <div class="lk-papers"><a href="#pub-cell">Cell 2019</a> &middot; <a href="#pub-neuron">Neuron 2020</a> &middot; <a href="#pub-tins">TINS 2020</a></div>
    </article>
  </div>
</section>

<!-- ===== PUBLICATIONS ===== -->
<section class="lk-section" id="publications">
  <h2>Publications</h2>
  <p class="lk-intro">Click a title to open the paper. <sup>*</sup>Equal contribution.</p>

  <h3 class="lk-sub">Preprints</h3>
  <ul class="lk-pubs">
    <li id="pub-integrators">
      <div class="lk-venue">bioRxiv<span class="lk-year">2026</span></div>
      <div>
        <a class="lk-pub-title" href="https://www.biorxiv.org/content/10.1101/2025.11.14.688540v3">Flexible foraging decisions by configuration of orthogonal integrator dynamics</a>
        <p class="lk-authors"><b>Kingsbury L</b>, Zhang G, Sanguinetti-Scheck JI, Uchida N</p>
        <p class="lk-extra"><span class="lk-pill">Under review</span></p>
      </div>
    </li>
    <li id="pub-dopamine">
      <div class="lk-venue">bioRxiv<span class="lk-year">2026</span></div>
      <div>
        <a class="lk-pub-title" href="https://www.biorxiv.org/content/10.64898/2026.10.21.760765v1">Dopaminergic reward signals shape foraging decisions through learned value expectations</a>
        <p class="lk-authors"><b>Kingsbury L*</b>, May HV*, Uchida N</p>
      </div>
    </li>
  </ul>

  <h3 class="lk-sub">Journal articles</h3>
  <ul class="lk-pubs">
    <li>
      <div class="lk-venue">Nature<span class="lk-year">2025</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1038/s41586-025-09196-4">Inter-brain neural dynamics in biological and artificial intelligence systems</a>
        <p class="lk-authors">Zhang X, Phi N, Li Q, Gorzek R, Zwingenberger N, Huang S, Zhou JL, <b>Kingsbury L</b>, Raam T, Wu YE, Wei D, Kao JC, Hong W</p>
      </div>
    </li>
    <li id="pub-bukwich">
      <div class="lk-venue">Neuron<span class="lk-year">2025</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1016/j.neuron.2025.07.008">Competitive integration of time and reward explains value-sensitive foraging decisions and frontal cortex ramping dynamics</a>
        <p class="lk-authors">Bukwich M, Campbell MG, Zoltowski D, <b>Kingsbury L</b>, Tomov MS, Stern J, Kim HR, Drugowitsch J, Linderman SW, Uchida N</p>
      </div>
    </li>
    <li>
      <div class="lk-venue">Nature<span class="lk-year">2021</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1038/s41586-021-03962-w">Neural control of affiliative touch in prosocial interaction</a>
        <p class="lk-authors">Wu YE, Dang J, <b>Kingsbury L</b>, Zhang M, Sun F, Hu RK, Hong W</p>
      </div>
    </li>
    <li id="pub-neuron">
      <div class="lk-venue">Neuron<span class="lk-year">2020</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1016/j.neuron.2020.06.020">Cortical representations of conspecific sex shape social behavior</a>
        <p class="lk-authors"><b>Kingsbury L*</b>, Huang S*, Raam T, Ye LS, Wei D, Hu RK, Ye L, Hong W</p>
      </div>
    </li>
    <li id="pub-tins">
      <div class="lk-venue">Trends in Neurosciences<span class="lk-year">2020</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1016/j.tins.2020.06.008">A multi-brain framework for social interaction</a>
        <p class="lk-authors"><b>Kingsbury L</b>, Hong W</p>
        <p class="lk-extra"><span class="lk-pill">Review</span></p>
      </div>
    </li>
    <li>
      <div class="lk-venue">Biological Psychiatry<span class="lk-year">2020</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1016/j.biopsych.2019.12.028">Reciprocal copy number variations at 22q11.2 produce distinct and convergent neurobehavioral impairments relevant for schizophrenia and autism spectrum disorder</a>
        <p class="lk-authors">Lin A, Vajdi A, Kushan-Wells L, Helleman G, Hansen LP, Jonas RK, Jalbrzikowski M, <b>Kingsbury L</b>, Raznahan A, Bearden CE</p>
      </div>
    </li>
    <li id="pub-cell">
      <div class="lk-venue">Cell<span class="lk-year">2019</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1016/j.cell.2019.05.022">Correlated neural activity and encoding of behavior across brains of socially interacting animals</a>
        <p class="lk-authors"><b>Kingsbury L*</b>, Huang S*, Wang J, Gu K, Golshani P, Wu YE, Hong W</p>
        <p class="lk-extra">Highlighted in <i>Cell</i> by Omer, Zilkha &amp; Kimchi &middot; <a href="https://www.nytimes.com/2021/05/25/science/optogenetics-brain-social-behavior.html">Covered in The New York Times</a></p>
      </div>
    </li>
    <li>
      <div class="lk-venue">Scientific Reports<span class="lk-year">2016</span></div>
      <div>
        <a class="lk-pub-title" href="https://doi.org/10.1038/srep33751">Myelinating glia differentiation is regulated by extracellular matrix elasticity</a>
        <p class="lk-authors">Urbanski MM, <b>Kingsbury L</b>, Moussouros D, Kassim I, Mehjabeen S, Paknejad N, Melendez-Vasquez CV</p>
      </div>
    </li>
  </ul>
</section>

<!-- ===== TALKS ===== -->
<section class="lk-section" id="talks">
  <h2>Invited Talks</h2>
  <p class="lk-intro">Seminars, symposia, and award lectures.</p>
  <div class="lk-years">
    <div><span class="yr">2026</span><ul><li>Harvard MCB <span>&middot; Slice of Science</span></li></ul></div>
    <div><span class="yr">2025</span><ul>
      <li>Harvard University, Department of Neurobiology <span>&middot; Seminar series</span></li>
      <li>Harvard MCB <span>&middot; Department retreat</span></li>
      <li>Helen Hay Whitney Foundation <span>&middot; Fellows meeting</span></li>
      <li>Southern Illinois University <span>&middot; Neuroscience seminar series</span></li>
    </ul></div>
    <div><span class="yr">2022</span><ul>
      <li>Keystone Symposium on Social Behavior <span>&middot; KAIST</span></li>
      <li>University of Z&uuml;rich <span>&middot; Brain Diseases Prize lecture</span></li>
    </ul></div>
    <div><span class="yr">2021</span><ul><li>UCLA <span>&middot; Samuel Eiduson Student Lecture</span></li></ul></div>
    <div><span class="yr">2020</span><ul><li>UCLA <span>&middot; Synapse to Circuits seminar</span></li></ul></div>
  </div>
</section>

<!-- ===== AWARDS ===== -->
<section class="lk-section" id="awards">
  <h2>Awards &amp; Fellowships</h2>
  <p class="lk-intro">Research prizes and competitive funding.</p>
  <div class="lk-two">
    <div>
      <h3 class="lk-sub">Prizes</h3>
      <ul class="lk-list">
        <li>Donald B. Lindsley Prize in Behavioral Neuroscience, Society for Neuroscience <span class="when">2022</span></li>
        <li>University of Z&uuml;rich Brain Diseases Prize <span class="when">2022</span></li>
        <li>Harold M. Weintraub Graduate Student Award <span class="when">2021</span></li>
        <li>Samuel Eiduson Student Lecture Award, UCLA <span class="when">2020</span></li>
        <li>SfN Travel Award, UCLA Brain Research Institute &amp; Semel Institute <span class="when">2019</span></li>
        <li>Else Seringhaus Award in Biological Sciences, Hunter College <span class="when">2015</span></li>
        <li>Most Outstanding Research Award <span class="when">2014</span></li>
      </ul>
    </div>
    <div>
      <h3 class="lk-sub">Fellowships &amp; funding</h3>
      <ul class="lk-list">
        <li>Helen Hay Whitney Foundation Postdoctoral Fellowship <span class="when">2023&ndash;26</span></li>
        <li>NIH F31 Ruth L. Kirschstein NRSA <span class="when">2018&ndash;21</span></li>
        <li>NIH/NINDS T32 Training Program in Neural Microcircuits <span class="when">2017&ndash;18</span></li>
        <li>ARCS Foundation Fellowship <span class="when">2016&ndash;19</span></li>
        <li>Thomas Hunter Honors Program, Hunter College <span class="when">2013&ndash;15</span></li>
      </ul>
    </div>
  </div>
</section>

<!-- ===== TEACHING & MENTORING ===== -->
<section class="lk-section" id="teaching">
  <h2>Teaching &amp; Mentoring</h2>
  <p class="lk-intro">I have taught neuroscience from high school to graduate level, and mentored twelve trainees, from high-school students to Ph.D. students, across three labs.</p>

  <h3 class="lk-sub">Teaching</h3>
  <div class="lk-courses">
    <div class="lk-course"><b>Experimental Neuroscience</b><span class="meta">Belmont Hill School &middot; Spring 2026</span><p>Hands-on electrophysiology in invertebrates and plants, plus statistics lectures, for advanced high-school students (with Dr. Harry Goldberg).</p></div>
    <div class="lk-course"><b>Systems Neuroscience</b><span class="meta">UCLA Neuro M205 &middot; Winter 2020</span><p>Graduate course on perception, learning and memory models, executive function, and motor control.</p></div>
    <div class="lk-course"><b>Neurophysiology</b><span class="meta">UCLA Neuro M202 &middot; Fall 2017</span><p>Graduate course on neuronal signaling, action potential models, and synaptic transmission.</p></div>
    <div class="lk-course"><b>Neuroscientific Methods</b><span class="meta">UCLA Neuro 210B &middot; Winter 2017</span><p>Co-designed and co-taught a new seminar curriculum on modern neuroscience techniques (with Amy Lin).</p></div>
    <div class="lk-course"><b>Functional Neuroanatomy</b><span class="meta">UCLA Neuro 201 &middot; Fall 2016</span><p>Developed and led lab exercises and group lessons for an undergraduate course.</p></div>
  </div>

  <h3 class="lk-sub">Trainees</h3>
  <div class="lk-labs">
    <div>
      <h3>Uchida Lab</h3><span class="where">Harvard &middot; 2021&ndash;present</span>
      <ul>
        <li>Marcos Garcia<span>Undergraduate &middot; current</span></li>
        <li>Cassidy Cheng<span>Undergraduate &middot; current</span></li>
        <li>Grace Zhang<span>Undergraduate &middot; 2 years</span></li>
        <li>Hugo Vernon May<span>Master's student, EPFL &middot; 6 months</span></li>
        <li>Tarek Jabri<span>Ph.D. student &middot; 4 months</span></li>
        <li>Zhiqin (Carol) Chen<span>Summer undergraduate &middot; 3 months</span></li>
      </ul>
    </div>
    <div>
      <h3>Hong Lab</h3><span class="where">UCLA &middot; 2016&ndash;2021</span>
      <ul>
        <li>Letizia Ye<span>Undergraduate, then Ph.D. student &middot; 3 years</span></li>
        <li>Jun Wang<span>Undergraduate &middot; 2.5 years</span></li>
        <li>Andrew Yang<span>High-school student &middot; 2 years</span></li>
        <li>Nguyen Phi<span>Ph.D. student &middot; 1 year</span></li>
        <li>Devyn Fisher<span>Undergraduate &middot; 1 year</span></li>
      </ul>
    </div>
    <div>
      <h3>Melendez-Vasquez Lab</h3><span class="where">Hunter College &middot; 2013&ndash;2015</span>
      <ul>
        <li>Brenda Abdelmesih<span>Undergraduate &middot; 1 year</span></li>
      </ul>
      <h3 class="lk-sub">Service</h3>
      <div class="lk-service">Ad hoc reviewer for <i>Nature</i>, <i>Nature Neuroscience</i>, <i>Neuron</i>, and <i>eLife</i></div>
    </div>
  </div>
</section>

<!-- ===== BACKGROUND ===== -->
<section class="lk-section" id="background">
  <h2>Background</h2>
  <p class="lk-intro">From bioinformatics and glial biology to circuits and behavior.</p>
  <ul class="lk-timeline">
    <li class="now">
      <span class="when">2021 &ndash; PRESENT</span>
      <b>Postdoctoral Researcher &middot; Helen Hay Whitney Fellow</b>
      <span class="where">Harvard University, Molecular and Cellular Biology &middot; Lab of Naoshige Uchida</span>
      <p>Neural dynamics and dopamine signals underlying flexible foraging decisions.</p>
    </li>
    <li>
      <span class="when">2016 &ndash; 2021</span>
      <b>Ph.D. in Neuroscience</b>
      <span class="where">University of California, Los Angeles &middot; Lab of Weizhe Hong</span>
      <p>Cortical coding of social cues and inter-brain neural dynamics, using <i>in vivo</i> microendoscope calcium imaging, dual-animal imaging, statistical models, and optogenetic circuit mapping.</p>
    </li>
    <li>
      <span class="when">2013 &ndash; 2015</span>
      <b>B.A. in Bioinformatics</b>
      <span class="where">Hunter College, City University of New York &middot; Lab of Carmen Melendez-Vasquez</span>
      <p>Signaling and extracellular-matrix mechanisms of myelin formation in glial cells.</p>
    </li>
    <li>
      <span class="when">2011 &ndash; 2012</span>
      <b>Interdisciplinary Science</b>
      <span class="where">Eugene Lang College, The New School</span>
    </li>
  </ul>
</section>

<!-- ===== CONTACT ===== -->
<footer class="lk-contact">
  <div>
    <h2>Get in touch</h2>
    <p><a href="mailto:{{ site.email }}">{{ site.email }}</a> &middot; Somerville, MA</p>
  </div>
  <p class="lk-updated">Last updated {{ site.time | date: "%B %Y" }} &middot; <a href="{{ '/cv.pdf' | relative_url }}">Full CV (PDF)</a></p>
</footer>

</div>
