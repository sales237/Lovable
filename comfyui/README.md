# MiniMax H3 – ComfyUI-workflow (teksti + kuvareferenssit)

Tiedosto: `MiniMax_H3_teksti_ja_kuvareferenssit.json`

## Asennus
MiniMax H3 on ComfyUI:n sisäänrakennettu **Partner/API Node** – mallia ei ladata koneelle, vaan ajo tapahtuu Comfy.orgin pilvessä ja maksetaan Comfy-krediiteillä.

1. Päivitä ComfyUI uusimpaan versioon (H3-solmut: *MiniMax H3 Text to Video* ja *MiniMax H3 Reference to Video*).
2. Kirjaudu Comfy-tilille: **Settings → User → Sign in** (tai API key) ja lisää krediittejä.
3. Raahaa JSON-tiedosto ComfyUI-ikkunaan.

## Käyttö
- **PROMPT**-solmu = teksti-input, joka menee molempiin ryhmiin.
- **Ryhmä A – vain teksti → video** (oletuksena päällä).
- **Ryhmä B – teksti + kuvareferenssit → video** (oletuksena ohitettu). Kytke päälle valitsemalla ryhmän solmut ja painamalla **Ctrl+B**, ja kytke A pois samalla tavalla.
- Kuvat ladataan solmuihin *Kuva 1–3*. Promptissa niihin viitataan: "Image 1", "Image 2"…
  - Vähemmän kuvia: ohita (Ctrl+B) ylimääräiset Kuva-solmut.
  - Lisää kuvia (max 9): uusi *Load Image* → vedä H3-solmun seuraavaan `image_N`-paikkaan.
  - Kuva vähintään 256×256 px, kuvasuhde 2:5 – 5:2.
  - Samaan solmuun voi kytkeä myös referenssivideoita (max 3) ja ääniä.
- Asetukset: model (H3 / H3 Max), resolution (768P / 2K), ratio, duration 4–15 s. Hinta näkyy solmun hintamerkissä.
- Valmis video: `ComfyUI/output/video/H3_teksti_*` tai `H3_referenssi_*`.
