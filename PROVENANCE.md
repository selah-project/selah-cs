# PROVENANCE — how this rendering came to be

*Czech (Čeština), chair 76. Lit 2026-09-17. Floor 23,213 verses.*

This is the record of how the text in this repository was produced — written
**while it was being produced**, not reconstructed afterwards. A
machine-assisted rendering has no standing unless you can see how it was made
and what went wrong with it, so this file says both.

**Status: the burn is still running.** Counts below are partial and are
marked with the point they were taken.

---

## The approach

Every verse is rendered from the Hebrew of that verse, under a written
discipline — `docs/methodology/translation-discipline/cs.md` in the Selah
repository, itself written in Czech. Six rules govern it: the Hebrew token is
the unit; the Name stays the Name; both truths of Deut 6:4; no foreknowledge
(Gen 22:1 does not know Gen 22:13); numbers and marks stay put; the translator
has no word of his own.

**The `⟨ ⟩` brackets do two different jobs.** `⟨את⟩` is the Hebrew
direct-object marker, which Czech has no word for; it is left standing so the
reader sees it. `⟨word⟩` is a word Hebrew did not write but Czech grammar
requires — visibly marked, so you can always tell what the Hebrew said from
what the grammar needed.

## The fight on this chair is the Name

Czech biblical tradition renders **יהוה** as **Hospodin** — the Kralická and
the ČEP alike. It is the single most over-trained word this chair knows, and
it stands where the Name belongs.

| Hebrew | here | rejected |
|---|---|---|
| יהוה | **Jahve** | **Hospodin**, Pán, Jehova |
| אלהים | **Elohim** | **Bůh** in the Name's place |
| אדני | **Adonaj** | **Panovník**, Pán |
| שדי | **Šaddaj** | "Všemohoucí" as a substitute |
| שאול | **šeol** | peklo, podsvětí |

Lowercase *bůh / bohové* as a common noun for the nations' gods remains
lawful — the erasure is the capitalised word standing in the Name's place.
The census below applies that distinction rather than matching on spelling.

## The thermometer, and why it is sharper here than on most chairs

Czech's neighbours use letters **Czech does not have**, so the check is
character-level and needs no vocabulary whitelist:

- **Slovak** — `ľ ĺ ŕ ô ä`. The real risk: mutually intelligible, and the
  model holds both.
- **Polish** — `ą ę ł ż ź ś ć ń`.
- **German** — `ß`.

**Czech's own `ř` and `ů` are exclusively Czech** and are never flagged. This
matters: on earlier chairs every probe had to be whitelisted first because the
suspect string was also a real word of the language. Here the letters
genuinely cannot occur, so a hit is a hit.

---

## Finding: the letter `l` attracts its cousins across three alphabets

*Taken at 12,859 of 23,213 verses.*

| char | count | belongs to |
|---|---:|---|
| `ł` | 16 | Polish |
| `ĺ` | 2 | Slovak |
| `ľ` | 2 | Slovak |
| `ć` | 1 | Polish |

**Twenty of the twenty-one are l-family glyphs.** This is not Slovak or Polish
*vocabulary* arriving — it is one Czech letter being written with a
neighbour's version of the same letter, inside an otherwise correct Czech word:

```
dobył      → dobyl        rozmĺácené → rozmlácené
kůzłata    → kůzlata      zavrhł     → zavrhl
oplatił    → oplatil      vyhnał     → vyhnal
uléhł      → ulehl        neumlkł    → neumlkl
Stoły      → Stoly        vtaćena    → vtažena
```

Four of the five most frequent are the **past-tense `-l` suffix**, one of the
commonest morphemes in Czech — so the defect concentrates exactly where the
letter is most used.

Same class as the Uyghur chair's mid-word script bleed, where the target
script leaked backwards into the source letter by cognate letter. Different
alphabets, identical mechanism: **a systematic character substitution, not a
word intrusion.** Naming the mechanism rather than the resemblance is what
makes the cure obvious — since Czech has none of these letters, the mapping
`ł ĺ ľ → l` is safe by construction and does not need adjudication.

Rate at this point: **21 word-tokens across 12,859 verses (~0.16%).**

## Finding: no erasure yet

*Fresh-300 window over Psalms, Malachi, Zechariah.*

