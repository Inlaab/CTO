---
title: Entornos de Desarrollo
tags: [ide, vscode, desarrollo, tools]
keywords: [VS Code, Extensiones, IDE, Editor de código, Productividad, Entorno de desarrollo]
description: Editores de código y entornos integrados de desarrollo que optimizan el proceso de creación de software.
---

# Documentation

# 8️⃣ Entornos de Desarrollo: VS Code y Extensiones

## Visual Studio Code

### Información General
* **Desarrollador**: Microsoft (código abierto)
* **Lanzamiento inicial**: 2015
* **Plataformas**: Windows, macOS, Linux
* **Lenguaje**: Electron (JavaScript/TypeScript)
* **Licencia**: MIT

### Características Principales
* **IntelliSense**: Autocompletado inteligente
* **Debugging integrado**: Soporte para múltiples lenguajes
* **Terminal integrada**: Multiterminal configurable
* **Control de versiones**: Integración nativa con Git
* **Extensibilidad**: Ecosistema masivo de extensiones
* **Live Share**: Colaboración en tiempo real
* **Remote Development**: Desarrollo en contenedores, SSH y WSL
* **Personalizable**: Temas, atajos, configuraciones

### Atajos de Teclado Esenciales

#### Generales
* `Ctrl+Shift+P` / `Cmd+Shift+P`: Paleta de comandos
* `Ctrl+P` / `Cmd+P`: Búsqueda rápida de archivos
* `Ctrl+,` / `Cmd+,`: Configuración de usuario
* `Ctrl+B` / `Cmd+B`: Mostrar/ocultar barra lateral
* `Ctrl+~` / `Cmd+~`: Mostrar/ocultar terminal

#### Edición
* `Alt+↑/↓` / `Opt+↑/↓`: Mover línea arriba/abajo
* `Shift+Alt+↑/↓` / `Shift+Opt+↑/↓`: Copiar línea arriba/abajo
* `Ctrl+/` / `Cmd+/`: Comentar/descomentar línea
* `Ctrl+Shift+K` / `Cmd+Shift+K`: Eliminar línea
* `Ctrl+D` / `Cmd+D`: Seleccionar próxima ocurrencia

#### Multi-cursor
* `Alt+Click` / `Opt+Click`: Insertar cursor
* `Ctrl+Alt+↑/↓` / `Cmd+Opt+↑/↓`: Insertar cursor arriba/abajo
* `Ctrl+U` / `Cmd+U`: Deshacer último cursor

#### Navegación
* `Ctrl+G` / `Cmd+G`: Ir a línea
* `Ctrl+Tab` / `Cmd+Tab`: Navegar entre pestañas
* `Ctrl+F` / `Cmd+F`: Buscar
* `Ctrl+H` / `Cmd+H`: Reemplazar
* `F12`: Ir a definición

## Extensiones Recomendadas por Categoría

### Generales
1. **ESLint**: Integración de linting JavaScript/TypeScript
   * Características: Autofix al guardar, reglas personalizables
   * Uso: Detecta y corrige problemas de código

2. **Prettier**: Formateador de código
   * Características: Soporte para múltiples lenguajes, reglas configurables
   * Uso: Formato automático al guardar

3. **GitLens**: Supercharging Git
   * Características: Blame, historial, comparación
   * Uso: Información detallada sobre commits y cambios

4. **Path Intellisense**: Autocompletado de rutas
   * Características: Sugerencias de rutas de archivos
   * Uso: Autocompletar importaciones y rutas

5. **Auto Rename Tag**: Renombra etiquetas HTML automáticamente
   * Características: Renombrado de etiquetas en pares
   * Uso: Facilita edición de HTML/JSX

### JavaScript/TypeScript
1. **JavaScript (ES6) code snippets**: Snippets para JS moderno
   * Características: Atajos para sintaxis común
   * Uso: Acelerar escritura de código JS

2. **TypeScript Hero**: Organizador de importaciones
   * Características: Ordenar y eliminar importaciones no usadas
   * Uso: Mantener código ordenado

3. **Quokka.js**: JavaScript/TypeScript playground
   * Características: Evaluación en tiempo real
   * Uso: Prototipar y experimentar rápidamente

4. **npm Intellisense**: Autocompletado para módulos npm
   * Características: Sugerencias de paquetes instalados
   * Uso: Facilitar importaciones desde node_modules

### React/Vue/Angular
1. **React Snippets**: Snippets para React
   * Características: Atajos para componentes y hooks
   * Uso: Acelerar desarrollo React

2. **Vetur**: Vue tooling
   * Características: Sintaxis, snippets, emmet, linting
   * Uso: Desarrollo completo de Vue

3. **Angular Language Service**: Soporte para Angular templates
   * Características: Autocompletado, diagnósticos, navegación
   * Uso: Desarrollo eficiente de Angular

