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
      <p class="tagline">Ingeniería de Sistemas — UNICEN</p>
    </div>
  </header>

  <section id="proyectos" aria-labelledby="proyectos-heading">
    <h2 id="proyectos-heading">Proyectos</h2>
    <div class="project-grid">
      {% for project in site.data.projects %}
      <article class="project-card">
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
    <h2 id="sobre-mi-heading">Sobre mí</h2>
    <div class="about">
      <p>
        Estoy por recibirme de Ingeniero en Sistemas en UNICEN.
        Hago cosas en Java, Python y C++ — Nada perfecto, siempre util.
      </p>
      <p>
        Fuera de la compu, jugué al handball durante más de una década
        y algo de beach handball también. Me gusta armar cosas que funcionen
        y mas si se ven bien.
      </p>
    </div>
  </section>

  <section id="stack" aria-labelledby="stack-heading">
    <h2 id="stack-heading">Stack</h2>
    <div class="stack-grid">
      <div class="stack-category">
        <h3>Lenguajes</h3>
        <div class="stack">
          <span>C++</span>
          <span>Java</span>
          <span>Python</span>
          <span>SQL</span>
        </div>
      </div>
      <div class="stack-category">
        <h3>Tecnologías</h3>
        <div class="stack">
          <span>PostgreSQL</span>
          <span>Docker</span>
          <span>FastAPI</span>
          <span>Git</span>
        </div>
      </div>
      <div class="stack-category">
        <h3>Intereses</h3>
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
    <h2 id="contacto-heading">Contacto</h2>
    <div class="contact-links">
      <a href="https://github.com/LautaroGarciaP" target="_blank" rel="noopener noreferrer me">GitHub</a>
      <a href="mailto:lautaro.pipi@gmail.com" rel="me">Email</a>
    </div>
  </section>
</main>

<footer role="contentinfo">
  &copy; {{ site.time | date: '%Y' }} {{ site.title }}
</footer>
