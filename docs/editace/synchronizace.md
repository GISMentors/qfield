# Synchronizace

Synchronizace dat mezi desktop počítačem a mobilním telefonem je možná různými způsoby.
V případě QField se nabízí v zásadě čtyři možnosti:

* Využití služby QField Cloud a zásuvného modulu pro QGIS QField Sync - online i offline
* Využití zásuvného modulu QField Sync bez využití služeb cloudu - přes USB kabel
* Ruční kopírování dat bez synchronizace - přes USB kabel
* Využití vlastní PostgreSQL/PostGIS připojení dat - pouze online

Velmi snadné je využití služby QFieldCloud. V omezené podobě je k dispozici zdarma 
(100MB uložiště, sdílení mezi uživately pouze pokud je projekt veřejný).

Ještě jednodušší je využití PostgreSQL/PostGIS připojení, protože k synchronizaci
dochází automaticky, bez nutnosti jakékoli činnosti ze strany uživatele. Toto řešení
však vyžaduje stabilní připojení k internetu. Je sice možné využít nějaké další nástroje
a toto omezení obejít, ale to již není tak triviální. 
Detailněji je tento způsob popsán dále. 

## Synchronizace dat na QFieldCloud

V případě, že jsme provedli nějaké změny na straně mobilní aplikace 
a máme projekt načten z QField Cloudu je synchronizace snadná. 

### Odeslání dat z QField na QFieldCloud

Zvolíme boční panel, který obsahuje ikonu mraku (cloudu), s informací o změnách.

![Boční panel](images/sync_mobile1.jpg){ class="img-small" }

/// caption
Boční panel.
///

Na následující obrazovce volíme buď:

- **Synchronizovat** - kompletní synchronizace, stáhnout se aktuální data a projekt z QFieldCloudu do QField, a poté se 
pošlou změny z QField do QFieldCloudu.
- **Push změny** - pouze odeslání změn z QField do QFieldCloudu (bez jakéhokoliv stahování z QFieldCloudu do QField)


![Synchronizovat](images/sync_mobile2.jpg){ class="img-small" }

/// caption
Možnosti synchronizace.
///

V obou případech dojde k nahrání dat na cloud, ze kterého můžeme načít data v QGIS,
tak jak je popsáno dále.

## Instalace zásuvného modulu QGIS - QFieldSync

QFieldSync se instaluje stejně jako jiné moduly z hlavního repozitáře QGIS.

![Instalace zásuvného modulu](images/sync1.png){ class="img-middle" }

/// caption
Instalace zásuvného modulu QFieldSync.
///

Nainstalovaný modul instaluje nástrojovou lištu, která slouží k sychronizaci jak přes cloud, tak i bez využití cloudu. Součástí lišty je i nastavení pro QField. 

![Nástrojová lišta modulu](images/sync2.png){ class="img-small" }

/// caption
Nástrojová lišta QFieldSync.
///

## Načtení dat z QFieldCloudu do QGIS

K načtení dat z QFieldCloudu slouží první dvě tlačítka na liště. První použijeme v případě,
že zatím projekt na disku nemáme k dispozici. Druhé v případě, že již projekt máme k dispozici
a je aktuálně otevřen v QGIS.

Po zvolení prvního tlačítka a přihlášení se do cloudu se zobrazí seznam naši projektů.

![Seznam projektů na cloudu](images/sync3.png){ class="img-middle" }

/// caption
Seznam projektů na cloudu.
///

Po vybrání projektu ze seznamu již můžeme provést synchronizaci pomocí druhého tlačítka.

![Aktivovaný projekt](images/sync4.png){ class="img-middle" }

/// caption
Aktivovaný projekt.
///

V případě, že projekt nemáme k dispozici, vyzve nás zásovný modul k zadání cesty,
kam se má projekt uložit.

![Cesta k projektu](images/sync5.png){ class="img-middle" }

/// caption
Cesta k projektu.
///

Následně již můžeme provést synchronizaci dat. V našem případě je situace
jednoduchá, protože lokálně nemáme žádná data, proto převezmeme data z cloudu.

![Stažení dat z cloudu](images/sync6.png){ class="img-middle" }

/// caption
Stažení dat z cloudu.
///

Pokud dojde ke stažení dat, objeví se potvrzení o stažení.

![Potvrzení stažení dat z cloudu](images/sync7.png){ class="img-middle" }

/// caption
Potvrzení stažení dat z cloudu.
///

Následně můžeme pomocí ikony Open otevřít stažený projekt.

![Otevřený stažený projekt](images/sync8.png){ class="img-middle" }

/// caption
Otevřený stažený projekt.
///

### Úprava dat v QGISu

V případě, že provedem úpravy na straně QGIS, můžeme je nahrát na cloud. Tento směr synchronizace (QGIS -> QFieldCloud -> QField) se využívá zejména pro úpravy QGIS projektu a dat, které nejsou editovány v terénu (viz následující upozornění) jako sjou podkladové mapy a další podpůrné vrstvy.

!!! warning "Upozornění"
    QFieldSync neumí data plně synchronizovat zpět na QFieldCloud. Komunikace QGIS (*local*) a QFieldCloud (*cloud*) nesynchronizuje, ale **přepisuje**, a vždy je třeba zvolit, které soubory preferujeme - local vs. cloud. QField a QFieldCloud, ale data plně synchronizuje, spojí .qpkg do jednoho, a verze jsou viditelné na webu QFieldCloud. Pokud je nutná úprava dat v QGIS jsou různá řešení pro různé případy (např. použití samostatné vrstvy nebo první synchronizovat projekt do QGIS a pak zpět za předpokladu že všechna data jsou již na cloudu)

    Příklad: Mapovatel v terénu přidá v QField nový bod do vrstvy `mereni.gpkg`. Operátor v kanceláři otevře projekt v QGIS, také preovede změny ve vrstvě `mereni.gpkg` a poté synchronizuje projekt s QFieldCloud, kde zvolí možnost *Prefer Local*. V tomto případě se data z QGIS **přepíší** na QFieldCloud a mapovatel v terénu již nebude mít přístup k bodu, který přidal v QField, protože verze vrstvy z jeho bodem byla přepsána verzí z QGIS, která tento bod neobsahuje.


