# Enviaments massius utilitzant CiviMail

L'ús de la funcionalitat d'enviaments massius que ofereix CiviMail proporciona molts
avantatges respecte l'activitat Envia un correu electrònic, permetent-vos fer el seguiment de les respostes
al vostre mailing, procesar els retornats i permetre a la gent donar-se de baixa dels
vostres mailings. Es discutiran aquests beneficis més endavant; en primer lloc mirarem de
crear i enviar un correu electrònic.

## Selecció dels destinataris: Grups versus resultats de cerques

Hi ha dues maneres de seleccionar els destinataris per als vostres enviamensts massius: fer l'enviament a
grups existents o fer l'enviament a resultats de cerca. La majoria dels passos per crear un
mailing són independents de com s'escullen els destinataris, no obstant hi ha una
diferència important.

Pels mailings a resultats de cerques,
heu d'escollir un grup en el menú desplegable grup de cancel·lació de subscripció.
Aquí el perquè: Cada enviament massiu necessita un mètode per fer el seguiment de les peticions de cancel·lació de
subscripció. En molts països és necessari per llei tenir un procés de cancel·lació de subcripció senzill
i pot ajudar a prevenir que els vostres mailings siguin tractats com a correu brossa.
Els mailings enviats a grups tenen aquesta capacitat integrada. La propera vegada
que s'enviï un correu massiu a aquest grup, qualsevol que hagi cancel·lat la subscripció
no serà inclòs. Tanmateix, els mailings enviats a resultats de cerca no
tenen aquest mètode integrat per fer el seguiment de qui ha cancel·lat la subscripció, de manera que necessiteu
proporcionar-ne un.

Així és com funciona: si un contacte que coincideix amb els vostres resultats de cerca
té la subscripció cancelada al grup de cancel·lació de subscripció que designeu,
no s'enviarà el mailing a aquest contacte. Si un contacte cancela la subscripció via
l'enllaç de cancel·lació de subscripció d'aquest mailing, se li cancel·larà la subscripció a
aquest grup i per tant no rebrà cap més correu electrònic a aquest grup.
Això és així tant si ja era un membre del grup com si no.

El grup de cancel·lació de subscripcions que hagueu designat recull només la informació de cancel·lació de
subscripcions; no afegeix cap contacte al mailing. En altres paraules,
els contactes que es troben en el grup de cancel·lació de subscripcions però no coincideixen amb el vostre
criteri de cerca no s'inclouran en el mailing. (Si voleu
incloure aquests contactes heu d'incloure el grup en qüestió.)

Per exemple: La vostra organització té un gran esdeveniment la propera setmana. Ja s'han
enviat diversos correus electrònics sobre aquest, però heu afegit força gent
nova a la base de dades en la darrera setmana i els hi voleu enviar un
anunci de l'esdeveniment. Feu una cerca pels nous contactes via **Cerca >
Cerca personalitzada > Data d'addició a CiviCRM**. Aquest és la cerca que és
la base del mailing. La vostra organització emmagatzema la llista de correus electrònics de l'esdeveniment en un
grup anomenat Alertes d'esdeveniments, per la qual cosa per aquest mailing, probablement voldreu
escollir-lo com el grup de cancel·lació de subscripcions.

Si encara no teniu un grup que sigui apropiat pel
grup de cancel·lació de subscripcions per al mailing que esteu planificant, potser voldreu crear-ne
un i anomenar-lo quelcom similar a miscel·lània de cancel·lació de subscripcions de correu electrònic. Després
podreu afegir aquest grup a altres mailings futurs per assegurar-vos que la
gent que ha cancel·lat la subscripció és exclosa d'aquests mailings futurs.

## Les pantalles de configuració del mailing

Si esteu enviant el correu electròǹic a un grup, aneu a **Mailings > Mailing
nou**. Veureu la següent pantalla.

![Bulk email based on existing groups](/img/email-compose-mailing.png)

Si esteu basant el mailing en resultats de cerca, realitzeu la cerca
(per exemple, utilitzant **Cerca > Cerca avançada**) i després escolliu
**Correu electrònic - Programa/Envia via CiviMail** des de el desplegable d'**Accions**.
Veureu la següent pantalla.

![Bulk email based on search results](/img/email-compose-search-based-mailing.png)


