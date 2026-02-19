# Smart4smart - Kalkulačka nabíjecích stanic

Moderní React aplikace pro výpočet orientační ceny instalace nabíjecích stanic pro elektromobily.

## Funkce

- **Tři segmenty**: Rodinný dům, Firemní prostředí, Bytový dům
- **Dynamický výpočet ceny**: Okamžitý přepočet ceny při změně konfigurace
- **Interaktivní formulář**: Intuitivní ovládání s vizuální zpětnou vazbou
- **Lead generation**: Formulář pro sběr kontaktních údajů
- **Responzivní design**: Optimalizováno pro desktop i mobil
- **Moderní UI**: Vysoká konverze s prémiovým vzhledem

## Technologie

- React 18
- Tailwind CSS 3
- Vite
- Modern JavaScript (ES6+)

## Instalace

```bash
# Nainstalujte závislosti
npm install

# Spusťte vývojový server
npm run dev

# Build pro produkci
npm run build
```

## Struktura projektu

```
Smart4Smart/
├── src/
│   ├── main.jsx              # Entry point
│   └── index.css             # Tailwind direktivy
├── ChargingStationCalculator.jsx  # Hlavní komponent kalkulačky
├── index.html                # HTML šablona
├── package.json              # Závislosti projektu
├── vite.config.js            # Konfigurace Vite
├── tailwind.config.js        # Konfigurace Tailwind CSS
└── postcss.config.js         # PostCSS konfigurace
```

## Kalkulační logika

### Rodinný dům

**Základní cena podle vzdálenosti:**
- Do 5m: 10 004 Kč
- 5-15m: 10 685 Kč
- 15+ m: 12 823 Kč

**Smart funkce:**
- Bez výběru: +15 305 Kč (základní stanice)
- Dynamické řízení výkonu: 36 366 Kč (zahrnuje plánování + RFID)
  - Možnost nabíjení v nízkém tarifu: +2 000 Kč (zvýhodněná cena)
- Individuální funkce (pokud není dynamické řízení):
  - Nízký tarif: 3 000 Kč
  - Plánování: 5 000 Kč
  - RFID: 4 000 Kč

### Firemní prostředí

- **Počet aut**: 1-2 (39k), 3-5 (156k), 6-12 (390k), 12+ (546k)
- **DC stanice**: 40-120kW (350k), 160-240kW (980k), 400kW (1.45M)
- **Rozúčtování nákladů**: +5 000 Kč
- **Stav přípravy**:
  - Připraveno: 0 Kč
  - Jiné úpravy: 20 000 Kč
  - Problém s kapacitou: 50 000 Kč

### Bytový dům

- **Počet stanic**: 1 (53k), 2 (87k), 3 (131k), 5 (203k), 10 (737k)
- **Společné rozvody**: +9 823 Kč

## Budoucí rozšíření

Aplikace je připravena pro implementaci:
- Email gate (zobrazení ceny až po vyplnění kontaktu)
- Backend integrace pro odesílání poptávek
- CRM integrace
- Analytics tracking
- A/B testování

## Autor

Vytvořeno pro Smart4smart

## Licence

Proprietární
