# NF5AA1-Enginyeria Social i Phishing

## Taula de Continguts

1. [Enginyeria Social, Fraus i Robatori d'Informació](#enginyeria-social-fraus-i-robatori-dinformació)
   - [1.1 El Factor Humà com a Vector d'Atac](#11-el-factor-humà-com-a-vector-datac)
   - [1.2 Principals Tècniques d'Enginyeria Social](#12-principals-tècniques-denginyeria-social)
   - [1.3 Impacte en Organitzacions i Empreses](#13-impacte-en-organitzacions-i-empreses)
   - [1.4 Estratègies de Prevenció i Mitigació](#14-estratègies-de-prevenció-i-mitigació)

---

## Enginyeria Social, Fraus i Robatori d'Informació

> **💡 Idea clau:** L'enginyeria social no busca vulnerabilitats en el codi o en el maquinari, sinó en el factor humà. És la manipulació psicològica de les persones perquè realitzin accions compromeses o revelin informació confidencial.

### 1.1 El Factor Humà com a Vector d'Atac

En la seguretat informàtica actual, les eines de protecció tecnològiques (com firewalls, IDS/IPS o antivirus) són cada cop més robustes i difícils de superar directament. Per aquest motiu, els ciberdelinqüents prefereixen **atacar la línia de defensa més feble: l'usuari final**.

Un atac d'enginyeria social reeixit pot invalidar completament el sistema de seguretat millor configurat, ja que és el mateix usuari autoritzat qui entrega les seves credencials, desactiva proteccions o executa malware involuntàriament.

### 1.2 Principals Tècniques d'Enginyeria Social

#### A. Suplantació d'Identitat Digital

- **Phishing (Engany massiu):** Enviament de correus electrònics que simulen provenir de fonts fiables (bancs, plataformes de comerç electrònic, proveïdors de serveis o la mateixa empresa) per enganyar l'usuari i capturar les seves contrasenyes o dades bancàries.

     ![Exemple de correu de phishing](./media/correo_phishing-sabadell.png)

- **Spear Phishing (Atac dirigit):** Variant personalitzada i altament elaborada adreçada a una persona o departament concret (per exemple, personal del departament de comptabilitat o recursos humans). La diferència principal amb el phishing massiu és que el spear phishing utilitza informació específica de la víctima (com el seu nom, càrrec o projectes en què està involucrat) per fer l'atac més convincent.

- **Whaling (Atac a alts càrrecs):** Atac de phishing dissenyat especialment per a executius de l'alta direcció (CEO, directors financers), on l'impacte potencial és elevadíssim. És una variant del spear phishing, però amb un enfocament en la jerarquia corporativa i amb missatges que poden incloure informació confidencial de l'empresa.

#### B. Canals Alternatius de Suplantació

- **Smishing (SMS Phishing):** Utilització de missatges de text al mòbil amb enllaços maliciosos o peticions urgents d'acció. Com és senzill falsificar la capçalera del remitent, el SMS fraudulent pot semblar legítim i fins i tot, aparèixer a un fil de missatges legítim.

     ![smishing DGT](./media/dgt_sms2.png)

- **Vishing (Voice Phishing):** Enginyeria social realitzada per via telefònica (veu), on l'atacant suplanta el suport tècnic, entitats bancàries o personal d'auditoria.

> ❗**Nota:** Amb els avanços que ha tingut la intel·ligència artificial, els atacants poden generar missatges de veu i fins i tot videoconferències falses amb gran realisme, fent que la suplantació sigui encara més creïble. S'està utilitzant amb èxit [4](https://kymatio.com/es/blog/vishing-deepfake-voice-fraude-ceo)

#### C. Tècniques Basades en la Contextualització i la Causalitat

- **Pretexting (Creació d'un pretext):** L'atacant elabora un escenari fictici o una història elaborada per guanyar-se la confiança de la víctima i fer que li faciliti accés a informació privilegiada o sistemes de l'organització: per exemple, fer-se passar per un tècnic de TI que necessita accedir a un servidor per solucionar un problema urgent.

- **Baiting (Ganxo):** Ús d'un esquer físic o digital atractiu. Un exemple clàssic és deixar una memòria USB infectada en un lloc públic (com l'aparcament o la recepció de l'empresa) amb una etiqueta cridanera (ex: `Nòmines_2026.xlsx`).

#### D. Tècniques d'Observació i Cerca de Residus

- **Shoulder Surfing (Mirada per sobre de l'espatlla):** Observació directa de les tecles o pantalles quan la víctima escriu contrasenyes, PINs o codis d'accés.

- **Dumpster Diving (Cerca a la brossa):** Recerca d'informació confidencial (llistes d'usuaris, manuals, contrasenyes anotades) en paper no destruït adequadament.

> 💡**Nota**: Kevin Mitnick va ser un dels hackers més famosos de la dècada dels 90 del segle XX. Era un expert en aconseguir accés mitjançant tècniques d'enginyeria social, entre elles la cerca d'informació a partir de la brossa de les empreses i organitzacions. Va ser detingut i després de passar uns anys a pressó, va treballar com expert en seguretat i va escriure un dels llibres clàssics del món hacker "The art of deception" on explica diverses tècniques d'enginyeria social.

### 1.3 Impacte en Organitzacions i Empreses

- **Frau del CEO / Frau del Proveïdor:** Mitjançant la suplantació d'identitat d'un directiu o la interceptació de factures de proveïdors, els atacants aconsegueixen que els empleats realitzin transferències bancàries fraudulentes a comptes controlats pels cibercriminals.

- **Infecció per Ransomware:** Més del 80% dels atacs de ransomware s'inicien amb un correu de *phishing* on l'usuari descarrega un fitxer adjunt infectat o fa clic en un enllaç maliciós.

- **Exfiltració de Dades i Sancions Legals (RGPD / LOPDGDD):** El robatori d'informació corporativa o dades personals comporta greus pèrdues econòmiques, danys reputacionals irreparables i sancions administratives elevades si no es comuniquen correctament i si no s'han pres mesures de seguretat adequades.

### 1.4 Estratègies de Prevenció i Mitigació

1. **Formació i Conscienciació Contínua:** Realització de simulacres de *phishing* periòdics i formació en la identificació d'indicadors de sospita (remetents estranys, urgència injustificada, dominis similars però falsos).

2. **Autenticació Multifactor (MFA / 2FA):** Implementar sistemes on, tot i que el ciberdelinqüent aconsegueixi la contrasenya via *phishing*, necessiti un segon factor de verificació (aplicació d'autenticació o clau de seguretat física).

3. **Principi del Mínim Privilegi:** Garantir que cada usuari només tengui accés a la informació i recursos estrictament necessaris per a les seves funcions laborals.

4. **Polítiques de Seguretat i Procediments de Resposta:** Establir protocols clars per a la gestió d'incidents, incloent la notificació immediata de possibles atacs i la desconnexió de sistemes compromesos.

## Enllaços d'Interès

1. [ESET-Phising](https://www.eset.com/es/caracteristicas/phishing/)

2. [INCIBE. Fraude del CEO: el engaño que puede vaciar la cuenta de tu pyme](https://www.incibe.es/empresas/blog/fraude-del-ceo-el-engano-que-puede-vaciar-la-cuenta-de-tu-pyme)

3. [Trend Micro. ¿Cuáles son los diferentes tipos de ataques de phishing?](https://www.trendmicro.com/es_es/what-is/phishing/types-of-phishing.html)

4. [Kymatio. Vishing & Deepfake Voice: La Guía Definitiva para Proteger a su Empresa del Fraude de Voz](https://kymatio.com/es/blog/vishing-deepfake-voice-fraude-ceo)

5. [BBC World Service. Can BBC reporter's AI clone fool his colleagues?. YouTube](https://youtu.be/lH608DfrAxU?si=ZKtUDBXFgj2LBODT)

6. [Kevin Mitnick. El arte del engaño: Controlando el elemento humano de la seguridad](https://elhacker.info/manuales/Hacking%20y%20Seguridad%20informatica/El_Arte_del_Engan%CC%83o.pdf)

7. [hackmetrix. Test de phising](https://test-phishing.hackmetrix.com)
