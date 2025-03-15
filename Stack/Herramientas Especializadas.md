---
title: Herramientas Especializadas
tags: [specialized, web, meta, tools]
keywords: [Bootpress, Meta, Facebook, Instagram, Herramientas especializadas, Desarrollo web]
description: Herramientas orientadas a dominios específicos de desarrollo que potencian la productividad en áreas concretas.
---

# Documentation

# 9️⃣ Herramientas Especializadas: Botpress y Meta

## Botpress

### Conceptos Fundamentales
* **Plataforma**: Framework de código abierto para crear chatbots
* **Arquitectura**: Modular y extensible
* **Lenguaje**: JavaScript/TypeScript
* **Tipo**: Conversational AI Platform

### Componentes Principales

#### 1. Content Types
```javascript
// Definición de tipo de contenido personalizado
module.exports = {
  id: 'greeting',
  title: 'Greeting Message',
  jsonSchema: {
    title: 'A greeting message',
    type: 'object',
    required: ['message'],
    properties: {
      message: { type: 'string', title: 'Message' },
      options: { type: 'array', title: 'Options' }
    }
  }
}
```

#### 2. Actions
```javascript
// Acción personalizada
const myAction = async () => {
  const user = event.target
  const response = await axios.get(`/api/users/${user}`)
  
  temp.userData = response.data
  
  return {
    success: true,
    data: response.data
  }
}
```

#### 3. Flow Builder
```javascript
// Definición de flujo
{
  "version": "0.1",
  "name": "main.flow",
  "flows": [
    {
      "name": "welcome",
      "nodes": [
        {
          "id": "entry",
          "type": "standard",
          "next": ["welcome-msg"]
        },
        {
          "id": "welcome-msg",
          "type": "say",
          "message": "Welcome to our bot!"
        }
      ]
    }
  ]
}
```

### Integración con NLU (Natural Language Understanding)

```javascript
// Entrenamiento de intenciones
module.exports = {
  intents: [
    {
      name: 'greet',
      utterances: [
        'hello',
        'hi',
        'hey there',
        'good morning'
      ]
    },
    {
      name: 'goodbye',
      utterances: [
        'bye',
        'goodbye',
        'see you later'
      ]
    }
  ]
}
```

### Hooks y Middleware

```javascript
// Hook antes de procesar mensaje
bp.events.registerMiddleware({
  name: 'user-logger',
  description: 'Logs user messages',
  order: 1,
  handler: async (event, next) => {
    if (event.type === 'text') {
      console.log(`User said: ${event.payload.text}`)
    }
    return next()
  }
})
```

### Configuración de Canal

```javascript
// Configuración de canal web
module.exports = {
  channels: {
    web: {
      enabled: true,
      port: 3000,
      host: 'localhost',
      cors: {
        enabled: true,
        origin: '*'
      }
    }
  }
}
```

## Meta (Facebook) APIs

### Facebook Graph API

#### 1. Configuración Inicial
```javascript
const FB = require('fb');
FB.setAccessToken('your-access-token');
```

#### 2. Publicar en Página
```javascript
FB.api(
  '/page-id/feed',
  'POST',
  { message: 'Hello from API!' },
  function(response) {
    if (!response || response.error) {
      console.error('Error:', response.error);
      return;
    }
    console.log('Post ID:', response.id);
  }
);
```

#### 3. Obtener Insights
```javascript
FB.api(
  '/page-id/insights',
  'GET',
  {
    metric: ['page_impressions', 'page_engaged_users'],
    period: 'day'
  },
  function(response) {
    console.log(response.data);
  }
);
```

### Instagram Graph API

#### 1. Publicar Contenido
```javascript
FB.api(
  '/instagram-account-id/media',
  'POST',
  {
    image_url: 'https://example.com/image.jpg',
    caption: 'Test post from API'
  },
  function(response) {
    if (response.id) {
      FB.api(
        '/instagram-account-id/media_publish',
        'POST',
        { creation_id: response.id },
        function(publishResponse) {
          console.log('Published:', publishResponse);
        }
      );
    }
  }
);
```

