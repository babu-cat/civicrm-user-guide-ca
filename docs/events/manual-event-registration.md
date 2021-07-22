# Inscripció manual a esdeveniments

Aquest capítol tracta com l'equip de l'organització pot inscriure a la gent als esdeveniments
a través de la interfície d'administració. Veureu com inscriure a una persona
participant manualment, com inscriure a múltiples participants i com
importar inscripcions des d'un origen extern.

## Inscripció manual d'un participant

Encara que el CiviCRM es pot configurar per permetre als teus constituent inscriure's
i pagar als esdeveniments directament a través del lloc web,
també proporciona l'opció d'inscriure els contactes manualment. Útil, per
exemple, si es vol inscriure a la gent per telèfon o correu electrònic, o si voleu
inscriure a la gent en el seu nom.

Per exemple, quan una persona truca a l'oficina per inscriure's en un esdeveniment,
la persona de l'equip que respon la trucada pot:

1.  Introduir el nom de la persona en el quadre de cerca ràpida.
2.  Seleccionar el contacte dels resultats.
3.  Clicar la pestanya d'esdeveniments a la fitxa del contacte que fa la trucada.
4.  Afegir a la persona a l'esdeveniment.

La pestanya d'esdeveniments de la fitxa del contacte de la captura de pantalla de sota,
mostra una llista del resum de reserves actuals i passades del contacte i
proporciona enllaços per inscriure el contacte a un nou esdeveniment.

![captura de pantalla](../img/EventsTab.png)

Hi ha dues opcions per a inscriure un contacte:

-   **Afegeix una inscripció a un esdeveniment**: per gent que vol pagar en un altre moment, com ara
    enviant un xec o pagant al mateix dia de l'esdeveniment.
-   **Registrant una inscripció a un esdeveniment amb targeta de crèdit**: per gent que paga
    immediatament amb una targeta de crèdit. Aquesta opció està disponible només si
    s'ha configurat un processador de pagaments que permet el pagament directe
    a través del lloc web. Si esteu atenent una inscripció al
    telèfon podeu preguntar per la informació de la seva targeta de crèdit i introduir-la
    manualment.

La interfície per a les dues opcions és molt similar, amb l'excepció
d'aquells camps que registren els detalls del pagament.

![captura de pantalla](../img/EventRegistration1.png)

![captura de pantalla](../img/EventRegistration2.png)

Mentre feu servir aquest formulari algunes seccions de la pàgina canvien per
reflectir les eleccions que feu. Per exemple, quan es selecciona l'esdeveniment i
el rol del participant, el
formulari carregarà automàticament els camps personalitzats predefinits que pertanyen
a aquestes seleccions.

