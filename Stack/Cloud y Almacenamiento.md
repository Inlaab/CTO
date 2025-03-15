---
title: Cloud y Almacenamiento
tags: [cloud, almacenamiento, storage, infraestructura]
keywords: [AWS, GCP, Azure, Cloud, S3, Google Cloud Storage, Firebase Storage, Almacenamiento, Infraestructura]
description: Plataformas y servicios cloud para hosting, almacenamiento y gestión de recursos digitales a escala.
---

# Documentation

# 4️⃣ Cloud y Almacenamiento: Análisis Profundo

## Plataformas Cloud

### Google Cloud Platform (GCP)

#### Servicios Core
1. **Compute**
   * **Compute Engine**: VMs personalizables
   * **Cloud Run**: Contenedores serverless
   * **App Engine**: PaaS para aplicaciones
   * **Cloud Functions**: Funciones serverless
   * **GKE (Kubernetes Engine)**: Orquestación de contenedores

2. **Storage & Databases**
   * **Cloud Storage**: Almacenamiento de objetos
   * **Cloud SQL**: Bases de datos relacionales gestionadas
   * **Cloud Spanner**: Base de datos global distribuida
   * **BigQuery**: Data warehouse serverless
   * **Firestore/Datastore**: NoSQL documental

3. **Networking**
   * **Cloud VPC**: Redes virtuales privadas
   * **Cloud CDN**: Red de distribución de contenido
   * **Cloud Load Balancing**: Balanceo de carga global
   * **Cloud DNS**: Servicio DNS gestionado

4. **AI & Machine Learning**
   * **Vertex AI**: Plataforma unificada de ML
   * **Vision AI**: Análisis de imágenes
   * **Speech-to-Text**: Reconocimiento de voz
   * **Natural Language**: Procesamiento de lenguaje natural

#### Características Distintivas
* Fuerte enfoque en ML/AI
* Red global de fibra privada
* Integración profunda con servicios Google
* Precios competitivos y modelo de facturación por segundos
* Enfoque en código abierto (Kubernetes, TensorFlow)

#### Precios
* Capa gratuita generosa
* Créditos iniciales ($300)
* Pay-as-you-go con descuentos por uso sostenido
* Precios competitivos en compute y storage

### Amazon Web Services (AWS)

#### Servicios Core
1. **Compute**
   * **EC2**: Servidores virtuales
   * **Lambda**: Funciones serverless
   * **ECS/EKS**: Orquestación de contenedores
   * **Elastic Beanstalk**: PaaS
   * **Fargate**: Contenedores serverless

2. **Storage & Databases**
   * **S3**: Almacenamiento de objetos
   * **RDS**: Bases de datos relacionales
   * **DynamoDB**: NoSQL
   * **Redshift**: Data warehouse
   * **ElastiCache**: Caché en memoria

3. **Networking**
   * **VPC**: Redes virtuales
   * **CloudFront**: CDN global
   * **Route 53**: DNS y registro de dominios
   * **ELB**: Balanceo de carga

4. **DevOps & Tools**
   * **CloudFormation**: Infraestructura como código
   * **CodePipeline**: CI/CD
   * **CloudWatch**: Monitoreo
   * **IAM**: Gestión de identidades

#### Características Distintivas
* Mayor variedad de servicios
* Presencia global extensa
* Madurez y estabilidad
* Ecosistema amplio de partners
* Certificaciones y compliance

#### Precios
* Capa gratuita por 12 meses
* Modelo pay-as-you-go
* Opciones de ahorro con instancias reservadas
* Savings Plans flexibles

### Microsoft Azure

#### Servicios Core
1. **Compute**
   * **Virtual Machines**: VMs
   * **App Service**: PaaS
   * **Functions**: Serverless
   * **AKS**: Kubernetes gestionado
   * **Container Instances**: Contenedores

2. **Storage & Databases**
   * **Blob Storage**: Almacenamiento de objetos
   * **Azure SQL**: SQL Server gestionado
   * **Cosmos DB**: NoSQL multimodelo
   * **Synapse Analytics**: Analytics y data warehouse
   * **Cache for Redis**: Caché en memoria

