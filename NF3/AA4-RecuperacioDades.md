# AA4 Recuperació de dades

## Introducció

La recuperació de dades (Data Recovery) és el conjunt de tècniques, eines i procediments utilitzats per accedir, extreure i restaurar la informació continguda en dispositius d'emmagatzematge secundari quan aquesta ha estat inaccessible, corrompuda, esborrada o danyada.

Dins de la seguretat informàtica, la recuperació de dades se situa com una mesura de seguretat activa i de resposta davant incidents. Encara que la prevenció (còpies de seguretat, sistemes RAID) és la primera línia de defensa, la recuperació lògica és el darrer recurs per restablir la **Disponibilitat** i la **Integritat** de la informació en el triat de la seguretat (CIA).

## Causes de la pèrdua de dades

La pèrdua d'informació en un sistema microinformàtic pot estar originada per diversos factors:

- **Errors Humans** (Accidentals): Esborrat d'arxius per equivocació, formatat de volums incorrectes o desconnexió a la bruta de unitats durant operacions d'escriptura.

- **Ataques Maliciosos** (Malware): Acció de ransomware (que xifra o destrueix la MFT/GPT), wipers (dissenyats per sobreescriure sectors clave) o modificacions no autoritzades del registre d'arrencada (MBR/VBR).

- **Errors de Programari i Sistema de Fitxers**: Caigudes de tensió o tancaments inesperats del sistema operatiu en el moment d'actualitzar les metadades d'un volum (causant un estat dirty o corruptor).

- **Degradació del Suport Suport Físic**: Desgast natural de les cel·les en memòries Flash, aparició de sectors defectuosos (bad sectors) en discs magnètics o danys al firmware.

Per tant, podem classificar la pèrdua de dades en avaries físiques o lògiques, segons si el suport d'emmagatzematge està físicament danyat o si el sistema de fitxers està corromput.

```text
                          ┌─ Avaria Lògica (Estructura de dades / Metadades)
                          │   └─ Esborrats, formatats, corrupció de FS/MBR
                          │
 Tipus d'Avaries ─────────|
                          │
                          └─Avaria Física o de Firmware(Mecànica / Electrònica)
                          │   └─ Capçals, plat magnètic, PCB, curtcircuits, corrupció de firmware
```

Identificar el tipus d'avaria és fonamental per determinar la tècnica de recuperació més adequada, en el cas de sospita d'ava

## Avaries físiques

Les avaries físiques impliquen que o bé el suport d'emmagatzematge està danyat físicament o bé que el firmware del dispositiu està corromput. En qualsevol dels casos, la recuperació de dades requereix un entorn controlat i especialitzat, com ara una sala blanca (clean room) per evitar contaminació i danys addicionals.

Existeixen diverses empreses especialitzades en recuperació de dades que ofereixen serveis professionals per a aquests casos, utilitzant eines i tècniques avançades per recuperar la informació de dispositius danyats.

