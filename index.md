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
            {% if project.url %}<a href="{{ project.url }}" target="_blank" rel="noopener noreferrer">{{ project.name }}</a>{% else %}{{ project.name }}{% endif %}
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
            {% if project.url %}<a href="{{ project.url }}" target="_blank" rel="noopener noreferrer">{{ project.name }}</a>{% else %}{{ project.name }}{% endif %}
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
