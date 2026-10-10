# ha-aqara-blueprints

Aqara sensörleri (Aqara Hub M3 / Zigbee) için hazırlanmış Home Assistant otomasyon blueprint'leri. Her `binary_sensor` ile çalışırlar.

## Blueprint'ler

### Hareketle ışık

Hareket algılanınca ışığı açar, hareket bittikten belirlenen süre sonra kapatır.

[![Blueprint'i Home Assistant'a aktar](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fanillozmen%2Fha-aqara-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fmotion_light.yaml)

| Girdi | Açıklama |
|---|---|
| Hareket sensörü | `motion` / `occupancy` sınıfında binary_sensor |
| Işık | Açılıp kapanacak ışık(lar) |
| Kapanma gecikmesi | Hareket bittikten sonra beklenecek süre (varsayılan 120 sn) |

### Kapı açık kaldı bildirimi

Kapı veya pencere belirlenen süreden uzun açık kalırsa telefona bildirim gönderir.

[![Blueprint'i Home Assistant'a aktar](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fanillozmen%2Fha-aqara-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fdoor_left_open.yaml)

| Girdi | Açıklama |
|---|---|
| Kapı/pencere sensörü | `door` / `window` / `garage_door` / `opening` sınıfında binary_sensor |
| Açık kalma süresi | Bildirim için eşik (varsayılan 5 dk) |
| Bildirim gidecek cihaz | Home Assistant uygulaması kurulu telefon |

## Elle kurulum

1. YAML dosyasını `config/blueprints/automation/anillozmen/` klasörüne kopyala.
2. **Ayarlar → Otomasyonlar ve Sahneler → Blueprint'ler** ekranından blueprint'leri yeniden yükle.
3. Blueprint'i seçip **Otomasyon oluştur** de.

## Lisans

MIT
