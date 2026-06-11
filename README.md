# Family VPN Config

Routing-правила и subscription-файлы для семейного VPN (3x-ui/VLESS на 194.87.216.51).

- `routing-family.json` — routing-профиль (Telegram/Google/YouTube/Instagram через прокси, RU-сервисы напрямую). Источник правды, раздаётся через jsDelivr.
- `sub/*.txt` — subscription-файлы, по одному на человека. Раздаются через jsDelivr — короткая ссылка-подписка с автообновлением.
- `telegram-fix-import-line.txt` — резервные правила одной строкой (inline base64) на случай блокировки jsDelivr.

## Текущая схема (2026-06-11)

Каждая подписка (`sub/<имя>.txt`) содержит:
1. `://autorouting/onadd/https://cdn.jsdelivr.net/gh/AstorTiko/family-vpn-config@main/routing-family.json` — правила маршрутизации (RU напрямую, Telegram/Google/Meta через VPN).
2. **🚀 ... Reality** — основной сервер, порт 443, VLESS+gRPC+Reality (маскировка под HTTPS к addons.mozilla.org, не душится DPI).
3. **🇳🇱 ...** — резервный сервер, порт 40545, naked VLESS (security=none).

Раздача — `family-delivery.md`. После любого изменения файлов в репо — purge кэша jsDelivr: `https://purge.jsdelivr.net/gh/AstorTiko/family-vpn-config@main/<file>`.
