# AA2 Seguretat física

## Seguretat a l'entorn físic

**Entorn físic**: espais on es troben els equips informàtics.Poden ser oficines, l’aula on estem ara mateix o bé espais especialitzats on s’ubiquen els servidors i equipament com armaris de comunicació que s’anomenen centres de processament de dades (CPD). Cal que aquest entorn físic compleixi unes normes de seguretat per minimitzar els riscos sobre el hardware de l’organització.

Les amenaces que poden afectar l’entorn físic són:

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

## La sala de servidors (CPD)

De tot l’equipament informàtic, el més crític a l’hora de protegir físicament és el que conforma l'estructura troncal de la infraestructura, això inclou servidors, sistemes emmagatzematge, equipament de xarxa, etc.

Habitualment se situen una sala de servidors o CPD (Centre de Processament de Dades) o en el cas de grans empreses o de proveïdors de serveis, en centres de dades (Data Center) que poden allotjar servidors de diferents empreses. Aquests espais han de complir una sèrie de requisits per garantir la seguretat física i la continuïtat del servei.

![CPD](./media/datacenter.png)

La sala que allotjarà el CPD ha de complir una sèrie de requisits:

- Seguretat a intrusions: control d’accessos, vigilància, alarmes, etc.
- Seguretat davant catàstrofes: sistemes de detecció i extinció d’incendis, sistemes de control d’humitat i temperatura, etc. Evitar soterranis pel risc d’inundació.
- Protecció davant interferències electromagnètiques que puguin afectar el funcionament dels equips.

> Òbviament, aquests requisits són més estrictes en un Data Center que en una sala de servidors d’una empresa, però el concepte és el mateix.

### Condicions ambientals

Cal protegir els equips i persones de:

- **Temperatura**: Els equips dissipen molta calor. Necessiten ventilació i una temperatura controlada.
- **Humitat**: Aigua i humitat ambiental alta poden provocar corrosió, i baixa electricitat estàtica. Potser necessari usar deshumidificadors.
- **Interferències electromagnètiques**: allunyar de màquines que poden generar-les (generadors elèctrics, maquinària industrial, fluorescents, etc).

#### Temperatura i humitat

Els equips informàtics generen molta calor, per això les sales de servidors s'anomenen sales fredes, perquè es mantenen a una temperatura baixa i constant. La temperatura ideal és d’uns 20-22ºC i la humitat relativa entre el 40% i el 60%. Per aconseguir-ho, s’instal·len sistemes de climatització i ventilació que permetin mantenir aquestes condicions.

Ens instal·lacions grans per afavorir la circulació d’aire s’utilitza la tècnica de **passadís fred i passadís calent**.

![Passadís fred i passadís calent](./media/passadis_fred_calent.png)

L'objectiu és que l’aire fred que surt dels equips de climatització arribi a la part frontal dels servidors i que l’aire calent que expulsen els servidors sigui evacuat per la part posterior. D’aquesta manera s’evita que l’aire calent es barregi amb l’aire fred i es manté una temperatura adequada.

### Detecció i extinció d’incendis

Un incendi representa un risc tant pels equips com per les persones.

Els sistemes informàtics es poden danyar segons el sistema d’extinció d’incendis emprat, òbviament no sembla gaire bona idea extingir un incendi amb una mànega d’aigua quan hi ha equips elèctrics.

Sistemes d'extinció d’incendis:

- Aigua nebulitzada: es tracta d’un sistema que allibera una boira d’aigua que redueix la temperatura i l’oxigen de l’aire. És un sistema segur per a les persones i els equips.

- Gasos inerts: es tracta d’un sistema que allibera gasos com el CO2 (ja no molt popular) o l'*Inergen*. Són un sistema segur per als equips però no per a les persones, ja que poden morir per asfíxia.

- Materials fluïds (Novec) líquids que permeten l'extinció i en no ser conductors no afecten els equips. És un sistema segur per a les persones i els equips.

En instal·lacions petites, no tindrem un sistema d’extinció d’incendis automàtic, però sí que haurem de disposar d’extintors i senyalització adequada.

Els més recomanats:

- Aigua polvoritzada: segur i net.
- Extitors CO2: no deixa residus.
- Halotron: gas inert i que no deixa residus.

En cap cas es bona idea usar extintors de pols, ja que deixen residus que poden danyar els equips.

---

| [⬆️](./README.md)Tornar a inici NF1 | [⬅️](./AA1-ConceptesSI.md)AA1 Conceptes de Seguretat Informàtica | [➡️](./AA3-SeguretatLogica.md)AA3 Seguretat Lògica |
| :--- | :--- | :--- |