Aquestes dues pantalles són forces similars, no obtstant això, com s'ha descrit a
[Selecció dels destinataris: Grups versus resultats de cerques](#Selecció dels destinataris: Grups versus resultats de cerques),
pels mailings basats en resultats de cerca heu d'escollir un grup de cancel·lació de subscripcions i
el grup de "Resultats de cerca" serà  inclòs (i no podrà ser eliminat d'ell) al llistat de destinataris. (A més, el panell
HTML s'obre per defecte. S'ha tancat per ajustar els butons inferiors en aquestes imatges.)

Recordeu que poeu desar el mailing en qualsevol estat clican al
botó **Desa l'esborrany**.

**Pas 1: Definició del mailing**

### Pestanya del mailing
Aquí trobareu:

**Nom del mailing**: Introduïu un nom per aquest correu electrònic. Seleccioneu un nom
que us permeti a vostè i a d'altres de la vostra organització identificar clarament
el propòsit d'aquest mailing. Es recomana que comenceu cada nom
amb la data (p.ex., "2015/04/25 - Buttletí mensual"). Això us permetrà
incloure o excloure més fàcilment els destinataris d'aquest correu electrònic en futurs
mailings. Aquest nom és només per ús internt i no es mostrarà als
destinataris. Més tard se us demanarà d'introduir l'assumpte del correu electrònic.

**Campanya**: Podeu associar aquest correu a una campanya en particular.

**Plantilla**: Aquí podeu seleccionar una plantilla de missatge existent per
omplir els camps de format HTML i format de text pla amb contingut
del missatges de la plantilla. Podeu editar el contingut per adaptar aquest mailing
en particular però no podeu actualitzar la plantilla o crear-ne una de nova mitjançant aquest
formulari. (El CiviCRM ve amb tres plantilles de butlletins d'exemple les quals els usuaris amb
  permissos d'administració de CiviCRM poden personalitzar junt amb els detalls de la vostra pròpia
  organització a **Administra > CiviMail > Plantilles de missatges**. Aquest és també el lloc on
  es poden crear les noves plantilles de missatges.)

**Remitent**: Aquest s'omplirà amb el valor per defecte de l'adreça remitent de correu electrònic.
Podeu escollir una alternativa er aquest mailing de la llista desplegable.
Els usuaris amb permissos d'administració de CiviCRM poden afegir adreces de correu electrònic addicionals
anant a **Administra > CiviMail > Adreces de correu electrònic de remitent**.

**Destinataris**: Aquí és on podeu escollir qui rebrà el
mailing (si és un mailing de grups) o refinar o afegir els destinataris del
correu electrònic (si és un mailing de resultats de cerca). Podeu escollir grups per

  El número final estimat de destinataris es mostra a la dreta del
camp "Destinataris" ressaltat en groc.

**La "clau"**: Està situada a la dreta del camp
"Destinataris" i a l'esquerra del número estimat de destinataris. Cliqueu-hi
per accedir a les **Opcions d'edició**.

![Civimail Recipients Edit Options](/img/civimail-recipients-edit-options.png)

  -   **Desduplica per correu electrònic:** El CiviCRM sempre desduplicarà el mailing basant-se en
     registres de contactes únics. Per exemple, si un contacte es troba en tres dels
      grups l'estareu incloent el el mailing i només se li enviarà una copia
      del correu electrònic. Tanmateix, si s'utilitza la mateixa adreça de correu electrònic per múltiples
      contactes, el nombre de correus electrònics que seran enviats ve determinat per aquesta casella. Si es
      desmarca llavors s'enviaran múltiples copies d'aquest correu electrònic - un per
      a cada contacte que estigui utilitzant aquesta adreça. Si està marcat només
      s'enviarà un correu electrònic per a cada adreça. Podeu definir el valor per defecte d'aquesta casella a
      **Administra > CiviMail > Configuració del component CiviMail** marcant
      o desmarcant "CiviMail desdupllica adreces de correu electrònic per defecte" però podeu
      sobreescriure aquest valor per defecte per qualsevol correu electrònic si ho necessiteu..

  -   **Tipus d'ubicació:** Per defecte els correus electrònic creats mitjançant CiviMail s'envien a
     les ubicacions d'adreces definides com "Enviaments massius" o, si no hi ha cap tipus d'ubicació
      amb aquesta configuració, a l'ubicació d'adreça definida com a "Principal". Podeu modificar
      el tipus d'ubicació i el mètode de
      selecció en la pantalla d'edició d'opcions.
     Podeu filtrar pel tipus d'ubicació i només enviar el mailing a les adreces
     de correu electrònic amb el tipus d'ubicació especificat o excloure les adreces
     de correu electrònic amb el tipus d'ubicació especificad.

**Grup de cancel·lació de subscripcions** (només pels mailings basats en cerques): S'ha
d'escollir amb cura. Pot ajudar llegir l'exemple del mailing basat en una
cerca de [Selecció dels destinataris: Grups versus resultats de cerques](#Selecció dels destinataris: Grups versus resultats de cerques).

**Assumpte**: és l'assumpte dels correus electrònics enviats. Podeu incloure-hi
[tokens](/common-workflows/tokens-and-mail-merge.md).
L'**Assumpte** (no el nom del mailing) s'utiltza quan es crea una
activitat o registre de mailing per a cada contacte.

**HTML** (secció expandible): Aquí és on podeu composar el contingut
del mailing. Recordeu que el CiviCRM us permet personalitzar cada correu electrònic utilitzant
[tokens](/common-workflows/tokens-and-mail-merge.md). Si només
voleu enviar un correu electrònic de text pla ignoreu la secció HTML. Cliqueu sobre
**Text pla** per obrir l'acordió i introduir el missatge en la capsa.

**Previsualització**: Aquest panell és el peu de pàgina a la pantalla de definició del mailing. Es
mostra a qualsevol pestanya que sigui seleccionada. Dins d'aquest panell hi ha les opcions per:
  -  Previsaulitzar les versions d'HTML o de text pla del correu electrònic. La previsualització HTML us mostrarà tota la informació formatada i amb els tokens convertits. No inclourà cap dels adjunts. No hi ha cap garantia que tots els clients de correu electrònic
      mostraran el correu electrònic exactament com es mostra en aquesta previsualització, però és
      util per comprovar coses com la consistència de les fonts, el disseny bàsic i el
      color.

  -  Enviar una prova de correu electrònic a una adreça de correu electrònic simple. Si l'adreça de correu electrònic encara no existeix al CiviCRM es crearà un nou registre de contacte.

  -  Enviar una prova de correu electrònic a un grup existent al CiviCRM.

      La prova del mailing s'omplirà amb tots els tokens i inclourà qualsevol dels adjunts que esteu planificant d'enviar.

     És una bona idea de provar el correu electrònic enviant-se'l a un mateix i
  visualitzant-lo en el vostre client de correu electrònic per assegurar que es visualitza com espereu.
  Si esteu enviant un correu electrònic amb un disseny cocomplex, envieu-lo al vostre
  grup de prova i verifiqueu-ho des de varis clients de correu electrònic (vegeu *Proves en
  plantilles* en la secció de configuració per a més consells sobre això). És
  preferible tenir més d'una personar ebent el vostre correu electrònic de prova i
  us aporti comentaris.

La pestanya **Mailing** pot ser l'única pestanya que necessiteu visitar quan esteu creant
el mailing. Conté tots els camps obligatoris que es necessiten definir per a
cada mailing nou. Les pestanyes restants són:

### Pestanya d'adjunts
Aquí és on podreu pujar fitxers per enviar com adjunts amb el correu electrònic.

### Pestanya de capçalera i peu
Cada mailining nou que creeu inclourà
  l'encapçalament i el peu per defecte tal com estan definits a
  **Mailings > Capçaleres, peus i missatges automatitzats**. Si no voleu
  utilitzar aquestes opcions per defecte, en aquesta pestanya podreu seleccionar la capçalera i/o
  el peu que vulgueu utilitzar per aquest mailing. Podeu definir capçaleres i peus
addicionals a través de **Mailings > Capçaleres, peus i missatges
automatitzats** (Vegeu *Configuració* per més detalls).

### Pestanya de publicació
Aquesta conté el camp de **Visibilitat del mailing**
que té dues opcions, "Només l'usuari i l'usuari administrador" i "Pàgines públiques."
Si escolliu **Pàgines públiques** fareu que
el contingut sigui visible com una pàgina web per qualsevol que tingui els permissos
"Visualitza contingut públic de CiviMail."
**"Només l'usuari i l'usuari administrador"** significa que només els usuaris que reben el mailing
o els adminstradors poden visualitzar el contingut d'aquest correu electrònic com una pàgina web;
els destinataris hauran d'iniciar sessió per tal de visualitzar el missatge.

 Per enllaçar a la versió web del correu electrònic, necessitareu tenir inserit
 el token de l'**Enllaç permanent** en el missatge del correu electrònic. Aquest token genera
una URL on es podrà visualitzar el missatge; per tal de mostrar-lo
en els missatges HTML, necessitareu afegir les etiquetes d'enllaç adequades utilitzant
l'icona d'editor de codi.

### Pestanya de respostes
-  Casella de **Seguiment de respostes**. Marcant aquesta opció s'enviaran respostes des dels
  mailings dels destinataris a una adreça específica del CiviMail en comptes de les adreces dels
  remitents de tal manera que podran emmagatzemar-se dins del CiviCRM. Marcant aquesta casella s'obriran les
  dues opcions descrites a continuació.
    -   **Reenviament de respostes:** Aquesta opció és només visible si el "Seguiment de respostes"
        està marcat. Necessitareu marcar aquesta opció si voleu que les adreces del
          remitent rebin també les respostes enviades als remitents.
    -   **Resposta automàtica a les respostes:** Aquesta opció us permet enviar una
        resposta automàtica especifica a qualsevol que respongui al vostre mailing. Necessiteu
          configurar una resposta automàtica a **Mailings >>
          Capçaleres, peus i missatges automatitzats**.

- **Missatge de baixa:** Aquest missatge s'enviarà al destinatari que es
  doni de baixa de totes les llistes de mailing
- **Missatge de resubscripció:** Aquest missatge s'enviarà al destinatari que es
  torni a subscriure a una de les llistes de mailing
- **Missatge de cancel·lació de subscripció:** Aquest missatge s'enviarà al destinatari que
  cancel·li la subscripció d'alguna de les llistes de mailing.

    Podeu editar aquests tres missatges a **Mailings >> Capçaleres, peus i missatges automatitzats**.

### Pestanya de seguiment
-  **Seguiment de clics registrats**: Aquesta opció farà el seguiment de quants i
    quins usuaris han clicat a tots els enllaços del missatge. Això
    s'aconsegueix redireccionant tots els enllaços cap al vostre servidor. Això
    significa que tots els enllaços seran sobreescrits amb enllaços personalitzats
    que contindran el vostre nom de domini.

    !!! nota "Nota per correus electrònics HTML"
        Alguns filtres de pesca de credencials poden marcar els enllaços que es mostrin
        diferents en el codi HTML i en el text com a insegurs. Per aquest motiu és
        millor no utilitzar quelcom similar a  
        `<a href="http://google.com">http://Google.com</a>`
        i utilitzar en el seu lloc 
        ` <a href="http://google.com">cliqueu aquí per anar a Google</a>`.

    !!! nota "Nota per correus electrònics en text pla"
        Si utilitzeu URL amigables curtes, seran totes sobreescrites
        per enllaços llargs que contindran el nom del vostre lloc i un codi llarg
        similar a
        http://yoursite.com/sites/all/modules/civicrm/extern/url.php?u=529&qid=29011.

-   **Seguiment d'obertures:** Aquesta opció us permet fer el seguiment de quanta gent
    ha obert el correu electrònic que heu enviat. Tanmateix, hi ha limitacions en
    l'efectivitat d'aquest mètode. Si el destinatari no permet mostrar imatges
    en el seu client de correu electrònic (sovint anomenat com "bloquejar el contingut
    remot"), el seu correu electrònic no es marcarà com a obert encara que
    l'hagi obert. Bloquejar el contingut remot és una pràctica molt comuna.

Un cop hagueu definit tots els aspectes del vostre mailing cliqueu a **Continua >**
(a baix a l'esquerra) per avançar al:

**Pas 2: Revisa i programa**

![CiviMail Review and Schedule screen](/img/civimail-review-and-scheduling.png)

### Panell de revisió

Aquest és el resum de tots els detalls del vostre correu electrònic. Les paraules en blau són
en realitat botons. Si cliqueu a **~XX destinataris** se us mostrarà
els noms dels contactes i les seves adreces de correu electrònic a les que fareu l'enviament. Si feu clic
a **HTML** o a **Text pla** se us mostrarà el correu electrònic que s'enviarà incloent
qualsevol capçalera i/o peu. Si feu clic en qualsevol dels sobres se us mostrarà
el missatge en qüestió. Les marques i les creus tatxades us mostren el que
heu i no heu escollit de fer en termes de seguiment i tractament de
respostes del correu electrònic. En altre paraules, **Revisió** és un petit panell brillant
que us permet confirmar que heu efectuat totes les eleccions correctes tot i la
multitud d'interrupcions que heu experimentat mentre definieu el mailing.

### Programació

 Podeu optar per enviar el correu electrònic immediatament o programar una data i
 hora per ser enviat. Finalment cliqueu a **Envia el Mailing**. Per defecte,
 el CiviMail comprova cada 15 minuts si hi ha cap correu electrònic a punt per enviar,
 pel que l'inici de l'enviament pot endarrerir-se fins a 15 minuts.

 Els mailings que s'envien a un gran nombre de destinataris s'envien en lots
del voltant de 400 per reduir la probabilitat de que els correus electrònics siguin capturats pels filtres de correu brossa.
Per tant, l'enviament actual del vostre enviament massiu de correus electrònics pot trigar varies hores
en funció de la configuració del vostre servidor.


## Seguiment d'enviaments massius enviats

Per revisar les estadístiques clau sobre els mailings enviats en el passat, aneu a
**Mailings > Mailings programats i enviats**. Un cop hagueu trobat el
mailing en el llistat o l'hagueu cercat utilitzat els filtres de sobre,
cliqueu **Informe** en la columna "acció". Això mostrarà la informació
bàsica en totes es accions de seguiment, incloent el número
d'obertures, els clics registrats d'enllaços o el percentatge de retornats (vegeu la "Gestió de 
retornats" a sota).

![](/img/CiviCRM_mailing_basicstatistics_1.png)

Per ampliar aquesta informació, cliqueu el nom d'una de les estadístiques
per mostrar un llistat dels contactes als quals s'aplica i altres detalls
diversos com ara l'hora en que el correu electrònic va ser obert (seguiment d'obertures). Quan s'ha
enviat l'enviament massiu del correu electrònic a un contacte, també podeu visualitzar el registre "Email massiu"
del mailing en la pestanya d'activitats del seu perfil.

Ara és possible que vulgueu filtrar aquesta informació més a fons. Per exemple, de
tots els destinataris que hagin obert l'enviament massiu del correu elecrònic, potser voldreu fixar-vos
només en els que estiguin en edats compreses entre els 21 i 30 anys o els inscrits
per un esdeveniment determinat. Cliqueu "Cerca avançada" al costat de l'estadística per començar
una cerca avançada amb els atributs del correu electrònic pre-emplenats; p.ex. si es clica
l'enllaç a continuació dels "Seguiment d'obertures", els camps de cerca s'establiran
per cercar tots els contactes que hagin obert el correu electrònic, a punt perquè afegiu
criteris extres. Per més informació sobre cerques avançades, vegeu
"Cerques".

![](/img/CiviCRM_mailing_advancedsearch.png)

## Gestió d'enviaments massius

Els enviaments massius es poden trobar en una de les tres àrees accessibles a través del
menú de **Mailings**:

**Mailings esborranys i no programats**: Tan aviat com poseu nom al vostre missatge
 en el pas 1 i cliqueu a continua, es situa en aquesta àrea. Si cliqueu
 **Desa i continua més endavant** o simplement abandoneu un missatge després d'alguns
 passos, podeu continuar treballant en ell clicant en
 l'enllaç **Continua** al costat del missatge llistat que apareix aquí.

!!! nota
    Els mailings basats en resultats de cerca no tindran llistat l'enllaç
    continua

 També podeu **Eliminar** missatges esborranys aquí.

**Mailings programats i enviats:** Quan envieu o programeu un mailing,
 s'ubicarà en aquesta àrea i romandrà aqueí fins que sigui arxivat
 o eliminat.

 Podeu fer el seguiment de l'èxit de l'entrega fent clic a l'enllaç de l'**Informe**
 al costat del missatge.

 Podeu començar també un altre mailing basat en un mailing anterior
 fent clic a l'enllaç **Reutilitza**. (Noteu, que l'enllaç reutilitza no està
 disponible per mailings basats en resultats de cerca.)

 Els enllaços **Arxiva** i **Elimina** són accessibles des de
 l'enllaç **més**. Per als mailings que han estat programats però encara no enviats,
 hi ha un ellaç **Cancel·la** disponible en comptes del **Arxiva**.

**Mailings arxivats:** Aquesta àrea llista tots el missatges que han estat
 arxivats des de l'àrea de mailings programats i enviats. Els mailings llistats
 aquí no estan disponibles per ser inclosos o exclosos del llistat de
 destinataris.

 Proporciona exactament la mateixa funcionalitat que Programa i envia
 mailings, inclosa la possibilitat de veure informes i reutilitzar-los.
