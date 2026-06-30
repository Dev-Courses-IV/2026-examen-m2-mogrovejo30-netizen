<script setup>
import ServicioCard from './ServicioCard.vue'

const servicios = [
  {
    id: 1,
    icono: '🤖',
    nombre: 'Chatbot de Ventas IA',
    descripcion: 'Automatiza la atención al cliente con un asistente inteligente que convierte visitantes en compradores las 24 horas del día, los 7 días de la semana.',
    precio: 'Desde $299/mes',
    badge: 'Popular',
    colorBg: 'rgba(108, 99, 255, 0.15)',
  },
  {
    id: 2,
    icono: '📊',
    nombre: 'Análisis Predictivo',
    descripcion: 'Predice tendencias de ventas y el comportamiento de tus clientes con algoritmos de machine learning entrenados con tus propios datos.',
    precio: 'Desde $499/mes',
    badge: 'Avanzado',
    colorBg: 'rgba(0, 212, 255, 0.15)',
  },
  {
    id: 3,
    icono: '⚡',
    nombre: 'CRM Automatizado',
    descripcion: 'Gestiona leads y clientes automáticamente con IA que prioriza oportunidades, agenda seguimientos y optimiza cada etapa del embudo de ventas.',
    precio: 'Desde $399/mes',
    badge: null,
    colorBg: 'rgba(245, 158, 11, 0.15)',
  },
  {
    id: 4,
    icono: '✍️',
    nombre: 'Generación de Contenido',
    descripcion: 'Crea emails, propuestas comerciales y material de marketing hiperpersonalizado para cada cliente usando modelos de lenguaje avanzados.',
    precio: 'Desde $199/mes',
    badge: null,
    colorBg: 'rgba(16, 185, 129, 0.15)',
  },
  {
    id: 5,
    icono: '🎯',
    nombre: 'Segmentación Inteligente',
    descripcion: 'Identifica y agrupa a tus clientes ideales con precisión milimétrica usando modelos de clustering y aprendizaje no supervisado.',
    precio: 'Desde $349/mes',
    badge: 'Nuevo',
    colorBg: 'rgba(236, 72, 153, 0.15)',
  },
  {
    id: 6,
    icono: '📈',
    nombre: 'Optimización de Precios',
    descripcion: 'Ajusta tus precios dinámicamente en tiempo real para maximizar ingresos según la demanda del mercado y el perfil de cada comprador.',
    precio: 'Desde $449/mes',
    badge: null,
    colorBg: 'rgba(249, 115, 22, 0.15)',
  },
]
</script>

<template>
  <section id="servicios" class="servicios-section">
    <div class="section-inner">
      <div class="section-header">
        <span class="section-tag">Nuestros Servicios</span>
        <h2 class="section-title">
          Soluciones de <span class="gradient-text">IA para Ventas</span>
        </h2>
        <p class="section-subtitle">
          Desde chatbots inteligentes hasta análisis predictivo, cada herramienta
          está diseñada para multiplicar tus resultados comerciales.
        </p>
      </div>

      <div class="cards-grid">
        <ServicioCard
          v-for="servicio in servicios"
          :key="servicio.id"
          :servicio="servicio"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.servicios-section {
  padding: 100px 24px;
}

.section-inner {
  max-width: 1200px;
  margin: 0 auto;
}

.section-header {
  text-align: center;
  margin-bottom: 64px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
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
  letter-spacing: 0.5px;
  text-transform: uppercase;
}

.section-title {
  font-size: clamp(28px, 4vw, 42px);
  font-weight: 800;
  color: #f1f5f9;
  line-height: 1.2;
  letter-spacing: -0.8px;
}

.section-subtitle {
  font-size: 16px;
  color: #64748b;
  max-width: 540px;
  line-height: 1.7;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

@media (max-width: 1024px) {
  .cards-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 640px) {
  .servicios-section {
    padding: 72px 16px;
  }
  .cards-grid {
    grid-template-columns: 1fr;
  }
}
</style>