![Nový geoprvek](images/sync9.png){ class="img-middle" }

/// caption
Nový geoprvek.
///

Změny nejdříve zapíšeme do souboru, nejlépe ukončením editace.
Pak zvolíme ikonu cloudu (druhou na liště zásuvného modulu).

![No action](images/sync10.png){ class="img-middle" }

/// caption
No action.
///

Výchozí je stav No action, tedy neprovede se žádná operace.
V tomto případě chceme nahrát data z lokálního počítače na cloud.
Volíme proto možnost lokálního počítače, buď zaškrtávacím tlačítkem
pod ikonou desktopu vedle položky, kterou chceme synchronizovat nebo talčítkem 
Prefer Local (zapne všechny položky v seznamu jako local).

![Prefer Local](images/sync11.png){ class="img-middle" }

/// caption
Prefer Local.
///

Zvolíme možnost Perform Actions, která provede synchronizaci.

![Synchronizace dokončena](images/sync12.png){ class="img-middle" }

/// caption
Synchronizace dokončena.
///

Na mobilním telefonu zvolíme nejdříve boční panel.

![Boční panel QField](images/sync13.jpg){ class="img-small" }

/// caption
Boční panel QField.
///

V panelu vybere ikonu cloudu a na další obrazovce dáme Synchronizovat.

![Synchronizovat](images/sync14.jpg){ class="img-small" }

/// caption
Synchronizovat.
///

Data se stáhnou z cloudu a již je máme k dispozici v mapě. 
Vidíme nově přidaný bod.

![Aktualizovaná data](images/sync15.jpg){ class="img-small" }

/// caption
Aktualizovaná data.
///

## Synchronizace kopírováním souborů

Sychronizace dat je možná také kopírováním souborů. Pokud pracujete např. jen s
jednou databází ve formátu GeoPackage (GPKG), stačí po zapsání změn tuto databázi 
překopírovat z jednoho zdroje na druhý.

Toto kopírování je možné realizovat buď přes správce souborů nebo ideální s využitím QFieldSync, který vytváří celý 
balíček projektu všetně dat.

V případě, že kopírujete ručně, pak je nutné dávat velký pozor na zámky souborů, 
přiložená data, apod.

V případě využití GUI obou nástrojů může být situace jednodušší, přesto se
může stát, že ne všechbo proběhne vždy bez problémů.

Obecně tuto varinatu sychnronizace nedoporučujeme, pokud nic nebrání využití cloudu.

## PostgreSQL/PostGIS

Jedna z možností jak se vyhnout potřebě synchronizace dat je využití 
databázového systému PostgreSQL/PostGIS. PostgreSQL je profesionální systém,
vyvíjený pod svobodnou licencí a je k dispozici zdarma. 

Pro neznalé podobných systémů se jedná o řízené tabulky s daty, kde se prvky zapisují
jako řádky tabulky. Ono je to samozřejmě složitější, 
ale v rámci našeho kurzu nebudeme řešit detaily.
Rozšíření PostGIS umožňuje zapsat geometrii geoprvků do jednoho z polí tabulky.

Z pohledu QGIS je pak možné takto ukládaná data připojit podobně jako připojujeme
mapové (datové) služby OGC (např. WMS, WFS). Podstatné je, že jakékoli změny provedené
na straně QGIS nebo QField se automaticky zapíší do PostGIS databáze a synchronizace
je tedy téměř okamžitá. Tento způsob připojení dat, však vyžaduje stabilní připojení k
síti (např. LTE). Při použití předplatného uložiště QfieldCloud Pro je možné takové připojení používat i s offline
synchronizací.

Více informací o tom jak připojit data z PostGIS v QGIS najdete v rámci materiálu pro kurz
PostGIS pro začátečníky:
[Připojení dat z PostGIS v QGIS](https://gismentors.github.io/postgis-zacatecnik/kapitoly/2_zaciname.html#zobrazujeme-data-v-qgis)

## Mergin Maps

Alternativou k QField je nástroj [Mergin Maps](https://merginmaps.com/). 
Nabízí obdobnou funkcionalitu jako QField. Liší se detailech a může někomu vyhovovat
více než QField. Funguje na podobném principu jako QField (využívá QGIS projekt, formuláře atd.), ale synchronizace dat 
probíhá technicky jiným způsobem, což umožňuje například  možné pohodleně editovat data i v QGIS

## GIS Quick

Další možnou alternativou je využití nástroje [GIS Quick](https://gisquick.org/).
Nejedná se úplně o cílené řešení pro mobilní mapování, ale tuto funkcionalitu nabízí.
Primárně slouží k publikování dat v prostředí WWW prohlížeče. 

Pomocí zásuvného modulu pro QGIS je možné velmi rychle publikovat data na 
server GIS Quick, který si může uživatel buď provozovat sám nebo využít existující server. 

Vypublikovaný QGIS projekt je pak dostupný v rámci WWW prohlížeče (např. Chrome)
a to i s optimalizací pro mobilní variantu. Klient umožńuje editaci dat stejně jako 
QField nebo Mergin Maps. 

Nevýhodou tohoto řešení je stejně jako v případě PostGIS nutnost stabilního připojení
k síti.
