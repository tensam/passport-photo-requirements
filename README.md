# Passport & visa photo requirements (machine-readable)

Official photo specifications for 12 passport and visa documents, as structured JSON: print size, digital pixel size, file-size window, head height and eye position (as a fraction of photo height), background rule, and the official source for each.

Maintained by [pixtidy](https://pixtidy.com) — a browser-based passport & visa photo maker that checks photos against these rules. Every value was taken from the linked government page (archived copies kept privately); where an authority publishes no number, the field is marked as not official.

| Document | Print | Digital (px) | File size | Head height | Eye line from bottom | Background | Source |
|---|---|---|---|---|---|---|---|
| United States Passport | 50.8×50.8 mm | 600×600 | — | 50–69% | 56–69% | white | [source](https://travel.state.gov/content/travel/en/passports/how-apply/photos.html) |
| United States Passport Online Renewal | — | 1200×1200 | 55–10000 KB | 45–60%* | — | white | [source](https://travel.state.gov/content/travel/en/passports/how-apply/online-renewal-photo.html) |
| United States Visa (DS-160) | 50.8×50.8 mm | 600×600 | 54–240 KB | 50–69% | 56–69% | white | [source](https://travel.state.gov/content/travel/en/us-visas/visa-information-resources/photos/digital-image-requirements.html) |
| United States Green Card (USCIS) | 50.8×50.8 mm | 600×600 | — | 50–69% | 56–69% | white | [source](https://www.uscis.gov/sites/default/files/document/forms/i-485instr.pdf) |
| United States Baby Passport | 50.8×50.8 mm | 600×600 | — | 50–69% | 56–69% | white | [source](https://travel.state.gov/content/travel/en/passports/how-apply/photos.html) |
| UK Visa | — | 1200×1500 | 51–6000 KB | 40–55%* | — | light | [source](https://www.gov.uk/guidance/how-to-take-a-photo-for-a-visa-application-or-permission) |
| India OCI Card | — | 600×600 | ≤200 KB | 50–69% | — | light-not-white | [source](https://ociservices.gov.in/onlineOCI/faq) |
| India e-Visa | — | 600×600 | 10–1000 KB | 50–69%* | — | light | [source](https://indianvisaonline.gov.in/evisa/tvoa.html) |
| Schengen Visa | 35×45 mm | 827×1063 | — | 71–80% | — | light | [source](https://home-affairs.ec.europa.eu/document/download/5bb16566-c8c2-4afb-b038-530f488cb72a_en?filename=icao_photograph_guidelines_en.pdf) |
| China Visa | 33×48 mm | 354×472 | 41–120 KB | 58–69% | 55–80% | white | [source](https://us.china-embassy.gov.cn/eng/lsfw/zj/qz2021/201612/t20161206_4410998.htm) |
| Vietnam e-Visa | — | 600×900 | ≤2000 KB | 45–60%* | — | white | [source](https://evisa.gov.vn/e-visa/foreigners) |
| New Zealand Passport | — | 1200×1600 | 256–5000 KB | 50–65%* | — | light | [source](https://www.passports.govt.nz/passport-photos) |

\* No official number — recommended framing (head and shoulders visible).

## Use

```js
const { specs } = await (await fetch("https://raw.githubusercontent.com/tensam/passport-photo-requirements/main/specs.json")).json();
const dsVisa = specs.find(s => s.id === "us-visa");
```

Fields: `head_height_ratio` is chin to top of hair ÷ photo height; `eye_from_bottom_ratio` is eye line from the bottom edge ÷ photo height; `crown_from_top_ratio` is the gap above the head ÷ photo height; byte limits include those derived from rules such as "compression ratio ≤ 20:1", and are chosen to satisfy both 1 KB = 1000 and 1 KB = 1024 readings of the official text (so a stated "54 KB" minimum appears as 55296 bytes).

Not included on purpose (their rules forbid self-cropped or non-studio photos): UK passport photo codes, Canadian passport/PR photos, Australian passport photos.

Rules change — always confirm with the issuing authority. Corrections welcome via issues or pull requests.

## License

Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — please credit "pixtidy (https://pixtidy.com)".
