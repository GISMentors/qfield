# Synchronizace

Synchronizace dat mezi desktop počítačem a mobilním telefonem je možná různými způsoby.
V případě QField se nabízí v zásadě čtyři možnosti:

* Využití služby QField Cloud a zásuvného modulu pro QGIS QField Sync
* Využití zásuvného modulu QField Sync bez využití služeb cloudu
* Ruční kopírování dat a automatická nebo poloautomatická synchronizace
* Využití PostgreSQL/PostGIS připojení

Velmi snadné je využití služby QField Cloud. V omezené podobě je k dispozici zdarma.

Ještě jednodušší je využití PostgreSQL/PostGIS připojení, protože k synchronizaci
dochází automaticky, bez nutnosti jakékoli činnosti ze strany uživatele. Toto řešení
však vyžaduje stabilní připojení k internetu. Je sice možné využít nějaké další nástroje
a toto omezení obejít, ale to již není tak triviální. 
Detailněji je tento způsob popsán dále. 

## Synchronizace dat na cloud

V případě, že jsme provedli nějaké změny na straně mobilní aplikace 
a máme projekt načten z QField Cloudu je synchronizace snadná. 

## Odeslání dat z QField na cloud

Zvolíme boční panel, který obsahuje ikonu cloudu, s informací o změnách.

<figure>
<img src="images/sync_mobile1.jpg" alt="Boční panel" class="img-small" />
<figcaption>Boční panel</figcaption>
</figure>

Na následující obrazovce volíme buď kompletní synchronizaci (Synchronizovat) nebo
jen synchronizaci dat (Push změny).

<figure>
<img src="images/sync_mobile2.jpg" alt="Boční panel" class="img-small" />
<figcaption>Boční panel</figcaption>
</figure>

V obou případech dojde k nahrání dat na cloud, ze kterého můžeme načít data v QGIS,
tak jak je popsáno dále.

## Instalace zásuvného modulu QGIS

Zásuvný modul se instaluje stejně jako jiné moduly z hlavního repozitáře QGIS.

<figure>
<img src="images/sync1.png" alt="Instalace zásuvného modulu" class="img-middle" />
<figcaption>Instalace zásuvného modulu</figcaption>
</figure>

Nainstalovaný modul instaluje nástrojovou lištu, která slouží k sychronizaci jak přes cloud,
dat bez využití cloudu. Součástí lišty je i nastavení pro QField. 

<figure>
<img src="images/sync2.png" alt="Nástrojová lišta modulu" class="img-small" />
<figcaption>Nástrojová lišta modulu</figcaption>
</figure>

## Načtení dat v QGISu

K načtení dat z cloudu slouží první dvě tlačítka na liště. První použijeme v případě,
že zatím projekt na disku nemáme k dispozici. Druhé v případě, že již projekt máme k dispozici
a je aktuálně otevřen v QGIS.

Po zvolení prvního tlačítka a přihlášení se do cloudu se zobrazí seznam naši projektů.

<figure>
<img src="images/sync3.png" alt="Seznam projektů na cloudu" class="img-middle" />
<figcaption>Seznam projektů na cloudu</figcaption>
</figure>

Po vybrání projektu ze seznamu již můžeme provést synchronizaci pomocí druhého tlačítka.

<figure>
<img src="images/sync4.png" alt="Aktivovaný projekt" class="img-middle" />
<figcaption>Aktivovaný projekt</figcaption>
</figure>

V případě, že projekt nemáme k dispozici, vyzve nás zásovný modul k zadání cesty,
kam se má projekt uložit.

<figure>
<img src="images/sync5.png" alt="Cesta k projektu" class="img-middle" />
<figcaption>Cesta k projektu</figcaption>
</figure>

Následně již můžeme provést synchronizaci dat. V našem případě je situace
jednoduchá, protože lokálně nemáme žádná data, proto převezmeme data z cloudu.

<figure>
<img src="images/sync6.png" alt="Stažení dat z cloudu" class="img-middle" />
<figcaption>Stažení dat z cloudu</figcaption>
</figure>

Pokud dojde ke stažení dat, objeví se potvrzení o stažení.

