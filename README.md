# Shadowrocket Seamless Config (`bmnd-config`)

Лёгкий автообновляемый конфиг маршрутизации для Shadowrocket (iOS / iPadOS / macOS) через быстрый CDN `jsDelivr`.
Не содержит серверов, IP-адресов и ключей — только правила маршрутизации.

## 1. Ссылка на конфиг (Shadowrocket → `Config` → `+`)

```text
https://cdn.jsdelivr.net/gh/bomondxxx-maker/bmnd-config@main/bmnd_config.conf
```

После загрузки тапнуть по `bmnd_config.conf` → **Use Config (Использовать конфиг)**, на главной выбрать `Global Routing` → **`Config`**.

## 2. Рекомендуемые настройки «поставил и забыл»

1. **Реальная проверка серверов:** `Settings → Advanced → Test Method → Connect`
2. **Автообновление правил в фоне:** `Settings → Config → Auto Background Update → Вкл`
3. **Автовыключение дома (чтобы не было двойного VPN на домашнем роутере):**
   `Settings → On Demand` → включить `On Demand` → внизу `On Demand Rules`:
   - `Wi-Fi` с SSID домашнего роутера (`IT_ROOM`, `IT_ROOM_5`, `Keenetic-8940`, `Olivia27_5G`) → **Disconnect**
   - `Cellular` и `Wi-Fi` (любой другой) → **Connect**
   - `Disconnect on Sleep` → **Выкл**

## 3. Быстрое добавление своих сайтов

- В VPN: добавить строку `DOMAIN-SUFFIX,example.com` в [`rules/custom_proxy.list`](rules/custom_proxy.list)
- Напрямую (мимо VPN): добавить строку `DOMAIN-SUFFIX,example.ru` в [`rules/custom_direct.list`](rules/custom_direct.list)
