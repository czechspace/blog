+++
date = 2021-04-24
update = 2021-04-26
title = 'První Blog'
description = 'Cvičný příspěvek s použitím dat z původních stránek CSO.'
slug = "test-blog" 				### URL prispevku (relativni adresa v prohlizeci)
[taxonomies]
categories = ["cs"] 			### Jazykova mutace
tags = ["návod"] 				### Temata
[extra]
author = "Jan"
popisky = ["Popis prvního obrázku","Zevrubný popis druhého obrázku. Klidně i několik vět.", "Obrázek číslo tři.", "Dosluhující raketoplán na prodej."] 	### Popis kazdeho obrazku, postupne, dle cislovani nazvu souboru
related = ["prvni-draft","neexistujici"] ### Příbuzné stranky
+++

Příspěvky jsou psány běžným textem využívajícím Markdown.
Markdown je metoda formátování strukturovaných dokumentů psaných prostým textem.
Používá značky zvolené dle zvyků ze psaní běžných e-mailů <!-- more --> a příspěvků v diskuzních sítích. 
Tedy na rozdíl od značkovacích jazyků jako HTML jde o formátování čitelné přednostně pro lidi.
K běžnému používání stačí znát [rychlý přehled formátování][1].
Pro pokročilé používání se může hodit plná [specifikace CommonMark], kterou tento systém plně implementuje.

Markdown jsem zvolil jako mezistupeň ke strojovému vytváření a správě jednotné, ale mnohopočetné sestavy webových stránek, jako například `czechspace.cz`. 
Pomocí Markdown je psáno pouze tělo příspěvku. 
Hlavička, která je ohraničena `+++` a obsahuje popisné záznamy (metadata), nepoužívá Markdown. 
Metadata popisují klíčové atributy, strukturu a vztahy v ucelené sestavě stránek.

Tato stránka je zapsána v souboru \
`<složka projektu>/content/prvni-blog/index.md` \
Hlavička metadat tohoto souboru má plnou sestavu všech podporovaných typů parametrů a vypadá následovně:
```
+++
date = 2021-04-24
update = 2021-04-26
title = 'První Blog'
description = 'Pokusný příspěvek s použitím dat z původních stránek CSO.'
slug = "test-blog" 		### URL prispevku (prebiji nazev slozky pro urceni URL)
[taxonomies]
categories = ["cs"] 		### Jazykova mutace
tags = ["návod"] 		### Temata
[extra]
author = "Jan"
popisky = ["Popis prvního orázku","Zevrubný popis druhého obrázku. Klidně i několik vět.", "Obrázek číslo tři.", "Dosluhující raketoplán na prodej."] 	### Popis kazdeho obrazku, postupne, dle cislovani nazvu souboru
related = ["prvni-draft","neexistujici"] ### Příbuzné stranky
+++
```
Naopak minimální sestava metadat je v `.md` souboru pro [první draft](/prvni-draft/).

## Spuštění a vypnutí systému
V projektovém adresáři je spustitelný nástroj \
`<složka projektu>/webstatic` \
K jeho použití otevři `Terminal` a jdi do projektového adresáře pomocí `cd <složka projektu>`.
Prvně je třeba spustit `webstatic` v modu sestavení statických stránek příkazem: \
`./webstatic build` \
Ten vygeneruje statické stránky (obyčejné HTML soubory) v adresáři `<složka projektu>/public/`. Obsah tohoto adresáře se pak bude synchronizovat s nějakým obyčejným HTTP serverem na Internetu.

Druhou funkcí je spuštění místního web-serveru pomocí `./webstatic serve` \
což umožní testování výsledných stránek v prohlížeči přes místní URL `http://127.0.0.1:1111`. Takto spuštěný `webstatic` se bude snažit samočinně obnovovat stránky dle redakčních změn v souborech a adresářích. K ukončení této funkce stiskni `CTRL-C`. Někdy `webstatic` se samočinnou obnovou neuspěje, nebo dokonce spadne. Pak je třeba nejdřív znovu provést  `./webstatic build` a až potom opět spustit `./webstatic serve`.

## Redakční práce
Veškerá tvorba a obměna obsahu stránek, stejně jako vytváření a mazání jednotlivých stránek příspěvků, se provádí běžnou manipulací složek a souborů výhradně v adresáři \
`<složka projektu>/content`.
To lze provádět pomocí běžného správce souborů a nejobyčejnějšího textového editoru. 

