---
title: Bases de Datos
tags: [basesdedatos, sql, nosql, datos]
keywords: [MongoDB, PostgreSQL, MySQL, Firebase Firestore, Airtable, SQL, NoSQL, Bases de datos]
description: Sistemas de gestión de datos estructurados y no estructurados para almacenar, recuperar y gestionar información en aplicaciones.
---

# Documentation

# 3️⃣ Bases de Datos: Análisis Profundo

## NoSQL

### Firebase Firestore

#### Arquitectura y Modelo de Datos
* **Tipo**: Base de datos documental NoSQL orientada a la nube
* **Estructura**: Organizada en colecciones y documentos anidables
* **Modelo de datos**: Documentos JSON con tipos de datos enriquecidos
* **Indexación**: Automática para campos simples, configurable para consultas complejas

#### Características Técnicas
* **Sincronización en tiempo real**: Actualización automática en todos los clientes conectados
* **Modo offline**: Caché local y resolución automática de conflictos
* **Seguridad**: Reglas declarativas a nivel de documento y campo
* **Consultas**: API para filtrado, ordenación y paginación
* **Transacciones**: Soporte para operaciones atómicas multi-documento
* **Lotes**: Procesamiento de múltiples operaciones en una sola solicitud

#### Rendimiento y Escalabilidad
* **Capacidad**: Automáticamente escalable a nivel global
* **Latencia**: Baja gracias a su red global de distribución
* **Límites**: 1MB por documento, 20,000 escrituras/s por colección
* **Particionamiento**: Automático basado en la carga
* **SLA**: 99.999% de disponibilidad

#### Precios
* **Almacenamiento**: 1GB gratuito, luego $0.18/GB/mes
* **Transferencia**: 10GB/mes gratuitos, luego $0.08-0.12/GB
* **Operaciones**:
  * 50,000 lecturas/día gratis, luego $0.06/100K
  * 20,000 escrituras/día gratis, luego $0.18/100K
  * 20,000 eliminaciones/día gratis, luego $0.02/100K

#### Ventajas Específicas
* Sincronización en tiempo real sin configuración adicional
* Integración perfecta con ecosistema Firebase
* Desconexión/reconexión transparente con modo offline
* Escalabilidad automática sin gestión de infraestructura
* Reglas de seguridad expresivas directamente en la base de datos

#### Limitaciones
* Consultas limitadas comparadas con SQL (no JOIN nativo)
* Tamaño máximo de documento de 1MB
* Costos pueden escalar rápidamente con volumen alto
* Transacciones limitadas a 500 operaciones
* Dificultad para migraciones o exportaciones complejas

### MongoDB

#### Arquitectura y Modelo de Datos
* **Tipo**: Base de datos documental NoSQL
* **Estructura**: Colecciones de documentos con esquema flexible
* **Modelo de datos**: BSON (Binary JSON) con tipos adicionales
* **Indexación**: Soporte para múltiples tipos (single-field, compound, text, geospatial)

#### Características Técnicas
* **Consultas**: Framework rico de queries con agregaciones
* **Sharding**: Particionamiento horizontal para escalabilidad
* **Replicación**: Conjuntos de réplicas con elección automática de primario
* **Transacciones**: ACID multi-documento desde v4.0
* **Vistas**: Consultas almacenadas como colecciones virtuales
* **Change Streams**: Seguimiento de cambios en tiempo real
* **Atlas Search**: Búsqueda full-text integrada

#### Rendimiento y Escalabilidad
* **Capacidad**: Escalable horizontal y verticalmente
* **Arquitecturas**: Standalone, replicación, sharding
* **Índices**: Soporte para diversos tipos de índices
* **Monitoreo**: Herramientas integradas de rendimiento
* **Límites**: 16MB por documento, personalizable para clúster

#### Opciones de Despliegue
* **Self-hosted**: Comunidad y Enterprise on-premise
* **MongoDB Atlas**: DBaaS en AWS, Azure, GCP
* **MongoDB Realm**: Backend serverless con sincronización

#### Precios
* **Community Edition**: Gratuito, auto-hospedado
* **Atlas Free Tier**: Clúster compartido con 512MB de almacenamiento
* **Atlas Dedicated**: Desde $57/mes (M10) para clústeres dedicados
* **Enterprise**: Licenciamiento por nodo con soporte premium

#### Ventajas Específicas
* Consultas expresivas con pipeline de agregación
* Escalabilidad probada a volúmenes masivos de datos
* Flexibilidad de esquema para evolución de aplicaciones
* Modelo de datos intuitivo para desarrolladores
* Ecosistema maduro de herramientas y conectores
* Opciones de despliegue flexibles (cloud, on-premise, híbrido)

