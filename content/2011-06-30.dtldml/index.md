+++
date = 2011-06-30
updated = 2018-11-04
title = "DTL/DML"
description = "Demonstrátor využití softwarových knihoven DTL/DML v družicovém řídícím středisku"
slug ="dtldml"
[taxonomies]
categories = ["cs"]
tags = ["programy-organizace-pecs","typy-clanku-tiskovina","programy-organizace-esa","uzivatele-firmy","typy-clanku-ukonceny-projekt","uzivatele-vedci"]
[extra]
author = ""
popisky = ["Mission Control System Evropské kosmické agentury SCOS-2000."]
+++

Ověření funkčnosti nových softwarových knihoven Trvání projektu: 2007 až 2010 Vedoucí projektu: Helena Kalenská V předcházejícím projektu „Advanced SCOS-2000 Monitoring“ spolupracovala firma ANF DATA na vývoji softwarových knihoven pro správu a přenos telemetrických dat v kontextu nové architektury pro pozemní operační systémy (ESA Ground Operation System, EGOS). Účelem tohoto projektu bylo ověřit funkčnost nových softwarových knihoven EGOS Data Transfer Library a Data Management Library (DTL/DML) v existujícím družicovém řídicím systému SCOS-2000. Hlavní výhodou nové architektury je, že základní komponenty pro distribuci dat nejsou závislé na existujících specifických knihovnách systému SCOS-2000. To umožňuje použití těchto komponent nejen v družicovém řídicím systému SCOS-2000, ale i v dalších aplikacích v rámci pozemního segmentu ESA. Nové základní komponenty pro distribuci dat (Basic Data Consumers, Providers, Distribution Nodes, and Filters) lze jednoduše upravit a použít pro distribuci libovolných datových typů nezávisle na platformě. Stačí nadefinovat nové datové typy s pomocí jazyka IDL (Interface Definition Language), odvodit datové filtry od již existujících základních filtrů (pokud je filtrování dat požadováno) a vytvořit instance příslušných datových zdrojů (data providers), distribučních uzlů (data distribution nodes) a uživatelských aplikací (data consumers). Základní distribuční komponenty byly použity i v SCOS-2000 demonstrátoru k nahrazení původního systému distribuce telemetrických dat – tj. subsystémů CPD (Centralized Packet Distribution) a PDS/PARC (Packet Archiving and Distribution servers). Dílčí, integrační a systémové testy byly provedeny s využitím nástroje pro automatické testování ART (Automated Regression Testing). Výkonostní testy prokázaly, že Demonstrátor družicového řídícího systému splňuje požadavky na distribuci dat v družicovém řídicím systému SCOS-2000. Pojekt se uskutečnil ve spolupráci s firmou Siemens Rakousko (hlavní dodavatel). ANF DATA ANF DATA jsou dceřinnou společností firmy Siemens AG Rakousko, byla založena v roce 1992. Společnost ANF DATA nabízí komplexní IT služby – vývoj softwarových řešení, integrace systémů, aplikační podporu, dodávky hardwaru, poradenství a školení pro zákazníky. Poskytuje řešení pro lokální i pro mezinárodní trh v různých oblastech, jako jsou průmysl, energetika, komunikace, pozemní segment kosmického průmyslu a inventory management. Oddělení Space vzniklo v ANF DATA v roce 1998 a od té doby spolupracuje se Siemens AG Rakousko na vývoji softwarových řešení pro Evropskou kosmickou agenturu (ESA), Německou kosmickou agenturu (DLR), evropský navigační systém Galileo a pro vedoucí družicové operátory. V rámci programu PECS se ANF DATA podílelo na třech mezinárodních projektech zaměřených na uplatnění moderních informačních technologií v řídících a informačních systémech ESA. Co vám účast v projektu přinesla? Vedoucí projektu Helena Kalenská: „Výsledný softwarový prototyp (DTL/DML based MCS Demonstrator) je založen na nové verzi družicového řídícího systému SCOS-2000 R5.0, která obsahuje mnoho nových konceptů a prvků (např. Packet Archiving Filing & Distribution servery, vylepšenou funkčnost multi-domén, oddělené GUI procesy, atd). Během této aktivity jsme měli možnost se s novou verzí SCOS-2000 detailně seznámit, což se ukázalo jako velmi důležité i pro náš pozdější projekt uskutečněný v rámci Pobídkového programu pro česká pracoviště v roce 2010. Naše zkušenosti z PECS programu nám také významně napomohly k tomu, že ANF DATA bylo vybráno jako tzv. Kvalifikovaný partner pro vývoj softwaru pro pozemní segment ESA (2010-2014).“

{{ galerie() }}

**Přílohy:**
[Factsheet DTL/DML]

[Factsheet DTL/DML]: csofactsheets-dtl-dml-web.pdf
