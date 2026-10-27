# Teapot Router

**Gateway de modelos de IA para desarrolladores** — una sola clave para Claude Code y el SDK de OpenAI en un único endpoint.

Sitio oficial: <https://teapotrouter.com/es>

## - **Doble protocolo**: Anthropic Messages (compatible con Claude Code) y OpenAI Chat Completions (`/v1`) con la misma clave
- **Pago por uso y precios públicos**, incl. API JSON gratuita (`/api/pricing`)
- **Registro de costes por petición**: modelo, tokens e importe en cada llamada
- **Claves de organización y registro de auditoría**
- **Failover automático multi-upstream**

## Inicio rápido (Claude Code)

```bash
export ANTHROPIC_BASE_URL=https://api.teapotrouter.com
export ANTHROPIC_AUTH_TOKEN=sk-xxxx
claude
```

## Inicio rápido (OpenAI SDK / Codex CLI)

```bash
export OPENAI_BASE_URL=https://api.teapotrouter.com/v1
export OPENAI_API_KEY=sk-xxxx
```

## Precios

Pago por uso (prepagado desde 1 $).
Precios: <https://teapotrouter.com/es> / JSON: <https://teapotrouter.com/api/pricing>

## Sobre el proyecto

- Proyecto de desarrollo independiente
- El nombre viene del código HTTP 418 "I'm a teapot" 🫖
- Contacto: support@teapotrouter.com