#### Limitaciones
* Mayor complejidad operativa comparada con BaaS
* Curva de aprendizaje para optimización y escalado adecuados
* Consistencia eventual en configuraciones distribuidas
* Uso de memoria relativamente alto
* Limitaciones en joins complejos comparado con SQL

## SQL

### PostgreSQL

#### Arquitectura y Modelo de Datos
* **Tipo**: Sistema de gestión de bases de datos objeto-relacional
* **Estructura**: Basada en ACID, esquemas, tablas y relaciones
* **Modelo de datos**: Relacional con tipos de datos extensibles
* **Conformidad**: ANSI SQL completo con extensiones propias

#### Características Técnicas
* **Tipos de datos**: Rico soporte incluyendo JSON, arrays, geometrías
* **Integridad**: Constraints, foreign keys, triggers, check constraints
* **Procedimientos**: Funciones y procedimientos almacenados en múltiples lenguajes
* **Concurrencia**: MVCC (Control de concurrencia multiversión)
* **Extensiones**: Sistema modular con +100 extensiones (PostGIS, pgVector, etc.)
* **Búsqueda**: Full-text search integrado
* **Replicación**: Streaming, logical, bi-directional

#### Rendimiento y Optimización
* **Indexación**: B-tree, Hash, GiST, SP-GiST, GIN, BRIN
* **Particionamiento**: Por rango, lista, hash
* **Query Planner**: Optimizador avanzado basado en costos
* **Paralelización**: Queries paralelas para operaciones complejas
* **VACUUM**: Gestión eficiente del espacio

#### Capacidades Avanzadas
* **PostGIS**: Potente extensión para datos espaciales/GIS
* **pgvector**: Búsqueda vectorial para IA/ML
* **Tablas heredadas**: Jerarquía de tablas
* **Window Functions**: Funciones analíticas avanzadas
* **Common Table Expressions (CTEs)**: Queries recursivas
* **FDW (Foreign Data Wrappers)**: Conexión con fuentes de datos externas

#### Precios
* **Software**: 100% gratuito y open source
* **Hosting**: Desde servicios gratuitos limitados hasta opciones enterprise
  * AWS RDS: Desde $12.41/mes (db.t4g.micro)
  * Google Cloud SQL: Desde $7.67/mes (db-f1-micro)
  * Azure Database: Desde $25.32/mes (Basic tier)
  * Supabase/Neon/etc: Planes gratuitos disponibles

#### Ventajas Específicas
* Cumplimiento estricto del estándar SQL
* Extremadamente extensible y personalizable
* Sólida integridad de datos
* Excelente para datos complejos y consultas analíticas
* Comunidad activa y documentación extensa
* Capacidades avanzadas como bases de datos geoespaciales
* Soporte para búsqueda vectorial (AI/ML)

#### Limitaciones
* Mayor complejidad de configuración y mantenimiento
* Consumo de recursos relativamente alto
* Curva de aprendizaje para optimización avanzada
* Escalado horizontal menos automático que soluciones NoSQL

### MySQL

#### Arquitectura y Modelo de Datos
* **Tipo**: Sistema de gestión de bases de datos relacional
* **Estructura**: Basada en tablas con relaciones y esquemas
* **Motores de almacenamiento**: InnoDB (default), MyISAM, Memory, Archive
* **Conformidad**: SQL estándar con extensiones propias

#### Características Técnicas
* **Transacciones**: ACID compliant con InnoDB
* **Replicación**: Master-slave, group replication
* **Particionamiento**: Horizontal por rangos, hash, listas
* **Triggers y Stored Procedures**: Programabilidad en la base de datos
* **Vistas**: Regulares y materializadas
* **Integridad referencial**: Foreign keys con InnoDB
* **Búsqueda de texto**: Full-text search con InnoDB y MyISAM

#### Rendimiento y Escalabilidad
* **Optimización**: Query cache (versiones anteriores), query optimizer
* **Indexación**: B-tree, hash, full-text
* **Clustering**: MySQL Cluster para alta disponibilidad
* **Thread pooling**: Gestión eficiente de conexiones
* **Buffer pool**: Caché de datos en memoria

#### Opciones de Despliegue
* **Community Edition**: Gratuita, open source (GPL)
* **Enterprise Edition**: Con herramientas adicionales y soporte
* **Cloud**: AWS RDS, Azure MySQL, Google Cloud SQL, Oracle MySQL HeatWave

