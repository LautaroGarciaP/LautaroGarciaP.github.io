---
layout: default
---

<main id="main-content">
  <header class="hero">
    <img
      src="https://avatars.githubusercontent.com/u/104364638?v=4"
      alt="Foto de perfil de Lautaro Garcia"
      class="avatar"
      width="96"
      height="96"
      loading="eager"
    >
    <div class="hero-text">
      <h1>Lautaro Garcia</h1>
      <p class="tagline" data-lang="en">{{ site.data.i18n.en.tagline }}</p>
      <p class="tagline" data-lang="es" hidden>{{ site.data.i18n.es.tagline }}</p>
    </div>
  </header>

  <section id="proyectos" aria-labelledby="proyectos-heading">
    <h2 id="proyectos-heading" data-lang="en">{{ site.data.i18n.en.projects_heading }}</h2>
    <h2 data-lang="es" hidden>{{ site.data.i18n.es.projects_heading }}</h2>
    <div class="project-grid">
      {% for project in site.data.projects_en %}
      <article class="project-card" data-lang="en">
        <div class="project-header">
          <h3>
            {{ project.name }}
            {% if project.url %}
            <a href="{{ project.url }}" target="_blank" rel="noopener noreferrer" class="project-github" aria-label="GitHub repository">
              <svg viewBox="0 0 24 24" width="22" height="22" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
            </a>
            {% endif %}
          </h3>
          {% if project.role %}
          <span class="project-role">{{ project.role }}</span>
          {% endif %}
        </div>
        <p>{{ project.description }}</p>
        {% if project.stack %}
        <div class="stack">
          {% for tech in project.stack %}
          <span>{{ tech }}</span>
          {% endfor %}
        </div>
        {% endif %}
      </article>
      {% endfor %}
      {% for project in site.data.projects_es %}
      <article class="project-card" data-lang="es" hidden>
        <div class="project-header">
          <h3>
            {{ project.name }}
            {% if project.url %}
            <a href="{{ project.url }}" target="_blank" rel="noopener noreferrer" class="project-github" aria-label="GitHub repository">
              <svg viewBox="0 0 24 24" width="22" height="22" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
            </a>
            {% endif %}
          </h3>
          {% if project.role %}
          <span class="project-role">{{ project.role }}</span>
          {% endif %}
        </div>
        <p>{{ project.description }}</p>
        {% if project.stack %}
        <div class="stack">
          {% for tech in project.stack %}
          <span>{{ tech }}</span>
          {% endfor %}
        </div>
        {% endif %}
      </article>
      {% endfor %}
    </div>
  </section>

  <section id="sobre-mi" aria-labelledby="sobre-mi-heading">
    <h2 id="sobre-mi-heading" data-lang="en">{{ site.data.i18n.en.about_heading }}</h2>
    <h2 data-lang="es" hidden>{{ site.data.i18n.es.about_heading }}</h2>
    <div class="about">
      <p data-lang="en">{{ site.data.i18n.en.about_p1 }}</p>
      <p data-lang="es" hidden>{{ site.data.i18n.es.about_p1 }}</p>
      <p data-lang="en">{{ site.data.i18n.en.about_p2 }}</p>
      <p data-lang="es" hidden>{{ site.data.i18n.es.about_p2 }}</p>
    </div>
  </section>

  <section id="stack" aria-labelledby="stack-heading">
    <h2 id="stack-heading" data-lang="en">{{ site.data.i18n.en.stack_heading }}</h2>
    <h2 data-lang="es" hidden>{{ site.data.i18n.es.stack_heading }}</h2>
    <div class="stack-grid">
      <div class="stack-category">
        <h3 data-lang="en">{{ site.data.i18n.en.cat_languages }}</h3>
        <h3 data-lang="es" hidden>{{ site.data.i18n.es.cat_languages }}</h3>
        <div class="stack">
          <span>C++</span>
          <span>Java</span>
          <span>Python</span>
          <span>SQL</span>
        </div>
      </div>
      <div class="stack-category">
        <h3 data-lang="en">{{ site.data.i18n.en.cat_tech }}</h3>
        <h3 data-lang="es" hidden>{{ site.data.i18n.es.cat_tech }}</h3>
        <div class="stack">
          <span>PostgreSQL</span>
          <span>Docker</span>
          <span>FastAPI</span>
          <span>Git</span>
        </div>
      </div>
      <div class="stack-category">
        <h3 data-lang="en">{{ site.data.i18n.en.cat_interests }}</h3>
        <h3 data-lang="es" hidden>{{ site.data.i18n.es.cat_interests }}</h3>
        <div class="stack">
          <span>Ciberseguridad</span>
          <span>Compiladores</span>
          <span>CLI Tools</span>
          <span>AI Agents</span>
        </div>
      </div>
    </div>
  </section>

  <section id="contacto" aria-labelledby="contacto-heading">
    <h2 id="contacto-heading" data-lang="en">{{ site.data.i18n.en.contact_heading }}</h2>
    <h2 data-lang="es" hidden>{{ site.data.i18n.es.contact_heading }}</h2>
    <div class="contact-links">
      <a href="https://github.com/LautaroGarciaP" target="_blank" rel="noopener noreferrer me">GitHub</a>
      <a href="mailto:lautarogarciap@duck.com" rel="me">Email</a>
    </div>
  </section>
</main>

<footer role="contentinfo">
  {{ site.data.i18n.en.copyright }} {{ site.time | date: '%Y' }} {{ site.title }}
</footer>
