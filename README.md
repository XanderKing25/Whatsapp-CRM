# 🤖 WhatsApp CRM & AuditBot 3000

> **Solución Ganadora - Hackathon Cúcuta 2026**
> Gestión de Clientes y Auditoría de Calidad con IA en Tiempo Real.

## 🚀 Descripción del Proyecto
Plataforma web "todo en uno" para gestionar clientes de WhatsApp Business. A diferencia de los CRM tradicionales, esta solución integra un **Auditor de IA (AuditBot)** que analiza automáticamente los chats para detectar mala atención, groserías y clientes insatisfechos sin intervención humana.

## 💡 El Pivote: Arquitectura Serverless & Client-Side
Originalmente concebido con un backend en Python, el equipo migró el núcleo lógico a **JavaScript Vanilla** para crear una solución más rápida, segura y fácil de desplegar.

**Ventajas de esta arquitectura:**
* ⚡ **Cero Latencia:** La IA y el procesamiento de datos ocurren directamente en el navegador del usuario.
* 🔒 **Privacidad:** Los datos sensibles de los clientes se guardan en `LocalStorage` y no viajan a servidores externos innecesarios.
* 📱 **Portabilidad:** Funciona como una Web App progresiva (PWA), accesible desde cualquier dispositivo.

---

## 🛠️ Stack Tecnológico

| Componente | Tecnología | Uso en el Proyecto |
| :--- | :--- | :--- |
| **Core** | **JavaScript (ES6+)** | Lógica de negocio, gestión de estado y control de vistas. |
| **Interfaz** | **HTML5 + Tailwind CSS** | Diseño responsivo, moderno y animaciones fluidas (`fade-in`). |
| **Persistencia** | **LocalStorage** | Base de datos en el navegador para persistencia de sesiones y clientes. |
| **IA Engine** | **Google Gemini API** | Integración directa vía REST para análisis de sentimiento y chatbot. |
| **Visualización** | **Chart.js** | Gráficas dinámicas de distribución de clientes en el Dashboard. |
| **Datos** | **PapaParse** | Motor de importación masiva de archivos CSV. |

---

## ⚙️ Módulos Principales

### 1. 📊 Dashboard Gerencial
Vista unificada con métricas en tiempo real:
* Total de clientes y desglose por estado (Nuevo, Seguimiento, Cerrado).
* Métricas de rendimiento de agentes.
* Gráfica de anillo (Doughnut Chart) para visualización rápida.

### 2. 🕵️ AuditBot (Auditoría IA)
El corazón del proyecto. Un motor de análisis que procesa historiales de chat para:
* **Detectar Sentimiento:** Clasifica mensajes en Positivo, Neutro o Negativo.
* **Alerta de Groserías:** Identifica lenguaje ofensivo tanto de clientes como de agentes.
* **Recomendaciones:** Sugiere acciones inmediatas (ej: "Escalar a Supervisor", "Agradecer").
* *Modo Híbrido:* Funciona con la API de Gemini o con un sistema de reglas (fallback) si no hay internet.

### 3. 🤖 Asistente IA (Chatbot RAG)
Chatbot inteligente capaz de responder preguntas sobre la base de datos local.
* *Ejemplo:* "¿Quién es el cliente más enojado hoy?" o "¿Cuántos clientes nuevos hay?".
* Utiliza inyección de contexto para que la IA "lea" los datos del navegador y responda.

### 4. 💬 Centro de Conversaciones
Interfaz tipo WhatsApp Web para:
* Ver historial de chats.
* Simular la recepción de mensajes en tiempo real.
* Asignar conversaciones a agentes específicos.

---

## 🚀 Instalación y Uso
¡No requiere instalación de servidores ni bases de datos!

1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/xanderking25/Whatsapp-CRM.git](https://github.com/xanderking25/Whatsapp-CRM.git)
    ```
2.  **Ejecutar:**
    Simplemente abre el archivo `index.html` en cualquier navegador moderno (Chrome, Edge, Firefox).

3.  **Configuración de IA:**
    * Ve a la pestaña **Auditoría**.
    * Ingresa tu API Key de Google Gemini (Opcional: el sistema funciona en modo básico sin ella).

---

## 📂 Estructura de Archivos
* `index.html`: Contiene toda la lógica (JS), estilos (Tailwind) y estructura (HTML). ¡Una joya de optimización!
* `data.csv`: Datos de prueba para importar y testear el sistema rápidamente.
* `LICENSE`: Licencia MIT de código abierto.

---

## 👥 Autores
Desarrollado por **Ruben Alexander Villegas Julio** y equipo para el Reto Tecnológico 2026.

> *"La mejor herramienta es la que funciona cuando más la necesitas."*