4. **Svelte for VS Code**: Soporte para Svelte
   * Características: Syntax highlighting, IntelliSense
   * Uso: Desarrollo completo de Svelte

### CSS/SCSS/Styling
1. **CSS Peek**: Navegación rápida a definiciones CSS
   * Características: Go-to-definition para selectores
   * Uso: Inspeccionar y editar estilos rápidamente

2. **Tailwind CSS IntelliSense**: Soporte para Tailwind
   * Características: Autocompletado, linting, hover preview
   * Uso: Desarrollo eficiente con Tailwind

3. **SCSS IntelliSense**: Autocompletado para SCSS
   * Características: Completado de variables, mixins, funciones
   * Uso: Desarrollo avanzado con SCSS

### Python
1. **Python**: Soporte oficial de Python
   * Características: IntelliSense, linting, debugging
   * Uso: Desarrollo completo de Python

2. **Jupyter**: Soporte para notebooks
   * Características: Edición, visualización, ejecución
   * Uso: Análisis de datos interactivo

3. **Pylance**: Language server para Python
   * Características: Tipo checking, performance
   * Uso: Mejorar productividad en Python

### Backend/API
1. **REST Client**: Testing de APIs
   * Características: Envío de requests HTTP
   * Uso: Pruebas de endpoints API sin salir del editor

2. **Thunder Client**: Cliente REST alternativo
   * Características: UI amigable, colecciones, variables
   * Uso: Testing avanzado de APIs

3. **Database Client**: Cliente de base de datos
   * Características: Conexión a múltiples DBMS
   * Uso: Consultas SQL desde VS Code

### DevOps
1. **Docker**: Integración de Docker
   * Características: Syntax highlighting, commands, containerization
   * Uso: Gestión de containers desde el editor

2. **Kubernetes**: Soporte para K8s
   * Características: Sintaxis, snippets, comandos
   * Uso: Gestión de clusters y manifiestos

3. **Remote Development**: Desarrollo remoto
   * Características: SSH, Containers, WSL
   * Uso: Desarrollo en entornos remotos

### Temas y Personalización
1. **One Dark Pro**: Tema basado en Atom
   * Características: Contraste equilibrado, soporte para lenguajes
   * Uso: Reduce fatiga visual

2. **Material Icon Theme**: Iconos para archivos
   * Características: +1000 iconos, personalizable
   * Uso: Identificación visual de archivos

3. **Peacock**: Color identifier para workspaces
   * Características: Colorear ventanas por proyecto
   * Uso: Diferenciar visualmente entre proyectos

### Productividad
1. **Settings Sync**: Sincronización de configuraciones
   * Características: Sincronizar settings, snippets, extensiones
   * Uso: Mantener configuración consistente entre dispositivos

2. **Project Manager**: Gestión de proyectos
   * Características: Guardar, organizar y cambiar entre proyectos
   * Uso: Acceso rápido a proyectos frecuentes

3. **Code Spell Checker**: Corrector ortográfico
   * Características: Detección multilenguaje
   * Uso: Evitar errores tipográficos en código y comentarios

## Configuraciones Recomendadas (settings.json)

```json
{
  // Editor
  "editor.fontSize": 14,
  "editor.fontFamily": "Fira Code, Menlo, Monaco, 'Courier New', monospace",
  "editor.fontLigatures": true,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.organizeImports": true
  },
  "editor.bracketPairColorization.enabled": true,
  "editor.guides.bracketPairs": true,
  "editor.minimap.enabled": false,
  "editor.wordWrap": "on",
  
  // Terminal
  "terminal.integrated.fontSize": 13,
  "terminal.integrated.fontFamily": "MesloLGS NF, Menlo, Monaco, 'Courier New', monospace",
  "terminal.integrated.defaultProfile.osx": "zsh",
  "terminal.integrated.defaultProfile.windows": "PowerShell",
  
  // Files
  "files.autoSave": "onFocusChange",
  "files.trimTrailingWhitespace": true,
  "files.insertFinalNewline": true,
  "files.exclude": {
    "**/.git": true,
    "**/.DS_Store": true,
    "**/node_modules": true,
    "**/dist": false
  },
  
  // Languages specific
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[css]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[python]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "ms-python.python"
  },
  
  // Git
  "git.enableSmartCommit": true,
  "git.confirmSync": false,
  "git.autofetch": true,
  
  // Prettier
  "prettier.singleQuote": true,
  "prettier.trailingComma": "es5",
  "prettier.printWidth": 100,
  
  // ESLint
  "eslint.validate": [
    "javascript",
    "typescript",
    "javascriptreact",
    "typescriptreact"
  ],
  
  // Live Share
  "liveshare.presence": true,
  "liveshare.audio.startCallOnShare": true,
  
  // Workbench
  "workbench.iconTheme": "material-icon-theme",
  "workbench.colorTheme": "One Dark Pro",
  "workbench.startupEditor": "newUntitledFile",
  "workbench.editor.enablePreview": false
}
```