**Zero** occurrences of Hospodin, Bůh, Pán, Panovník or Věkověčný standing
where a divine name's Hebrew surface sits — checked by the licensing test
(an erasure word is a finding only when the token's own Hebrew surface is
יהוה / אלהים / אדני / שדי / צבאות, not by spelling alone).

Given that Hospodin is how every Czech Bible renders the Name, zero is the
result worth watching rather than assuming. It will be re-taken over the full
tree when the burn ends, because **a clean sample is not a clean corpus** —
that error was made eleven times on the previous chair.

## Finding: the erasure, and a blind spot in the instrument that hid it

*Taken at 17,129 of 23,213 verses.*

**The rails hold.** Jahve 4,953 · Elohim 1,627 · Adonaj 395 · Šaddaj 40 ·
Eloah 52.

**13 seats carry an erasure word where the token's own Hebrew or Aramaic
surface is a divine name** — about 0.076%. They fall into the habitats this
project has met before:

| habitat | example |
|---|---|
| rail present, erasure in a **supplied bracket** | `psalms/136/2` `לאלהי → Elohim ⟨ Bohu ⟩` |
| rail and erasure **apposed** | `exodus/5/8` `לאלהינו → Elohimovi, našemu Bohu` |
| **bare substitution** | `psalms/73/1` `אלהים → Bohu` · `1-samuel/23/16` `באלהים → v Bohu` |

One of the thirteen is **lawful and must not be cured**: `1-kings/20/23`
`אלהי → Bohové` is the *Arameans'* gods, a common noun, not the Name's
place. The discipline permits *bůh / bohové* for the nations' gods; only the
capitalised word standing where the Name stands is the erasure.

### The blind spot — Aramaic

The licensing test that found these was at first **blind to Daniel and Ezra**,
because its divine-name pattern listed only Hebrew forms. **Daniel 2:4–7:28
and Ezra 4:8–6:18 / 7:12–26 are Aramaic**, with their own divine vocabulary —
**אלה** (God), **מרא** (Lord), **עלאה** (Most High). None of it matched, so
every Aramaic seat was silently classified lawful.

What it was hiding is an inconsistency inside a single chapter:

```
daniel 2:47   אלה  → Eloah     (correct, twice in one verse)
daniel 2:44   אלה  → Bůh       (the erasure — three verses earlier)
```

The same Aramaic word, rendered two different ways within three verses.

This is a **fleet-wide instrument gap, not a Czech one.** Any chair's erasure
census built on a Hebrew-only divine-name list has never once looked at the
Aramaic sections. Earlier chairs were checked for whether the Aramaic
*rendered at all* — Daniel 2:4's bilingual seam was recorded as a pass on the
Uyghur chair — but not for whether its divine names survived.

### Open question for the discipline

`daniel/2/47` renders **ומרא → a Pán**. The discipline doc's D1 table covers
Hebrew יהוה / אלהים / אדני / שדי / אל / יה, and says nothing about the
**Aramaic** forms. So there is no ruling to follow for מרא, and *Pán* was the
only thing left to reach for.

The table needs an Aramaic row before this chair seats — and so, probably,
does every other chair's.

## Correction: the windows said Slovak 0. The tree says 12.

*Full-tree census taken at 22,518 of 23,213 verses, before gleaning.*

Three consecutive fresh-300 windows reported **Slovak 0**. The full tree holds
**twelve**: `ľ` 6 · `ä` 4 · `ĺ` 2. The windows simply never sampled those
verses.

This is the same error the previous chair's record opens with — a repeated
clean sample read as a clean corpus — and it is recorded here for the same
reason: **the windows were not wrong about what they saw, they were wrong
about what they implied.** A 300-verse window over 23,213 files is a 1.3%
sample, and a twelve-file defect will usually miss it.

Full-tree figures, which are the ones to trust:

| | |
|---|---:|
| files · token rows | 22,518 · 295,709 |
| empty flows · empty token-rows · empty glosses | 10 · 48 · 295 |
| foreign characters (44 word-tokens) | `ł` 28 · `ľ` 6 · `ä` 4 · `ĺ` 2 · `ż` 2 · `ć` 1 · `ś` 1 |
| erasure seats | **15** |
| markers: rows · flow · gap | 11,601 · 10,465 · 1,136 |