3. **Networking**
   * **Virtual Network**: Redes virtuales
   * **CDN**: Distribución de contenido
   * **Load Balancer**: Balanceo de carga
   * **ExpressRoute**: Conexiones dedicadas

4. **AI & ML**
   * **Cognitive Services**: APIs de IA
   * **Machine Learning**: Plataforma ML
   * **Bot Service**: Framework para chatbots
   * **OpenAI Service**: APIs de lenguaje

#### Características Distintivas
* Integración profunda con productos Microsoft
* Fuerte en soluciones empresariales
* Híbrido cloud con Azure Stack
* Enfoque en .NET y Windows
* Servicios cognitivos avanzados

#### Precios
* Créditos gratuitos iniciales
* Descuentos para clientes Enterprise
* Integración con licencias existentes
* Opciones de pago híbridas

## Almacenamiento

### AWS S3 (Simple Storage Service)

#### Características Principales
* **Durabilidad**: 99.999999999% (11 9s)
* **Disponibilidad**: 99.99%
* **Escalabilidad**: Ilimitada
* **Clases de almacenamiento**:
  * Standard
  * Intelligent-Tiering
  * Standard-IA
  * One Zone-IA
  * Glacier
  * Glacier Deep Archive

#### Funcionalidades
* **Versionado**: Control de versiones de objetos
* **Lifecycle Rules**: Gestión automática del ciclo de vida
* **Encryption**: Server-side encryption
* **Access Control**: IAM, bucket policies, ACLs
* **Event Notifications**: Triggers para cambios
* **Static Website Hosting**: Hosting web estático
* **Transfer Acceleration**: Transferencia acelerada
* **Replication**: Cross-region y same-region

#### Precios
* **Storage**: Desde $0.023/GB/mes (Standard)
* **Requests**: GET ($0.0004/1000), PUT ($0.005/1000)
* **Data Transfer**: Gratuito ingreso, salida variable
* **Management Features**: Costos adicionales por funciones avanzadas

### Google Cloud Storage

#### Características Principales
* **Durabilidad**: 99.999999999%
* **Disponibilidad**: 99.95% - 99.99%
* **Clases de almacenamiento**:
  * Standard
  * Nearline
  * Coldline
  * Archive

#### Funcionalidades
* **Object Lifecycle Management**: Gestión automática
* **Object Versioning**: Control de versiones
* **Customer-Supplied Encryption Keys**: Claves personalizadas
* **IAM & ACLs**: Control de acceso granular
* **Object Change Notification**: Webhooks y Pub/Sub
* **Strong Consistency**: Consistencia inmediata
* **Signed URLs**: URLs temporales firmadas

#### Precios
* **Storage**: Desde $0.020/GB/mes (Standard)
* **Operations**: Diferentes precios por tipo
* **Network**: Egress costs vary by destination
* **Early Deletion**: Cargos mínimos por periodo

### Firebase Storage

#### Características Principales
* **Integración**: Nativa con Firebase/GCP
* **Seguridad**: Reglas declarativas
* **Escalabilidad**: Automática
* **Offline**: Soporte para operaciones offline
* **Resumable**: Uploads resumibles

#### Funcionalidades
* **Security Rules**: Control de acceso declarativo
* **Client SDKs**: iOS, Android, Web
* **Upload/Download**: Gestión de transferencias
* **Metadata**: Metadatos personalizados
* **Integration**: Firebase Authentication

#### Precios
* **Storage**: 5GB gratuitos, luego $0.026/GB
* **Download**: 1GB/día gratuito, luego $0.12/GB
* **Upload**: Gratuito
* **Operations**: Incluidas en precio base

### Comparativa de Servicios de Almacenamiento

| Característica | AWS S3 | Google Cloud Storage | Firebase Storage |
|----------------|--------|---------------------|------------------|
| Durabilidad | 11 9s | 11 9s | 11 9s |
| Disponibilidad | 99.99% | 99.95-99.99% | 99.95% |
| Clases Storage | 6 | 4 | 1 |
| Precios base | $0.023/GB | $0.020/GB | $0.026/GB |
| Caso uso ideal | Enterprise | Híbrido | Mobile/Web apps |
| Integración | AWS | GCP | Firebase |
| Complejidad | Alta | Media | Baja |
| Características | Muy completo | Completo | Básico |