- [Recovery Labs](https://www.recoverylabs.com/)
- [Ontrack](https://www.ontrack.com/)
- [DriveSavers](https://www.drivesaversdatarecovery.com/)
- [Gillware](https://www.gillware.com/)

## Avaries lògiques

Aquí el suport físic (hardware) funciona correctament, però les dades són inaccessibles a causa d'errors en el sistema de fitxers, la taula de particions, esborrats accidentals o accions malicioses.

### Protocol d'actuació

Quan s'enfronta un procés de recuperació de dades lògica, cal seguir rigorosament aquestes dues normes per evitar la pèrdua irreversible de la informació:

- **No escriure mai sobre el suport d'emmagatzematge afectat**: Qualsevol operació d'escriptura pot sobreescriure les dades que es volen recuperar, fent-les irrecuperables.

- **Treballar si es pot sobre una còpia del suport d'emmagatzematge**: Crear una imatge del dispositiu afectat i realitzar les operacions de recuperació sobre aquesta còpia, preservant així l'estat original del suport. En els casos de peritatge forense, on la integritat de les proves és essencial, preservar la integritat de la unitat original és essencial.

### Tècniques de recuperació

#### Recuperació basada en el sistema de fitxers (undelete)

Quan s'esborra un fitxer en un sistema de fitxers (NTFS, FAT32, EXT4), el sistema operatiu no esborra el contingut real dels sectors, sinó que:

1. Marca l'entrada del fitxer com a "lliure" en la taula d'assignació de fitxers (FAT, MFT, etc.).
2. Marca els blocs de dades com a disponibles per a noves escriptures.

Si els sectors no s'han sobreescrit, és possible recuperar el fitxer utilitzant eines especialitzades que escanegen la taula d'assignació i recuperen les entrades marcades com a lliures.

#### Carving de fitxers (raw recovery)

Aquesta tècnica s'utilitza quan la taula de particions o les metadades del sistema de fitxers estan corruptes o han estat destruïdes.

Mecanisme: S'analitza la imatge del disc sector per sector buscant Magic Numbers (capçaleres o headers i peus o footers característics de cada tipus de fitxer).

Exemples de Magic Numbers:

- PDF: Comença per %PDF (45 50 44 46 en hexadecimal).
- JPEG: Comença per FF D8 FF E0 i acaba per FF D9.
- ZIP / DOCX / XLSX: Comença per PK (50 4B 03 04).

> 💡En els sistemes *nix podeu consultar de quin tipus és un fitxer amb la comanda `file`que consulta la capçaler dels fitxers per llegir aquests "magic numbers".

**Inconvenient**: Aquesta tècnica no recupera els noms dels fitxers ni la seva estructura de directoris, només el contingut dels fitxers. En sistemes operatius com FAT32 que provocaven força fragmentació, el carving pot resultar en fitxers incomplets si els blocs de dades han estat sobreescrits o dispersos.

#### Recuperació de taula de particions

Restaura l'estructura de les particions del disc si l'MBR (Master Boot Record) o la GPT (GUID Partition Table) s'han corrupt :

- Es busquen les estructures del sector de arrencada de les particions (Boot Sectors o Superblocks).

- Es reescriu la taula de particions original per fer de nou accessible el volum sense haver de restaurar fitxer per fitxer.

### Eines de recuperació de dades

Existeixen diverses eines de recuperació de dades, tant de codi obert com comercials, que poden ajudar en la recuperació de fitxers i particions. Aquí teniu alguns exemples d'eines:

| Eina          | Tipus d'interfíce | Ús principal                                     | Sistema Operatiu        |
|------         |-------------------|--------------                                    |------------------       |
| dd/ddrescue   | CLI               | Còpia de disc sector per sector                  | Linux, Windows*, macOS  |
| ftk Imager    | CLI               | Creació d'imatges forenses                       | Linux, Windows, macOS   |
| testdisk      | CLI/TUI           | Recuperació de particions i fitxers              | Linux, Windows, macOS   |
| photorec      | CLI/TUI           | Carving de fitxers                               | Linux, Windows, macOS   |
| recuva        | GUI               | Recuperació de fitxers                           | Windows                 |
| autopsy       | GUI               | Anàlisi forense digital i recuperació avançada   | Linux, Windows, macOS   |
| foremost      | CLI               | Carving de fitxers                               | Linux, Windows          |
| magicrescue   | CLI               | Carving de fitxers                               | Linux                   |

\* A Windows `dd` no és una eina del sistema, sinó que existeixen un port `dd` per Windows: [https://www.chrysocome.net/dd](https://www.chrysocome.net/dd) que és una eina de línia de comandes que permet copiar i convertir fitxers i imatges de disc.

### Exemple d'actuació

Davant de la unitat de la qual volem recuperar dades esborrades, un exemple de procediment seria:

1. **Crear una imatge del dispositiu**: Utilitzar eines com `dd`, `ddrescue` o `ftk Imager` per crear una còpia sector per sector del dispositiu afectat. Això preserva l'estat original del dispositiu i permet treballar sobre la còpia sense risc de perdre més dades.

2. **Executar TestDisk sobre la imatge**: Utilitzar TestDisk per analitzar la imatge i recuperar les particions eliminades o corrompudes.

3. **Recuperar fitxers amb PhotoRec**: Si les particions no es poden recuperar, utilitzar PhotoRec per realitzar un carving de fitxers i recuperar el contingut dels fitxers.

## Enllaços d'interès

- [IBM Thik. ¿Qué es la recuperación de datos?](https://www.ibm.com/es-es/think/topics/data-recovery)

- [DFIRScience. Starting a New Digital Forensic Investigation Case in Autopsy 4.19+ (YouTube)](https://youtu.be/fEqx0MeCCHg?si=pP6LEEnM3vwPNM8F)

- [Geeknetic. Recuva: Cómo recuperar Archivos Eliminados](https://www.geeknetic.es/Guia/2341/Recuva-Como-recuperar-Archivos-Eliminados.html)
