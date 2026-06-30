<script setup>
const navLinks = [
  { label: 'Inicio', href: '#inicio' },
  { label: 'Servicios', href: '#servicios' },
  { label: 'Nosotros', href: '#nosotros' },
  { label: 'Contacto', href: '#contacto' },
]
</script>

<template>
  <nav class="navbar">
    <div class="navbar-inner">
      <a href="#inicio" class="logo">
        <span class="logo-icon">⚡</span>
        <span class="logo-name">Crear <span class="logo-accent">IA</span></span>
      </a>

      <ul class="nav-links">
        <li v-for="link in navLinks" :key="link.label">
          <a :href="link.href">{{ link.label }}</a>
        </li>
      </ul>

      <a href="#contacto" class="btn-nav">Empezar ahora</a>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  background: rgba(10, 11, 20, 0.85);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(108, 99, 255, 0.2);
}

.navbar-inner {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
  height: 68px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 32px;
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  flex-shrink: 0;
}

.logo-icon {
  font-size: 24px;
}

.logo-name {
  font-size: 22px;
  font-weight: 700;
  color: #e2e8f0;
  letter-spacing: -0.5px;
}

.logo-accent {
  background: linear-gradient(135deg, #6c63ff, #00d4ff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 32px;
}

.nav-links a {
  color: #94a3b8;
  text-decoration: none;
  font-size: 15px;
  font-weight: 500;
  transition: color 0.2s;
}

.nav-links a:hover {
  color: #e2e8f0;
}

.btn-nav {
  background: linear-gradient(135deg, #6c63ff, #00d4ff);
  color: #fff;
  padding: 10px 22px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 600;
  text-decoration: none;
  transition: opacity 0.2s, transform 0.2s;
  white-space: nowrap;
  flex-shrink: 0;
}

.btn-nav:hover {
  opacity: 0.88;
  transform: translateY(-1px);
}

@media (max-width: 768px) {
  .nav-links {
    display: none;
  }
  .navbar-inner {
    justify-content: space-between;
  }
}
</style>
