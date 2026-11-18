# ZORA FILMS — GitHub + Cloudflare Pages

## Verzija

- Paket: Zora Films v6 — potpuno spreman statički build.
- Izvorni Lovable ZIP (SHA-256): `8899cf0b53439e427d205b74c1251d10c861e2ac5f8154356d4088ab3c21370e`
- Jedina ciljana izmjena na izvozu: mobilna navigacija prikazuje **Gallery**.
- Sadržaj mape `public/`: 431 datoteka.

## GitHub struktura

Ovaj paket sadrži sva tri elementa u korijenu repozitorija:

```text
DEPLOY-ZORA-FILMS.md
ORIGINAL-VERIFY-SHA256.txt
public/
```

## Zamjena postojećeg sadržaja

1. Raspakiraj ZIP.
2. Otvori lokalnu mapu postojećeg GitHub repozitorija `Zora-Guruji`.
3. Zamijeni **samo tri gornja elementa** novima iz raspakiranog ZIP-a. Ne kopiraj cijeli ZIP unutar mape `public`.
4. **Ne briši skriveni `.git` direktorij** — on čuva vezu s repozitorijem.
5. U GitHub Desktopu napravi **Commit to main → Push origin**.

## Postavke Cloudflare Pages

- Project: `zora-guruji`
- Production branch: `main`
- Framework preset: `None`
- Build command: `exit 0`
- Build output directory: `public`

Datoteke u `public/` već su izgrađene; **nije potreban npm install ni npm build**. Cloudflare Pages automatski objavljuje novu verziju nakon pushanja.

Ne mijenjaj DNS, domene ni e-mail zapise.

## Provjera datoteka (opcionalno)

`ORIGINAL-VERIFY-SHA256.txt` sadrži SHA-256 kontrolne vrijednosti datoteka unutar `public/` za ovu završnu verziju. Iz korijena repozitorija može se provjeriti naredbom:

```bash
sha256sum -c ORIGINAL-VERIFY-SHA256.txt
```

Ova provjera nije uvjet za deployment.
