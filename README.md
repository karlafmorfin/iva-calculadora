# Calculadora de IVA (Azure Static Web Apps + GitHub)

Esta es una web estática (HTML/JS) para calcular IVA. Ideal para desplegar en **Azure Static Web Apps** usando **GitHub Actions**.

## Estructura
- `index.html` — la app (sin build: HTML + JS puro).
- `.github/workflows/azure-static-web-apps.yml` — workflow para desplegar.

## Pasos rápidos (manual con token)
1. Crea un **Azure Static Web App** (plan *Free*).
2. Copia el **Deployment Token** del recurso (Portal → tu SWA → *Manage deployment token*).
3. En tu repo de GitHub: **Settings → Secrets and variables → Actions → New repository secret**:
   - Nombre: `AZURE_STATIC_WEB_APPS_API_TOKEN`
   - Valor: pega el token.
4. Haz push a `main`. El workflow desplegará a `https://<algo>.azurestaticapps.net`.

> Alternativa recomendada: crea la SWA desde el portal eligiendo **GitHub** como fuente; el portal generará el workflow y el secreto automáticamente.
