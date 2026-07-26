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