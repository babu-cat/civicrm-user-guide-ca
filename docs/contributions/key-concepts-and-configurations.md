# Conceptes clau i configuracions

Aquesta secció explica els conceptes clau que fonamenten el CiviContribute i esboça
la configuració a alt nivell necessària per al seu ús.

Abans de començar és útil llistar els tipus de contribucions que rep la vostra
organització (o que li agradaria rebre) i identificar en quin d'aquests
voleu fer un seguiment utilitzant el CiviCRM.

## Tipus financers, comptes financers i codis de comptabilitat

Les organitzacions que utilitzen CiviCRM tenen diferents necessitats en termes d'informes
financers. Algunes tan sols volen conèixer el total de donacions o de socis entrants
registrats en el CiviCRM mentre d'altres volen ser capaces d'exportar un conjunt complet de
partides dobles de transaccions financeres per importar-les en els seus programes de comptabilitat.

CiviCRM possibilita a tots dos grups, mitjançant l'ús dels **Tipus financers**, ocultar la
complexitat de la comptabilitat de partida doble a qualsevol que no necessiti saber-ne
res, i a la vegada continuar registrant aquestes transaccions per a les organitzacions que
les necessitin.

Cada **tipus financer** es vincula a un número de **comptes financers** que
poden fer el seguiment d'ingressos, actius, taxes i recompenses (si aplica) com sigui
requerit tal com es mostra pels quatre tipus financers de la següent imatge.


![financial types and accounts](../img/civicontribute-financial-types-and-accounts.png)


Els **comptes financers** haurien d'estar basats en la taula de comptes de la vostra
organització. A CiviCRM cada contribució s'ha d'assignar a un tipus financer.
Quan la contribució és desada, els crèdits i dèbits corresponents es
registren automàticament pels comptes financers vinculats al tipus financer.
(Si estu utilitzant
conjunts de preus, cada opció en el conjunt de preus pot ser vinculada a un tipus financer
diferent i el CiviCRM seguirà registrant els dèbits i crèdits
corresponents per tots els comptes financers vinculats.)  

Haurieu de consultar el comptable o administrador de la vostra organització abans
de configurar per primera vegada o modificar els tipus financers o comptes financers
existents.

### Tipus financers

Els tipus financers estàndards inclosos en el CiviCRM són les quotes d'esdeveniments, les quotes de membres,
les donacions i les contribucions de campanyes tal com es mostra a la imatge de sota, però podeu
modificar els comptes existents o configurar nous tipus financers per adaptar-los a les vostres necessitats.

En general necessitareu un tipus financer per a cada tipus d'ingrés
que rebeu en el CiviCRM i del que en feu seguiment en els vostres comptes. Per tant, si doneu compte de donacions
de campanyes de desgravació d'impostos, donacions de festes solidàries i donacions recurrents de manera separada,
llavors, tenir únicament un tipus financer "Donatius" en el CiviCRM no serà suficient,
necessitareu un tipus financer "Campanyes de desgravació", un altre "Festes
solidàries" i encara un altre "Donatius recurrents".

Per crear un nou tipus financer navegueu a **Administra > CiviContribute >
Tipus financers**,  i clicar a **Afegeix un tipus financer**

![Adding Financial Type](../img/civicontribute-financial-types-add-new.png)

Quan creeu un tipus financer amb un nom específic, el CiviCRM crearà automàticament
un compte d'ingressos amb nom similar i l'assignarà junt amb
els comptes per defecte d'actius, despeses i cost de vendes al nou tipus
financer. Si necessiteu editar els comptes assignats a un tipus financer,
ho podeu fer clicant a **Comptes** a la dreta del tipus financer
corresponent a **Administra > CiviContribute > Tipus financers**.
L'objectiu d'aquest procés de dos passos és
el de simplificar el cas comú on una organització només té un únic
compte de dipòsit bancari, un únic compte per cobrar i un únic compte per pagar, però proporciona
la flexibilitat per configuracions més sofisticades.

