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

TODO

## Nahrání upravených data zpět na cloud

TODO

## Synchronizace kopírováním souborů

TODO

## PostGIS

TODO

## Mergin Maps

TODO

## GIS Quick

TODO
