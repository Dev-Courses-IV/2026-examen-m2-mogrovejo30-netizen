<script setup>
defineProps({
  servicio: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="card">
    <div class="card-header">
      <span class="card-icon" :style="{ background: servicio.colorBg }">
        {{ servicio.icono }}
      </span>
      <span v-if="servicio.badge" class="card-badge" :class="`badge-${servicio.badge.toLowerCase()}`">
        {{ servicio.badge }}
      </span>
    </div>

    <h3 class="card-title">{{ servicio.nombre }}</h3>
    <p class="card-desc">{{ servicio.descripcion }}</p>

    <div class="card-footer">
      <span class="card-precio">{{ servicio.precio }}</span>
      <button class="card-btn">Ver más</button>
    </div>
  </div>
</template>

<style scoped>
.card {
  background: #111224;
  border: 1px solid rgba(108, 99, 255, 0.15);
  border-radius: 16px;
  padding: 28px;
  display: flex;
  flex-direction: column;
  gap: 14px;
  transition: transform 0.25s, border-color 0.25s, box-shadow 0.25s;
}

.card:hover {
  transform: translateY(-6px);
  border-color: rgba(108, 99, 255, 0.5);
  box-shadow: 0 20px 40px rgba(108, 99, 255, 0.12);
}

.card-header {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}

.card-icon {
  width: 52px;
  height: 52px;
  border-radius: 12px;
  font-size: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card-badge {
  font-size: 11px;
  font-weight: 700;
  padding: 4px 10px;
  border-radius: 20px;
  text-transform: uppercase;
  letter-spacing: 0.6px;
}

.badge-popular {
  background: rgba(108, 99, 255, 0.2);
  color: #a78bfa;
  border: 1px solid rgba(108, 99, 255, 0.4);
}

.badge-nuevo {
  background: rgba(16, 185, 129, 0.15);
  color: #34d399;
  border: 1px solid rgba(16, 185, 129, 0.35);
}

.badge-avanzado {
  background: rgba(0, 212, 255, 0.15);
  color: #67e8f9;
  border: 1px solid rgba(0, 212, 255, 0.35);
}

.card-title {
  font-size: 18px;
  font-weight: 700;
  color: #f1f5f9;
  line-height: 1.3;
}

.card-desc {
  font-size: 14px;
  color: #94a3b8;
  line-height: 1.65;
  flex-grow: 1;
}

.card-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 4px;
  padding-top: 16px;
  border-top: 1px solid rgba(255, 255, 255, 0.06);
}

.card-precio {
  font-size: 13px;
  font-weight: 600;
  color: #6c63ff;
}

.card-btn {
  background: transparent;
  border: 1px solid rgba(108, 99, 255, 0.5);
  color: #a78bfa;
  padding: 7px 16px;
  border-radius: 7px;
  font-size: 13px;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.2s, color 0.2s;
}

.card-btn:hover {
  background: rgba(108, 99, 255, 0.15);
  color: #c4b5fd;
}
</style>