## Características Avanzadas

### Snippets Personalizados
Crear en: `File > Preferences > User Snippets`

Ejemplo para React functional component:
```json
{
  "React Functional Component": {
    "prefix": "rfc",
    "body": [
      "import React from 'react';",
      "",
      "interface ${1:ComponentName}Props {",
      "  $2",
      "}",
      "",
      "export const ${1:ComponentName}: React.FC<${1:ComponentName}Props> = (props) => {",
      "  return (",
      "    <div>",
      "      $0",
      "    </div>",
      "  );",
      "};",
      ""
    ],
    "description": "React Functional Component with TypeScript"
  }
}
```

### Tasks y Launch Configurations
Archivo `.vscode/tasks.json` para automatizar tareas:
```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Build",
      "type": "npm",
      "script": "build",
      "group": {
        "kind": "build",
        "isDefault": true
      }
    },
    {
      "label": "Test",
      "type": "npm",
      "script": "test",
      "group": {
        "kind": "test",
        "isDefault": true
      }
    }
  ]
}
```

Archivo `.vscode/launch.json` para debugging:
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Debug Server",
      "program": "${workspaceFolder}/src/server.js",
      "skipFiles": ["<node_internals>/**"]
    },
    {
      "type": "chrome",
      "request": "launch",
      "name": "Debug React",
      "url": "http://localhost:3000",
      "webRoot": "${workspaceFolder}/src",
      "userDataDir": "${workspaceFolder}/.vscode/chrome",
      "sourceMapPathOverrides": {
        "webpack:///src/*": "${webRoot}/*"
      }
    }
  ],
  "compounds": [
    {
      "name": "Full Stack",
      "configurations": ["Debug Server", "Debug React"]
    }
  ]
}
```

### Dev Containers
Archivo `.devcontainer/devcontainer.json` para desarrollo en contenedores:
```json
{
  "name": "Node.js Development",
  "image": "mcr.microsoft.com/devcontainers/javascript-node:18",
  "settings": {
    "editor.formatOnSave": true
  },
  "extensions": [
    "dbaeumer.vscode-eslint",
    "esbenp.prettier-vscode",
    "ms-azuretools.vscode-docker"
  ],
  "forwardPorts": [3000, 5000],
  "postCreateCommand": "npm install"
}
```

## Integración con GitHub Copilot

### Características
* **Autocompletado de código**: Sugerencias basadas en IA
* **Completado de funciones**: Implementaciones automáticas
* **Generación de pruebas**: Creación de tests
* **Documentación**: Generación automática de comentarios
* **Explicación de código**: Análisis de código existente

### Configuración Óptima
```json
{
  "github.copilot.enable": {
    "*": true,
    "yaml": true,
    "plaintext": true,
    "markdown": true
  },
  "github.copilot.inlineSuggest.enable": true,
  "editor.inlineSuggest.enabled": true,
  "github.copilot.advanced": {
    "indentationMode": true
  }
}
```

### Atajos para Copilot
* `Alt+]` / `Opt+]`: Ver siguiente sugerencia
* `Alt+[` / `Opt+[`: Ver sugerencia anterior
* `Tab`: Aceptar sugerencia
* `Esc`: Rechazar sugerencia
* `Ctrl+Enter` / `Cmd+Enter`: Abrir panel Copilot

## Trucos Avanzados

### Multiroot Workspaces
Para trabajar con varios proyectos relacionados:
1. `File > Add Folder to Workspace`
2. `File > Save Workspace As`

### Profile Manager (VS Code 1.75+)
Crear perfiles para diferentes flujos de trabajo:
1. `F1 > Profiles: Create Profile`
2. Seleccionar extensiones, configuraciones y temas

### Timeline View
Ver historial de cambios en archivos:
1. Abrir archivo
2. Click en icono "Timeline" en el panel secundario

### Embedder Terminal
Configurar terminales personalizadas:
```json
"terminal.integrated.profiles.windows": {
  "PowerShell (Admin)": {
    "path": "pwsh.exe",
    "args": ["-NoExit", "-Command", "Start-Process pwsh -Verb RunAs"]
  }
}
```

### WSL Integration
Desarrollo directo en WSL (Windows):
1. Instalar extensión "Remote - WSL"
2. `F1 > Remote-WSL: New Window`

### Customizar Status Bar
```json
"workbench.statusBar.visible": true,
"workbench.statusBar.feedback.visible": false,
"workbench.statusBar.compact": true
```

### Zen Mode Personalizado
```json
"zenMode.hideLineNumbers": true,
"zenMode.hideStatusBar": true,
"zenMode.hideTabs": true,
"zenMode.fullScreen": false,
"zenMode.restore": true
```

¿Te gustaría que profundice en alguna de estas secciones o prefieres que abordemos otro tema relacionado con entornos de desarrollo?