Tingueu en compte que podeu utilitzar CiviCRM's el sistema de permissos basat en rols per controlar l'accés dels usuaris a la informació de les contribucions definint els [Permissos de tipus financer](../initial-set-up/permissions-and-access-control.md#financial-type-permissions).

![Editing accounts linked to financial type](../img/civicontribute-financial-types-linked-accounts.png)

### Comptes financers

De la mateixa manera que amb els tipus financers, la llista dels comptes financers preconfigurats
s'ajustarà a les necessitats de gran part de les organitzacions però pot ser personalitzat si la vostra
organització requerix canvis o afegits. (Recordeu, cada tipus financer nou
afegirà un nou compte d'ingressos amb el mateix nom.)

Podeu editar els comptes financers a **Administra > CiviContribute > Comptes financers**.

Els únics camps requerits són el Nom i Tipus de compte financer. Pels comptes
d'ingressos aquests seran definits quan creeu el tipus financer.

![Editing Financial Account](../img/civicontribute-financial-account-edit.png)

Quants dels altres camps empleneu dependrà del vostre flux de treball.
Si teniu previst exportar les transaccions financeres del CiviCRM per importar-les en el vostre
programa de comptabilitat necessitareu el codi comptable (sense
espais extra o sobrants).  Si utulitzeu Quickbooks necessitareu també el
codi de tipus de compte.

!!! note
    Si es modifica el nom del compte financer es modificarà també el nom del tipus financer.

## Processadors de pagament

El CiviCRM us proporciona la possibilitat de fer pagaments en línia en el vostre
lloc web. Podeu fer pagaments per diferents raons incloent
campanyes de captació de fons, quotes de membres i assistència a esdeveniments.

Per començar a fer pagaments en línia necessiteu [configurar un processador de pagaments](payment-processors.md)
que connectarà el vostre lloc web amb la targeta de crèdit i amb la infraestructura bancària
que en realitat processa el pagament.

## Mètodes de pagament

Navegueu a **Administra > CiviContribute > Mètodes de pagament** per
editar les opcions existents que poden ser utilitzades pels contribuents o per afegir una nova
opció a partir de **Afegeix mètodes de pagament**. Les opcions més comunes - targeta de
crèdit, efectiu, xec, targeta de dèbit i transferència bancària - es troben instal·lades per defecte. Haureu de
confirmar amb el vostre administrador o comptable per confirmar que cada mètode de pagament es troba vinculat
a l'actiu comptable correcte.


## Targetes de crèdit acceptades

Navegueu a **Administra > CiviContribute > Targetes de crèdit acceptades** per
editar les targetes de crèdit existents acceptades o definiu una nova opció a través de
**Afegeix targetes de crèdit acceptades**.

!!! note
    Si la informació de facturació es recull en el lloc web del processador de pagament
    llavors necessitareu configurar les targetes de crèdit i mètodes de pagament acceptats en aquest
    lloc.


## Estat

Totes les contribucions tenen un estat, els més comuns són:

**Pendent (Pagament diferit)** indica que una contribució que ha estat introduïda però no pagada encara no s'ha rebut. Generalment per xecs en paper o electrònics.

**Pendent (Incompleta)** ha estat introduïda al CiviCRM i enviada al processat en línia. No obstant, el pagament no s'ha completat en el processador, o la resposta del processador encara no s'ha rebut. Les contribucions que quedin perpetuament en aquest estat en el CiviCRM però quedin completades en el processador requereixen una investigació de les comunicacions entre els dos sistemes.

**Fallida** ha estat introduïda en el CiviCRM i reenviada per processar. Malgrat això, el procés ha estat declinat, refusat o ha rebut un error i ha retornat aquest resultat al CiviCRM.

**Completada** introduïda al CiviCRM, pagament processat i resposta rebuda satisfactòriament.

Altres estats com En progrés, Vençuda, Parcialment pagada són utlitzats per funcionalitats opcionals per a pagaments parcial i pagaments recurrents automatitzats. Es possible modificar els noms dels estats de contribució a **Administra > Configuració del sistema > Grups d'opcions** però no es recomana afegir estats addicionals en la mesura que pot interferir amb la validació contable al CiviCRM.

## Necessitat de dades i camps

CiviContribute té un conjunt de camps predefinits per fer el seguiment de la informació
de les contribucions. Si necessiteu fer el seguiment de més informació sobre contribucions,
ho podeu fer definint nous camps personalitzats de dades. Les dades personalitzades poden ser
útils per categoritzar amb més profunditat les vostres contribucions o fer el seguiment d'informació
addicional.

Escriviu tota la informació sobre la que voleu fer un seguiment de les vostres
contribucions, incloent els informes (descrits més tard en aquest capítol), llavors
compareu les vostres necessitats d'informació amb els camps de CiviCRM predefinits. Una manera senzilla de
fer això és mirar la pantalla per afegir una nova contribució. Moltes
funcionalitats útils estan construïdes en els camps de contribució del nucli amb la qual cosa
no té sentit duplicar-les amb camps personalitzats, però la vostra
organització pot tenir necessitats específiques que requereixin de camps personalitzats.

Si necessiteu crear camps personalitzats per satisfer les vostres necessitats, llegiu [Creació de camps personalitzats](../organising-your-data/creating-custom-fields.md).