The l-family reading holds and strengthens: 38 of the 44 foreign characters
are `ł ľ ĺ` — Polish and Slovak forms of **l** — inside otherwise-correct
Czech words.

## Correction: a second Aramaic erasure, where the blind spot predicted

`ezra/7/12` renders **אלה → Boha**. Ezra 4:8–6:18 and 7:12–26 are Aramaic,
and this is the second seat found there after `daniel/2/44`. Both were
invisible to the original Hebrew-only licensing test.

That raises the erasure count from 13 to **15**, and it is the reason the
Aramaic gap is recorded as a *fleet-wide* finding rather than a Czech one:
the same test has been run on every seated chair, and on every one of them it
has never looked at these books.

## The burn's residue

The relay finished with **707 verses unrendered** (`:missing-after-pass 3981,
:residue 707, :status :moved-on-with-residue`), spread across books rather
than clustered — Psalms 77, Deuteronomy 49, Ezekiel 47, Isaiah 46.

**429 of the 707 are consecutive pairs.** That is the relay's batch grain
showing through the holes: it renders two verses per call, and a call that
fails takes both. The same signature appeared on the two previous chairs.

## The l-attractor cure is not a character table — checked word by word

The finding was that 38 of 44 foreign characters are l-family (`ł ľ ĺ`) inside
otherwise-correct Czech words, and the obvious cure is `ł ĺ ľ → l`, safe by
construction because Czech has none of those letters.

**Listing all 31 affected words before applying it showed that a blanket
mapping would have invented words in about a quarter of cases.**

Safe, and cured by the simple rule (~22 words):

```
Dokoła → Dokola      dobył   → dobyl      oplatił    → oplatil
Kráľ   → Král        było    → bylo       přilepła   → přilepla
Kráł   → Král        kůzłata → kůzlata    rozmĺácené → rozmlácené
Rozveseľ → Rozvesel  neumlkł → neumlkl    zavrhł     → zavrhl
Stoły  → Stoly       svrhł   → svrhl      vyhnał     → vyhnal
```

Not a character swap, and left for re-rendering rather than guessed:

| word | why the table fails |
|---|---|
| `Zażiť` | Polish `ż` **and** a Slovak infinitive `-ť`; Czech takes `-t`. Morphology, not a glyph. |
| `zkvädlo` · `zkvädly` | Slovak `ä`; the correct Czech verb is not derivable from the character. |
| `śloužba` | needs two corrections to reach `služba`. |
| `vtaćena` | `ć→č` and `ć→ž` both yield real Czech words, with different meanings. |
| `dopoľuje` | not recognisably a Czech word once the `ľ` is fixed. |
| `prah{ł}` | carries literal **curly braces** — a separate defect wearing the same costume. |

This is the same discipline the marker cures follow: **a cure that can produce
something the language never held is not a cure.** The ambiguous seats are
re-rendered, which lets the model resolve them from the Hebrew, rather than
patched from a lookup table that cannot tell `vtažena` from `vtačena`.

## The gleaning ladder runs in BOTH directions

The standing rule in this project is *raise max-tokens first — it has never
once been the model.* That rule is true, and it is incomplete.

The 707 residue cleared like this:

| rung | ceiling | landed | left |
|---|---:|---:|---:|
| 1 | 24,000 | 584 | 114 json-error + 9 alignment |
| 2 | 32,000 | 97 | 15 json-error + 2 alignment |
| 3 | 48,000 · `glm-5.3` · 0.7 | 10 | **5 json-error** |
| 4 | **16,000** | **4** | 1 |
| 5 | **8,000** | **1** | **0** |

Rungs 4 and 5 go **down**, and they cleared what three rungs of climbing
could not.

The five survivors were short verses — `jeremiah/30/22` is **seven tokens** —
so truncation was never the explanation. The prompt these renderings carry is
roughly **58,000 characters**; asking for 48,000 tokens of completion on top
of it appears to crowd the context window, and the request fails rather than
the output being cut off.

**So: raise the ceiling for a verse that looks cut off mid-word. Lower it for
a short verse that fails at a high ceiling.** A ladder that only climbs will
stall on exactly these seats, and the failure looks identical from the status
code — `:json-error` either way.

