# Desduplicació i combinació

## Què és la desduplicació?

Els contactes duplicats poden aparèixer en les dades per diversos moutius, com ara
errors dels usuaris que no s'adonen que estan creant un contacte d'algú
que ja està al CiviCRM, duplicats que no s'han detectat en el
procés d'importació i registres duplicats creats quan la gent emplena formularis
en el vostre lloc sobre ells mateixos sense adonar-se que es troben ja en la
llista de contactes (potser amb els seus noms escrits d'una altra manera o amb una
adreça de correu electrònic diferent).

Alguns exemples d'escenaris on contactes duplicats poden entrar a la
base de dades:

-   Quan un administrador o usuari creen un contacte nou a través de
    la interfície i aquest contacte ja existeix.
-   Quan un contacte es crea a ell mateix publicant o registrant-se en línia i
    l'usuari ho fa amb una altra adreça de correu electrònic o nom.
-   Quan els contactes s'importen a la base de dades.

## Funcionalitats CiviCRM per a desduplicar contactes

El CiviCRM està equipat amb diverses funcionalitats per tractar amb els contactes
duplicats. Algunes intenten evitar que el contacte duplicat s'acabi
creant i d'altres ajuden a cercar, identificar i combinar els contactes
duplicats existents en la base de dades.

Aquestes funcionalitats es divideixen entre aquelles que actuen "automàticament" (conegudes
com a "no supervisades") i les que actuen manualment (conegudes com a
"supervisades").

Aquestes funcionalitats inclouen:

-   Escaneig de duplicats de la base de dades utilitzant una regla de desduplicació seleccionada
    (veieu a sota) i combinant la informació necessària del contacte duplicat.
-   Selecció manual de dos contactes utilitzant la cerca i posteriorment escollint
    de combinar-los.
-   Escaneig automàtic de la base de dades i suggeriment de duplicats quan
    els contactes s'afegeixen o editen a través de la interfície d'usuari.
-   Combinació automàtica dels detalls d'una persona en un contacte existent quan
    una persona es registre en línia a esdeveniments, pertinences,
    contribucions o pàgines de perfil.
-   Combinació automàtica dels detalls d'una persona quan s'importen contactes.

## Regles de desduplicació

Les regles de desduplicació són una manera d'especificar a aquestes funcionalitats quan el CiviCRM
ha de considerar els contactes com a duplicats. Per exemple una regla pot
establir que quan un correu electrònic i el nom entre dos contactes
coincideix, el CiviCRM ha de considerar aquests contactes com a duplicats.

## Utilització de regles predeterminades per cercar i combinar contactes duplicats

Si no voleu configurar les regles de desduplicació en aquest punt podeu
senzillament utilitzar les regles predeterminades per trobar duplicats a la base de dades.

En primer lloc visualitzeu les regles de desduplicació. Aneu a **Contactes > Cerca i combina
contactes duplicats** en el menú de navegació. Es mostrarà la següent
pantalla:

![Selecció de regles de cerca de duplicats](../img/duplicates-choose-find-rule.png)

Diferents regles estan configurades per a cada tipus de contacte (persones,
organitzacions i llars) Una regla supervisada predeterminada i una regla
no supervisada predeterminada està configurada per a cada tipus de contacte. Les regles predeterminades
s'utilitzen quan el CiviCRM aplica verificació automàtica, de maneres que s'explicaran amb més
detall més a sota.

## Entenent les regles de desduplicació: supervisades, no supervisades i generals

El CiviCRM ara inclou tres categories de regles de desduplicació:

**No supervisada:** La regla 'no supervisada' per a cada tipus de contacta s'utilitza
automàticament quan es creen nous contactes a través de registres
en línia incloent esdeveniments, pertinences, contribucions i pàgines de
perfil. Es seleccionen també com a predeterminades quan s'importen contactes. En
general es configuren amb una definició estricte del que constitueix un
duplicat per evitar que una falsa coincidència sigui combinada per accident.

