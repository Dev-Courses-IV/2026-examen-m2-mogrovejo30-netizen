<script setup>
import NavBar from './components/NavBar.vue'
import ServiciosSection from './components/ServiciosSection.vue'
</script>

<template>
  <div id="app">
    <NavBar />

    <!-- Hero -->
    <section id="inicio" class="hero">
      <div class="hero-glow"></div>
      <div class="hero-inner">
        <span class="hero-badge">🚀 Agencia de Inteligencia Artificial #1 en España</span>
        <h1 class="hero-title">
          Transforma tus Ventas<br />
          con el poder de la <span class="gradient-text">IA</span>
        </h1>
        <p class="hero-subtitle">
          En <strong>Crear IA</strong> diseñamos soluciones de inteligencia artificial
          a medida que automatizan, predicen y escalan tus resultados comerciales.
          Deja que la tecnología trabaje por ti.
        </p>
        <div class="hero-actions">
          <a href="#servicios" class="btn-primary">Ver servicios</a>
          <a href="#contacto" class="btn-ghost">Hablar con un experto →</a>
        </div>

        <div class="hero-stats">
          <div class="stat-item">
            <span class="stat-number">+300%</span>
            <span class="stat-label">Aumento promedio en ventas</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat-item">
            <span class="stat-number">500+</span>
            <span class="stat-label">Clientes satisfechos</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat-item">
            <span class="stat-number">24/7</span>
            <span class="stat-label">Automatización continua</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Servicios -->
    <ServiciosSection />

    <!-- Nosotros -->
    <section id="nosotros" class="about-section">
      <div class="about-inner">
        <div class="about-text">
          <span class="section-tag">Sobre Crear IA</span>
          <h2 class="about-title">
            Expertos en IA aplicada a <span class="gradient-text">negocios reales</span>
          </h2>
          <p class="about-desc">
            Somos un equipo de ingenieros, científicos de datos y estrategas comerciales
            apasionados por una única misión: hacer que la inteligencia artificial trabaje
            para tu empresa. No vendemos promesas, entregamos resultados medibles.
          </p>
          <ul class="about-features">
            <li>✅ Implementación en menos de 2 semanas</li>
            <li>✅ Soporte dedicado en español</li>
            <li>✅ Sin costes ocultos ni contratos largos</li>
            <li>✅ Resultados garantizados o te devolvemos el dinero</li>
          </ul>
        </div>
        <div class="about-card">
          <div class="about-metric">
            <span class="metric-value">98%</span>
            <span class="metric-label">Tasa de satisfacción del cliente</span>
          </div>
          <div class="about-metric">
            <span class="metric-value">€12M+</span>
            <span class="metric-label">Generados para nuestros clientes en 2025</span>
          </div>
          <div class="about-metric">
            <span class="metric-value">3 años</span>
            <span class="metric-label">Liderando la IA comercial en Europa</span>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Contacto -->
    <section id="contacto" class="cta-section">
      <div class="cta-inner">
        <h2 class="cta-title">¿Listo para multiplicar tus ventas?</h2>
        <p class="cta-subtitle">
          Agenda una demo gratuita y descubre cómo la IA puede transformar tu negocio en semanas.
        </p>
        <form class="cta-form" @submit.prevent>
          <input type="email" placeholder="tu@empresa.com" class="cta-input" />
          <button type="submit" class="btn-primary">Solicitar demo gratis</button>
        </form>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="footer-inner">
        <span class="logo-name">⚡ Crear <span class="logo-accent">IA</span></span>
        <p class="footer-copy">© 2026 Crear IA — Todos los derechos reservados.</p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
/* Hero */
.hero {
  position: relative;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 120px 24px 80px;
  overflow: hidden;
  text-align: center;
}

.hero-glow {
  position: absolute;
  top: 10%;
  left: 50%;
  transform: translateX(-50%);
  width: 700px;
  height: 400px;
  background: radial-gradient(ellipse at center, rgba(108, 99, 255, 0.18) 0%, transparent 70%);
  pointer-events: none;
}

.hero-inner {
  max-width: 820px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 24px;
  position: relative;
  z-index: 1;
}

.hero-badge {
  background: rgba(108, 99, 255, 0.12);
  border: 1px solid rgba(108, 99, 255, 0.3);
  color: #a78bfa;
  padding: 8px 20px;
  border-radius: 24px;
  font-size: 13px;
  font-weight: 600;
}

.hero-title {
  font-size: clamp(36px, 6vw, 68px);
  font-weight: 900;
  color: #f1f5f9;
  line-height: 1.1;
  letter-spacing: -1.5px;
}