#### 2. Obtener Métricas
```javascript
FB.api(
  '/instagram-account-id/insights',
  'GET',
  {
    metric: ['impressions', 'reach', 'profile_views'],
    period: 'day'
  },
  function(response) {
    console.log(response.data);
  }
);
```

### WhatsApp Business API

#### 1. Enviar Mensaje
```javascript
const axios = require('axios');

async function sendWhatsAppMessage(phoneNumber, message) {
  try {
    const response = await axios.post(
      `https://graph.facebook.com/v13.0/${phoneNumber}`,
      {
        messaging_product: 'whatsapp',
        to: phoneNumber,
        type: 'text',
        text: { body: message }
      },
      {
        headers: {
          'Authorization': `Bearer ${process.env.WHATSAPP_TOKEN}`
        }
      }
    );
    return response.data;
  } catch (error) {
    console.error('Error:', error);
    throw error;
  }
}
```

#### 2. Plantillas de Mensaje
```javascript
async function sendTemplateMessage(phoneNumber, templateName, components) {
  try {
    const response = await axios.post(
      `https://graph.facebook.com/v13.0/${phoneNumber}`,
      {
        messaging_product: 'whatsapp',
        to: phoneNumber,
        type: 'template',
        template: {
          name: templateName,
          language: {
            code: 'es'
          },
          components: components
        }
      },
      {
        headers: {
          'Authorization': `Bearer ${process.env.WHATSAPP_TOKEN}`
        }
      }
    );
    return response.data;
  } catch (error) {
    console.error('Error:', error);
    throw error;
  }
}
```

### Messenger Platform

#### 1. Configuración de Webhook
```javascript
const express = require('express');
const app = express();

app.post('/webhook', (req, res) => {
  if (req.body.object === 'page') {
    req.body.entry.forEach(entry => {
      entry.messaging.forEach(event => {
        if (event.message) {
          handleMessage(event);
        }
      });
    });
    res.status(200).send('EVENT_RECEIVED');
  } else {
    res.sendStatus(404);
  }
});
```

#### 2. Enviar Respuesta
```javascript
async function handleMessage(event) {
  const senderId = event.sender.id;
  const message = event.message.text;

  try {
    await axios.post(
      `https://graph.facebook.com/v13.0/me/messages`,
      {
        recipient: {
          id: senderId
        },
        message: {
          text: `Echo: ${message}`
        }
      },
      {
        headers: {
          'Authorization': `Bearer ${process.env.PAGE_ACCESS_TOKEN}`
        }
      }
    );
  } catch (error) {
    console.error('Error sending message:', error);
  }
}
```

### Meta Pixel

#### 1. Instalación Básica
```html
<!-- Meta Pixel Code -->
<script>
!function(f,b,e,v,n,t,s)
{if(f.fbq)return;n=f.fbq=function(){n.callMethod?
n.callMethod.apply(n,arguments):n.queue.push(arguments)};
if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
n.queue=[];t=b.createElement(e);t.async=!0;
t.src=v;s=b.getElementsByTagName(e)[0];
s.parentNode.insertBefore(t,s)}(window, document,'script',
'https://connect.facebook.net/en_US/fbevents.js');
fbq('init', 'your-pixel-id');
fbq('track', 'PageView');
</script>
```

#### 2. Eventos Personalizados
```javascript
// Seguimiento de conversión
fbq('track', 'Purchase', {
  value: 99.99,
  currency: 'USD',
  content_ids: ['123'],
  content_type: 'product'
});

// Evento personalizado
fbq('trackCustom', 'UserAction', {
  category: 'engagement',
  action: 'click',
  label: 'signup_button'
});
```

### Meta Authentication

#### 1. Login con Facebook
```javascript
FB.login(function(response) {
  if (response.status === 'connected') {
    // Usuario logueado y autenticado
    const accessToken = response.authResponse.accessToken;
    const userID = response.authResponse.userID;
  } else {
    // Usuario no autenticado
  }
}, {scope: 'email,public_profile'});
```

#### 2. Verificación de Estado
```javascript
FB.getLoginStatus(function(response) {
  if (response.status === 'connected') {
    // Usuario ya logueado
  } else if (response.status === 'not_authorized') {
    // Usuario no autorizado
  } else {
    // Usuario no logueado
  }
});