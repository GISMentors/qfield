# Formuláře

## QGIS Projekt

Většina nastavení se přenáší jako součást projektu.
Projekt je soubor ve formátu XML komprimovaný metodou ZIP.
Symboly pro ikony, barvy nebo nastavení pro QFiled jsou součástí projektu.
Pokud je váš projekt datově malý, pak se doporučuje umisťovat data 
a projekt do stejné složky nebo projekt od složky a data do podřízených složek.

Když pak chcete např. projekt předat někomu jinému stačí hlavní složky komprimovat 
a předat např. e-mailem. 

Projekt se ukloží pomocí ikony diskety v hlavní nástrojové liště QGIS.

## GPKG formát

Formát GPKG je malou souborovou geodatabází. Může obsahovat více vrstvev geodat.
Jeho výhodou je, že se jedná o jeden soubor, který obsahuje jak data tak metadata.
Některá pravidla však mohou uživatelům komplikovat práci s tímto formátem.
Přesto, pokud k tomu není nějaký zásadní důvod, vám ho doporučujeme jako výchozí formát
pro ukládání geodat v případě práce s QField. 

# Formuláře

Součástí projektu jsou formuláře, kde je možné pro každou vrstvu nastavit,
jak bude vypadat formulář pro editaci atributů. Např. můžete definovat, že se 
do některého pole mohou zapisovat pouze konkrétní hodnoty z výčtu.

Formuláře se dají konfigorovat přes nastavení vlastností vrstvy.

<figure>
<img src="images/forms_1.png" alt="Vlastnosti vrstvy" class="img-middle" />
<figcaption>Vlastnosti vrstvy</figcaption>
</figure>

## Widgety

Pro nastavení jak má zadávání hodnot vypadat je možné specifikovat Widgety, 
což jsou malé kousky kódu s GUI, které zajišťují korektní vstupy.

Následující obrázek demonstruje, jak je možné pro pole typ, které je 
celé číslo specifikovat výčet hodnot, které je možné zadávat. 

<figure>
<img src="images/forms_2.png" alt="Výčet hodnot" class="img-middle" />
<figcaption>Výčet hodnot</figcaption>
</figure>

Při vytváření nebo editaci atributů prvku se pak tento seznam hodnot 
zobrazuje místo čísla, ale do databáze se zapisuje číslo.

<figure>
<img src="images/forms_3.png" alt="Výběr z výčtu hodnot" class="img-middle" />
<figcaption>Výběr z výčtu hodnot</figcaption>
</figure>

Stejně se pak po synchronizaci projektu a dat chová QField.

<figure>
<img src="images/forms_4.jpg" alt="Výběr z výčtu hodnot v QField" class="img-small" />
<figcaption>Výběr z výčtu hodnot v QField</figcaption>
</figure>

Oblíbeným Widgetem je Widget pro fotografie (resp. obecně přílohy).

Podrobně je problematika popsána v rámci školení 
[QGIS pro pokročilé](https://gismentors.github.io/qgis-pokrocily/pokrocile_upravy/index.html)

## Další pravidla pro pole

Mezi další pravidla pro pole, která se mohou nastavovat je např. 
* Omezení, že hodnota musí být uvedena - Není null
* Unikátní hodnota - musí být vždy jedinečná hodnota v rámci vrstvy
* Výchozí hodnota - zapíše se jako výchozí, pokud uživatel nespecifikuje

<figure>
<img src="images/forms_5.png" alt="Další pravidla pro pole" class="img-small" />
<figcaption>Další pravidla pro pole</figcaption>
</figure>
