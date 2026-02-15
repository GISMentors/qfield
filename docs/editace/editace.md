# Editace

Editace v QField je možná pomocí editace atributů existujících geoprvků
editací geometrie existujících geoprvků nebo vytvářením nových geoprvků.
Geoprvky nebo hodnoty atributů je možné také mazat.

## Vytváření geoprvků

V případě bodové vrstvy je přidávání velmi pdobné jako přidávání
bodů měření. Posuneme mapu tak aby kurzor byl v místě kam chceme
umísti bod a zvolíme talčítko Plus.

<figure>
<img src="images/create_point1.jpg" alt="Umístění kurzoru" class="img-small" />
<figcaption>Umístění kurzoru</figcaption>
</figure>

Zobrazí se formulář s atributy geoprvku, které můžeme vyplnit.

<figure>
<img src="images/create_point2.jpg" alt="Vyplnění atributů" class="img-small" />
<figcaption>Vyplnění atributů</figcaption>
</figure>

Po potvrzení je bod umístěn do mapy a vykreslen symbolem
dle pravidel vrstvy.

<figure>
<img src="images/create_point3.jpg" alt="Vytvořený geoprvek" class="img-small" />
<figcaption>Vytvořený geoprvek</figcaption>
</figure>

## Editace geoprvků

K editaci geoprvků využijeme kliknutí (dotyk) na geoprvek, kurzor může být mimo něj.  

<figure>
<img src="images/edit_point1.jpg" alt="Kurzor mimo geoprvek" class="img-small" />
<figcaption>Kurzor mimo geoprvek</figcaption>
</figure>

Po kliknutí na geoprvek se zobrazí seznam geoprvků s aktivním geoprvkem. 
Geoprvek je rovněž zvýrazněn jinou ikonou v mapě.

<figure>
<img src="images/edit_point2.jpg" alt="Vybraný geoprvek" class="img-small" />
<figcaption>Vybraný geoprvek</figcaption>
</figure>

Klikneme (dotkneme se) geoprvku v seznamu (na obrázku text "A"), 
čímž aktivujeme další funkce.

<figure>
<img src="images/edit_point3.jpg" alt="Funkce pro editaci geoprvku" class="img-small" />
<figcaption>Funkce pro editaci geoprvku</figcaption>
</figure>

Pro editaci atributů volíme ikonu A s tužkou.
Hodnoty můžeme přepsat a potvrdit zelenou potvrzovací ikonou.

<figure>
<img src="images/edit_point4.jpg" alt="Editace atributů" class="img-small" />
<figcaption>Editace atributů</figcaption>
</figure>

Pro editaci geometrie volíme ikonu geometrie s tužkou.
Po aktivaci se automaticky přepneme do režimu editace vertexů 
(bodů nebo lomových bodů geometrie).

<figure>
<img src="images/edit_point5.jpg" alt="Editace geometie" class="img-small" />
<figcaption>Editace geometie</figcaption>
</figure>

Klikneme na vertex (bod). Ikona se změní na modré kolečko. Tímto je vertex vybrán.

<figure>
<img src="images/edit_point6.jpg" alt="Vybraný bod" class="img-small" />
<figcaption>Vybraný bod</figcaption>
</figure>

Posuneme kurzor na místo, kam chceme bod umístit tak že posuneme mapu.
Posouvá se pouze kurzor s modrým kolečkem.

<figure>
<img src="images/edit_point7.jpg" alt="Nové umístění bodu" class="img-small" />
<figcaption>Nové umístění bodu</figcaption>
</figure>

Umístění potvrdíme zelenou potvrzovací ikonou. Bod se přesune na nové místo.

<figure>
<img src="images/edit_point8.jpg" alt="Potvrzení nového umístění bodu" class="img-small" />
<figcaption>Potvrzení nového umístění bodu</figcaption>
</figure>

## Mazání geoprvků

Mazání prvků se realizuje přes formulář prvků, který jsme již viděli
v části editace.

K formuláři je možné se tedy dostat stejně jako v případě editace a to dotykem (kliknutím)
na prvek v mapě a následně výběrem prvku ze seznamu.

Druhá možnost je dlouhým stiskem na geoprvek v mapě.
V případě dlouhého stisku se aktivujě kontextová nápověda, která obsahuje
referenci na geoprvek a zobrazení formuláře.

<figure>
<img src="images/delete_point1.jpg" alt="Kontextová nabídka" class="img-small" />
<figcaption>Kontextová nabídka</figcaption>
</figure>

Na formuláři v pravé části najdeme možnost zobrazení dalších funkcí. Jedna z nich
je Odstranit prvek.

<figure>
<img src="images/delete_point2.jpg" alt="Funkce formuláře" class="img-small" />
<figcaption>Funkce formuláře</figcaption>
</figure>

Odstranění prvku musíme potvrdit na následujícím dialogu.

<figure>
<img src="images/delete_point3.jpg" alt="Potvrzení odstranění geoprvku" class="img-small" />
<figcaption>Potvrzení odstranění geoprvku</figcaption>
</figure>

## Topologická editace geoprvků

Podobně jako v QGIS Desktop je možné zapnout topologickou editaci.
