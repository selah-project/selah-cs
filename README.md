# Tanach — český překlad (selah-cs)

Toto je český překlad hebrejského Tanachu. Každý verš leží ve svém
vlastním souboru a každé slovo je připoutáno ke svému hebrejskému
originálu.

**Písmo: latinka s českou diakritikou.** Text je ve spisovné češtině.

## Tvar souboru

```
<kniha>/<kapitola>/<verš>.json
```

Každý soubor:

```json
{
  "translation": "tok verše",
  "tokens": [{"surface": "hebrejské slovo", "gloss": "český význam"}]
}
```

`surface` — hebrejský záznam. Není náš, abychom jej psali; přichází
z originálu a nemění se.

`gloss` — český význam **právě tohoto** hebrejského slova. Počet
glos se rovná počtu hebrejských slov. Vždy.

`translation` — tentýž verš čtený souvisle, aby jej bylo možné číst
nahlas.

## Co znamenají značky ⟨ ⟩

Slouží dvěma věcem a rozlišovat mezi nimi je důležité.

**1 · ⟨את⟩ — hebrejská značka, která se nepřekládá.** Slovo את stojí
před předmětem věty. Čeština pro ně nemá protějšek, a tak je necháváme
stát tak, jak je psáno. Není to chyba sazby; je to slovo, které v textu
skutečně je.

**2 · ⟨doplněné slovo⟩ — čeština, kterou hebrejština nemá.** Hebrejština
často vynechává sponu. Kde ji čeština potřebuje, aby věta vůbec stála,
je dodána v lomených závorkách: `Blahoslavený ⟨je⟩ národ`. Závorky
říkají: *toto slovo přidal překladatel, v hebrejštině nestojí.*

**V závorce nikdy nestojí cizí jazyk.** Uvnitř ⟨ ⟩ je čeština, nebo
hebrejská značka — nic třetího.

## Jména

Boží Jméno se **nepřekládá, přepisuje se**.

| hebrejsky | zde | co jsme odmítli |
|---|---|---|
| יהוה | **Jahve** | **Hospodin**, **Pán**, **Jehova** |
| אלהים | **Elohim** | **Bůh** na místě Jména |
| אל | **El** | „bůh“ jako druhové jméno |
| אדני | **Adonaj** | **Panovník**, **Pán** |
| שדי | **Šaddaj** | „Všemohoucí“ |
| צבאות | **Cevaot** | „zástupů“ |
| שאול | **šeol** | „peklo“, „podsvětí“ |

**Hospodin je v české bibli doma čtyři sta let** — od Kralické po ČEP.
Přesto zde nestojí. Je to překlad *titulu*, ne Jména; na místě, kde text
říká יהוה, je to slovo, které Jméno zakrývá. Kdo chce slyšet tradici,
najde ji v každé jiné české bibli. Zde stojí to, co je psáno.

Skloňování je v pořádku, pokud kmen zůstane celý: **Jahve, Jahveho,
Jahvem; Elohim, Elohima, Elohimovi.** Co se nesmí, je zlomit kmen.

## Obecné *bůh* a *pán* jsou v pořádku

Kde hebrejština mluví o bozích národů nebo o lidském pánu, stojí zde
malé *bůh*, *bohové*, *pán* — to není zakrytí Jména, to je překlad.
Rozhoduje hebrejská značka daného slova, ne samo české slovo.
V 1. Královské 20,23 mluví Aramejci o svých bozích; **Bohové** tam
stojí právem.

## Celé pravidlo

Kázeň, podle níž tento text vznikl, je zapsána v hlavním úložišti
Selah: `docs/methodology/translation-discipline/cs.md`.

Cesta, kterou tento překlad prošel — co selhalo, co se muselo
rozhodnout, co se opravilo — je v `PROVENANCE.md`.

## Stav

Úplný Tanach: **23 213 veršů**, všech 39 knih. Hebrejský základ je
OSHB / WLC 4.20.

Tento text je **první průchod**. Není to poslední slovo; je to jeden
svědek. Čti jej vedle hebrejštiny.

## Licence

Creative Commons Attribution-ShareAlike 4.0 International. Viz
`LICENSE.md`.
