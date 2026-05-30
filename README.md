# Numa

Een rekenmachine-app voor de iPhone (web) die eruitziet als een **TI-84 Plus schoolrekenmachine** — met een verborgen, privé videokluis erin.

Aan de buitenkant is het een werkende grafische rekenmachine in TI-84 Plus-stijl (typ een berekening en druk op ENTER). Achter een geheime code zit een complete videospeler met bibliotheek.

---

## 1. Hoe open ik de geheime kluis?

1. Open de app (de TI-84 rekenmachine).
2. Typ je **geheime cijfercode** in op het toetsenblok.
3. Druk op **`ENTER`** (rechtsonder, blauw).
4. De kluis opent.

> **Standaardcode: `1984`**
> Wijzig deze meteen in de kluis bij **Instellingen → Geheime code wijzigen**.

De kluis vergrendelt automatisch zodra je de app wegklikt of naar de achtergrond stuurt (uit te zetten bij Instellingen). Met het slotje rechtsboven sluit je hem handmatig.

> Normaal rekenen werkt gewoon: typ bv. `12+3` en `ENTER` → `15`. Alleen als je exact je geheime code typt en op ENTER drukt, opent de kluis.

---

## 2. Op GitHub zetten (GitHub Pages)

1. Maak een nieuwe **publieke** repository aan op GitHub (bijv. `numa`).
2. Upload deze 4 bestanden in de hoofdmap van de repo:
   - `index.html`
   - `manifest.json`
   - `icon.svg`
   - `README.md` (optioneel)
3. Ga in de repo naar **Settings → Pages**.
4. Kies bij *Build and deployment* → *Source*: **Deploy from a branch**.
5. Kies branch **`main`** en map **`/ (root)`**, klik **Save**.
6. Na ~1 minuut staat je app live op:
   `https://<jouw-gebruikersnaam>.github.io/numa/`

Open die link op je iPhone in Safari.

### Toevoegen aan beginscherm (voelt als een echte app)
In Safari: deelknop (vierkantje met pijl) → **Zet op beginscherm**. Het pictogram en de naam tonen alleen "Numa".

---

## 3. Wat kan de kluis?

- **Video's toevoegen** vanaf je apparaat (meerdere tegelijk) of via een directe link (`.mp4`, `.webm`, …).
- **Automatische miniaturen** (thumbnails) en duur per video.
- **Mooie videospeler**: spelen/pauzeren, ±10 sec (ook dubbeltik links/rechts), scrubben met buffer-indicatie, snelheid 0,5×–2×, herhalen, beeld-in-beeld, volledig scherm, en **hervatten** waar je gebleven was.
- **Slimme secties**: Verder kijken, Recent toegevoegd, Meest bekeken, Favorieten.
- **Bibliotheek** met sorteren (recent / meest bekeken / naam / oudste / favorieten).
- **Albums** om video's te groeperen.
- **Zoeken** op titel of album.
- **Shuffle ▶** om willekeurig te starten.
- **Opslagstatistieken** + knop om de opslag "vast te zetten".

---

## 4. Belangrijk over privacy & opslag

- Alle video's worden **lokaal op je toestel** bewaard (in de IndexedDB van de browser). Ze worden **niet** geüpload en verlaten je apparaat niet.
- Dit is **privacy door verberging** met een PIN — geen sterke versleuteling. Iemand met technische toegang tot je toestel/browseropslag zou de bestanden in theorie kunnen vinden. Bewaar er dus geen onmisbare bestanden zonder eigen back-up.
- Omdat de opslag aan de browser hangt: leeg je Safari-gegevens of "website-data", dan kan de inhoud verdwijnen. Gebruik daarom **Instellingen → Opslag → Vastzetten** en bewaar back-ups van belangrijke video's.
- iOS kan opslag van web-apps na lange inactiviteit opruimen. Voor heel grote, langdurige opslag is een echte (native) app betrouwbaarder.

---

## 5. Aanpassen

Alles zit in één bestand: `index.html` (HTML + CSS + JavaScript).
- Andere "dekmantel"-naam: pas `<title>`, de meta-tags en de teksten bovenin aan.
- Andere standaardcode: zie `DEFAULT_CODE` in het script (of wijzig hem gewoon in de app).
- Kleuren/thema: de CSS-variabelen bovenin (`:root`).
