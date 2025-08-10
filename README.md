# CrestaTrainer • Demo desplegable en Vercel

## Requisitos
- Cuenta en OpenAI (clave API).
- Cuenta en GitHub.
- Cuenta en Vercel.

## Pasos (no necesitas instalar nada en tu PC)
1. **Descarga este ZIP** y descomprímelo en una carpeta.
2. Entra a **GitHub** → *New repository* → ponle nombre `cresta-trainer-demo`.
3. Sube todos los archivos de esta carpeta al repositorio (botón **Upload files**).
4. Entra a **Vercel** → *New Project* → **Import Git Repository** → elige `cresta-trainer-demo`.
5. Cuando te pida **Environment Variables** añade:
   - `OPENAI_API_KEY` = tu clave (desde platform.openai.com → API keys).
6. Pulsa **Deploy**. En 1-3 minutos tendrás una URL pública.
7. Abre la URL → verás el chat. Escribe tu respuesta y la IA contestará como cliente. Pulsa **Finalizar** para ver la evaluación en **JSON**.

## Configurable
- Caso y nivel: se cambian en `public/index.html` en el `fetch('/api/simulate', { body: ... })`.
- Modelo: en `api/*.js` puedes cambiar `gpt-4o-mini` por otro.

## Observaciones
- Este demo no guarda datos en BBDD. Para producción usa Postgres/Firestore.
- Escala razonablemente bien para pruebas; para 200 concurrentes añade colas y límites.