**Supervisada:** La regla 'supervisada' per a cada tipus de contacte s'utilitza
automàticament per verificar possibles duplicats quan els contactes
s'afegeixen o s'editen via la interfície d'usuari. La interfície alertarà a l'usuari si un
dels contactes que crea coincideix amb algun altre contacte utilitzant la regla.
L'usuari pot després decidir editar el contacte existent o continuar
creant un nou contacte. Les regles supervisades es poden configurar amb
definició més amplia del que constitueix un duplicat i així l'usuari pugui
decidir si actuar sobre la regla o no.

**General:** Només es pot configurar una regla 'no supervisada' i una de
'supervisada' per a cada tipus de contacte, però es pot configurar qualsevol
número de regles 'generals' addicionals per proporcionar un altre criteri per escanejar
possibles duplicats.

## Configuració de regles

Per determinar quan dos contactes són duplicats, el CiviCRM verifica fins a
5 camps que podeu especificar. També podeu definir una longitud de valor que
determina quants caràcters del camp es compararan. Per
exemple, si definiu una longitud de 2 en el camp **Nom**, el nom
de "Miquel" coincidirà amb "Mikel" i ambdós es reconeixeran com
duplicats, perquè els primers 2 caràcters són els mateixos. No obstant, si
d'altre manera definiu la longitud a 3, "Miquel" no coincidirà amb "Mikel" i
ambdós es consideraran com contactes diferents. Si el valor de la longitud es
deixa en blanc, la comparació es fa amb el valor sencer del camp.

Cada camp es configura amb un pes numèric que determina la
importància relativa d'una coincidència en aquest camp. Quan una coincidència és descoberta
en un camp, el pes d'aquest s'afegeix en el pes total de la
regla. Un cop cada camp ha estat verificat, si el pes total és igual o
més gran que el llindar numèric definit a la regla, els contactes
comparats s'identifiquen com a possibles duplicats.

## Utilització de regles i combinació manual de contactes duplicats

!!! tip "Consell"
    una interfície d'usuari diferent està disponible a [the deduper extension](https://github.com/eileenmcnaughton/deduper/blob/master/Readme.md)

1.  Anar a **Contactes > Cerca i combina contactes duplicats**.
2.  Clicar a l'enllaç **Utilitza la regla** per escanejar contactes duplicats utilitzant
    la regla seleccionada.

3.  Podeu seleccionar cercar duplicats sobre tots els contactes o
    limitar la cerca a un grup en particular. Si escolliu limitar la
    cerca a un grup específic, el CiviCRM cercarà els duplicats on almenys
    un dels contactes en qualsevol parella de duplicats identificada estigui en
    el grup seleccionat.

    ![Selecció de grup en la cerca de duplicats](../img/duplicates-select-group.png)  

    Els contactes del tipus associat a la regla
    s'escanejaran i compararan. Si la cerca entre els dos
    contactes coincideix o excedeix la puntuació del llindar de la regla, els contactes
    es mostraran en la següent pantalla de possibles duplicats.
    Es presentaran en un llistat de possibles duplicats amb algunes
    caselles de verificació mostra/amaga; Adreça del carrer, Codi postal, Conflictes i Llindar.

    ![Llistat de possibles duplicats](../img/duplicates-list-of-possibles.png)  

4.  Fent clic a **combina** per a qualsevol parella de contactes apareix una taula
    mostrant els detalls per a cada contacte. El CiviCRM designa un registre com
    el registre duplicat i mostra la seva informació en la columna
    esquerra. El registre de la columna dreta es considera el registre
    original en el qual es combinarà la informació seleccionada del registre
    duplicat.
5.  Si voleu moure la informació en la direcció oposada,
    podeu intercanviar els contactes duplicat i original escollint **Intercanvia
    la posició dels contactes original i duplicat** a dalt de la pàgina.

    ![Pantalla de combinació de duplicats](../img/duplicate-merge-screen.png)  