<figure>
<img src="images/sync7.png" alt="Potvrzení stažení dat z cloudu" class="img-middle" />
<figcaption>Potvrzení stažení dat z cloudu</figcaption>
</figure>

Následně můžeme pomocí ikony Open otevřít stažený projekt.

<figure>
<img src="images/sync8.png" alt="Otevřený stažený projekt" class="img-middle" />
<figcaption>Otevřený stažený projekt</figcaption>
</figure>

## Úprava dat v QGISu

V případě, že provedem úpravy na straně QGIS, můžeme je nahrát na cloud.

<figure>
<img src="images/sync9.png" alt="Nový geoprvek" class="img-middle" />
<figcaption>Nový geoprvek</figcaption>
</figure>

Změny nejdříve zapíšeme do souboru, nejlépe ukončením editace.
Pak zvolíme ikonu cloudu (druhou na liště zásuvného modulu).

<figure>
<img src="images/sync10.png" alt="No action" class="img-middle" />
<figcaption>No action</figcaption>
</figure>

Implicitně je stav No action, tedy se neprovede, žádná operace.
V tomto případě chceme nahrát data z lokálního počítače na cloud.
Volíme proto možnost lokálního počítače, buď zaškrtávacím tlačítkem
pod ikonou desktopu vedle položky, kterou chceme synchronizovat nebo talčítkem 
Prefer Local (zapne všechny položky v seznamu jako local).

<figure>
<img src="images/sync11.png" alt="Prefer Local" class="img-middle" />
<figcaption>Prefer Local</figcaption>
</figure>

Zvolíme možnost Perform Actions, která provede synchronizaci.

<figure>
<img src="images/sync12.png" alt="Synchronizace dokončena" class="img-middle" />
<figcaption>Synchronizace dokončena</figcaption>
</figure>

Na mobilním telefonu zvolíme nejdříve boční panel.

<figure>
<img src="images/sync13.jpg" alt="Boční panel QField" class="img-small" />
<figcaption>Boční panel QField</figcaption>
</figure>

V panelu vybere ikonu cloudu a na další obrazovce dáme Synchronizovat.

<figure>
<img src="images/sync14.jpg" alt="Synchronizovat" class="img-small" />
<figcaption>Synchronizovat</figcaption>
</figure>

Data se stáhnou z cloudu a již je máme k dispozici v mapě. 
Vidíme nově přidaný bod.

<figure>
<img src="images/sync15.jpg" alt="Aktualizovaná data" class="img-small" />
<figcaption>Aktualizovaná data</figcaption>
</figure>

## Synchronizace kopírováním souborů

Sychronizace dat je možná také kopírováním souborů. Pokud pracujete např. jen s
jednou databází ve formátu GeoPackage (GPKG), stačí po zapsání změn tuto databázi 
překopírovat z jednoho zdroje na druhý.

Toto kopírování je možné realizovat buď přes správce souborů nebo 
s využitím nástrojů zásuvného modulu pro QGIS resp. s využitím QField.

V případě, že kopírujete ručně, pak je nutné dávat velký pozor na zámky souborů, 
přiložená data, apod.

V případě využití GUI obou nástrojů může být situace jednodušší, přesto se
může stát, že ne všechbo proběhne vždy bez problémů.

Obecně tuto varinatu sychnronizace nedoporučujeme, pokud nic nebrání využití cloudu.

## PostGIS

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
síti (např. LTE).

Více informací o tom jak připojit data z PostGIS v QGIS najdete v rámci materiálu pro kurz
PostGIS pro začátečníky:
[Připojení dat z PostGIS v QGIS](https://gismentors.github.io/postgis-zacatecnik/kapitoly/2_zaciname.html#zobrazujeme-data-v-qgis)

## Mergin Maps

Alternativou k QField je nástroj [Mergin Maps](https://fr.merginmaps.com/). 
Nabízí obdobnou funkcionalitu jako QField. Liší se detailech a může někomu vyhovovat
více než QField. Synchronizace dat probíhá obdobně jako v případě QField a to s využitím
cloudu Mergin Maps.

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
