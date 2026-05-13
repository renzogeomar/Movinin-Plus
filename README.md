# Movinin+ · IPS 2026-A · EPIS-UNSA

[![GitHub Pages](https://img.shields.io/badge/Sprint%200-GitHub%20Pages-brightgreen)](https://movidinteam.github.io/Movinin-Plus/)
[![Based on](https://img.shields.io/badge/based%20on-aelassas%2Fmovinin-blue)](https://github.com/aelassas/movinin)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Course](https://img.shields.io/badge/course-Ingeniería%20y%20Procesos%20de%20Software-orange)](https://epis.unsa.edu.pe/)

![Movinin+ Cover](https://movinin.dynv6.net:3004/)

## Movinin+

Movinin+ es una extensión del proyecto de código abierto [Movin' In](https://github.com/aelassas/movinin), desarrollada como parte del curso **Ingeniería y Procesos de Software (IPS 2026-A)** en la **EPIS-UNSA**, bajo la guía del profesor Robert Arisaca.

El proyecto parte de la plataforma original de gestión de propiedades en alquiler (MERN stack) y añade mejoras enfocadas en el mercado latinoamericano: soporte multi-moneda con detección automática de región (PEN/USD/EUR), sistema de reseñas y valoraciones, cupones de descuento, chat en tiempo real entre arrendatario y agencia, y un módulo de incidencias/mantenimiento.

## Repositorio original

Este repositorio es un fork funcional del proyecto original. Para clonar el repositorio original en el tuyo:

```bash
# 1. Clona el repositorio original de Movin' In
git clone https://github.com/aelassas/movinin.git

# 2. Entra al directorio
cd movinin

# 3. Agrega tu repositorio como remoto adicional
git remote add movinin-plus https://github.com/MovidinTeam/Movinin-Plus.git

# 4. Verifica los remotos configurados
git remote -v

# 5. Empuja el código al repositorio de Movinin-Plus
git push movinin-plus main
```

O si prefieres trabajar directamente desde el repositorio de Movinin-Plus:

```bash
git clone https://github.com/MovidinTeam/Movinin-Plus.git
cd Movinin-Plus
```

## Índice rápido

- [Descripción del producto](#movinin)
- [Características añadidas](#características-añadidas)
- [Backlog del producto](#backlog-del-producto)
- [Cronograma de hitos](#cronograma-de-hitos)
- [Stack tecnológico](#stack-tecnológico)
- [Equipo](#equipo)
- [Documentación original](#documentación-original)
- [Licencia](#licencia)

## Características añadidas

Las siguientes épicas son las mejoras que Movinin+ agrega sobre el proyecto base:

### Sistema de Reseñas y Valoraciones
- Reseñas verificadas post-estadía con puntuación 1-5 estrellas
- Respuestas públicas de agencias a comentarios
- Widget de rating agregado en listados de propiedades

### Cupones de Descuento y Promociones
- CRUD completo de cupones (porcentaje / monto fijo)
- Validación en tiempo real en el checkout
- Rastreo de uso y expiración automática

### Chat en Tiempo Real
- Mensajería WebSocket entre arrendatario y agencia
- Historial de conversaciones persistido en MongoDB
- Notificaciones push de nuevos mensajes

### Módulo de Incidencias y Mantenimiento
- Reporte de incidencias durante el alquiler (fotos + descripción)
- Panel de gestión para agencias con estados (Abierto → En revisión → Resuelto)
- Historial trazable por propiedad

### Calendario de Disponibilidad Visual
- Vista mensual con slots de disponibilidad en el frontend
- Integración con el scheduler existente del backend
- Exportación iCal para sincronización con calendarios externos

### Programa de Fidelización (Puntos)
- Acumulación de puntos por reserva completada
- Canje de puntos como descuento en la siguiente reserva
- Panel de historial y saldo de puntos para el usuario

### Dashboard Analytics para Agencias
- Métricas de ocupación, ingresos y satisfacción
- Gráficas interactivas con filtros por período
- Exportación de reportes en CSV/PDF

### Soporte Multi-moneda Dinámico
- Tasas de cambio actualizadas diariamente (PEN, USD, EUR)
- Auto-detección de región por IP (PEN por defecto en Perú)
- Selector global de divisa en la barra de navegación

## Backlog del producto

El Product Backlog completo está disponible en [GitHub Projects](https://github.com/MovidinTeam/Movinin-Plus/projects) del repositorio, con las historias de usuario organizadas por épicas y sprints.

## Cronograma de hitos

| Sprint | Período | Descripción |
|--------|---------|-------------|
| Sprint 0 | Semana 1–2 | Análisis, selección del producto y documentación base |
| Sprint 1 | Semana 3–5 | Reseñas + Cupones + Infraestructura base |
| Sprint 2 | Semana 6–8 | Chat en tiempo real + Incidencias |
| Sprint 3 | Semana 9–11 | Calendario visual + Fidelización |
| Sprint 4 | Semana 12–14 | Analytics + Multi-moneda + QA final |

## Stack tecnológico

Movinin+ hereda el stack del proyecto original y añade dependencias específicas para las nuevas funcionalidades:

| Capa | Tecnología |
|------|-----------|
| Backend | Node.js · Express.js · MongoDB · Mongoose |
| Frontend | React · Vite · TypeScript · MUI |
| Mobile | React Native · Expo |
| Tiempo real | Socket.IO (WebSocket) |
| Pagos | Stripe · PayPal |
| Autenticación | JWT · bcrypt · Google/Facebook/Apple OAuth |
| DevOps | GitHub Actions · GitHub Pages · Docker |
| Gestión | GitHub Projects · GitHub Issues |

## Herramientas DevOps

| Herramienta | Uso en el proyecto |
|-------------|-------------------|
| **GitHub Projects** | Tablero Kanban/Scrum: organiza el backlog y los sprints |
| **GitHub Actions** | CI/CD: build, tests y despliegue automático |
| **GitHub Pages** | Publicación de la demo del sprint y documentación |
| **GitHub Issues** | Registro de historias de usuario y bugs |

## Equipo

| # | Nombre | Responsabilidad Sprint 0 |
|---|--------|--------------------------|
| E1 | Renzo Geomar Mamani Quispe | GitHub Pages |
| E2 | Emanuel David Hilacondo Begazo | GitHub Projects |
| E3 | Sergio Emilio Estrada Arce | Product Backlog |
| E4 | Christian Alexander Yana Huanca | Análisis del producto |
| E5 | Brayan Carlos Auccacusi Conde | Cronograma |

**Curso:** Ingeniería y Procesos de Software · EPIS-UNSA 2026-A  
**Profesor:** Robert Arisaca

## Documentación original

Para instalar y configurar la plataforma base de Movin' In, consulta la documentación oficial del proyecto original:

- [Visión general](https://github.com/aelassas/movinin/wiki/Overview)
- [Guía de instalación (self-hosted)](https://github.com/aelassas/movinin/wiki/Installing-(Self%E2%80%90hosted))
- [Guía de instalación (Docker)](https://github.com/aelassas/movinin/wiki/Installing-(Docker))
- [Build de la app móvil](https://github.com/aelassas/movinin/wiki/Build-Mobile-App)
- [Pasarelas de pago](https://github.com/aelassas/movinin/wiki/Payment-Gateways)
- [Documentación completa](https://github.com/aelassas/movinin/wiki)

## Licencia

Este proyecto está licenciado bajo la [MIT License](LICENSE), la misma que el proyecto original [aelassas/movinin](https://github.com/aelassas/movinin).

```
MIT License

Copyright (c) 2024 Akram El Assas
Copyright (c) 2026 MovidinTeam · EPIS-UNSA

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