Si l'esdeveniment seleccionat és un esdeveniment de pagament, podreu veure una secció de tarifes d'esdeveniment
que s'haurà definit en els detalls de configuració de l'esdeveniment, i
una opció per registrar els detalls de la transacció financera (Registra un pagament)
serà visible. Això ens condueix a un concepte important i central del
CiviEvent (això com d'altre mòdul): els registres d'inscripcions en el
CiviCRM són independent de, però poden relacionar-se amb, una transacció
financera. Mentre això pot semblar confús per organitzacions acostumades
a veure les inscripcions a esdeveniments com essencialment una transacció financera,
ofereix una distinció important i valuosa.

Una inscripció a un esdeveniment comunica la participació del contacte a un
esdeveniment de l'organització. La corresponent transacció financera indica
el valor monetari associat amb aquesta participació. Tot i que relacionats,
ambdós són diferents.

La distinció s'entén millor si es considera el comú escenari
d'una organització renunciant a les quotes per als vips, un conferenciant, o algú que
participa en un esdeveniment d'una manera limitada. En aquests casos, voldreu
inscriure les persones però voldreu no crear una transacció
financera associada. El CiviCRM respecta aquesta distinció registrant
la inscripció de l'esdeveniment sota la pestanya Esdeveniments, registrant el
registre financer sota la pestanya Contribucions, i seguidament enllaçant
els dos registres.

Si l'esdeveniment és un esdeveniment amb pagament, cliqueu la casella **Registra el pagament** i
introduïu informació en la secció d'Informació del pagament. Aquest
procés essencialment enllaça mútuament la inscripció a l'esdeveniment i el
registre de contribució per aquest contacte. Un cop registrada la inscripció,
tindreu la possibilitat de visualitzar la inscripció a l'esdeveniment i veure la
el registre de la contribució relacionada al final (veieu la captura de pantalla). Si
no seleccioneu la casella de Registra un pagament, només es crearà un registre
de la inscripció.

![captura de pantalla](../img/EventContributionTab.png)

### Inscripció d'un participant que paga només un dipòsit (pagament parcial)

Si esteu inscrivint un participant manualment, podeu introduir un pagament
d'import inferior al de la tarifa de l'esdeveniment, per més endavant fer un o més pagaments
addicionals fins que la tarifa sigui pagada al complet.

Durant la inscripció manual haureu d'introduir l'import
pagat en aquest moment en el camp **Import** en la secció Informació
del pagament i definir el camp **Estat del participant** a parcialment pagat.

![captura de pantalla](../img/EventIntialPartialPayment.png)

L'esperat és que es facin pagaments addicionals fins
que la tarifa de l'esdeveniment no es pagui per complet, per això la inscripció **Parcialment pagada**
s'inclou en el total de participants de la mateixa manera que una inscripció **Pendent de
pagament diferit**.

Per realitzar un pagament addicional en aquesta inscripció:

1.  Aneu a la fitxa del contacte inscrit.
2.  Cliqueu a la pestanya d'**Esdeveniments** en aquest contacte.
3.  Cliqueu a **més** a la dreta de tot del registre de l'esdeveniment parcialment
    pagat.
4.  Seleccioneu **Registra un pagament** o **Registrant un pagament amb targeta
    de crèdit**

![captura de pantalla](../img/EventPartialPayment.png)

![captura de pantalla](../img/EventPartialPaymentCC.png)

Podeu fer més d'un pagament addicional. Quan la tarifa de l'esdeveniment sigui
pagada en la seva totalitat l'**Estat del participant** canviarà automàticament a
**Inscrit** (tot i que podeu sobreescriure'l escollint una opció d'estat
diferent quan realitzeu el darrer pagament) i l'estat de la
contribució enllaçada canviarà automàticament a **Completada**.

Veient això des d'una perspectiva comptable, quan la inscripció es
crea, la tarifa de l'esdeveniment s'afegeix a els comptes a cobrar. Cada pagament
parcial s'anirà afegint com una partida individual separada fins que la tarifa sigui pagada en
la seva totalitat.

Fixeu-vos que en la inscripció a l'esdeveniment i en la contribució enllaçada
l'import mostrat serà sempre la tarifa sencera de l'esdeveniment. Podreu veure com quant
queda a deure escollint a **Visualitza** de la inscripció de l'esdeveniment. Seleccionant **›› visualitza els pagament** (sota de l'import **Total Pagat**) es mostrarà un
resum de cada pagament.

![captura de pantalla](../img/EventPaymentView.png)

Una altra opció és veure els pagaments clicant la fletxa al costat del registre de contribució al final.

![captura de pantalla](../img/EventPaymentView2.png)

## Inscripcions en bloc

El CiviEvent ofereix una funcionalitat que permet estalviar temps registrant múltiples
contactes per un esdeveniment a la vegada. Tornant a
l'escenari del taller de lideratge juvenil, Arts en Acció preveu una alta
taxa d'assistència de participants del taller anterior. L'equip
fa una cerca per cercar els participants anteriors i els inscriu en bloc,
definint cada estat de participant a **Pendent**. La llista de
contactes pendent després s'utilitza per trucar-los o enviar-ls-hi un correu electrònic per veure si finalment
vindran. Si la persona diu que assistirà, l'organitzador de l'esdeveniment pot
canviar l'estat de la persona de **Pendent** a **Inscrit**.

### Passos per a la inscripció en bloc:

1.  Cerqueu el conjunt de contactes que us interessin (per Arts en Acció
    caldria navegar a **Cerca > Cerca participants** per cercar tots els
    participants del taller anterior).
2.  A la pàgina dels resultats de la cerca, o bé escolliu **Tots els x registres** o marqueu
    la casella contigua a cada contacte que us interessi. Un exemple
    de pàgina de resultats de cerca apareix en la següent captura de pantalla.

![captura de pantalla](../img/EventBatchRegistration.png)

3.  Del llistat d'accions just a sobre dels resultats de la cerca, escolliu **Inscriu participants a un esdeveniment** i  cliqueu **Vés.**
4.  Escolliu l'esdeveniment on voleu inscriure els participants. Fixeu-vos
    que actualment no podeu inscriure participants en bloc a esdeveniments
    passats.
