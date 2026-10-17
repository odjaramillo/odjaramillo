## Oscar Jaramillo

Estudiante de Ingeniería Informática en la UCAB (Caracas), enfocado en **backend y datos**.
Trabajo principalmente con NestJS, PostgreSQL y Docker, y me interesa la parte de las bases
de datos que va más allá del CRUD: modelado dimensional, integridad, y automatización de
pipelines.

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)

---

### En qué estoy trabajando

- **Sistema de control financiero multi-tenant** para un cliente real — lidero backend e
  infraestructura en un equipo de 3. Row-Level Security en PostgreSQL, libro contable
  inmutable de partida doble, cierre de cajas y tasas BCV/paralela. NestJS + React +
  Docker. v1.0 desplegada, en aceptación con el cliente. *(repositorio privado)*
- **Punto de venta e inventario para una tienda de repuestos de motos** — catálogo con compatibilidad
  pieza–moto, búsqueda con embeddings (pgvector) y punto de venta multimoneda (Bs, USD,
  Zelle) sobre un servidor local en la tienda. NestJS + SvelteKit + PostgreSQL. Unos 650
  PRs fusionados; instalación en la tienda en curso. *(repositorio privado)*
- **[Monitor de caídas bancarias](https://github.com/odjaramillo/monitor-caidas-bancarias)**
  — prototipo que muestra dónde se rompe un pago entre bancos en Venezuela, a partir de
  reportes de usuarios. SvelteKit + Fastify + PostgreSQL + Redis. Se desarrolla en la
  asignatura Computación en la Nube, UCAB.
- **Homelab en Proxmox** — infraestructura autohospedada: virtualización, backups, passthrough
  de GPU y experimentos con agentes de IA locales. Es donde rompo cosas sin costo.

---

### Proyectos públicos

| Proyecto | Qué es | Stack |
| :--- | :--- | :--- |
| [**smart-city-sgbd**](https://github.com/odjaramillo/smart-city-sgbd) | Data warehouse para monitoreo de resiliencia eléctrica (SAIDI/SAIFI/CAIDI). Dimensiones SCD Tipo 2 con denominador dinámico, ingesta vía n8n y consumo desde Power BI. | `PostgreSQL` `n8n` `Docker` |
| [**ecommerce-ai-model**](https://github.com/odjaramillo/ecommerce-ai-model) | Predicción de intención de compra sobre 12.330 sesiones de navegación. Random Forest, búsqueda de hiperparámetros, ajuste de umbral según métricas de negocio y API REST para inferencia. 89,4 % de accuracy. | `Python` `scikit-learn` `FastAPI` |
| [**custom-rules**](https://github.com/odjaramillo/custom-rules) | Registro centralizado de reglas, roles y skills para agentes de código: 159 skills modulares con metadatos validados por esquema. Licencia CC0. | `TypeScript` `Node.js` |
| [**soyucab**](https://github.com/odjaramillo/soyucab) | Red social universitaria (proyecto académico). Esquema de 25 tablas con triggers, Row-Level Security y vistas analíticas. | `PostgreSQL` `Express` `React` |
| [**ucab-tasks**](https://github.com/odjaramillo/ucab-tasks) | API REST de referencia siguiendo Clean Architecture y patrón repositorio. | `TypeScript` |
| [**gestion-bibliotecaria-sqa**](https://github.com/odjaramillo/gestion-bibliotecaria-sqa) | Sistema de gestión bibliotecaria trabajado desde la perspectiva de aseguramiento de calidad. | `Python` |

---

### Stack

| Área | Tecnologías |
| :--- | :--- |
| **Backend** | NestJS · TypeScript · Node.js · Python · Java · Spring Boot |
| **Datos** | PostgreSQL · Modelado dimensional · Row-Level Security · Redis |
| **Infraestructura** | Docker · Proxmox · Git |
| **Automatización** | n8n · Agentes de código |

---

### Notas

Varios de mis proyectos son privados porque son trabajos para clientes. Si te interesa el
detalle técnico de alguno, escribime y lo conversamos con gusto.

📫 oscardan.jtorres@gmail.com
