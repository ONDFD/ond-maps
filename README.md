# OND Fault Detective — offline map packs / Çevrimdışı harita paketleri

These files are offline map packs used by the OND Fault Detective application. The application downloads them
when the user taps "Download Map" and uses them without internet in the field.

Bu dosyalar OND Arıza Dedektifi uygulamasının çevrimdışı harita paketleridir. Uygulama, kullanıcı "Harita İndir"e
bastığında internet varken indirir ve sahada internetsiz kullanır.

## Files / Dosyalar

| File | Content |
|---|---|
| `catalog.json` | List of available regions with size and SHA-256 checksum |
| `ankara-1.ondmap` | Ankara city centre (test region), roads / railways / water / parks |

## Data source and licence / Veri kaynağı ve lisans

The map data is © OpenStreetMap contributors and is available under the Open Database Licence (ODbL) 1.0:
<https://www.openstreetmap.org/copyright> · <https://opendatacommons.org/licenses/odbl/1-0/>

The packs are a derived database made from an OpenStreetMap extract (Overpass API). They contain only feature types and
geometry (no names). Anyone using these packs must keep the "© OpenStreetMap contributors" attribution and the ODbL terms.

Harita verisi © OpenStreetMap katkıcılarıdır ve Open Database License (ODbL) 1.0 altında sunulur. Paketler, OpenStreetMap
verisinden türetilmiş bir veri tabanıdır; yalnız öğe türü ve geometri içerir (isim yok). Kullanan herkes
"© OpenStreetMap katkıcıları" kaynak yazısını ve ODbL koşullarını korumalıdır.

## Format

`.ondmap`: `ONDMAP1` header, payload length, gzip payload (coordinates in 1e-6 degrees, delta + zigzag varint).
Created with `tools/MapPackBuilder` of the OND Fault Detective project. No warranty.