Nicméně mnohem výhodnější je používat textový editor s podporou složek - což umožňuje otevřít vybraný adresář přímo v textovém editoru. Doporučuji nainstalovat si buď editor [Studio Code][2] a nebo [Sublime][3], oba jsou velice kvalitní a zdarma. Po spuštění editoru otevři adresář `<složka projektu>/content` a hierarchická struktura složek a souborů se objeví na levé straně editoru. Levým klikem otevíráš jednotlivé soubory a rozbaluješ adresáře. Pravým klikem na adresář v něm lze vytvořit nové soubory a složky.

## Obrázky
Připusťme, že systematické rozmístění textu v grafické šabloně tak aby hezky vypadala každá stránka z mnohopočetné a různorodé sestavy webových stránek, je poměrně složitá věc.
Pak přidání obrázků do této "rovnice" z toho dělá hotové peklo. 
Proto je systém navržen tak, že maximální možné množství rozhodnutí o obrázcích dělá program.

Redakční činnosti ohledně obrázků jsou následující: 
1. přidání a mazání souboru s obrázkem do/ze složky příspěvku.
2. nutnost označení pořadí v názvu souboru obrázku. 
3. (nedoporučeno) vložení jednotlivé obrázku do těla příspěvku.

Například součástí tohoto příspěvku jsou soubory:
```
$ ls content/prvni-blog/
_1_swarm_na_90tem_obletu.gif  _3_iac2009.jpg  csofactsheets-gseland-web.pdf
_2.krychli_uvnitr_dutiny.png  _4post-bg.jpg   index.md
```
Pořadí se značí pomocí čísla za podtržítkem na začátku názvu souboru obrázku.
Značení se provádí ručně přejmenováním souborů. 
Obrázek jehož název souboru začíná `_1` je samočinně použit na pozadí titulku příspěvku.
Nesprávné označení pořadí znemožní například popisky obrázků.
Ty se zadávají v hlavičce metadat příslušného `.md` souboru (popsané již výše) v poli `popisky`.
Počet obrázků je omezen na maximálně devět v jednom příspěvku.
Podporovány jsou obrázky s koncovkami `.png`, `.jpg` a `.gif`. 
Ale pozor, je nutné zajistit aby obrázek byl skutečně v uváděném formátu, jinak systém přestane fungovat.

Markdown umožňuje vkládat jednotlivé obrázky na vybraném místě v těle textu.
Například zde je vložen obrázek `_4post-bg.jpg` 

![foo bar](_4post-bg.jpg "Popis ručně vloženého obrázku." )

Tento způsob nelze doporučit.
Je velmi nesystematický, způsobuje potíže se vzhledem, správou i zpracováním, a často se stává i zbytečně pracný.
Uvážíme-li již výše popsanou nutnou "gymnastiku" s přípravou souborů obrázků, ručně vkládané obrázky do těla příspěvku znamená jen další ruční zpracování závislosti - například při změně souboru obrázku.
V původním webu `czechspace.cz` také NEJSOU jednotlivé obrázky součástí textu příspěvku, ale jsou ve sjednoceném přehledu v dané části šablony stránky.
Tento přístup doporučuji používat i nadále i přesto, že v tomto řešení nelze sestavovat stránky dynamicky.
Implementace je zajištěna systémovým příkazem {{`galerie()`}}, který se vloží ke konci těla každého příspěvku v místě, kde se má zobrazit.

Galerie, která je vidět i na konci této stránky, je číslovaný přehled zmenšených obrázků v jednotné velikosti zobrazených ve dvou sloupcích. 
Popisek každého obrázku se zobrazí při umístění kursoru na obrázek. 
Číslo obrázku je odkaz na vlastní soubor obrázku. 
Po shlédnutí původního souboru je nutné použít funkci "Zpět / Back" v prohlížeči. 
Obecně je řešení obrázků spíše drátenická práce, kterou v tomto stavu zatím nechám, a uvidím jak se situace vyvine dál.

<!-- Systémový generátor obrázků vytváří přehled obrázků v příspěvku -->
{{ galerie() }}

**Přílohy:**\
[Factsheet GSE LAND]

[Factsheet GSE LAND]: csofactsheets-gseland-web.pdf

**Odkazy:**\
[Alpbach Summer School]\
[Rychlý přehled formátování metodou Markdown][1]\
[specifikace CommonMark]\

[Alpbach Summer School]: http://www.summerschoolalpbach.at/
[specifikace CommonMark]: https://spec.commonmark.org/0.29/
[1]: https://commonmark.org/help/
[2]: https://code.visualstudio.com/Download
[3]: https://www.sublimetext.com/3
