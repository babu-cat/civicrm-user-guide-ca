# Visualització del tauler de CiviContribute

La pàgina principal del CiviContribute o el tauler resumeix les contribucions fetes,
incloent les llistes de contribucions rebudes en el mes actual fins a dia d'avui, de l'any
fins a dia d'avui i acumulatiu des del començament (p.ex. tots els registres de contribucions en
  la vostra instal·lació CiviCRM). Això us permet explorar fàcilment les contribucions
  que s'han anat registrant automàticament o s'han afegit manualment. El tauler també
  proporciona botons per gestionar i afegir pàgines de contribucions.

Per visualitzar els resums hi ha disponibles diferents disposicions. La següent captura de pantalla
mostra les contribucions més recents d'una campanya utilitzant la pestanya disposició en taula:

![ContactSummary1a](../img/CiviCRM-CiviContribute-EveryDayTasks-ContactSummary1a-en.png)

També podeu visualitzar gràfics de barres o circulars per comparar les contribucions totals al llarg
dels mesos d'un any determinat i al llarg dels anys clicant en la pestanya de disposició en gràfic.

![ContactSummary1b](../img/CiviCRM-CiviContribute-EveryDayTasks-ContactSummary1b-en.png "ContactSummary1b")

Finalment, podeu afegir qualsevol número de [Contenidors d'informes](../the-user-interface/menu-dashboard-and-dashlets.md#dashlets) de contribucions al vostre
tauler personal de CiviCRM. Això pot incloure un gràfic resum de barres de les
contribucions de l'any fins avui per tipus financer o mes, un llistat dels 10 primers donants, etc.

# Cerca de contribucions

El CiviCRM fa una important distinció entre les contribucions i la
gent que fa les contribucions. És important apreciar la
diferència entre les dues quan cerqueu contribucions. Per
exemple, si voleu enviar un obsequi a tota la gent que a fet una
contribució en el darrer any, que seria el més apropiat? Contactes
o contribucions? La resposta depèn de si voleu enviar dos obsequis
a la gent que ha fet dues contribucions i no hi ha per suposat cap
resposta bona ni dolenta - tan sols depèn del vostre enfocament. És
important pensar sobre això cada vegada que es faci una cerca.

La **Cerca contribucions** us permet cercar en base a les dades de les
contribucions i retornar els registres de contribució. La podeu trobar a **Contribucions > Cerca
contribucions**.

![Contribution Find Screenshot](../img/contributions-find-search.png)

Podeu cercar en funció d'una sèrie de criteris, com ara l'interval de dates, l'import
de la contribució, l'estat de la contribució, etc. Les contribucions han de coincidir amb tots els criteris de cerca especificats
per ser retornades, així que com més criteris introduïu, més reduïda serà
 la cerca. Per exemple, cercant pel tipus financer "donatiu" i l'interval de
 dates "1 de gener fins a 31 de maig" es retornaran les contribucions que coincideixin
 amb ambdós criteris. Els intervals de dates relatives com ara "El mes passat" o "L'any passat" són sovint
 força útils.

 A més del subconjunt de registres resultants d'una cerca, la pantalla de resultats
 d'una cerca de contribucions mostra l'import total, el nombre de
 contribucions, la contribució mitjana i la moda dels resultats de la cerca.

 ![Screen shot batch update from search](../img/contributions-find-editcriteria.png)

 Podeu seleccionar una acció per realitzar del menú d'**Accions** un cop hagueu seleccionat
 tots o un subconjunt dels resultats. Podeu:

 - **Actualitza múltiples contribucions**: Això és útil si voleu actualitzar un
 gran nombre de dates d'agraïment de contribucions d'un sol cop, per exemple. Necessiteu
 [crear el perfil](../organising-your-data/profiles.md) que voleu utilitzar *abans*
 de realitzar la cerca i l'actualització per lots.

 - **Elimina les contribucions**: Això elimina les contribucions per complet del
 sistema, com si mai no haguessin estat introduïdes. Editar
 les contribucions i actualitzar el seu estat a cancel·lat proporciona un seguiment d'auditoria
 millor, però poden haver-hi situacions on vulgueu eliminar-les, com una
 contribució introduïda en el registre de contacte equivocat.
 - **Exporta les contribucions**: Això és una exportació de contribucions. Si voleu
 escollir exportar múltiples contribucions d'un mateix contacte acabareu
 amb una fila per a cada contribució en el fitxer d'exportació. Si voleu fer
 cerques que retornin un resultat per contacte, utilitzeu la cerca avançada de contactes.

 - **Rebuts - Imprimeix o envia un correu electrònic de la contribució:** Això us permet crear un fitxer
 PDF de tots els rebuts de la cerca, o enviar els rebuts per correu electrònic als donants
 associats. Vegeu "Enviament de cartes d'agraïment" a sota per a més informació.

 - **Correu electrònic - envia ara**: Envia un correu electrònic a tots els contactes o als seleccionats trobats en la
 cerca.

 - **Cartes d'agraïment - imprimeix o envia un correu electrònic**: Crea una carta PDF personalitzada per a cada
 una de les contribució seleccionades, amb l'opció d'actualitzar la data del rebut o agraïment
 per a cada un.

 - **Actualitza l'estat de les contribucions pendents**: Això us permet registrar els detalls de
 pagaments i actualitzar l'estat de la contribució per a totes les contribucions en línia o seleccionades
 amb "pagament diferit". Aquesta opció només funciona en contribucions amb
 l'estat de pendent (pagament diferit) i el mateix estat de la contribució serà aplicat
 per totes les contribucions seleccionades per actualitzar.

La **Cerca avançada** retorna contactes per defecte, però podeu escollir
**Contribucions** al camp **Mostra els resultats com a** per mostrar contribucions
en comptes de contactes. Els criteris de cerca estàndards estan disponibles
quan expandiu el panell de contribució, però també podeu filtrar els resultats
amb criteris addicionals ("Troba tots els donatius amb dret a desgravació fets per membres de l'organització" o "Mostra tots els contactes que han contribuït més de
100€ l'últim any i que viuen a Barcelona").