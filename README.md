## Oscar Jaramillo

Estudiante de Ingeniería Informática en la UCAB (Caracas) y desarrollador **backend**.
Construyo software para negocios reales en Venezuela (cajas, inventario, control financiero)
con NestJS, PostgreSQL y Docker. Me importa que funcione de verdad: QA automatizado, reglas
convertidas en checks y desarrollo con agentes de IA sobre una infraestructura que opero yo.

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)

---

### En qué estoy trabajando

- **Sistema de control financiero multi-tenant** para un cliente real — lidero backend e
  infraestructura y coordino un equipo de 3. Row-Level Security en PostgreSQL, libro
  contable inmutable de partida doble, cierre de cajas y tasas BCV/paralela. NestJS + React
  + Docker. v1.0 desplegada en producción. *(repositorio privado)*
- **Punto de venta e inventario para una tienda de repuestos de motos** — catálogo con compatibilidad
  pieza–moto, búsqueda con embeddings (pgvector) y punto de venta multimoneda (Bs, USD,
  Zelle) sobre un servidor local en la tienda. NestJS + SvelteKit + PostgreSQL. Unos 650
  PRs fusionados; instalación en la tienda en curso. *(repositorio privado)*
- **[Monitor de caídas bancarias](https://github.com/odjaramillo/monitor-caidas-bancarias)**
  — prototipo que muestra dónde se rompe un pago entre bancos en Venezuela, a partir de
  reportes de usuarios. SvelteKit + Fastify + PostgreSQL + Redis. Se desarrolla en la
  asignatura Computación en la Nube, UCAB.

---

### Infraestructura propia

Mantengo un homelab con Proxmox VE: 6 máquinas virtuales y contenedores, passthrough de dos
GPUs NVIDIA, servicios publicados con Cloudflare Tunnel detrás de Cloudflare Access, y
Tailscale para el acceso remoto. Lo opero como si fuera producción:

- **Runners propios de GitHub Actions** para un proyecto de cliente: la suite de tests bajó
  de 410 s a 55 s (7,4x) y dejó de pagar minutos excedentes de CI.
- **Backups diarios con simulacro de restauración** documentado, no backups que nadie probó.
- **Sondas con alertas por Telegram**, cada una escrita después de una falla silenciosa real:
  una VM que perdió su IP durante semanas, un timer que reportaba éxito sin copiar nada.

### Desarrollo agéntico

Programo con agentes de IA (Claude Code, Codex, OpenCode, Pi, Cursor). Probé armar mis
propios harnesses y terminé adoptando
[gentle-ai](https://github.com/Gentleman-Programming/gentle-ai), con memoria persistente en
[Engram](https://github.com/Gentleman-Programming/engram) autohospedado. Encima construí mi
propia capa, cada pieza a partir de un problema real *(repositorios privados)*:

- **10 skills propias.** Por ejemplo: `socratic-intake` saca a la luz las suposiciones de un
  requisito antes de escribirlo, `decision-costing` le pone costo a cada opción contra el
  código antes de elegir, y `qa-standard` audita los gates de calidad de un repo.
- **12 plugins para Claude Code** que convierten reglas escritas en checks que se cumplen
  solos: detectar dos sesiones trabajando sobre la misma rama, mostrar qué archivos puede
  tocar un agente, frenar comandos que rompen una regla. Cada uno con tests.
- **Un benchmark en Python** que mide costo y cobertura de cada subagente para elegir modelo y
  esfuerzo con datos, no a ojo.
- **Subagentes adaptados de gentle-ai** con modelo y esfuerzo fijados, mientras se resuelve
  [gentle-ai#4928](https://github.com/Gentleman-Programming/gentle-ai/issues/4928), que reporté.

Reporté 6 defectos reproducibles en esas herramientas; 5 ya los cerraron sus mantenedores:
[engram#778](https://github.com/Gentleman-Programming/engram/issues/778) ·
[engram#779](https://github.com/Gentleman-Programming/engram/issues/779) ·
[gentle-ai#2777](https://github.com/Gentleman-Programming/gentle-ai/issues/2777) ·
[gentle-ai#3042](https://github.com/Gentleman-Programming/gentle-ai/issues/3042) ·
[gentle-ai#4928](https://github.com/Gentleman-Programming/gentle-ai/issues/4928) ·
[gentle-ai#4929](https://github.com/Gentleman-Programming/gentle-ai/issues/4929)

---

### Proyectos públicos

| Proyecto | Qué es | Stack |
| :--- | :--- | :--- |
| [**gestion-bibliotecaria-sqa**](https://github.com/odjaramillo/gestion-bibliotecaria-sqa) | Ecosistema de calidad automatizado sobre una app Spring Boot + Vue: 7 workflows (análisis estático, JaCoCo, Playwright, métricas) y un [dashboard de KPIs](https://odjaramillo.github.io/gestion-bibliotecaria-sqa/) publicado en Pages. | `GitHub Actions` `Java` `Python` |
| [**smart-city-sgbd**](https://github.com/odjaramillo/smart-city-sgbd) | Data warehouse para monitoreo de resiliencia eléctrica (SAIDI/SAIFI/CAIDI). Dimensiones SCD Tipo 2 con denominador dinámico, ingesta vía n8n y consumo desde Power BI. | `PostgreSQL` `n8n` `Docker` |
| [**ecommerce-ai-model**](https://github.com/odjaramillo/ecommerce-ai-model) | Predicción de intención de compra sobre 12.330 sesiones de navegación. Random Forest, búsqueda de hiperparámetros, ajuste de umbral según métricas de negocio y API REST para inferencia. 89,4 % de accuracy. | `Python` `scikit-learn` `FastAPI` |
| [**custom-rules**](https://github.com/odjaramillo/custom-rules) | Mi primera colección de reglas y skills para agentes de código (enero 2026, los inicios del desarrollo agéntico): 159 skills con metadatos validados por esquema y un CLI que las instala. Licencia CC0. | `TypeScript` `Node.js` |
| [**soyucab**](https://github.com/odjaramillo/soyucab) | Red social universitaria (proyecto académico). Esquema de 25 tablas con triggers, Row-Level Security y vistas analíticas. | `PostgreSQL` `Express` `React` |
| [**ucab-tasks**](https://github.com/odjaramillo/ucab-tasks) | API REST de referencia siguiendo Clean Architecture y patrón repositorio. | `TypeScript` |

---

### Stack

| Área | Tecnologías |
| :--- | :--- |
| **Backend** | NestJS · TypeScript · Node.js · Python · Java · Spring Boot |
| **Datos** | PostgreSQL · Modelado dimensional · Row-Level Security · Redis |
| **Infraestructura** | Docker · Proxmox VE · Cloudflare Tunnel/Access · Tailscale · GitHub Actions · Linux |
| **Automatización e IA** | n8n · Claude Code · Codex · OpenCode · Engram |

---

### Notas

Varios de mis proyectos son privados porque son trabajos para clientes. Si te interesa el
detalle técnico de alguno, escribime y lo conversamos con gusto.

📫 oscardan.jtorres@gmail.com
