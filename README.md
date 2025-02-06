# TaggFagAI 📂🤖 - Automatisk fagsortering av filer

TaggFagAI er et smart sorteringsprogram som hjelper lærere med å organisere filer automatisk basert på faglige emner. Med støtte for flere filformater, inkludert PDF, Word, PowerPoint og HTML, kan TaggFagAI analysere innholdet og legge til riktige macOS-Tagger. Dette gjør det enklere å finne og holde orden på undervisningsmateriell! 📚✨

## 🔥 Hovedfunksjoner
- 📄 **Automatisk tekstanalyse** – Leser innhold fra dokumenter og gjenkjenner fag.
- 🏷 **MacOS-Tagging** – Legger til relevante emne-Tagger for enkel filtrering.
- 🤖 **Kunstig intelligens (LM Studio)** – Bruker lokalt kjørende språkmodeller for nøyaktig fagsortering.
- 📂 **Støtte for mange filtyper** – PDF, DOCX, PPTX, TXT, RTF, HTML, og mer.
- 🔍 **OCR (optisk tegngjenkjenning)** – Bruker Tesseract til å hente tekst fra skannede PDF-er.
- 🎥 **Filnavn-analyse for videoer** – Sorterer videofiler basert på filnavnet.

---

## 🚀 Kom i gang
### 1️⃣ Installere avhengigheter
Kjør følgende kommando for å installere nødvendige pakker:
```bash
pip install requests pypdf python-pptx odfpy pytesseract beautifulsoup4 macos-Taggs pdf2image
```

### 2️⃣ Starte LM Studio
For at TaggFagAI skal fungere, må du ha **LM Studio** kjørende med en passende språkmodell.
1. **Last ned og installer** [LM Studio](https://lmstudio.ai/)
2. **Start en kompatibel modell** (f.eks. Mistral-7B eller lignende) og noter API-adressen (som standard `http://localhost:1234`)

### 3️⃣ Kjør programmet
Start programmet ved å kjøre:
```bash
python TaggFagAI1.0.py
```
Velg en mappe med filer, og programmet vil automatisk analysere og sortere dem. ✅

---

## 🛠 Hvordan fungerer det?
### 🔎 Logikken bak sorteringen
1. **Lese innhold** – Programmet analyserer tekst fra dokumentet eller filnavnet (for videoer).
2. **Be om fagsortering fra AI** – Forespør LM Studio om hvilket fag innholdet tilhører.
3. **Legge til Tagger** – Hvis AI-en finner et fag, merkes filen med en macOS-Tagg.
4. **Oppdaterer logg** – En oppsummeringsfil (`Taggs added.txt`) holder oversikt over alle Taggede filer.

### 📌 Endre eller tilpasse fag
Vil du legge til eller endre fagene som brukes?
- Åpne `Taggfagai.py`
- Finn listen over fag i koden:
  ```python
  subjects = ["Matematikk", "Samfunnsfag", "Norsk", "Religion", "KunstOgHåndverk", "Uteskole", ...]
  ```
- Legg til eller fjern fag etter behov.

---

## 💡 Brukstips
💾 **Backup filer** før du kjører programmet, spesielt hvis du har viktige data.
🎯 **Eksperimenter med ulike språkmodeller** i LM Studio for å forbedre treffsikkerheten.
🛠 **Tilpass sorteringslogikken** ved å justere hvordan tekst hentes fra filer.

---

Bidra gjerne med forbedringer! Pull requests er velkomne. 🙌🎉

