# Popis rozhraní

Po spuštění aplikace QField je možné zvolit otevření buď lokálních projektů
nebo projektů z úložiště na cloudu (např. QFieldCloud). V rámci QField je
možné rovněž vytvářet nové projekty.

![Projekty](images/open.jpg){ class="img-small" }

/// caption
Projekty.
///

![Lokální projekty](images/local_projects.jpg){ class="img-small" }

/// caption
Lokální projekty.
///


![Projekty na cloudu](images/qfield_cloud_projects.jpg){ class="img-small" }

/// caption
Projekty na cloudu.
///

## Mapové okno

Po otevření projektu se zobrazí mapové okno do kterého se načtou
data z projektu. Mapové okno se ovládá podobně jako jiné mapové 
aplikace tedy s využitím prstů.

Přiblížení tedy s využitím dvou prstů a jejich oddálení od sebe při 
dotyku obou prstů obrazovky.

Oddálení pak s využitím dvou prstů a jejich přiblížení k sobě při
dotyku obou prstů obrazovky.

Posun mapy se realizuje pomocí jednoho prstu.

![Mapové okno](images/view.jpg){ class="img-small" }

/// caption
Mapové okno.
///


## Panel vrstev

Přepínač vrstev zobrazuje všechny vrstvy projektu. Jejich zobrazení
poskytuje rychlou informaci o jejich pozici a grafickém zobrazení v
mapovém okně. 

![Panel vrstev](images/layers.jpg){ class="img-small" }

/// caption
Panel vrstev.
///

Podržením prstu na vrstvě aktivujeme informace o vrstvě,
jako je průhlednost, počet prvků nebo možnost zobrazení seznamu prvků.

![Informace o vrstvě](images/layer_info.jpg){ class="img-small" }

/// caption
Informace o vrstvě.
///

Dotykem na ikonu oka vedle názvu vrstvy můžeme vrstvu zobrazit nebo
skrýt.

## Měření vzdálenosti

V rámci Panelu vrstev najdeme další funkce. Jednou z nich je
měření vzdálenosti. Vzdálenost měříme postupným přidáváním bodů
do polylinie. Přidávání bodů se realizuje posunem mapy tak, aby
kurzor, který je uprostřed byl umístěn na místo, kam chceme umístit
bod. 

![Umístění kurzoru na výchozí místo měření](images/measure1.jpg){ class="img-small" }

/// caption
Umístění kurzoru na výchozí místo měření.
///

Následně zvolíme ikonu Plus pro přidání bodu. Pak posuneme mapu, 
tak aby druhý bod měření byl n amístě kurzoru. Interaktivně se nám
zobrazuje délka segmentu a azimut linie vůči severu ve stupních.

![Umístění kurzoru na druhý bod měření](images/measure2.jpg){ class="img-small" }

/// caption
Umístění kurzoru na druhý bod měření.
///

Takto můžeme postupně přidat další body měření. V případě dalších bodů
vidíme vždy celkovou délku (Délka) a délku aktuálně měřeného 
segmentu (Segment).

![Umístění kurzoru na třetí bod měření](images/measure3.jpg){ class="img-small" }

/// caption
Umístění kurzoru na třetí bod měření.
///

## Profil terénu

Měření vzdálenosti umožňuje zobrazení profilu modelu terénu.
Jedná se velmi orientační hodnoty vycházející z modelu Mapzen Global Terrain (MGT)
Jsou to data o přibližně ~30 m / pixel. 

![Profil terénu](images/elevation_profile.jpg){ class="img-small" }

/// caption
Profil terénu.
///

V případě, že potřebujete přesnější model je toto možné nastavit v projektu QGIS.
