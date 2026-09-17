# NOTES — selah-cs, chair 76

Working notes in English. The reader-facing documents (`README.md`,
`CONTRIBUTING.md`, `LICENSE.md`) are in Czech, as this chair's own
documents should be. The full account of what went wrong and what was
decided is in `PROVENANCE.md`.

Lit 2026-09-17. Burn and cure complete the same day. Floor 23,213 verses
/ 305,507 token rows.

First **West Slavic** chair, and the first chair whose thermometer is
sharper than its neighbours' — see below.

---

## Burn signature

| | |
|---|---|
| relay | `batch/relay-move-on! [:cs]`, engine-side |
| gleaning | five rungs, **both directions** |
| residue cleared | 707 |
| final | 23,213 / 23,213 verses · **305,507 / 305,507 token rows** |

### The gleaning ladder runs BOTH directions

| rung | ceiling | landed | left |
|---|---:|---:|---:|
| 1 | 24,000 | 584 | 123 |
| 2 | 32,000 | 97 | 17 |
| 3 | 48,000 · glm-5.3 · 0.7 | 10 | 5 |
| 4 | **16,000** | **4** | 1 |
| 5 | **8,000** | **1** | **0** |

The last two rungs go **down**, and cleared what three rungs of climbing
could not. The survivors were short verses — `jeremiah/30/22` is seven
tokens. The discipline prompt is ~58,000 characters, so a large
`max_tokens` on top of it crowds the context window and the request
fails; the output is not being cut off at all.

**Both failure modes report the identical `:json-error`.** The status
cannot tell you which way to move. The verse length can.

Proven again at the cure stage, where a 52-seat residue was walked
through `[32000 8000 48000 4000 24000]` per seat: **42 landed climbing
to 32,000 and 10 landed descending to 8,000.** Neither direction alone
would have cleared it.

---

## What this chair's thermometer is, and why it is sharper

Czech's letter inventory is closed: á č ď é ě í ň ó ř š ť ú ů ý ž, and
nothing else. So the probe is **the letters Czech does not have** —
Slovak `ľ ĺ ŕ ô ä`, Polish `ą ę ł ż ź ś ć ń`, German `ß`. That is a
character-level test with no vocabulary dependence and therefore no
whitelist, which is what every non-Latin chair before this one needed.

`ř` and `ů` are exclusively Czech. Their presence is a good sign.

**The limit of the probe**, worth knowing: it cannot see a misspelling
built from letters Czech does have. `neubereťe` for `neuberete` uses
only Czech letters and passes clean.

Final: **Slovak 0 · Polish 0 · German 0.**

---

## Hand verses

Nine seats were decided by hand and are recorded with their reasons in
`dev/scripts/cs_hand_pass.clj` in the Selah repo.

| seat | what | why |
|---|---|---|
| `psalms/47/9` | Kraľuje → Kraluje | Slovak ľ; safe swap |
| `2-chronicles/15/8` | dobył → dobyl | Polish ł; safe swap |
| `lamentations/2/1` | svrhł → svrhl | Polish ł; and *svrhl* is exactly right — the splendour of Israel cast down from heaven to earth |
| `exodus/5/8` | Elohimovi, našemu Bohu → našemu Elohimovi | a doublet that supplies the erasure after giving the rail is still the erasure |
| `isaiah/3/1` | Pán → Adonaj | האדון, adon without the yod, is the divine Lord |
| `deuteronomy/11/13` | '' → ⟨k⟩ | empty row, directional אל |
| `ezekiel/43/19` | '' → ⟨k⟩ | same |
| `daniel/3/12` | '' → je | the Aramaic object marker — see below |
| `exodus/14/9` | flow marker restored | row marked אותם, flow carried none |

