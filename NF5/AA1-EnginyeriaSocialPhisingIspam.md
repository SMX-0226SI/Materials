# NF5AA1-Enginyeria Social, Phishing i Spam

## Taula de Continguts

1. [Enginyeria Social, Fraus i Robatori d'Informació](#enginyeria-social-fraus-i-robatori-dinformació)
   - [1.1 El Factor Humà com a Vector d'Atac](#11-el-factor-humà-com-a-vector-datac)
   - [1.2 Principals Tècniques d'Enginyeria Social](#12-principals-tècniques-denginyeria-social)
   - [1.3 Impacte en Organitzacions i Empreses](#13-impacte-en-organitzacions-i-empreses)
   - [1.4 Estratègies de Prevenció i Mitigació](#14-estratègies-de-prevenció-i-mitigació)
2. [Minimització del Trànsit de Correu Brossa i Publicitat](minimització-del-trànsit-de-correu-brossa-i-publicitat)
   - [2.1 Conceptes de Spam, Adware i Malvertising](#21-conceptes-de-spam-adware-i-malvertising)
   - [2.2 Importància de la Minimització del Trànsit](#22-importància-de-la-minimització-del-trànsit)
   - [2.3 Arquitectura de Protecció per Capes](#23-arquitectura-de-protecció-per-capes)
   - [2.4 Tipus i Tècniques de Filtrat Antispam](#24-tipus-i-tècniques-de-filtrat-antispam)
   - [2.5 Taula Comparativa de Tècniques](#25-taula-comparativa-de-tècniques)
3. [3. Resum de Bones Pràctiques per a Administradors de Sistemes](#3-resum-de-bones-pràctiques-per-a-administradors-de-sistemes)

---

## Enginyeria Social, Fraus i Robatori d'Informació

> **💡 Idea clau:** L'enginyeria social no busca vulnerabilitats en el codi o en el maquinari, sinó en el factor humà. És la manipulació psicològica de les persones perquè realitzin accions compromeses o revelin informació confidencial.

### 1.1 El Factor Humà com a Vector d'Atac

En la seguretat informàtica actual, les eines de protecció tecnològiques (com firewalls, IDS/IPS o antivirus) són cada cop més robustes i difícils de superar directament. Per aquest motiu, els ciberdelinqüents prefereixen **atacar la línia de defensa més feble: l'usuari final**.

Un atac d'enginyeria social reeixit pot invalidar completament el sistema de seguretat millor configurat, ja que és el mateix usuari autoritzat qui entrega les seves credencials, desactiva proteccions o executa malware involuntàriament.

### 1.2 Principals Tècniques d'Enginyeria Social

#### A. Suplantació d'Identitat Digital

- **Phishing (Engany massiu):** Enviament de correus electrònics que simulen provenir de fonts fiables (bancs, plataformes de comerç electrònic, proveïdors de serveis o la mateixa empresa) per enganyar l'usuari i capturar les seves contrasenyes o dades bancàries.
- **Spear Phishing (Atac dirigit):** Variant personalitzada i altament elaborada adreçada a una persona o departament concret (per exemple, personal del departament de comptabilitat o recursos humans).
- **Whaling (Atac a alts càrrecs):** Atac de phishing dissenyat especialment per a executius de l'alta direcció (CEO, directors financers), on l'impacte potencial és elevadíssim.

#### B. Canals Alternatius de Suplantació

- **Smishing (SMS Phishing):** Utilització de missatges de text al mòbil amb enllaços maliciosos o peticions urgents d'acció.
- **Vishing (Voice Phishing):** Enginyeria social realitzada per via telefònica (veu), on l'atacant suplanta el suport tècnic, entitats bancàries o personal d'auditoria.

#### C. Tècniques Basades en la Contextualització i la Causalitat

- **Pretexting (Creació d'un pretext):** L'atacant elabora un escenari fictici o una història elaborada per guanyar-se la confiança de la víctima i fer que li faciliti accés a informació privilegiada o sistemes de l'organització.
- **Baiting (Momic / Ganxo):** Ús d'un esquer físic o digital atractiu. Un exemple clàssic és deixar una memòria USB infectada en un lloc públic (com l'aparcament o la recepció de l'empresa) amb una etiqueta cridanera (ex: `Nòmines_2026.xlsx`).

#### D. Tècniques d'Observació i Cerca de Residus

- **Shoulder Surfing (Mirada per sobre de l'espatlla):** Observació directa de les tecles o pantalles quan la víctima escriu contrasenyes, PINs o codis d'accés.
- **Dumpster Diving (Cerca a la brossa):** Recerca d'informació confidencial (llistes d'usuaris, manuals, contrasenyes anotades) en paper no destruït adequadament.

### 1.3 Impacte en Organitzacions i Empreses

- **Frau del CEO / Frau del Proveïdor:** Mitjançant la suplantació d'identitat d'un directiu o la interceptació de factures de proveïdors, els atacants aconsegueixen que els empleats realitzin transferències bancàries fraudulentes a comptes controlats pels cibercriminals.
- **Infecció per Ransomware:** Més del 80% dels atacs de ransomware s'inicien amb un correu de *phishing* on l'usuari descarrega un fitxer adjunt infectat o fa clic en un enllaç maliciós.
- **Exfiltració de Dades i Sancions Legals (RGPD / LOPDGDD):** El robatori d'informació corporativa o dades personals comporta greus pèrdues econòmiques, danys reputacionals irreparables i sancions administratives elevades.

### 1.4 Estratègies de Prevenció i Mitigació

1. **Formació i Conscienciació Contínua:** Realització de simulacres de *phishing* periòdics i formació en la identificació d'indicadors de sospita (remetents estranys, urgència injustificada, dominis similars però falsos).
2. **Autenticació Multifactor (MFA / 2FA):** Implementar sistemes on, tot i que el ciberdelinqüent aconsegueixi la contrasenya via *phishing*, necessiti un segon factor de verificació (aplicació d'autenticació o clau de seguretat física).
3. **Principi del Mínim Privilegi:** Garantir que cada usuari només tengui accés a la informació i recursos estrictament necessaris per a les seves funcions laborals.

## 2. Criteri d'Avaluació 4.2: Minimització del Trànsit de Correu Brossa i Publicitat

> **💡 Idea clau:** El correu brossa (spam) i la publicitat massiva no només són una molèstia per als usuaris, sinó que representen una amenaça directa per a la seguretat de la xarxa, el rendiment dels servidors i l'eficiència tecnològica de les organitzacions.

### 2.1 Conceptes de Spam, Adware i Malvertising

- **Spam (Correu brossa):** Missatges no sol·licitats enviats de forma massiva. Tot i que tradicionalment tenien caràcter comercial, en entorns corporatius s'utilitzen majoritàriament com a vehicle de transport per atacs (phishing, distribució de malware).
- **Adware i Publicitat Maliciosa (Malvertising):** Programari o anuncis web destinats a mostrar publicitat no desitjada. En molts casos, aquests anuncis incorporen scripts maliciosos que s'executen en el navegador sense que l'usuari hagi de fer-hi cap acció explícita.

### 2.2 Importància de la Minimització del Trànsit

| Àrea d'Impacte | Conseqüències de la No-Minimització |
| :--- | :--- |
| **Amplada de Banda** | Consum massiu del flux de xarxa per la recepció de gigabytes de dades inútils, saturant els enllaços d'accés a Internet. |
| **Servidors i Emmagatzematge** | Sobrecàrrega de CPU, memòria RAM i espai de disc en els servidors de correu (*Mail Transfer Agents - MTA*), que han de processar i emmagatzemar missatges brossa. |
| **Productivitat de l'Usuari** | Pèrdua de temps diari dedicat a revisar, filtrar i esborrar correus no desitjats o publicitat molestosa. |
| **Reducció de la Superfície d'Atac** | Com menys trànsit de publicitat/spam entri a la xarxa, menor serà la probabilitat que un usuari cliqui en un enllaç maliciós o descarregui un element infectat. |

### 2.3 Arquitectura de Protecció per Capes

```text
[ Internet ] 
     │
     ▼
[ Firewall / Filtre DNS (Pi-hole) ]  ───> Bloqueig d'ad servers i dominis maliciosos
     │
     ▼
[ Antispam Gateway (MTA / Cloud) ]   ───> Anàlisi IP, RBL, SPF/DKIM/DMARC, Heurística
     │
     ▼
[ Servidor de Correu Local / Cloud ] ───> Filtrat Bayesià i regles de la bústia
     │
     ▼
[ Client / Navegador Web ]           ───> AdBlockers (uBlock Origin), Antivirus Endpoint
```

#### A. Nivell de Servidor i Correu Electrònic (MTA)

- **Mecanismes d'Autenticació de Correu:**
  - **SPF (Sender Policy Framework):** Registre DNS que especifica quins servidors d'enviament tenen permís per enviar correus en nom d'un domini concret.
  - **DKIM (DomainKeys Identified Mail):** Afegeix una signatura digital a les capçaleres dels correus per verificar que el missatge no ha estat modificat en trànsit.
  - **DMARC (Domain-based Message Authentication, Reporting, and Conformance):** Defineix la política que ha d'aplicar el servidor de destinació si falla la verificació de SPF o DKIM (rebutjar, posar en quarantena o acceptar).
- **Filtres Antispam en Passarel·la (Gateways):** Solucions com *Apache SpamAssassin*, *Microsoft Defender for Office 365* o *Barracuda Spam Firewall* que analitzen la reputació IP i el contingut.

#### B. Nivell de Xarxa i Navegació Web

- **Filtrat DNS i DNS Sinkholes:** Bloqueig d'accés a dominis publicitaris i maliciosos abans que la petició surti de la xarxa local (resolució DNS a `0.0.0.0` o `127.0.0.1`, com fa *Pi-hole*).

- **Proxies i Next-Generation Firewalls (NGFW):** Inspecció de trànsit web (HTTP/HTTPS) i filtrat de continguts per categories, bloquejant xarxes de publicitat i servidors de distribució de malware.

#### C. Nivell de Client (Endpoint)

- **Bloquejadors d'Anuncis (AdBlockers):** Ús d'extensions com *uBlock Origin* als navegadors corporatius per prevenir l'execució de scripts de publicitat no desitjats.
- **Regles i Integració en Clients de Correu:** Configuració de regles automàtiques i filtres integrats en clients com *Mozilla Thunderbird* o *Microsoft Outlook*.

### 2.4 Tipus i Tècniques de Filtrat Antispam

#### 1. Filtrat Heurístic (Basat en Regles)

- **Funcionament:** Analitza l'estructura i el contingut del correu buscant un conjunt de regles predefinides. Cada regla violada o detectada suma o resta punts de sospita (*score*). Si la puntuació total supera un llindar establert (*threshold*), el correu es classifica com a spam.
- **Exemples de regles:**
  - Assumpte escrit integrament en majúscules (`+1.5 punts`).
  - Ús de paraules clau sospitoses com "VIAGRA", "CRÈDIT IMMEDIAT", "URGENT" (`+2.0 punts`).
  - El cos del missatge conté només una imatge sense text (`+2.5 punts`).
  - L'adreça IP del remetent té un registre PTR (DNS invers) vàlid (`-1.0 punts`).
- **Eina de referència:** *Apache SpamAssassin*.

> **Nota:** El filtrat heurístic pot generar falsos positius, especialment en correus legítims que contenen paraules o patrons similars a els de spam.

#### 2. Filtrat Bayesià (Estatístic / Aprenentatge Automàtic)

- **Funcionament:** Basat en el teorema matemàtic de Bayes, calcula la **probabilitat** que un missatge sigui spam segons la freqüència d'aparició de determinades paraules o caràcters en correus prèviament classificats.
- **Capacitat adaptativa (Entrenament):** No depèn de regles estàtiques escrites per un administrador. El filtre aprèn directament de les accions dels usuaris quan marquen un correu com a "Spam" o "No és spam" (*Ham*).
- **Avantatge:** S'adapta contínuament a les noves tècniques que utilitzen els *spammers*.

> 💡En aquest [repositori](https://github.com/carlesalonso/BayesianFilter) teniu un exemple molt bàsic de filtre bayesià ingenu (naive Bayesian filter) programat amb Python que analitza frases per classificar-les com spam o no.

#### 3. Filtrat per Llistes (IPs i Dominis)

- **Llistes Negres en Temps Real (RBL / DNSBL):** Consultes en temps real a bases de dades públiques mantingudes per empreses de seguretat. Si la IP del servidor que envia el correu està llistada per enviar spam anteriorment, el correu es rebutja directament durant la negociació SMTP.
- **Llistes Blanques (Whitelists):** Adreces IP, dominis o correus de confiança que s'eximeixen de passar pels filtres d'spam.
- **Llistes Grises (Greylisting):**
  - Quan un servidor desconegut intenta lliurar un correu, el filtre el rebutja temporalment amb un codi d'error `4xx` ("intenta-ho més tard").
  - Un servidor de correu legítim compleix el protocol SMTP i reintentarà l'enviament passats uns minuts (moment en què serà acceptat).
  - Els servidors d'spam massiu (*spambots*) solament fan un intent i no tornen a provar-ho per no malgastar recursos, quedant descartats.

#### 4. Filtrat per Signatura o Petjada Digital (Fingerprinting / Hashes)

- **Funcionament:** Genera un codi hash únic (una "petjada digital") del cos del correu entrant i el compara amb una xarxa global de servidors centralitzats.
- **Mecanisme:** Quan milers d'usuaris arreu del món reben exactament el mateix correu electrònic, el hash d'aquest missatge es registra a nivell mundial com a spam massiu.
- **Eines conegudes:** *Razor*, *Pyzor*, *DCC (Distributed Checksum Clearinghouse)*.

#### 5. Filtrat d'Autenticació de Domini (Anti-Spoofing)

- **Mètodes:** Ús coordinat de **SPF**, **DKIM** i **DMARC** per validar la legitimitat de la font.
- **Objectiu:** Evitar que un atacant suplanti la identitat d'un domini real. Si un correu diu provenir de `@banc.com` però la comprovació SPF/DKIM determina que la IP d'origen no està autoritzada per aquest domini, el correu es marca com a falsificació o *phishing*.

#### 6. Anàlisi d'Enllaços i Entorns d'Aïllament (Sandboxing)

- **Anàlisi d'URLs:** Inspecciona els enllaços inclosos en el cos del correu. Si apunten a servidors web amb mala reputació, acurtadors d'enllaços sospitosos o llocs de *phishing* coneguts, el missatge es bloqueja.
- **Sandboxing de fitxers adjunts:** Executa els fitxers adjunts (PDFs, executables, documents Office amb macros) en un entorn virtual aïllat (*sandbox*) per observar si realitzen accions malicioses abans de permetre que el fitxer arribi a l'usuari final.

### 2.5 Taula Comparativa de Tècniques

| Tècnica | On s'aplica? | Avantatge principal | Inconvenient principal |
| :--- | :--- | :--- | :--- |
| **Greylisting** | Nivell de connexió (MTA) | Estalvia molta CPU i l'amplada de banda | Introdueix un retard inicial en la recepció del correu |
| **Llistes Negres (RBL)** | Nivell de connexió (IP) | Molt ràpid i eficaç contra *spambots* coneguts | Risc de falsos positius si una IP legítima és llistada per error |
| **Heurística** | Contingut del correu | Molt flexible i altament configurable | Requeriment elevat de processament (CPU) |
| **Bayesià** | Contingut del correu | S'adapta automàticament a cada organització | Requereix un període d'entrenament inicial |
| **Sandboxing** | Fitxers adjunts / Enllaços | Detecta amenaces de dia zero (*Zero-Day*) | Augmenta el temps de lliurament i el cost d'infraestructura |

## 3. Resum de Bones Pràctiques per a Administradors de Sistemes

1. **Implementar el triple factor d'autenticació de correu (SPF + DKIM + DMARC)** en tots els dominis administrats de l'organització.
2. **Combinar protecció a la xarxa i a l'endpoint:** No confiar només en el navegador; aplicar filtrat a nivell de DNS/Firewall corporatiu.
3. **Mantenir regles i llistes actualitzades:** Configurar actualitzacions automàtiques de les regles d'SpamAssassin i de les llistes DNSBL.
4. **Fomentar la cultura de seguretat:** Recordar que cap eina tecnològica és 100% infallible si l'usuari desactiva proteccions o lliura voluntàriament credencials.
