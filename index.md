---
layout: default
og_title: "Siddhant Tiwary - Software Engineer & AI Systems Architect"
og_description: "Software engineer specializing in AI systems, app development, and backend architecture."
---

<header id="about" class="hero">
  <h1>Hey, I'm <span class="name-accent">Siddhant</span>.</h1>
  <p class="lede">
    Senior Software Engineer based in Bangalore. I architect high-throughput backends, distributed systems, and the orchestration layers for agentic AI.
  </p>
</header>

<section id="experience" class="page-section" aria-labelledby="experience-heading">
  <div class="section-head">
    <h2 id="experience-heading">Experience</h2>
    <p class="section-kicker">Roles &amp; impact</p>
  </div>
  <div class="section-stack">
    <article class="card">
      <header class="card-head">
        <h3 class="card-title">Founding Engineer</h3>
        <p class="card-org">Stealth AI startup</p>
        <p class="card-meta">Remote · Jan 2026 – Mar 2026</p>
      </header>
      <ul class="card-list">
        <li>Architected an LLM orchestration layer combining real-time biometrics (HealthKit/EHR) with knowledge graphs and semantic search; used pre-aggregated profiles to reduce compute while surfacing medical insights via tool-calling.</li>
        <li>Integrated VAPI as a voice layer on the existing conversation engine with VAD-based turn detection without duplicating conversation state.</li>
        <li>Built a stratified prompt-context layer and instrumented LangSmith tracing for tighter evals.</li>
        <li>Led HIPAA-oriented security design for PHI and coordinated App Store and regulatory workstreams.</li>
      </ul>
    </article>
    <article class="card">
      <header class="card-head">
        <h3 class="card-title">Software Engineer, Core Platform</h3>
        <p class="card-org"><a href="https://lyric.tech/" target="_blank" rel="noopener noreferrer">Lyric</a></p>
        <p class="card-meta">Bangalore · Mar 2025 – Feb 2026</p>
      </header>
      <ul class="card-list">
        <li>Introduced Argo Workflows to orchestrate and track executions with configurable resources.</li>
        <li>Deployed an in-cluster Harbor proxy cache to avoid upstream rate limits, speed up image pulls, and cut network cost.</li>
        <li>Built a centralized migration service for schema and data migrations across multiple databases.</li>
      </ul>
    </article>
    <article class="card">
      <header class="card-head">
        <h3 class="card-title">Software Engineer, BankConnect</h3>
        <p class="card-org"><a href="https://finbox.in/" target="_blank" rel="noopener noreferrer">FinBox</a></p>
        <p class="card-meta">Bangalore · Jun 2022 – Mar 2025</p>
      </header>
      <ul class="card-list">
        <li>Migrated production workloads from AWS Lambda to Kubernetes on spot instances, cutting latency ~68% and cost ~50%; used Ray for distributed workloads.</li>
        <li>Designed and shipped a multi-tenant FIU module for bank account data aggregation, serving 5M+ users across 100+ clients.</li>
        <li>Improved DynamoDB access with a Redis cache layer, reducing RCU use and eliminating read throttles.</li>
        <li>Replaced an O(n) completion tracker with an atomic O(1) counter for distributed extraction jobs.</li>
        <li>Stood up Kafka (streaming), Vector (batching), and ClickHouse for analytics and monitoring.</li>
      </ul>
    </article>
  </div>
</section>

<section id="projects" class="page-section" aria-labelledby="projects-heading">
  <div class="section-head">
    <h2 id="projects-heading">Projects</h2>
    <p class="section-kicker">Selected work</p>
  </div>
  <div class="section-stack">
    {% for p in site.data.projects %}
    <article class="card card--compact project-card">
      <header class="card-head">
        <div class="card-head-text">
          <h3 class="card-title">{{ p.title }}</h3>
          <p class="card-meta">{{ p.period }}</p>
        </div>
        <p class="card-actions">
          {% if p.live %}
          <a class="btn-live" href="{{ p.live }}" target="_blank" rel="noopener noreferrer nofollow">
            <svg class="btn-github-icon" width="16" height="16" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6M15 3h6v6M10 14 21 3"/></svg>
            Live
          </a>
          {% endif %}
          <a class="btn-github" href="{{ p.github }}" target="_blank" rel="noopener noreferrer">
            <svg class="btn-github-icon" width="16" height="16" viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path fill="currentColor" d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.111.825-.261.825-.585 0-.291-.015-1.256-.015-2.28-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .33.225.705.825.585A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
            GitHub
          </a>
        </p>
      </header>
      <ul class="card-list">
        {% for point in p.points %}
        <li>{{ point }}</li>
        {% endfor %}
      </ul>
    </article>
    {% endfor %}
  </div>
</section>

<section id="blogs" class="page-section" aria-labelledby="blogs-heading">
  <div class="section-head">
    <h2 id="blogs-heading">Blogs</h2>
    <p class="section-kicker">Writing</p>
  </div>
  <div class="section-stack">
    {% for b in site.data.blogs %}
    <article class="card card--compact blog-card">
      <header class="card-head">
        <div class="card-head-text">
          <h3 class="card-title">
            <a href="{{ b.url }}" target="_blank" rel="noopener noreferrer">{{ b.title }}</a>
          </h3>
          <p class="card-meta">{{ b.publication }}</p>
        </div>
      </header>
    </article>
    {% endfor %}
  </div>
</section>

<section id="education" class="page-section" aria-labelledby="education-heading">
  <div class="section-head">
    <h2 id="education-heading">Education</h2>
    <p class="section-kicker">Background</p>
  </div>
  <div class="section-stack">
    <article class="card">
      <header class="card-head">
        <h3 class="card-title">B.Tech in Computer Science</h3>
        <p class="card-org"><a href="https://vit.ac.in/" target="_blank" rel="noopener noreferrer">Vellore Institute of Technology</a></p>
        <p class="card-meta">Vellore · Jul 2018 – May 2022 · GPA 9.16/10</p>
      </header>
    </article>
  </div>
</section>

<section id="connect" class="page-section page-section--connect" aria-labelledby="connect-heading">
  <div class="section-head">
    <h2 id="connect-heading">Connect</h2>
    <p class="section-kicker">Email &amp; social</p>
  </div>
  <div class="section-body">
    {% include connect-social.html %}
  </div>
</section>
