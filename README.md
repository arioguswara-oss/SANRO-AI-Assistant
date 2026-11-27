# SANRO AI Assistant

Standalone WordPress & WooCommerce customer service plugin. Slug: `sanro-ai-assistant`. Target V1.0.0; initial development V0.1.0-dev. First deployment candidate: KaosCetak.id (staging first).

## Scope V1
- Floating responsive chat, minimized icon bottom right, expand/minimize without losing session, no automatic popup by default; configurable page visibility, name, avatar, colors, greeting, tone, language and optional language detection.
- Configurable quick actions (FAQ, AI question, direct action/link), WhatsApp human handover via wa.me, configurable number and message; optional sanitized conversation summary with consent.
- Knowledge Base from approved WordPress content and manual FAQs; WooCommerce products, prices, variations and stock as authoritative live data. Unanswered questions reviewed by admin before adding answers. Conversation dashboard, retention configurable (proposed 30 days).
- WooCommerce native CRUD/HPOS read-only integration. Pending/on-hold/processing/completed/cancelled/failed/refunded mapping; processing indicates processing, completed with shipment evidence indicates sent. No separate production workflow. Read shipment metadata, carrier, tracking link and history if available; configurable mapping. Never invent tracking data.
- Guest order lookup without account registration; verify ownership before disclosing order-specific data, using signed order link or email OTP; logged-in users only their own orders. Order number alone is not authentication. No transaction writes, refunds, discounts or cancellations by AI.
- Optional external tracking module, default OFF, BYOK. No mandatory carrier API/webhook. Only verified store shipments; cache per carrier/resi (proposed 12h), no polling, no customer forced refresh, atomic deduplication, stop refreshing delivered parcels, daily request and monthly budget caps (proposed 100/day and Rp50,000/month, configurable). Fall back to WooCommerce data/link.
- AI router: OpenRouter, Gemini, OpenAI-compatible adapter initially proposed; configurable provider/model/key, fallback, connection test. FAQ and deterministic WooCommerce actions first, AI only when necessary. Strict business context default ON; configurable refusal, no unrelated answers or invented data. Rate limits, message size limits, anti-spam, usage metrics, request/token caps, bounded fallback; protect credentials server-side and minimize personal data sent to providers. FAQ/order/WhatsApp remain available when AI unavailable.
- One plugin ZIP, modular architecture, one license per WordPress site, BYOK separate from license, no Hermes dependency. License server, migration and outage policy to be specified; staging test license proposed.

## Development policy
Development First; one integration branch `develop` after initialization; max five related tasks per cycle. Targeted lint/security/runtime tests during development; comprehensive audit near 90%. Staging only; merge and production require explicit owner approval. No Codex/Hermes execution without owner authorization. Keep secrets and customer data out of public repository.

## Initial checkpoint — 2026-11-27
Implementation baseline: 0%. Documentation only; no plugin code, tests, deployment or release yet. Pending: verify shipment metadata, provider APIs/pricing, license infrastructure and guest verification UX. Proposed defaults above are subject to owner confirmation.

## First development cycle
1. Initialize plugin skeleton and integration branch.
2. Establish checkpoint and progress ledger.
3. Admin settings and identity/language.
4. Responsive floating widget, shortcuts and WhatsApp handover.
5. Knowledge Base and basic WooCommerce read-only integration.
