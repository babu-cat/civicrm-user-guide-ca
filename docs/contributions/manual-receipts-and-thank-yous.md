# Enviament de rebuts i cartes d'agraïment

## Rebuts

Els donants que fan contribucions mitjançant un formulari en línia reben
automàticament, per correu electrònic, un rebut pel seu pagament en cas 
que hagin escollit aquesta opció durant la configuració de la pàgina de
contribució. Si voleu enviar o reenviar posteriorment un rebut,
ho podeu fer editant la contribució i marcant l'opció **Enviar rebut?**. 
El rebut s'enviarà després de clicar **Desar**.

Podeu enviar rebuts fora de línia a múltiples contactes a la vegada 
a través de la cerca[Cerca contribucions](finding-and-viewing-contributions.md).
Un cop seleccionats els contactes, seleccioneu **Rebuts - imprimir o enviar per correu**
en el selector d'accions.

![ContributionReceiptsManual](../img/civicontribute-receipts-manual.png)

Podeu triar l'opció d'enviar els rebuts per correu electrònic o crear rebuts 
en PDF per enviar-los per correu als donants.

![Contributions search result with the action menu expanded.](../img/Print_contribution_receipt_options.png)

Per defecte, l'enviament per correu electrònic o la creació de rebuts
en PDF actualitzaran la data del rebut per a totes les contribucions
seleccionades, però podeu mantenir la data d'enviament existent en
cas necessari. També podeu ignorar l'opció **No enviar correu electrònic**
per a què s'enviï un rebut a tots els contribuents.

El rebut de contribució estàndard conté informació limitada. El podeu personalitzar,
però això requereix coneixements d'Smarty. També es poden enviar rebuts
fora de línia mitjançant el sistema de cartes d'agraïment.

## Cartas d'agraïment

És possible enviar cartes d'agraïment als donants de campanyes específiques
informant-los de l'import total recaptat. També podeu enviar un rebut
a cada contacte al final de l'any fiscal, informant de les deduccions
fiscals de les contribucions realitzades al llarg de l'any. Aquestes dues opcions,
entre d'altres, estan disponibles mitjançant la funcionalitat de "Cartes
d'agraïment per Contribucions". Aquesta acció està disponible des de
la pàgina de resultats de cerca de contribucions (no de contactes).
Els passos per fer-ho són:

1.  Utilitzant **Cerca contribucions** o la **Cerca avançada** amb l'opció
    **Contribucions** seleccionada al desplegable **Mostra resultats com a**
    per a la cerca. 
2.  Seleccionar les contribucions per a l'enviament de cartes d'agraïment
    o rebuts combinats. 
3.  Escollir l'acció **Cartes d'agraïment - imprimir o enviar correu electrònic**.
    Es mostrarà el següent missatge:
    ![ContributionThankyouLettersNogrouping](../img/civicontribute-thank-you-letters-no-grouping.png)
4.  Escollir **Actualitzar les dates d'agraïment per aquestes contribucions** o
    **Actualitzar les dates de rebut per aquestes contribucions**. The
    current date will be entered into the appropriate field.   
5.  Hi ha tres **Opcions d'impressió i correu electrònic** autoexplicatives:
    -   Generar PDFs per imprimir (només)
    -   Enviar correus electrònics quan sigui possible. Generar PDFs per a contactes
        que no poden rebre correus electrònics.
    -   Enviar correus electrònics quan sigui possible. Generar PDFs per a tots els contactes.
6.  Algunes persones poden haver fet més d'una contribució. Per enviar una carta
    per cada contribució, cal seleccionar l'opció **"no agrupar-"** al selector
    **Agrupar contribucions per**. Alternativament, podeu escollir mostrar les dades de 
    múltiples contribucions del mateix contacte al cos de la carta. Hi ha cinc
    opcions d'"agrupar per".
