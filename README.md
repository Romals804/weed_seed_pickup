Název: weed_seed_pickup

Popis:
Skript umožňuje hráčům sbírat semínka trávy z předdefinovaných míst na mapě.
Používá ox_target pro interakci a ox_lib pro progress bar.

-----------------------------------
Instalace:
1. Nakopíruj složku "weed_seed_pickup" do složky "resources" na serveru.
2. Do server.cfg přidej řádek:
   ensure weed_seed_pickup

-----------------------------------
Požadavky:
- ESX framework
- ox_target
- ox_inventory
- ox_lib

-----------------------------------
Konfigurace:
Otevři soubor config.lua

- Nastav model objektu (např.):
    Config.Prop = `prop_weed_02`

- Přidej nebo uprav pozice pro sběr semínek:
    Config.Positions = {
        vec3(-415.546, 4320.651, 59.776),
        vec3(-411.470, 4316.280, 58.702),
        ...
    }

- Nastav vzdálenost pro interakci:
    Config.TargetDistance = 1.5

- Nastav cooldown pro obnovení semínka (v sekundách):
    Config.Cooldown = 1800  -- např. 30 minut

-----------------------------------
Použití:
1. Hráč přijde k rostlině.
2. Zobrazí se možnost "Sesbírat semínka trávy" (pomocí ox_target).
3. Po stisknutí klávesy začne animace zahradníka.
4. Běží progress bar "Sbíráš semínka..." (cca 15 sekund).
5. Po dokončení hráč dostane náhodně 1–5 ks itemu "weed_og_seed".
6. Objekt (rostlina) zmizí a po cooldownu se znovu objeví.

-----------------------------------
Překlad hlášek:
Sbíráš semínka...  → Zobrazuje se při sběru
Sesbírat semínka trávy → Možnost interakce u objektu

-----------------------------------
Autor skriptu: Romals22
Verze: 1.0.0