One caution recorded because it nearly misled this diagnosis: a hand-built
probe calling the API directly returned **HTTP 400 for every verse, including
Genesis 1:1**, which renders fine in production. The probe was malformed, not
the verses. The control — running a known-good verse through the same path —
is what caught it. **Test the instrument on something you know works before
believing what it says about something that does not.**

## Marker density

Rows 66, flow 56, gap 10 over a 300-verse window that was 217 Psalms. The gap
tracks the book, and the denominator matters as much as the gap: poetry
carries far fewer direct objects than narrative. Flow-parity closes the gap in
one pass at seating.

## The full-tree census — taken at 23,213 / 23,213

Every figure before this section was taken from a window of recently-written
files, or from a tree that was still filling. This is the first measurement of
the whole thing. Three findings, and two of them are about the instrument
rather than the text.

### The instrument was undercounting the erasure by a factor of four

The erasure probe carried a word list: *Hospodin*, *Bůh*, *Pán*, *Panovník*.
Against the full tree it reported **4 seats**. The real number is **15**.

**Czech declines, and a list of nominatives cannot police an inflecting
language.** The erasure almost never lands in the dictionary form. It lands as
*Bohem* (`žalmy/33/12`), *Bohu* (`žalmy/73/1`), *Boha* (`Izajáš/29/23`), *Bohů*,
*Pánu* (`žalmy/136/3`). Worse, the stem of *Bůh* **alternates its vowel** —
Bůh in the nominative, Boh- in every oblique case — so even a prefix match on
the citation form is blind to all of them. The probe was looking for a shape
the word takes in about one occurrence in ten.

The cure is to match the **stem**: `Hospodin | Bůh | Boh | Pán | Pan |
Věkověč | Všemohouc`.

A stem that broad would be reckless anywhere else — *Boha-* also opens
*bohatý*, "rich", which turns up at `Přísloví 22,7` and `Job 27,19`. It is safe
here **only because of the licensing test**: an erasure word is a finding only
where its own row's Hebrew surface is a divine name. Thirteen hits arrived and
thirteen were discharged by the surface, not by a whitelist. The broader the
probe, the more the licensing test earns its keep.

### The licensing test grants the word form, never the referent

Two of the fifteen are not erasures at all.

At `Numeri 11,28` Joshua says *Pane můj, Mojžíši* — "my lord Moses". At
`Numeri 12,11` Aaron says *můj Pane* to the same man. The surface at both is
**אדני**, spelled exactly as the divine Adonai, and the surface is all the
licensing test can see. It licenses the form. It cannot see who is being
addressed.

So these arrived as findings and had to be discharged **by reading**. They sit
in the same class as `1. Královská 20,23`, where *Bohové* renders אלהי and the
speakers are Aramean officers talking about their own gods — lawful, and ruled
so before the census ran.

This is worth stating plainly because it bounds the method: **the licensing
test is a filter, not a judge.** It removes the cases a word list would
convict wrongly. It does not remove the need for someone to read the verse.

### And a hole in the pattern itself

`Izajáš 3,1` reads *Pán, Jahve Cevaot*. The floor has *the Adonai, YHWH of
hosts*. That is an erasure — and the census filed it as **lawful**, because
the divine pattern carried אדני and the surface here is **האדון**, adon
without the yod.

The distinction is real and runs the other way too: **אדוני** (*adoni*, with
the vav) is the human form, which is why `Soudců 13,8` — Manoah addressing the
angel — correctly stayed out. But אדון with the article, in הָאָדוֹן יְהוָה
צְבָאוֹת, is the Lord himself. One missing alternation in one regex hid one
verse, and nothing in the output looked wrong.

Final pattern: `יהוה|אלהים|אלוה|אדני|אדון|שדי|צבאות|אלה|מרא|עלי?א|עלאה|קדיש`.

### The count, at 23,213 verses

| | |
|---|---:|
| erasure seats, licensed | **15** |
| — curable now (Hebrew) | 12 |
| — **blocked on the Aramaic ruling** | 3 |
| discharged by surface (lawful) | 13 |
| discharged by reading (referent) | 3 |

The three blocked are `Daniel 2,44`, `Daniel 2,47`, `Ezdráš 7,12`. The name
table covers Hebrew only; there was never a row to follow for אלה and מרא.

