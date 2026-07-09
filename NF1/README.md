# NF1 Seguretat passiva

RA1. Aplica mesures de seguretat passiva en sistemes informàtics descrivint característiques d'entorns i relacionant-les amb les seves necessitats.

Durada prevista: 15 hores

---

## Introducció

En aquest primer bloc començarem fent una petita introducció a la seguretat informàtica, una justificació de la seva importància i una classificació de les diferents categories que hi ha. Tot seguit, ens centrarem en la seguretat passiva, que és l’objectiu principal d’aquest bloc, veient els la seguretat física i finalment, la seguretat lògica.

## Taula de continguts

- [AA1. Conceptes bàsics de seguretat informàtica](#aa1-conceptes-bàsics-de-seguretat-informàtica)
- [AA2. Seguretat a l'entorn físic](#aa2-seguretat-a-lentorn-físic)
- [AA3. Seguretat lògica](#aa3-seguretat-lògica)

---

## AA1. Conceptes bàsics de seguretat informàtica

Disciplina encarregada de protegir la informació i els sistemes informàtics.

Conceptes relacionats:

- Ciberseguretat: defensa dels sistemes informàtics davant d’atacs maliciosos. És una part de la seguretat informàtica.
- Seguretat de la informació: conjunt de mesures que permeten protegir la informació (no només amb sistemes informàtics).

És una de les disciplines que més importància ha adquirit en els darrers anys, ja que la majoria de les activitats humanes es realitzen amb l’ajuda de sistemes informàtics i per tant, la informació que es genera i s’emmagatzema en aquests sistemes és molt valuosa.

> **Cas real: SEPE**
>
> El Servicio Público de Empleo Estatal (SEPE) va patir un atac informàtic de tipus ransomware (Ryuk) que es va detectar el 9 de març del 2022. L’atac va afectar al funcionament del servei d’ocupació durant mesos, va provocar la caiguda de la web i la pèrdua d’expedients que es van haver de tornar a generar, amb les molèsties que això va suposar per a les persones usuàries i el cost en hores extra de treball per a l’administració pública.

Per tant, és evident que caldrà aplicar mesures de seguretat per evitar que es produeixin incidents com aquest, i si es produeixen, minimitzar-ne les conseqüències. Però cal tenir clar que la **seguretat absoluta no existeix**.

>“The only truly secure system is one that is powered off, cast in a block of concrete and sealed in a lead-lined room with armed guards — and even then, I have my doubts.”
>
>Eugene Spafford. Prof. Universitat de Purdue i expert en seguretat informàtica.

### Principis bàsics de la seguretat informàtica

En el camp de la seguretat de la informació, hi ha tres principis bàsics que cal tenir en compte:

- **Confidencialitat**: només les persones autoritzades poden accedir a la informació.
- **Integritat**: la informació no pot ser modificada per persones no autoritzades.
- **Disponibilitat**: la informació ha d’estar disponible quan sigui necessària.

Aquests principis són coneguts com a **CIA** (Confidentiality, Integrity, Availability) i són la base de qualsevol política de seguretat informàtica.

A més d’aquests principis, la seguretat informàtica afegeix dos conceptes més:

- **Autenticació**: permet verificar la identitat d’una persona o sistema.
- **Vinculació**: garanteix que una persona no pugui negar haver realitzat una acció. Exemple, en una transacció bancària, que el client no pugui negar haver realitzat la transferència i el receptor no pot negar haver-la rebut.

Per això, en el camp de la seguretat informàtica, es parla de **CIA + AV** (Confidentiality, Integrity, Availability + Authentication, Verification) o **CIDAV** si fem l'acrònim en català.

### Actius

I què cal protegir? Els elements que cal protegir s’anomenen **actius** i poden ser de diferents tipus:

- **Actius físics**: ordinadors, servidors, impressores, etc.
- **Actius lògics**: sistemes operatius, aplicacions, bases de dades, etc.
- **Informació**: el contingut que es genera i s’emmagatzema en els sistemes informàtics, com ara documents, correus electrònics, fitxers multimèdia, etc.
- **Reputació**: la imatge que una empresa o persona té davant de la societat. La pèrdua de reputació pot tenir conseqüències econòmiques molt importants.

> **Cas real: Sony PlayStation Network**
>
> L'any 2011, la plataforma en línia PlayStation Network va patir un atac històric. Els delinqüents van robar dades de milions de comptes, inclosos noms i es rumoreja que informació bancària. Sony va haver de tancar la xarxa durant setmanes. Això va provocar una reacció negativa dels usuaris i una pèrdua de confiança en la marca, afectant les vendes i el valor de la companyia (les accions van patir una força caiguda).

### Ciberdelinqüència

La ciberdelinqüència és l’activitat delictiva que es realitza amb l’ajuda de sistemes informàtics, conforme ha augmentat la dependència de les tecnologies de la informació, l'activitat delictiva ha crescut exponecialment. Segons diversos estudis, s'estima que el cost de la ciberdelinqüència a nivell mundial és de **10,5 bilions de dòlars anuals** (bilions: milions de milions de dòlars) [Font: StationX](https://app.stationx.net/articles/cybercrime-statistics).

El cibercrim mou directament diners, ja sigui a través de robatori d’informació bancària, extorsió amb ransomware, estafes en línia, etc. Al 2022 es valorar que movia al voltant del bilió de dolars, superant altres negocis il·lícits com el tràfic de drogues o el tràfic de persones.

![Valor del cibercrim](./media/secure-it-grafico-cibercrimen.jpg)
> Font: [IT User](https://www.ituser.es/actualidad/2023/06/el-valor-del-cibercrimen-se-aproxima-al-15-del-pib-mundial)

### Classificació de la seguretat informàtica

La seguretat informàtica és una disciplina molt àmplia que es pot classificar en diferents categories segons l’objectiu que es vulgui aconseguir:

- **Seguretat passiva**: pretén minimitzar els danys d'un incident digital un cop s'hagi produït. El seu objectiu és assegurar-se que vostè pot recuperar les seves dades i tornar a la normalitat el més aviat possible. Exemple, les còpies de seguretat.

- **Seguretat activa**: mesures preventives dissenyades per bloquejar les amenaces en temps real i evitar que un atac tingui èxit o que es produeixi un incident. El seu objectiu principal és la proactivitat. Per exemple, un tallafocs o un antivirus.

També es classifica segons el tipus d’actiu que es vulgui protegir:

- **Seguretat física**: protegeix els dispositius físics. Exemple, un SAI o un sistema de control d’accés a una sala de servidors.

- **Seguretat lògica**: protegeix les dades i les aplicacions, com la contrasenya d'accés a un sistema o el xifrat de la informació.

## AA2. Seguretat a l'entorn físic

L'entorn físic són els espais on es troben els equips informàtics. Poden ser oficines, l’aula on estem ara mateix o bé espais especialitzats on s’ubiquen els servidors i equipament com armaris de comunicació que s’anomenen centres de processament de dades (CPD).

Cal que aquest entorn físic compleixi unes normes de seguretat per minimitzar els riscos sobre el hardware de l’organització.

I quines amenaces hi ha sobre l’entorn físic? Poden ser de diferents tipus:

- Fallada dels serveis de subministrament:
  - Tall de comunicacions
  - Talls elèctrics
  - Pujades de tensió

- Catàstrofes:
  - Inundacions
  - Incendis

- Intrusions:
  - Robatoris
  - Accessos no autoritzats

- Accions d'usuaris:
  - Danys intencionats a l’equipament
  - Danys accidentals a l’equipament

### Els CPD o datacenters

De tot l’equipament informàtic, el més crític són els serveis d'infraestructura que solen estar formats pels servidors, però també pels sistemes d'emmagatzematge i de comunicacions. Aquests serveis solen estar ubicats en espais especialitzats anomenats centres de processament de dades (CPD).

Aquests espai pot ser una sala dedicada dins l'edifici de la organització, però en organitzacions molt grans o bé en empreses que ofereixen serveis a tercers, solen ser construccions dedicades en exlusiva que reben el nom de datacenters.



## AA3. Seguretat lògica
