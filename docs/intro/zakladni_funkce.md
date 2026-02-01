# Popis rozhraní

Po spuštění aplikace QField je možné zvolit otevření buď lokálních projektů
nebo projektů z úložiště na cloudu (např. QFieldCloud). V rámci QField je
možné rovněž vytvářet nové projekty.

<figure>
<img src="images/open.jpg" class="large"
alt="Projekty" />
<figcaption>Projekty</figcaption>
</figure>


<figure>
<img src="images/local_projects.jpg" class="large"
alt="Lokální projekty" />
<figcaption>Lokální projekty</figcaption>
</figure>

<figure>
<img src="images/qfield_cloud_projects.jpg" class="large"
alt="Projekty na cloudu" />
<figcaption>Projekty na cloudu</figcaption>
</figure>

## Mapové okno

Po otevření projektu se zobrazí mapové okno do kterého se načtou
data z projektu. Mapové okno se ovládá podobně jako jiné mapové 
aplikace tedy s využitím prstů.

Přiblížení tedy s využitím dvou prstů a jejich oddálení od sebe při 
dotyku obou prstů obrazovky.

Oddálení pak s využitím dvou prstů a jejich přiblížení k sobě při
dotyku obou prstů obrazovky.

Posun mapy se realizuje pomocí jednoho prstu.

<figure>
<img src="images/view.jpg" class="large"
alt="Mapové okno" />
<figcaption>Mapové okno</figcaption>
</figure>

## Panel vrstev

Přepínač vrstev zobrazuje všechny vrstvy projektu. Jejich zobrazení
poskytuje rychlou informaci o jejich pozici a grafickém zobrazení v
mapovém okně. 

<figure>
<img src="images/layers.jpg" class="large"
alt="Panel vrstev" />
<figcaption>Panel vrstev</figcaption>
</figure>

Podržením prstu na vrstvě aktivujeme informace o vrstvě,
jako je průhlednost, počet prvků nebo možnost zobrazení seznamu prvků.

<figure>
<img src="images/layer_info.jpg" class="large"
alt="Informace o vrstvě" />
<figcaption>Informace o vrstvě</figcaption>
</figure>

Dotykem na ikonu oka vedle názvu vrstvy můžeme vrstvu zobrazit nebo
skrýt.

## Měření vzdálenosti

V rámci Panelu vrstev najdeme další funkce. Jednou z nich je
měření vzdálenosti. Vzdálenost měříme postupným přidáváním bodů
do polylinie. Přidávání bodů se realizuje posunem mapy tak, aby
kurzor, který je uprostřed byl umístěn na místo, kam chceme umístit
bod. 

<figure>
<img src="images/measure1.jpg" class="large"
alt="Umístění kurzoru na výchozí místo měření" />
<figcaption>Umístění kurzoru na výchozí místo měření</figcaption>
</figure>

Následně zvolíme ikonu Plus pro přidání bodu. Pak posuneme mapu, 
tak aby druhý bod měření byl n amístě kurzoru. Interaktivně se nám
zobrazuje délka segmentu a azimut linie vůči severu ve stupních.

<figure>
<img src="images/measure2.jpg" class="large"
alt="Umístění kurzoru na druhý bod měření" />
<figcaption>Umístění kurzoru na druhý bod měření</figcaption>
</figure>

Takto můžeme postupně přidat další body měření. V případě dalších bodů
vidíme vždy celkovou délku (Délka) a délku aktuálně měřeného 
segmentu (Segment).

<figure>
<img src="images/measure3.jpg" class="small"
alt="Umístění kurzoru na třetí bod měření" />
<figcaption>Umístění kurzoru na třetí bod měření</figcaption>
</figure>

## Profil terénu

Měření vzdálenosti umožňuje zobrazení profilu modelu terénu.
Jedná se velmi orientační hodnoty vycházející z modelu (TODO) 

<figure>
<img src="images/elevation_profile.jpg" class="small"
alt="Profil terénu" />
<figcaption>Profil terénu</figcaption>
</figure>