.hero-subtitle {
  font-size: clamp(15px, 2vw, 18px);
  color: #64748b;
  max-width: 620px;
  line-height: 1.75;
}

.hero-subtitle strong {
  color: #a78bfa;
}

.hero-actions {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 8px;
}

.btn-primary {
  background: linear-gradient(135deg, #6c63ff, #00d4ff);
  color: #fff;
  padding: 14px 32px;
  border-radius: 10px;
  font-size: 15px;
  font-weight: 700;
  text-decoration: none;
  border: none;
  cursor: pointer;
  transition: opacity 0.2s, transform 0.2s;
}

.btn-primary:hover {
  opacity: 0.88;
  transform: translateY(-2px);
}

.btn-ghost {
  color: #94a3b8;
  padding: 14px 24px;
  border-radius: 10px;
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
  transition: color 0.2s;
}

.btn-ghost:hover {
  color: #e2e8f0;
}

.hero-stats {
  display: flex;
  align-items: center;
  gap: 32px;
  margin-top: 24px;
  padding: 28px 40px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.07);
  border-radius: 16px;
  flex-wrap: wrap;
  justify-content: center;
}

.stat-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
}

.stat-number {
  font-size: 28px;
  font-weight: 900;
  background: linear-gradient(135deg, #6c63ff, #00d4ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.stat-label {
  font-size: 12px;
  color: #475569;
  text-align: center;
}

.stat-divider {
  width: 1px;
  height: 40px;
  background: rgba(255, 255, 255, 0.08);
}

/* About */
.about-section {
  padding: 100px 24px;
  background: rgba(108, 99, 255, 0.04);
  border-top: 1px solid rgba(108, 99, 255, 0.1);
  border-bottom: 1px solid rgba(108, 99, 255, 0.1);
}

.about-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 64px;
  align-items: center;
}

.about-text {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.section-tag {
  display: inline-block;
  background: rgba(108, 99, 255, 0.15);
  color: #a78bfa;
  border: 1px solid rgba(108, 99, 255, 0.35);
  padding: 6px 18px;
  border-radius: 20px;
  font-size: 13px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  align-self: flex-start;
}

.about-title {
  font-size: clamp(24px, 3.5vw, 36px);
  font-weight: 800;
  color: #f1f5f9;
  line-height: 1.2;
  letter-spacing: -0.5px;
}

.about-desc {
  font-size: 15px;
  color: #64748b;
  line-height: 1.75;
}

.about-features {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.about-features li {
  font-size: 14px;
  color: #94a3b8;
  font-weight: 500;
}

.about-card {
  background: #111224;
  border: 1px solid rgba(108, 99, 255, 0.2);
  border-radius: 20px;
  padding: 36px;
  display: flex;
  flex-direction: column;
  gap: 28px;
}

.about-metric {
  display: flex;
  flex-direction: column;
  gap: 4px;
  padding-bottom: 24px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.about-metric:last-child {
  border-bottom: none;
  padding-bottom: 0;
}

.metric-value {
  font-size: 32px;
  font-weight: 900;
  background: linear-gradient(135deg, #6c63ff, #00d4ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.metric-label {
  font-size: 13px;
  color: #64748b;
}

@media (max-width: 768px) {
  .about-inner {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}

/* CTA */
.cta-section {
  padding: 100px 24px;
  text-align: center;
}

.cta-inner {
  max-width: 600px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}

.cta-title {
  font-size: clamp(26px, 4vw, 42px);
  font-weight: 800;
  color: #f1f5f9;
  letter-spacing: -0.8px;
}

.cta-subtitle {
  font-size: 16px;
  color: #64748b;
  line-height: 1.65;
}

.cta-form {
  display: flex;
  gap: 12px;
  width: 100%;
  margin-top: 8px;
  flex-wrap: wrap;
  justify-content: center;
}

.cta-input {
  flex: 1;
  min-width: 200px;
  background: #111224;
  border: 1px solid rgba(108, 99, 255, 0.3);
  color: #e2e8f0;
  padding: 14px 18px;
  border-radius: 10px;
  font-size: 15px;
  outline: none;
  transition: border-color 0.2s;
}

.cta-input::placeholder {
  color: #475569;
}

.cta-input:focus {
  border-color: rgba(108, 99, 255, 0.7);
}

/* Footer */
.footer {
  border-top: 1px solid rgba(255, 255, 255, 0.06);
  padding: 32px 24px;
}

.footer-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 12px;
}

.logo-name {
  font-size: 18px;
  font-weight: 700;
  color: #e2e8f0;
}

.logo-accent {
  background: linear-gradient(135deg, #6c63ff, #00d4ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.footer-copy {
  font-size: 13px;
  color: #475569;
}
</style>