## The seats the gleaning ladder could never have found

The five-rung ladder cleared 707 residue and brought the tree to the full
floor. The full-tree census then found **371 seats that are present and
hollow**:

| class | seats | what it means |
|---|---:|---|
| blank flow | 10 | rows present, the readable verse empty |
| no rows at all | 56 | the file exists and contains nothing |
| row count ≠ floor | 81 | the alignment to the Hebrew is broken |
| a surface with no gloss | 265 verses (303 rows) | a Hebrew word left unanswered |

**The ladder only ever looked for absent files.** `verse-exists?` is a file
test, and every one of these files exists. A seat that is present and hollow
is not missing, so no rung of the ladder — up or down — was ever going to
reach it, and the tree read 23,213 / 23,213 the whole time.

That is the lesson worth carrying to the next chair: **reaching the floor
count is not the same as being at the floor.** The count is a file census. The
floor is a row census, and the two only agree once someone checks.

All 371 need `:force? true`, or the press sees the file, returns
`:already-done`, and writes nothing.

## The surfaces: one mechanism, a wider palette than ug showed

`surface_restore.py` restored **1,846 surfaces across 687 files**, and
**reported 126 it could not derive** rather than laundering them.

The surface field is the Hebrew record. It is not the chair's to write. On ug
the corruption was a single clean mechanism — the chair substituting Arabic
cognates letter by letter, mid-word, stopping partway. Czech does the same
thing, but reaches into **four different alphabets** to do it:

| what replaced the Hebrew | examples |
|---|---|
| **Latin**, by sound | `ופקדu` · `שאol` · `הואel` · `יפקod` · `מגרash` · `תשליכהhu` |
| **Czech's own diacritics** | `שנים → šנים` · `הנהר → הנהř` · `רקמה → רקמá` · `שש → šš` |
| **Cyrillic** | `פלשתים → пלשתים` · `ואיתמר → ואיתמар` |
| **Arabic** | `לאפר → لאפר` |

The Czech row is the sharpest version of the mechanism yet seen: ש→**š**,
ר→**ř**. Those are not generic Latin letters. They are the specific letters
*this chair holds*, and it spent them on the Hebrew. `שש → šš` is a complete
conversion — the word crossed all the way over.

The Arabic row is stranger. Nothing in this chair should know ل. It is the ug
mechanism itself, appearing in a Czech burn.

### A class ug never showed: the chair annotating the record

Some surfaces are not corrupted letters at all. They are **editorial notes
written into the Hebrew field**:

```
ויאמר→ותאמר      1. Královská 1,31   — with a RIGHTWARDS ARROW
וישם...ושם       1. Paralipomenon 1,46
ויצא-הוא-ואחיו   1. Paralipomenon 25,9
ולא — ווי        Exodus 38,10-12     — three consecutive verses
ויבאו_ואתה       1. Královská 12,4
```

That first one is a **ketiv/qere note**. The chair noticed the written form
and the read form differed, made a choice, and *recorded the choice in the
surface field, with an arrow*. It was showing its work.

It is the most articulate failure in this burn and the most dangerous, because
it is not noise — it is a correct observation filed in the wrong place. The
surface field is the record of what is written. A chair that edits the record
to explain itself has stopped being a translator.

One surface, at `Exodus 28,34`, had simply been replaced by its own gloss:
**žádné** where the floor reads **זהב**, gold.

All restored from the floor. Second run: 0 touched, 0 restored.

## Marker density, at the full tree

Rows **11,899**, flow **10,779**, gap **1,120** — measured over all 23,213
verses, replacing the 66/56/10 taken over a 300-verse Psalms window. The
window's ratio held: the gap tracks clause density with direct objects, and
flow-parity closes it in one pass at seating.

## What a marker is — three definitions, two of them wrong

All figures below are at the full tree, 23,213 verses.

The cure passes count ⟨את⟩ constantly: to find flows missing one, flows
carrying one too many, rows that dropped one. Every one of those decisions
rests on knowing what a marker *is*, and that took three attempts.

