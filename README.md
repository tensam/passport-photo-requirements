# Passport & visa photo requirements (machine-readable)

Official photo specifications for 21 passport and visa documents, as structured JSON: print size, file-size window, head height and eye position (as a fraction of photo height), background rule, the official rules as quoted text, and the official source for each. `pixtidy_output` is the pixel size pixtidy exports within the official limits; it is not an official value.

Maintained by [pixtidy](https://pixtidy.com) — a browser-based passport & visa photo maker that checks photos against these rules. Every value was taken from the linked government page; where an authority publishes no number, the field is marked as not official.

Prefer a human-readable version? The same requirements are in one table at [pixtidy.com/photo-requirements](https://pixtidy.com/photo-requirements).

## Looking for a tool rather than data?

[pixtidy](https://pixtidy.com) uses exactly this dataset:

- Your photo is never uploaded. Face detection (MediaPipe) and cropping run entirely in the browser; nothing is sent to a server.
- Checks every rule before you pay: head height, eye line, background colour and evenness, lighting, focus, eyes open, mouth closed, and the file-size window (for example 54–240 KB for a US DS-160 photo).
- No retouching or AI edits, because officials reject altered photos. It only crops, levels and resizes.
- Covers all documents in the table below (US passport, DS-160 visa, green card, Schengen 35×45 mm, UK visa, India OCI, China visa and more), in English, Spanish, Portuguese, French, German and Italian, with a 4×6 print sheet.
- Already have a photo? Check it for free, no sign-up: [US passport](https://pixtidy.com/passport-photo-checker) · [US visa (DS-160)](https://pixtidy.com/us-visa-photo-checker) · [en español](https://pixtidy.com/es/verificador-foto-visa-pasaporte) · [em português](https://pixtidy.com/pt/verificador-foto-visto-passaporte) · [en français](https://pixtidy.com/fr/verificateur-photo-visa-passeport) · [auf Deutsch](https://pixtidy.com/de/foto-pruefen-usa-visum) · [in italiano](https://pixtidy.com/it/verifica-foto-visto-usa).
- Already have a studio or booth photo? When it can be reused, with the numbers per document: [English](https://pixtidy.com/guides/use-existing-passport-photo) · [en español](https://pixtidy.com/guides/foto-que-ya-tengo-visa-pasaporte) · [en français](https://pixtidy.com/guides/reutiliser-photo-passeport-visa) · [em português](https://pixtidy.com/guides/foto-que-ja-tenho-visto-passaporte) · [auf Deutsch](https://pixtidy.com/guides/vorhandenes-passfoto-visumfoto-verwenden) · [in italiano](https://pixtidy.com/guides/usare-foto-che-ho-gia-visto-passaporto). For a UK visa, GOV.UK rules out a scan or photo of another photo, and the same photo that is in your passport or identity card.

| Document | Print | pixtidy output (px)† | File size | Head height | Eye line from bottom | Background | Source |
|---|---|---|---|---|---|---|---|
| United States Passport | 50.8×50.8 mm | 600×600 | — | 50–69% | 56–69% | white | [source](https://travel.state.gov/content/travel/en/passports/how-apply/photos.html) |
| United States Passport Online Renewal | — | 1200×1200 | 55–10000 KB | 45–60%* | — | white | [source](https://travel.state.gov/en/passports/renew-replace/online/upload-digital-photo.html) |
| United States Visa (DS-160) | 50.8×50.8 mm | 600×600 | 54–240 KB | 50–69% | 56–69% | white | [source](https://travel.state.gov/content/travel/en/us-visas/visa-information-resources/photos/digital-image-requirements.html) |
| United States Green Card (USCIS) | 50.8×50.8 mm | 600×600 | — | 50–69% | 56–69% | white | [source](https://www.uscis.gov/sites/default/files/document/forms/i-485instr.pdf) |
| United States Baby Passport | 50.8×50.8 mm | 600×600 | — | 50–69% | 56–69% | white | [source](https://travel.state.gov/content/travel/en/passports/how-apply/photos.html) |
| UK Visa | — | 1200×1500 | 51–6000 KB | 40–55%* | — | light | [source](https://www.gov.uk/guidance/how-to-take-a-photo-for-a-visa-application-or-permission) |
| UK ETA | — | 1200×1500 | 51–6000 KB | 40–55%* | — | light | [source](https://www.gov.uk/eta/apply) |
| India OCI Card | — | 600×600 | ≤200 KB | 50–69% | — | light-not-white | [source](https://ociservices.gov.in/onlineOCI/faq) |
| India e-Visa | — | 600×600 | 10–1000 KB | 50–69%* | — | light | [source](https://indianvisaonline.gov.in/evisa/tvoa.html) |
| Schengen Visa | 35×45 mm | 827×1063 | — | 71–80% | — | light | [source](https://home-affairs.ec.europa.eu/document/download/5bb16566-c8c2-4afb-b038-530f488cb72a_en?filename=icao_photograph_guidelines_en.pdf) |
| China Visa | 33×48 mm | 354×472 | 41–120 KB | 58–69% | 55–80% | white | [source](https://us.china-embassy.gov.cn/eng/lsfw/zj/qz2021/201612/t20161206_4410998.htm) |
| Vietnam e-Visa | — | 600×900 | ≤2000 KB | 45–60%* | — | white | [source](https://evisa.gov.vn/e-visa/foreigners) |
| Thailand e-Visa | — | 600×800 | ≤3000 KB | 70–80% | — | light | [source](https://www.thaievisa.go.th/) |
| Australia Visa | — | 1200×1600 | 72–3500 KB | 64–78%* | — | light | [source](https://immi.homeaffairs.gov.au/help-text/evidence/Pages/et-h0369.aspx) |
| Brazil e-Visa | 50.8×50.8 mm | 600×600 | — | 50–69%* | — | white | [source](https://www.gov.br/mre/pt-br/consulado-miami/information-about-visas-in-english/electronic-visitor-visa-e-visa) |
| New Zealand Passport | — | 1200×1600 | 256–5000 KB | 50–65%* | — | light | [source](https://www.passports.govt.nz/passport-photos) |
| New Zealand NZeTA | — | 2100×2800 | 524–3000 KB | 70–80% | — | light-not-white | [source](https://www.immigration.govt.nz/process-to-apply/applying-for-a-visa/applying-online/uploading-documents-and-photos/visa-and-nzeta-photos/) |
| Nigeria Passport | — | 600×800 | 72–2000 KB | 50–69% | 56–69% | white | [source](https://passport.immigration.gov.ng/) |
| Pakistan Visa | 35×45 mm | 413×531 | ≤60 KB | 70–80% | — | white | [source](https://visa.nadra.gov.pk/download/photograph-guidelines/) |
| Tanzania e-Visa | — | 413×531 | ≤500 KB | 60–75%* | — | light | [source](https://visa.immigration.go.tz/guidelines) |
| Ethiopia e-Visa | 50.8×50.8 mm | 600×600 | ≤2000 KB | 50–69%* | — | white | [source](https://www.evisa.gov.et/) |

\* No official number — recommended framing (head and shoulders visible).

† Not an official value: the pixel size pixtidy exports, chosen inside the official limits. The official pixel rules are quoted in each spec's `rules`.

## Use

```js
const { specs } = await (await fetch("https://raw.githubusercontent.com/tensam/passport-photo-requirements/main/specs.json")).json();
const dsVisa = specs.find(s => s.id === "us-visa");
```

Fields: `head_height_ratio` is chin to top of hair ÷ photo height; `eye_from_bottom_ratio` is eye line from the bottom edge ÷ photo height; `crown_from_top_ratio` is the gap above the head ÷ photo height; byte limits include those derived from rules such as "compression ratio ≤ 20:1", and are chosen to satisfy both 1 KB = 1000 and 1 KB = 1024 readings of the official text (so a stated "54 KB" minimum appears as 55296 bytes).

Not included on purpose (their rules forbid self-cropped or non-studio photos, or photos are taken on site): UK passport photo codes, Canadian passport/PR photos, Australian passport photos, Philippine passports.

Rules change — always confirm with the issuing authority. Corrections welcome via issues or pull requests.

## License

Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — please credit "pixtidy (https://pixtidy.com)".
