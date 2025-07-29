# 🤖 Rasa Chatbot - Proyecto Base

Este proyecto contiene una plantilla base generada con `rasa init`. Usa procesamiento de lenguaje natural para construir un asistente conversacional personalizado.

---

## 📦 Requisitos

- Python 3.8.10
- pip
- Entorno virtual
- Rasa 3.6.21 
- Rasa SDK 3.6.2

---

## 🚀 Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/BCarreonC/rasa-bot1.git
cd rasa-bot1

2. Crear y activar entorno virtual

python -m venv venv

Ingresa al entorno virtual

# En Linux/macOS:
source venv/bin/activate
# En Windows:
venv\Scripts\activate

3. Instalar Rasa

pip install rasa

⚙️ Inicialización del proyecto

Crear un proyecto nuevo (solo si partes desde cero)

rasa init

Esto generará:
.
├── actions/             # Acciones personalizadas en Python
├── data/                # Intenciones, historias y reglas
├── tests/               # Historias para pruebas
├── config.yml           # Configuración del pipeline NLU y políticas
├── domain.yml           # Intenciones, respuestas, entidades, acciones
├── credentials.yml      # Configuración de canales (REST, Telegram, etc.)
├── endpoints.yml        # Endpoints para acciones, tracker store, etc.

🧠 Entrenar el modelo

rasa train

Esto generará un modelo dentro de la carpeta models/.

💬 Probar el bot en consola

rasa shell

🔁 Ejecutar el bot con servidor y acciones personalizadas

Terminal 1: iniciar el servidor de acciones

rasa run actions

Terminal 2: iniciar el servidor del bot

rasa run

Para probar el webhook REST(Pruebas de usuario):

curl -X POST http://localhost:5005/webhooks/rest/webhook \
     -H "Content-Type: application/json" \
     -d '{"sender": "test_user", "message": "hola"}'

🧪 Ejecutar pruebass

rasa test
