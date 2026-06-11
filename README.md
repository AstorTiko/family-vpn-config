# Family VPN Config

Routing-правила и subscription-файлы для семейного VPN (3x-ui/VLESS на 194.87.216.51).

- `routing-family.json` — routing-профиль (Telegram/Google/YouTube/Instagram через прокси, RU-сервисы напрямую). Источник правды.
- `sub/*.txt` — subscription-файлы, по одному на человека. Правила **вшиты inline** в base64 (`://routing/onadd/<base64>`), сервер — vless-строкой.
- `telegram-fix-import-line.txt` — те же правила одной строкой для разового импорта.

## Важно (2026-06)

Правила больше **не тянутся с GitHub**. `raw.githubusercontent.com` режется в РФ (особенно на мобильных операторах) → раньше с телефонов правила не докачивались, Telegram уходил напрямую и душился, а Wildberries видел VPN. Теперь правила вшиты в подписку и скачивать ничего не нужно.

**Доставка пользователям — вставкой текста подписки (paste), а НЕ по URL с github.** Этот репозиторий — бэкап/история; импорт делается из `family-delivery.md`.