5.  Completeu el formulari d'inscripció, escollint les opcions adequades
    per aquest conjunt de persones, com configurar a **Pendent** l'**Estat
    del participant**. Les eleccions triades aquí s'aplicaran a tots els contactes contactes
    en aquest conjunt.
6.  Clique **Desa**.

### Limitacions de les inscripcions en bloc

Les opcions que escolliu (en el pas 3) s'apliquen uniformement al
conjunt sencer dels contactes seleccionats. Per evitar aquesta limitació, feu una
inscripció en bloc diverses vegades, cada cop escollint les opcions desitjades
per a cada conjunt de contactes. Per exemple, podríeu seleccionar un conjunt dels
contactes als qual teniu previst trucar i invitar-los amb un **Estat de participant**
**Pendent**, seguidament afegir un altre conjunt dels contactes a l'esdeveniment, com ara organitzadors
de l'esdeveniment que sabeu que hi assistiran, amb un **Estat de participant**
**Inscrit**.

No podeu fer una inscripció en bloc de participants en esdeveniments passats.

Tampoc podeu aplicar informació de contribucions, com ara un pagament en diferit
o una transacció de targeta de crèdit, en una acció en bloc. És per això que
les inscripcions en bloc són millors en esdeveniments gratuïts o per a contactes que no
necessiten pagar una tarifa en aquest punt. Sempre podreu afegir detalls de pagaments
per contactes persona més tard.

## Importació d'inscripcions

Importar la informació d'inscripcions és una manera ràpida d'afegir múltiples
inscripcions a l'esdeveniment. La informació a ser importada ha d'estar disposada en
un fitxer de valors separats per comes (CSV). Si la majoria dels contactes ja es
troben en el CiviCRM, serà més ràpid de fer una acció d'inscripció en bloc com
hem explicat anteriorment en aquest capítol.

L'eina d'importació per participants és similar a la de contactes, però
hi ha alguns prerequisits que cal complir abans d'executar la
importació. En primer lloc, els participants no es poden importar si no existeixen ja
les Persones en la base de dades com a contactes. Si necessiteu
importar participants per contactes que encara no estan disponibles, executeu
primer una importació de contactes, preferiblement incloent un identificador extern únic
(sovint un identificador assignat per la base de dades o l'aplicació de la qual
esteu important els registres). Hi ha dues maneres de relacionar un participant amb un
contacte:

-   Utilitzeu l'identificador extern de contacte per incloure l'identificador en una columna
    en el fitxer (si aquest identificador no es va importar amb els contactes, però el
    conserveu en els registres, una segona importació de contactes pot ser executada per actualitzar
    aquest camp, abans que importeu els participants).
-   També podeu relacionar els participants amb els contactes basant-vos amb les
    regles de desduplicació de contactes, p.ex. mitjançant la inclusió del nom, cognoms
    i adreça de correu electrònic de les persones en cada contacte del
    fitxer. Si un contacte coincideix amb aquests tres camps, la participació de
    l'esdeveniment se li assignarà.

### Perparant les dades

Quan prepareu les dades per a la importació és útil saber quins camps són
requerits per a la importació. Haureu d'assegurar-vos que aquests camps
s'inclouen en el fitxer CSV d'importació. A continuació hi ha una llista dels camps
requerits. Tingueu en compte que només necessitareu un dels camps marcats **(coincident amb el
contacte)**, no els necessitareu tots.

-   **Identificador del contacte (coincident amb el contacte)**
-   **Correu electrònic (coincident amb el contacte)**
-   **Identificador de l'esdeveniment**
-   **Identificador extern del contacte (coincident amb el contacte)**
-   **Estat del participant**

### Passos per importar inscripcions

1.  Des del menú de navegació aneu a **Esdeveniments > Importació de participants**.
2.  Navegueu al fitxer de dades en el vostre ordinador local.
3.  Seleccioneu el tipus de contacte apropiat, format de data i altres opcions,
    i cliqueu **Continua**.
4.  Relacioneu els camps del vostre fitxer CSV amb els camps del CiviCRM.
5.  Si això és quelcom que repetireu en un futur, marqueu
    **Desa** en la casella d'aquest mapeig de camps.
6.  **Previsualitzeu** i **Deseu**.

![captura de pantalla](../img/EventImportParticipants.png)
