# Family VPN Config

Routing-правила и subscription-файлы для семейного VPN (3x-ui/VLESS на 194.87.216.51).

- `routing-family.json` — autorouting профиль (Telegram/Google/YouTube/Instagram через прокси, RU-сервисы напрямую).
- `sub/*.txt` — subscription-файлы для импорта в INcy, по одному на человека.

При смене сервера (IP/порт/UUID) обновляются только файлы в `sub/`, пользователям ничего менять не нужно — INcy подхватит обновление по `profile-update-interval`.
