<div align="center">

# Teapot Router — gateway de API LLM para agentes de código

**Una clave. Dos protocolos. Pagas por uso — y el saldo nunca caduca.**

Gateway alojado para Claude Code, Codex CLI y herramientas con OpenAI SDK: cambia dos variables de entorno y todas tus herramientas de código con IA pasan por un mismo endpoint, un mismo saldo y un libro de costes por solicitud.

[Empezar](https://teapotrouter.com/es/register) · [Precios — públicos, JSON legible por máquinas](https://teapotrouter.com/api/pricing) · [Documentación](https://teapotrouter.com/es/docs)

</div>

---

## ¿Por qué un gateway para agentes de código?

Si usas Claude Code junto a herramientas del OpenAI SDK, ya conoces el problema: cada herramienta quiere su endpoint y su clave, y la factura es una caja negra mensual.

Un gateway ordena la fontanería:

| | Conexión directa (por proveedor) | Vía gateway |
| --- | --- | --- |
| Endpoints y claves | uno por proveedor | **una clave, dos protocolos** |
| Facturación | N paneles, totales mensuales | un saldo, **libro por solicitud** |
| Visibilidad de coste | "fueron $84" | "esa sesión costó $6.20 — el 78% fue contexto reenviado" |
| Condiciones | política por proveedor | aquí: **el saldo no caduca**, reembolso por saldo restante |

## Configuración: dos variables de entorno

```bash
# Claude Code (protocolo Anthropic)
export ANTHROPIC_BASE_URL="https://api.teapotrouter.com"
export ANTHROPIC_AUTH_TOKEN="sk-****"

# OpenAI SDK / Codex CLI — misma clave, endpoint /v1
# base_url = https://api.teapotrouter.com/v1
```

Guías paso a paso (registro → primera petición → resolución de problemas): [teapotrouter.com/es/docs](https://teapotrouter.com/es/docs)

## Qué puedes ver en el sitio

- [Blog] ¿A dónde va realmente una factura de Claude Code?(https://teapotrouter.com/es/blog/where-does-a-claude-code-bill-go)
- [Calculadora de costes gratuita (sin registro, tarifas en vivo)](https://teapotrouter.com/es/claude-code-cost-calculator) — suscripción vs pago por uso
- **Precios públicos** — tarifa base y precio real de cada modelo, con un endpoint JSON sin login ([`/api/pricing`](https://teapotrouter.com/api/pricing)) para comparar por script
- **Página de precios por modelo** — p. ej. [claude-opus-5-5](https://teapotrouter.com/es/pricing/claude-opus-5-5)
- **Guía de precios de Claude Code** — suscripción vs pago por uso vs gateway, con el cálculo real: [documentación](https://teapotrouter.com/es/docs/claude-code-pricing)
- **Guía de resolución de problemas** — conexión, 401 y errores de cuota emparejados con su solución: [documentación](https://teapotrouter.com/es/docs/claude-code-troubleshooting)

## Dos preguntas que deberías hacer a cualquier gateway (también a este)

- **¿De dónde salen los modelos?** De canales API oficiales/autorizados, medidos y pagados por uso. Sin cuentas compartidas ni reventa de suscripciones.
- **¿Qué se registra?** Solo metadatos de facturación (modelo, tokens, coste, latencia) — es lo que hace posible el libro por solicitud. No hacemos teatro de "cero logs"; no tocamos el contenido de las conversaciones.

## Límites honestos

Proyecto de una sola persona, lanzado hace poco, sin presupuesto de marketing — el endpoint de precios muestra siempre la lista viva de modelos, así que compruébalo tú mismo en vez de fiarte de este README. El failover multi-upstream está integrado, pero un gateway sigue siendo una dependencia: deja una ruta alternativa.

Contacto: support@teapotrouter.com

---

<div align="center">

El nombre viene del código de estado HTTP 418 "I'm a teapot" 🫖 — [la historia completa](https://teapotrouter.com/es/418)

**[Teapot Router](https://teapotrouter.com/es)** — gateway de IA stability-first para Claude Code y GPT.

</div>