7.  **Separador (contribucions agrupades)** només és aplicable si s'ha seleccionat
    alguna opció diferent de **- no agrupar -** per a les contribucions. Aquestes opcions
    s'expliquen amb més detall més endavant a *Cartes d'agraïment de contribucions agrupades*.
8.  Comprobar  la configuració de **Format de pàgina**.
9.  Podeu fer servir una plantilla existent, crear una carta d'un sol ús o crear una nova carta
    i desar-la com a nova plantilla.
    [Tokens i combinació de correspondència](../common-workflows/tokens-and-mail-merge.md) i
    [Comunicaciones per correu postal](../common-workflows/postal-mail-communications.md)
    ofereixen més informació sobre la creació de plantillas de cartes.
10. Clicant sobre **Fer cartes d'agraïment**, es generaran les cartes i es crearà una
    acció per cada carta amb l'**Assumpte** especificat.

### Cartes d'agraïment de contribucions agrupades

Podeu enviar rebuts de declaracions tributàries als vostres contactes si trieu 
una opció diferent de **-no agrupar-** en el camp **Agrupar contribucions per**.

En una instalació estàndard de CIVICRM, las cartas que es poden generar agrupant 
les contribucions són força rudimentàries.

Si trieu la **Coma** com a **Separador**, els imports de les contribucions i/o
dates aniran una rere l'altra separades per comes. Per exemple, "Gràcies per la
seva generosa aportació de {contribution.total_amount} rebuda el {contribution.receive_date}
respectivament." es mostrà com "Gràcies per les seves generoses aportacions 
de 100,00€, 150,00€, 325,00€ rebudes el 3 de gener de 2015, el 5 de març de
2015, el 16 de maig de 2015 respectivament."

Si trieu **Cel·la de taula** com a **Separador**, cada contribució es mostrarà
en una columna. Per exemple:

![Thank you letter with tokens.](../img/thank_you_letters_as_table_template.png)

es mostrarà com:

![Thank you letter with expanded tokens.](../img/thank_you_letters_as_table_1.png)

Aquest format és adequat si només s'han rebut unes poques contribucions al 
llarg de l'any, però la taula pot arribar a ser més ampla que la pàgina en
cas de contribucions mensuals, quinzenals o setmanals.

En cap cas es pot mostrar a la carta l'import anual de contribucions.

Per incloure a la carta l'import anual de les contribucions i per generar una 
carta més adient per mostrar diverses contribucions d'una mateixa persona, es
pot habilitar la funcionalitat Smarty per als correus electrònics
([http://wiki.civicrm.org/confluence/display/CRMDOC/Smarty+in+mail+templates](http://wiki.civicrm.org/confluence/display/CRMDOC/Smarty+in+mail+templates)).

Un cop fet això, podeu incloure l'import anual de les contribucions
fent servir el token `{$contribution_aggregate}`.

Per exemple, si el codi HTML de la teva carta és:

```html
<p>Dear {contact.first_name}</p>
<p>Thank you for donating ${$contribution_aggregate} to help the arts during the 2014 financial year</p>
<p>Your donation is tax deductible and the details are given below.</p>
<p>with appreciation for your generosity,</p>
<p>the CEO</p>
  <table class="table" style="width: 500px;" border="1" cellspacing="0" cellpadding="2" align="left">
    <tbody>
      <tr>
        <th>Date</th>
        <th>Amount</th>
        <th>Receipt Number</th></tr>
    <!--
    {foreach from=$contributions item=contribution} {assign
    var="date" value=$contribution.receive_date|date_format:"%d %B
    %Y"}
  -->
      <tr>
        <td>{$date}</td>
        <td>{$contribution.total_amount}</td>
        <td>{$contribution.id}</td>
      </tr>
   <!--
    {/foreach}

 --></tbody>
  </table>
```
les cartes es mostraran de la següent manera:

![Thank you letter with expanded tokens.](../img/thank_you_letters_as_with_smarty_enabled_2.png)
