# Handover - KPI Dashboard (Tailwind v4)

## Prompt inicial (resumen)

Se solicitó construir un dashboard de KPIs en HTML semántico, usando únicamente Tailwind CSS v4 (con opción de usar Charts.css), con enfoque mobile-first, navegación por secciones tipo tabs/header, y visual por canal con estas reglas:

- Instagram en morado.
- YouTube en rojo.
- TikTok en naranja.
- Variaciones por opacidad dentro del mismo canal.
- Funnel en verde (opacidades).
- Quality metrics en azul (opacidades).
- Dashboard dinámico por canal: al elegir un canal, mostrar solo datos asociados.
- Validar cobertura completa de KPIs del checklist inicial.

## Qué se implementó

### 1) Fuente única de dashboard

- Entrada principal en index.html.
- dashboard.html deprecado y convertido en redirección a index.html para evitar divergencia.

### 2) Estructura funcional completa

- Top block con grupos KPI completos:
  - Volume, Revenue, Engagement, Retention, Performance, Satisfaction, Efficiency.
- Drivers con módulos completos:
  - Sales funnel, Quality metrics, Performance by platform, Engagement by platform, Performance by product, Activity by platform.
- Bottom/Operations completo:
  - Products table, Platforms table, Campaigns table, Alerts y Lists with filters.

### 3) Dinámica por canal

- Filtros por canal en header: All, Instagram, TikTok, YouTube.
- Tabs navegables: Outcomes, Drivers, Operations.
- Filtrado por data-channel en filas e ítems del dashboard.
- Actualización dinámica de métricas de funnel y quality según canal activo.

### 4) Sistema visual

- Colores por canal aplicados en charts y filas:
  - Instagram: morado.
  - TikTok: naranja.
  - YouTube: rojo.
- Funnel: escala verde por opacidad.
- Quality: escala azul por opacidad.

### 5) Ajustes de legibilidad recientes

- Performance by product migrado a chart tipo tabla (barras), en lugar de línea.
- Ajustes de labels y spacing para evitar cortes de texto en móviles:
  - Mayor labels-size en quality y product charts.
  - Padding horizontal adicional en celdas de label.
  - Reglas anti-corte (nowrap, normal word-break, normal overflow-wrap, hyphens none).
  - Padding de cards ajustado a p-3 sm:p-4 en esos módulos.

## Documentación actualizada

- README.md actualizado con entry point real.
- README.es.md actualizado con entry point real.
- README.cn.md actualizado con entry point real.
- Nota de deprecación de dashboard.html incluida.

## Commit principal ya publicado

- Commit: 8f51f28
- Mensaje: Build channel-aware KPI dashboard and docs updates
- Rama: main

## Siguientes mejoras sugeridas (opcionales)

- Ajustar label widths finos para viewports extremadamente angostos.
- Incorporar test visual manual por breakpoints (320, 375, 390, 768, 1024).
- Extraer data del dashboard a un objeto/config para mantenimiento más simple.