6.  Les files en la pantalla de combinació estan codificades per colors.
    - El verd indica que la informació és la mateixa
    per a cada contacte. Aquesta es pot ocultar fent clic a **Mostra/oculta files amb la mateixa informació en cada registre de contacte**.
    - El vermell indica que la informació és diferent pels dos contactes. Per a cada camp, podeu escollir quan conservar la informació original
    mostrada a la dreta (no marqueu la casella de verificació de la columna del mig),
    o utilitzar en canvi el valor del contacte duplicat (marqueu la casella de verificació).
    Pel que fa a les adreces de correu electrònic o als números de telèfon, podeu decidir de mantenir-los
    ambdós valors, el valor del duplicat i el valor de l'original (marqueu ambdues
    caselles de verificació de la columna del mig i la de "Afegeix nova" de la columna de la dreta)
    per copiar la informació duplicada.
    - El groc indica una fila on l'opció predeterminada és una marca en la
    casella de verificació que significa que la informació del contacte duplicat s'**afegirà** a la informació existent
    en el registre original. Això s'aplica a les etiquetes, grups i informació d'activitats
    (incloent assistència als esdeveniments, contribucions, etc.). Si desmarqueu
    la casella de verificació la informació provinent del duplicat es perdrà.
7.  Cliqueu a **Combina...** per completar la combinació, o **Marca aquest parell com a no
    duplicat** si creieu que els dos contactes no són el mateix.
8.  Quan es marca com a 'no duplicat', aquests contactes s'exclouran de
    tots els llistats de resultats de desduplicació. Per revisar el llistat de contactes marcats com a 'no duplicats', cliqueu a "Visualitza les excepcions d'eliminació de duplicats" a dalt de la pantalla principal de "Cerca i combina els contactes duplicats".

## Combinació de múltiples contactes de cop
En alguns casos pot ser indicat combinar múltiples parelles de duplicats a la vegada.
Això es pot fer des de la pantalla de possibles contactes duplicats on es poden mostrar fins a 100 files.

   ![Llista de possibles duplicats per a una combinació en lot](../img/duplicate-list-of-possibles-detail.png)

Podeu **Processar la combinació de tots els duplicats** (Això combinarà **tots** els duplicats trobats,
no només els mostrats a la pantalla) o **Processar la combinació dels duplicats seleccionats**
p.ex. aquells que seleccioneu marcant la casella a l'esquerra de la fila. Aquestes
opcions de processat de combinats es mostren per sota la llista de duplicats descoberta.
En la mateixa regió trobareu **Intercanvia els duplicats seleccionats**. Quan els duplicats
són combinats el contacte 1 es manté i el contacte 2 es combina i posteriorment s'elimina, així en ocasions
podeu intercanviar l'ordre dels registres abans de combinar-los.

La funcionalitat de combinació per lots combinarà tots els contactes sota una regla donada
o tots els contactes seleccionats, sempre
que no hi hagi conflictes en les dades. Per exemple, dues persones amb nom
"Miquel Blasi" poden coincidir en base al seu nom i cognoms idèntics,
amb cap dels dos amb un correu electrònic registrat. Si es conserven les dades
en ambdós contactes és exactament el mateix, o si un contacte conté
informació que l'altre no té (p.ex. un número de telèfon de la feina, on l'altre
el té com a mòbil), els dos seran combinats. No obstant, si ambdós contactes
tenen diferents números de telèfons diferents, els registres es saltaran; els
dos contactes no es combinaran.

Un cop un procés de combinació en lot s'ha completat, tornareu a la
llista original. Si qualsevol dels registres saltats per causa d'un conflicte de dades
com l'exemple de dalt, es mostrarà el missatge de continuació. Per
visualitzar una llista actualitzada dels contactes duplicats (aquells que no s'han combinat
pel procés de desduplicació) heu de clicar **Recarrega els duplicats**; la
pàgina no es recarregarà automàticament, només en el cas que la base de dades sigui molt
gran i la cerca de duplicats provoqui un retard significatiu. Després
podeu continuar avaluant i combinant els duplicats restant manualment.