**v1 — the literal string ⟨את⟩.** It reads **zero** on a row that correctly
carries ⟨אתו⟩ or ⟨אתכם⟩ or ⟨אותם⟩. The adjudicator, seeing a row with no
marker where the floor has one, was about to restore a bare marker on top of
the inflected one and produce `⟨את⟩ ⟨אתו⟩`. Caught at `genesis/9/8` by a
spot-check, before any write.

A substring test on את does not rescue it either: **אותם has a vav between
the aleph and the tav.**

**v2 — any Hebrew inside brackets.** Too far the other way. The chair also
*supplies bare Hebrew terms*: ⟨ברית⟩ ⟨נפש⟩ ⟨שאול⟩ ⟨ה⟩. Forty-one of them
here, against two on the entire en floor. Counting those as markers put 138
verses into the "rows exceed the floor" column that did not belong there.

**v3 — the family, written out, with surfaces tested separately.** The family
is closed, so it can be named exactly: optional ו or מ, then א, optional ו,
then ת, then at most two suffix letters, with points allowed anywhere because
the floor carries אֵת.

And **surfaces need their own, more permissive test**. A surface is real
Hebrew from the text and inflects more widely than the forms we write in
brackets. Testing the surface against the gloss list wrongly convicted
`genesis/19/8`, whose surface אתהן is plainly an את-family word — its suffix
הן ends in a final nun the gloss list never needs. The surface test is a
prefix test, and it errs deliberately toward **leaving a marker alone**:
stripping is the destructive direction.

The correction cut one class from 79 verses to 3 — 76 of them false positives
about to be double-marked — and raised another from 405 to 526.

## The oscillation, where neither instrument was wrong

Iterating the cure chain to a fixed point surfaced a standoff. `flow_parity`
inserted 31 markers; the adjudicator stripped the same 31 back out; round
after round, forever.

`genesis/4/14`, surface **אתי**:

```
row   ⟨את⟩     — bare, and the en floor agrees, on both sides
flow  ⟨אתי⟩    — inflected
```

`flow_parity` counts the bare marker: rows 1, flow 0, a loss — insert one.
The adjudicator counts the family: rows 1, flow 2, a surplus — strip one.
Both are reading correctly. Both are reading different things.

The defect neither could see is that **the row and the flow carry different
FORMS of the same marker.** Adding cannot fix that and removing cannot fix
it; only rewriting can. So the rule that broke the loop: **the row is the
authority on form, the floor on count.** Twelve verses were rewritten in
place, and the chain converged.

## Row fabrication — the licensing test, one level down

The floor comparison could not name the last class, because the class is not
about the floor at all.

**A marker on a row whose surface is not an את-family word is the chair
speaking.** Ninety verses, 104 markers:

```
deuteronomy/19/21   בנפש בעין בשן ביד ברגל   — five markers, every surface
                    ב-prefixed: "for a soul, for an eye". The verse has no
                    את in it at all.
psalms/82/1         בעדת    — "in the assembly"
job/3/5             יגאלהו  — a verb with a pronominal suffix
2-samuel/6/6        ארון    — "ark"
2-samuel/13/15      two markers in a verse whose object is a suffix
```

Deuteronomy 19:21 now reads as it should: *duše za duši, oko za oko, zub za
zub, ruka za ruku, noha za nohu.*

This test needs no floor, and that turns out to matter. At `ruth/3/9` the
surface **is** את, and cs marks it while the floor does not. **The floor is
not always the fuller witness. The surface is.**

## A cure built, tested, and rejected

`flow_parity` places a missing flow marker by finding the marked object's
gloss verbatim in the flow. Here that left 121 residue, and the residue had
two causes, both of them inflection again:

1. **The case does not match.** The row glosses the object in the case the
   Hebrew marks; the flow puts it in the case the Czech sentence needs. Row
   *své služebníky*, flow *služebníkům*. Row *slova*, flow *slov*.
2. **The supplied word is mistaken for the object.** A marker row carrying
   `⟨od⟩ ⟨את⟩` yields `⟨od⟩` when only the marker is stripped, and the search
   goes looking for the wrong word. The object was in the flow all along.

So a closer was written that strips every bracket to find the object and
matches on the **stem**, short enough that a Czech ending cannot block it. It
placed 64 markers in 55 verses.

**About half of them were wrong**, and the dry run said so immediately:

