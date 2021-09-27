# Vefforritun 1, 2021: Verkefni 6, CSS #4

[Kynning í fyrirlestri](https://youtu.be/gDeKrPH7KQM).

Halda skal áfram með viðmót fyrir Vefforritunarfréttir úr [verkefni 4](https://github.com/vefforritun/vef1-2021-v4/) og [verkefni 5](https://github.com/vefforritun/vef1-2021-v4/). Nú skal setja þróunartól: `browser-sync`, `sass`, og `stylelint`.

## Útlit

Sama gildir um útlit og í verkefni 5, útlit ætti að haldast alveg það sama, eina sem breytist er hvernig verkefnið er uppsett.

## Tæki og tól

Til þess að geta notað þessi tól þarf að [setja upp Node.js, sækið „Recommended For Most Users“](https://nodejs.org/en/). Eftir að þið hafið keyrt uppsetningar forrit getið þið opnað Command prompt/terminal/skel og keyrt:

```bash
> node -v
v14.17.6 # eða sú útgáfa sem þið sóttuð
> npm -v
7.24.1 # eða álíka
```

Ef þið fáið villu eftir að hafa keyrt annað hvort og uppsetning á Node.js gekk sem skildi skulið þið prófa að endurræsa tölvu. Ef ennþá ekki að virka, leitið hjálpar í dæmatímum.

Setja skal upp `sass`, `browser-sync`, `stylelint` og `concurrently` til að nýta Sass og geta gert breytingar sem sjást strax í vafra.

Fyrst þarf að búa til `package.json` með því að keyra `npm init` í verkefnamöppu.

Síðan þarf að sækja hvert tól með `npm install <nafn á tóli>`.

[Sjá nánar í fyrirlestri 6.2: Node.js og npm](https://github.com/vefforritun/vef1-2021/blob/main/vikur/06/06.2.npm.md).

### Sass

Skipta skal CSS upp í mismunandi skrár undir `styles/`, sjá viðeigandi komment í hverju og einu skjali.

Í `styles/config.scss` skal geyma allar stillingar fyrir verkefni og nota þær á viðeigandi stöðum.

Nota skal _nesting_ en aðeins upp á eitt level.

```scss
.card {
  .title {
    // ok

    .item {
      // ekki ok, þriðja level
    }
  }
}
```

### Browser sync & concurrently

Þegar skipunin `npm run dev` er keyrð skal verkefnið keyra upp vefþjón með browser-sync, þýða sass skrár og fylgjast með breytingum á HTML og Sass.

[Sjá fyrirlestur 6.3: Sass & stylelint](https://github.com/vefforritun/vef1-2021/blob/main/vikur/06/06.3.sass-stylelint.md) og í [Sass + browser-sync](https://github.com/vefforritun/vef1-2021/tree/main/vikur/06/daemi/3.sass-stylelint/03.sass-browser-sync).

### Linting

Setja skal upp stylelint með `stylelint-config-sass-guidelines` og `stylelint-config-standard`.

Þegar skipunin `npm run lint -s` er keyrð skal keyra stylelint með þessum reglum og ættu engar villur að koma fram.

[Sjá fyrirlestur 6.3: Sass & stylelint](https://github.com/vefforritun/vef1-2021/blob/main/vikur/06/06.3.sass-stylelint.md) og í [Stylelint dæmi](https://github.com/vefforritun/vef1-2021/tree/main/vikur/06/daemi/3.sass-stylelint/04.stylelint).

## Mat

* 40% – CSS flutt yfir í Sass
* 40% – stylelint uppsett og engar villur
* 20% – Verkefni sett upp með `package.json` og viðeigandi scriptum

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 27. september 2021.

## Skil

Skila skal í Canvas í seinasta lagi fyrir lok dags þriðjudaginn 5. október 2021.

Skilaboð skulu innihalda zip skjali með lausn. Athugið **að ekki skal skila `node_modules/` möppu!**

Hver dagur eftir skil dregur verkefni niður um 10%, allt að 20% ef skilað fimmtudaginn 7. október 2021 en þá lokar fyrir skil.

## Einkunn

Leyfilegt er að ræða, og vinna saman að verkefni en **skrifið ykkar eigin lausn**. Ef tvær eða fleiri lausnir eru mjög líkar þarf að færa rök fyrir því, annars munu allir hlutaðeigandi hugsanlega fá 0 fyrir verkefnið.

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 5% hvert, samtals 40% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 10%, samtals 20% af lokaeinkunn.

> Útgáfa 0.1
