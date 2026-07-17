# AA1 Proteging les dades

## Les dades com actiu

La informació (les dades) és un dels actius més valuosos per les empreses, si el disc dur s’avaria els programes es poden tornar a instal·lar, però les dades si es perden no es poden recuperar. Per aquest motiu les dades també són un dels objectius més cercats pels delinqüents, el segrest de les dades (ransomware) s'ha convertit en una de les principals amenaces per a les empreses.

![Ransomware](../img/ransomware.png)

Què podem fer? Aquí tenim dues estratègies complementàries:

- **Continuitat de negoci**: protegim les dades de manera que davant d'un incident es pugui seguir treballant sense pèrdua de dades.
- **Recuperació de desastres**: protegim les dades de manera que davant d'un incident es pugui recuperar la informació i tornar a l'estat anterior.

## Continuïtat de negoci

La clau per seguir operant i ser resistents davant d'un incident és l'**alta disponibilitat**. La alta disponibilitat consisteix a disposar d'una infraestuctura que permeti garantir l’accés a les dades malgrat es produeixin incidents, per tant, estem parlant de **sistemes tolerants a fallades**.

Per disposar de redundància, és a dir, de duplicació de components, podem utilitzar diferents estratègies:

- Servidors redundants: tenir més d’un servidor amb la mateixa informació encara que estiguin a la mateixa ubicació. Aquesta estratègia es pot implantar a la pròpia organització o usant serveis de cloud, on tots els proveïdors ofereixin la possibilitat de tenir servidors redundants, tant dins el mateix data center com en diferents ubicacions geogràfiques.

- Sistemes d'emmagatzematge redundants: tenir més d’un sistema d’emmagatzematge amb la mateixa informació. Aquesta és l'estratègia que **sempre s'aplica**. Els sistemes d'emmagatzematge redundants són els que permeten que davant d'una avaria d'un disc o SSD, el sistema continuï funcionant sense pèrdua de dades.

> ❗La redundància és cara per tant cal analitzar quin nivell d’alta disponibilitat es necessita per cada cas concret.

## Recuperació de desastres

L’objectiu és recuperar el funcionament normal en el mínim temps possible si l'incident ha provocat la pèrdua de les dades o del seu accés. Aquí normalment tenim dos escenaris:

- Recuperació dels sistemes: usant imatges de restauració, es pot recuperar el sistema operatiu i les aplicacions en un temps ràpid.

- Recuperació de les dades: usant còpies de seguretat, es poden recuperar les dades.

## Protecció de les dades

La protecció de les dades implica també la seguretat física per evitar els accessos no autoritzats (com hem vist en el bloc anterior) i el xifrat de la informació per evitar que si les dades són robades, no es puguin llegir, tema que veurem en el bloc següent.

Per últim, un aspecte important de la protecció de la informació és gestionar el **cicle de vida de les dades**, és a dir, com es creen, s’emmagatzemen, s’utilitzen i finalment es destrueixen els suports físics un cop arriben al final de la seva vida útil.

> ❗Un [estudi](https://www.pcmag.com/news/many-used-hard-drives-sold-on-ebay-still-contain-leftover-data) realitzat al 2019 descobrir que 3 de cada 5 disc durs de segona mà encara contenien dades personals i confidencials.

I com es destrueixen de forma segura les dades d'aquests suports? Doncs depenent del tipus de suport, del nivell de seguretat necessari i del destí que se li doni al dispositiu, podem utilitzar diferents estratègies:

- **Destrucció física**: destruir el suport físic de manera que no es pugui recuperar la informació. Aquesta estratègia és la més segura però  no permet reutilitzar el dispositiu. Es poden usar trituradores, màquines perforadores, etc.

- **Desmagnetització**: També es pot fer servir la desmagnetització (desmagnetitzar el suport) però només és efectiva en suports magnètics (discs durs, cintes, etc.) i no permet reutilitzar el dispositiu.

- **Sobrescriptura**: consisteix a sobreescriure la informació amb dades aleatòries. Aquesta estratègia és efectiva en suports magnètics i en suports de memòria flash (SSD, USB, targetes SD, etc.) i permet reutilitzar el dispositiu. Òbviament, no es pot usar en dispostius d'un sol ús com DVD o similar. La sobrescriptura es pot fer amb diferents estratègies, com per exemple, sobreescriure una vegada amb zeros, sobreescriure tres vegades amb dades aleatòries i finalment sobreescriure una vegada amb uns. Aquesta estratègia és la que recomana el Departament de Defensa dels Estats Units (DoD 5220.22-M).

> ❗Tot i que pensem en les unitats dels ordinadors, la informació pot estar en altres dispositius. Per exemple, les impressores i fotocopiadores digitals tenen memòria interna on es poden emmagatzemar les dades que s’han imprès o escanejat. Per tant, cal tenir en compte aquests dispositius a l’hora d'evitar filtracions de dades [Vídeo: Copy Machines, a Security Risk?](https://youtu.be/iC38D5am7go?si=d__dJDAlE-Zwb85A).