#### Precios
* **Community**: Gratuito
* **Enterprise**: Desde $5,000/año por servidor
* **Cloud services**:
  * AWS RDS MySQL: Desde $12.41/mes (db.t4g.micro)
  * Google Cloud SQL: Desde $7.67/mes (db-f1-micro)
  * Azure MySQL: Desde $25.32/mes (Basic tier)

#### Ventajas Específicas
* Extremadamente popular con amplio soporte y ecosistema
* Rendimiento optimizado para operaciones OLTP
* Menor consumo de recursos que PostgreSQL
* Ampliamente documentado con muchos recursos disponibles
* Fácil de configurar y mantener para casos simples
* Bien soportado por frameworks y CMS populares

#### Limitaciones
* Menos funcionalidades avanzadas que PostgreSQL
* Implementación menos estricta del estándar SQL
* Limitaciones en consultas complejas y recursivas
* Replicación tradicionalmente menos robusta (mejorada en versiones recientes)
* Escalabilidad vertical antes que horizontal

## Alternativas Low-Code

### Airtable

#### Concepto y Arquitectura
* **Tipo**: Híbrido entre base de datos relacional, hoja de cálculo y plataforma colaborativa
* **Estructura**: Bases organizadas en tablas con registros y campos
* **Modelo**: Relacional simplificado con interfaz visual
* **Enfoque**: Centrado en el usuario final, no-code/low-code

#### Características Principales
* **Interfaces**: Múltiples vistas (grid, kanban, calendar, form, gallery, Gantt)
* **Tipos de campos**: 20+ incluyendo attachments, formulas, lookups, rollups
* **Automations**: Flujos de trabajo sin código basados en triggers y acciones
* **Apps**: Mini-aplicaciones personalizables para visualización y manipulación
* **Interfaces**: Creación de dashboards y formularios personalizados
* **Colaboración**: Edición en tiempo real, comentarios, historial de revisiones
* **API**: RESTful API para integración con otros sistemas
* **Blocks**: Extensiones de funcionalidad pre-construidas

#### Integraciones y Extensibilidad
* **Sync**: Conexión bidireccional con servicios externos
* **Scripting**: Personalización con JavaScript
* **Integraciones nativas**: Slack, GSuite, Jira, Zapier, etc.
* **Webhooks**: Para automatizaciones avanzadas
* **On-demand automation runs**: Ejecución de acciones vía API

#### Precios
* **Free**: Hasta 1,200 registros por base, 2GB adjuntos
* **Plus**: $10/usuario/mes, 5,000 registros/base, 5GB adjuntos
* **Pro**: $20/usuario/mes, 50,000 registros/base, 20GB adjuntos
* **Enterprise**: Personalizado, registros ilimitados, SSO, admin features

#### Ventajas Específicas
* Curva de aprendizaje extremadamente baja
* Interfaz intuitiva tipo hoja de cálculo
* Flexibilidad para adaptarse a múltiples casos de uso
* Capacidades relacionales sin necesidad de SQL
* Excelente para colaboración en equipos no técnicos
* Rápida creación de aplicaciones internas y sistemas de gestión

#### Limitaciones
* Límites de registros y capacidad en planes no Enterprise
* Limitado para operaciones transaccionales de alto volumen
* Rendimiento puede degradarse con bases grandes o complejas
* Menos control granular que bases de datos tradicionales
* Portabilidad limitada de datos y lógica
* No adecuado para aplicaciones de misión crítica

### Comparativa General de Bases de Datos

| Característica | Firestore | MongoDB | PostgreSQL | MySQL | Airtable |
|----------------|-----------|---------|------------|-------|----------|
| Modelo de datos | Documental | Documental | Relacional | Relacional | Relacional simplificado |
| Escalabilidad | Automática | Manual/Atlas | Manual | Manual/Cluster | Limitada |
| Esquema | Flexible | Flexible | Estricto | Estricto | Semi-flexible |
| Transacciones | Limitadas | Multi-documento | Completas ACID | Completas ACID | No soportadas |
| Consultas complejas | Limitadas | Buenas (agregación) | Excelentes | Buenas | Básicas |
| Tiempo real | Nativo | Change Streams | Triggers/Listen | Triggers | Limitado |
| Facilidad de uso | Alta | Media | Baja | Media | Muy alta |
| Casos de uso ideales | Apps móviles, tiempo real | Datos heterogéneos, volúmenes medios | Datos complejos, analítica | OLTP, aplicaciones web | Proyectos internos, prototipos |
| Mantenimiento | Ninguno | Bajo-Medio | Alto | Medio | Ninguno |