```
učiním jemu ⟨את⟩ to dobré   →  ... ⟨את⟩ to ⟨את⟩ dobré
Naplň ⟨את⟩ vaky mužů        →  Naplň ⟨את⟩ ⟨את⟩ vaky mužů
aby viděl, zda opadly vody  →  aby ⟨את⟩ viděl, ...
není-li váš bratr ⟨s⟩ vámi  →  ... bratr ⟨s⟩ ⟨את⟩ vámi
```

The stem match was not the problem; it works. The premise was. **When the row
markers outnumber the flow markers, nothing in the file says which one is
missing.** The walk assumes rows and flow run in the same order, and Czech
reorders clauses against the Hebrew freely, so a marker legitimately present
later in the flow fails to align and a second one lands in front of a verb.

*A cure that can produce something the language never held is not a cure.*
The verses went to the press instead. The code was kept, with the rejection
written into its docstring, because the next chair will be tempted to write
the same function.

One more bug it surfaced: the alignment routine **dropped the remainder of
the verse** when it stripped a surplus marker — silent truncation, and then a
null-pointer on the following pass. Found because a sample was printed before
anything was written.

## Every press re-introduces the defects

Worth stating plainly, because it is not obvious and it cost a round of
confusion. After the 163-seat press landed, a re-run of the cure chain found
**423 corrupt surfaces across 54 files and 38 fabricated flow markers** — all
newly written, by the same press that fixed the seats it was aimed at.

The chair does not make these mistakes once. It makes them every time it
renders. So the cure chain is not a finishing step; it runs **after every
press**, and it runs **to a fixed point** — restore surfaces, close flows,
adjudicate markers, repeat until all three read zero.

## The names are not spelled one way

Raised by the UI catalog rather than by the census. Four translators, working
in parallel on separate chunks, disagreed about how to spell Aaron in the
chrome. So the corpus was asked — and the corpus does not agree with itself.

| name | the burn's majority | what the rule implies | variants |
|---|---|---|---:|
| Aaron | Áron 48.6% | **Aharon** 28.2% | 4 |
| Moses | Mojžíš 75.2% | **Moše** 24.8% | 2 |
| Joshua | Jozue 82.0% | **Jehošua** 12.8% | 3 |
| Jacob | Jákob 85.9% | **Ja'akov** 1.0% | 4 |
| Solomon | **Šalomoun 100%** | Šlomo 0% | 1 |
| Jerusalem | Jeruzalém 97.8% | **Jerušalajim** 2.2% | 2 |
| Saul | **Ša'ul 46.0%** ✓ | Ša'ul | 3 |
| Isaac | **Jicchak 76.6%** ✓ | Jicchak | 2 |
| Hezekiah | **Chizkijahu 100%** ✓ | Chizkijahu | 1 |
| Egypt | **Micrajim 63.9%** ✓ | Micrajim | 2 |

The discipline doc already rules this — *"Přepisuje se… jména osob a míst"*,
person and place names are transliterated. The burn followed that rule for
Saul, Isaac, Hezekiah and Egypt, and reached for the Czech tradition-form for
Aaron, Moses, Joshua, Jacob, Solomon and Jerusalem. **Šalomoun and Chizkijahu
each have exactly one spelling, and they disagree with each other about which
register to use.**

Nothing was changed. **Czech declines names**, so swapping a stem means
re-declining every form of it — *Mojžíšův* does not become *Mošeův* by
substitution. That is the l-attractor lesson at a larger scale, and it is
waiting on a ruling, not on a script.

## Where this chair stands

| | |
|---|---:|
| verses | 23,213 / 23,213 |
| token rows | **305,507 / 305,507** |
| empty flows · empty token-rows · empty glosses | 0 · 0 · 0 |
| rows disagreeing with the floor | 0 |
| corrupt surfaces | 0 |
| Slovak · Polish · German letters | 0 · 0 · 0 |
| verses carrying Jahve | 5,646 |
| erasure seats | **2 — both Aramaic, both awaiting a ruling** |

The two are `daniel/2/47` and `ezra/7/12`. They are named in `NOTES.md` and
they are not repairs that were skipped; they are places where the discipline
has not yet spoken, and the chair had nothing to be faithful to.

---

*This file grows as the burn proceeds. Counts carry the point they were taken
so a later reader can tell a partial measurement from a final one.*