**The l-cure is not a character table.** 22 of 31 flagged words took
`ł ĺ ľ → l` safely; the rest had to be re-rendered, because swapping the
letter would have produced a word Czech never held — `Zażiť` carries a
Polish ž *and* a Slovak infinitive ending; `vtaćena` can go to `č` or to
`ž` with different meanings; `dopoľuje` is not Czech even after the
swap; `prah{ł}` had literal curly braces in it.

---

## Cruxes

**The Name.** Czech Bibles have used *Hospodin* for four centuries, from
the Kralická to the ČEP. The rails choose **Jahve**. *Hospodin*
translates a title; where the text says יהוה it is the word that covers
the Name. 5,646 verses carry Jahve.

**Bůh and Pán have lawful seats**, which is why the erasure probe is
token-guided: the nations' gods, and a human lord. `1-kings/20/23` has
Aramean officers talking about their own gods, and *Bohové* stands there
by right.

**אדני addressed to a man.** `numbers/11/28` is Joshua saying "my lord
Moses"; `numbers/12/11` is Aaron saying it to the same man. The surface
is spelled exactly like the divine Adonai. These had to be discharged by
reading, not by pattern.

**`2-chronicles/10/10`** — אתו here is the preposition *with him*, not
the object marker, and it sits in the open question of whether את is one
word or two. Left as it stands rather than cured blind.

---

## Open, and named on purpose

**Two Aramaic erasure seats remain, and they are not oversights.**

```
daniel/2/47   ומרא → a Pán
ezra/7/12     אלה  → Boha
```

Daniel 2:4–7:28 and Ezra 4:8–6:18 / 7:12–26 are in **Aramaic**, which
carries its own divine vocabulary — אלה (God), מרא (Lord), עליא/עלאה
(Most High). **The name table in the discipline doc covers Hebrew
only.** There was no row to follow, so the chair had nothing to be
faithful to, and these two seats are waiting on a ruling rather than on
a repair.

The blind spot is not this chair's. Every chair's erasure census before
cs used a Hebrew-only divine-name list, and none has examined those
passages.

**Aramaic also has its own object marker.** `daniel/3/12` carries
`יתהון` — ית + הון, Aramaic's ⟨את⟩, and the only occurrence in the
Tanakh. The en floor glosses it plainly as "them", with no bracket, so
the floor does not treat it as a marker either. Matched the floor; filed
with the same question.

**The names are spelled more than one way.** Not one of ten checked
names is consistent — *Áron* 48.6% against *Aharon* 28.2%, *Mojžíš*
75.2% against *Moše*, *Jozue* 82% against *Jehošua*. The doc's own rule
says person and place names are transliterated, and the burn followed it
for Saul, Isaac, Hezekiah and Egypt while reaching for the Czech
tradition-form for the rest. *Šalomoun* and *Chizkijahu* each have
exactly one spelling and disagree with each other about which register
to use. This is not auto-curable: Czech declines names, so changing a
stem means re-declining every form of it, and that is the l-cure lesson
at scale. Awaiting a ruling. Measured by `dev/scripts/cs_name_scan.clj`.

---

## Instruments built at this chair

All in the Selah repo, all general to any chair, all idempotent.

- **`cs_census.clj`** — full-tree census. The erasure probe matches
  **stems**, not citation forms, because a nominative word-list cannot
  police an inflecting language: *Bůh/Pán* found 4 seats where the stems
  found 15, and *Bůh*'s stem alternates its vowel (Bůh → Boh-).
- **`cs_repress.clj`** — forced re-press with the bidirectional ladder.
- **`marker_adjudicate.clj`** — decides ⟨את⟩ gains against the floor,
  which `flow_parity.py` deliberately refuses to touch. Four classes:
  row dropped, flow fabricated, **form mismatch**, **row fabricated**.
- **`cs_name_scan.clj`** — name-register consistency.
- **`cs_hand_pass.clj`** — the nine seats above, with reasons.

`marker_adjudicate` also contains **`close-flow`, a cure that was built,
tested, and rejected** — kept rather than deleted, with the rejection
written into its docstring, because the next chair will be tempted to
write the same function.