Si voleu incrementar el nombre de parelles que poden ser resoltes en un lot
de combinació l'extensió [deduper](https://github.com/eileenmcnaughton/deduper/blob/master/Readme.md)
proporciona un rang de resolucions, permetent fer coses com
especificar que els conflictes de certs camps no siguin necessàriament bloquejants o
gestionant noms diacrítics.

La combinació en lot es pot realitzar des de la línia de comandes - p.ex.

```
 echo '{"search_limit": 10000, "criteria":{"contact" : {"id" : {">" : 200}}}}'
   | drush --in=json cvapi Job.process_batch_merge

```

Cercarà tots els contactes que coincideixin amb qualsevol de

"els primers 10.000 contactes trobats amb un id més gran de 200"
i intentarà combinar-los automàticament utilitzant els modes segurs predeterminats
(saltant quan hi hagi conflictes) i les regles predeterminades per a persones.



![captura de pantalla](../img/CiviCRM_dedupe_batchmerge.png)

!!! warning "Atenció"
    Abans que considereu d'utilitzar la desduplicació en lot, tingueu cura de prendre en consideració
    els punts de continuació.

    *  Aquesta funcionalitat està prevista per utilitzar-se en grans conjunts de dades que tenen estructures de camps estrictament gestionades. Si la vostra és una base de dades petita amb només pocs duplicats, us recomanem de combinar-los manualment utilitzant el vostre propi judici.
    *  Un cop combinats, els enllaços entre els contactes duplicats i els registres de qualsevol altra part del sistema seran transferits al contacte original (p.ex. registres de participants d'esdeveniments, grups, etiquetes, contribucions, activitats, casos i pertinences). NO tindreu la possibilitat de revertir aquest canvi.
    *  Els registres duplicats, un cop combinats, seran eliminats i no seran recuperables, a no ser que tingueu el registre de base de dades habilitat. Us recomanem encoratjadament fer una còpia de seguretat de la informació abans de córrer un procés de combinació.

## Un procés de desduplicació en vàries etapes

Sovint utilitzant un a única regla de deduplicació comporta que quedin alguns duplicats en el sistema.
A sota es proporciona una manera de processar sistemàticament múltiples aplicacions. Si la vostra regla no supervisada per persones no és prou estricta llavors podeu estalviar-vos la desduplicació en lots duran la primera etapa i desduplicar manualment en la segona etapa.

1.  Comenceu cercant duplicats utilitzant la regla "No supervisada" per persones:
    cliqueu l'enllaç **utilitza la regla** (tipus de contacte "Persona" i ús
    "no supervisat").
2.  Seleccioneu **Tots els contactes** o un grup particular.
3.  Cliqueu **Continua**.
4.  Si trobeu duplicats, combineu o elimineu els contactes duplicats.
5.  A continuació cerqueu els duplicats utilitzant una regla "supervisada" o "general" per
    trobar els que s'han escapat amb la regla més estricta: cliqueu l'enllaç **utilitza la
    regla** per "Persona supervisada" (tipus de contacte "Persona"
    i ús "supervisat").
6.  Seleccioneu **Tots els contactes** o un grup particular.
7.  Cliqueu **Continua**.
8.  Si es troben duplicats, combineu-los o marqueu-los amb 'no és un duplicat'.


## Combinant contactes des de resultats de cerca

Si observeu contactes duplicats dins d'un conjunt de resultats d'una cerca podeu
combinar-os directament des dels resultats de la cerca en comptes d'utilitzar el
procés separat de **Cerca i combinació de contactes duplicats**. Aquesta és una bona
manera de netejar la base de dades durant el vostre flux de treball diari amb
una interrupció mínima.

1.  Seleccionar els contactes duplicats des dels resultats de cerca fent clic
    a la casella de selecció al lateral esquerra de cada registre.
2.  Seleccionar **Combina els contactes** en el menú d'**Accions**.
3.  Seguir els passos normals per combinar els contactes duplicats.
