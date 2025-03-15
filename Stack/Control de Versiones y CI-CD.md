---
title: Control de Versiones y CI/CD
tags: [git, github, cicd, devops]
keywords: [GitHub, Git, CI/CD, Control de versiones, Integración continua, Despliegue continuo, DevOps]
description: Herramientas para gestionar cambios en el código fuente y automatizar los procesos de integración y despliegue de software.
---

# Documentation

# 7️⃣ Control de Versiones y CI/CD

## Git

### Conceptos Fundamentales
* **Tipo**: Sistema de control de versiones distribuido
* **Desarrollador**: Linus Torvalds (2005)
* **Arquitectura**: Distribuida con repositorios locales completos

### Comandos Esenciales
1. **Básicos**:
```bash
git init            # Inicializar repositorio
git clone <url>     # Clonar repositorio
git add <files>     # Añadir archivos al staging
git commit -m ""    # Confirmar cambios
git push           # Subir cambios
git pull           # Obtener cambios
git status         # Ver estado actual
git log            # Ver historial
```

2. **Branching**:
```bash
git branch                  # Listar ramas
git branch <name>          # Crear rama
git checkout <branch>      # Cambiar rama
git checkout -b <branch>   # Crear y cambiar rama
git merge <branch>         # Fusionar ramas
git rebase <branch>        # Rebasar rama
```

3. **Avanzados**:
```bash
git stash                  # Guardar cambios temporalmente
git cherry-pick <commit>   # Aplicar commit específico
git reset --hard <commit>  # Revertir a commit específico
git revert <commit>        # Crear nuevo commit que deshace cambios
git tag -a v1.0 -m ""     # Crear tag anotado
```

### Flujos de Trabajo (Git Flow)
1. **Main/Master**:
   * Código en producción
   * Siempre estable
   * Tags para releases

2. **Develop**:
   * Rama principal de desarrollo
   * Integración de features

3. **Feature Branches**:
   * Rama por funcionalidad
   * Se crean desde develop
   * Se fusionan en develop

4. **Release Branches**:
   * Preparación para producción
   * Correcciones menores
   * Se fusionan en main y develop

5. **Hotfix Branches**:
   * Correcciones urgentes en producción
   * Se crean desde main
   * Se fusionan en main y develop

### Mejores Prácticas
1. **Commits**:
   * Mensajes descriptivos y concisos
   * Una funcionalidad por commit
   * Usar convenciones (Conventional Commits)

2. **Branches**:
   * Nombres descriptivos
   * Eliminar ramas fusionadas
   * Mantener ramas actualizadas

3. **Seguridad**:
   * No commitear secretos
   * Usar .gitignore
   * Firmar commits importantes

## GitHub

### Características Principales
1. **Repositorios**:
   * Públicos y privados
   * Wikis y páginas
   * Releases y tags
   * Paquetes

2. **Colaboración**:
   * Pull Requests
   * Code Review
   * Issues y Projects
   * Discussions
   * Actions

3. **Seguridad**:
   * Dependabot
   * Code scanning
   * Secret scanning
   * Security advisories

### GitHub Actions (CI/CD)

#### Estructura Básica
```yaml
name: CI/CD Pipeline

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v2
    
    - name: Setup Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '16'
        
    - name: Install dependencies
      run: npm install
      
    - name: Run tests
      run: npm test
      
    - name: Build
      run: npm run build
```

#### Características Avanzadas
* **Matrices**: Pruebas en múltiples entornos
* **Secretos**: Gestión segura de credenciales
* **Artefactos**: Almacenamiento de builds
* **Cache**: Optimización de builds
* **Environments**: Gestión de despliegues
* **Composite actions**: Acciones reutilizables

## GitLab CI/CD

### Pipeline Básico
```yaml
stages:
  - build
  - test
  - deploy

build:
  stage: build
  script:
    - npm install
    - npm run build
  artifacts:
    paths:
      - dist/

test:
  stage: test
  script:
    - npm run test

deploy:
  stage: deploy
  script:
    - echo "Deploying..."
  only:
    - main
```

### Características
1. **Runners**:
   * Shared runners
   * Specific runners
   * Docker executors
   * Shell executors

2. **Variables**:
   * Predefinidas
   * Custom variables
   * Masked variables
   * File variables

3. **Environments**:
   * Staging
   * Production
   * Review apps

4. **Auto DevOps**:
   * Build automático
   * Tests automáticos
   * Security scanning
   * Code quality

## Jenkins

### Pipeline Declarativo
```groovy
pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
```

### Características
1. **Plugins**:
   * Extensible
   * Gran ecosistema
   * Integración con herramientas

2. **Agentes**:
   * Distribuidos
   * Docker
   * Kubernetes

3. **Seguridad**:
   * RBAC
   * Credentials management
   * Audit logging

## Comparativa de Herramientas CI/CD

| Característica | GitHub Actions | GitLab CI | Jenkins |
|---------------|----------------|-----------|---------|
| **Hosting** | Cloud | Cloud/Self-hosted | Self-hosted |
| **Configuración** | YAML | YAML | Groovy/YAML |
| **Curva aprendizaje** | Baja | Media | Alta |
| **Escalabilidad** | Buena | Muy buena | Excelente |
| **Personalización** | Media | Alta | Muy alta |
| **Integración** | Excelente con GitHub | Nativa GitLab | Universal |
| **Precio** | Gratis para público | Freemium | Gratis |
| **Comunidad** | Muy grande | Grande | Muy grande |

### Mejores Prácticas CI/CD

1. **Automatización**:
   * Build automático
   * Tests automáticos
   * Despliegue automático
   * Rollback automático

2. **Testing**:
   * Unit tests
   * Integration tests
   * E2E tests
   * Security tests

3. **Seguridad**:
   * Scan de dependencias
   * Análisis estático
   * Scan de secretos
   * Firmas digitales

4. **Monitoreo**:
   * Logs centralizados
   * Métricas de pipeline
   * Alertas
   * Dashboards

5. **Gestión de Versiones**:
   * Semantic versioning
   * Tags automáticos
   * Changelog automático
   * Release notes