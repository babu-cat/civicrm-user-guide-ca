Comunicacions per correu postal
===============================

Aquest capítol tracta les diferents maneres en que CiviCRM ajuda amb el correu postal i les campanyes de correu postal. Us serà d'ajuda si teniu coneixements sòlids en funcions de cerca en el CiviCRM, com també de camps personalitzats, activitats, perfils i com realitzar combinacions de correspondència utilitzant eines de processament de text.

Planificació de l'enviament de correu
-------------------------------------

Abans de començar qualsevol activitat de comunicació, preneu-vos el temps per identificar els objectius i planificar els passos a seguir. Pel als nostres propòsits, hi ha algunes qüestions claus a fer-se abans d'enviar els correus postals.

-   Quin tipus d'enviament de correu enviareu als vostres constituents?
-   Els enviaments de correu s'enviaran sempre a tothom que es trobi a la base de dades o es dirigiran freqüentment a un seleccionat grup de contactes?
-   Com us voleu adreçar als destinataris (p.ex "Estimada Jane" o "Estimada Jane
    Doe")?

Hi ha tres maneres en que podeu utilitzar el CiviCRM per als enviaments postals:

1.  Generació d'etiquetes: imprimiu etiquets d'adreces estàndards quan no hagueu de personalitzar el contingut, per exemple per enviar una fulletó imprès.
2.  Exportació de contactes i combinació de correspondència mitjançant una eina externa (com ara LibreOffice o Microsoft Word). Consulteu el capítol sobre Exportació anterior a aquesta secció per instruccions detallades d'exportació.
3.  Utilització de la funció Impressió de cartes PDF de CiviCRM per fer la combinació directament en el CiviCRM (vegeu més a vall per saber més).

Moltes organitzacions no lucratives dels Estats Units necessiten organitzar els destinataris d'un enviament de correus en funció del codi postal per propòsits d'enviaments massius. Si això també succeeix a la vostra organització, és recomanable que creeu les etiquetes per l'enviament utilitzant un processador de textos on pugueu controlar l'ordre de classificació, en comptes que ho faci el CiviCRM. Podeu utilitzar el mateix full de càlcul per a la combinació de correspondència.

Salutacions
-----------

Podeu configurar un format de salutació postal específica per a cada contacte. Hi ha diverses opcions des de les més informals com "Estimat John", fins a les més formals com "Benvolgut Sr. John Doe". També podeu introduir una *salutació personalitzada* ("Molt honorable"). Les salutacions postals es poden editar en la secció de Preferències de comunicación del formulari d'edició del contacte. Si necessiteu definir o reiniciar les salutacions postals massivament, consulteu el capítol *Tasques Programades* en aquesta secció i la documentació a la wiki a:

[http://wiki.civicrm.org/confluence/display/CRMDOC/Update+Greetings+and+Address+Data+for+Contacts](http://wiki.civicrm.org/confluence/display/CRMDOC/Update+Greetings+and+Address+Data+for+Contacts)


Impressió de cartes PDF
-----------------------

El flux de treball consisteix en primer lloc en seleccionar els contactes als quals us voleu dirigir, per després imprimir una carta com una acció en lot. Les cartes seran emeses en format PDF, permetent-vos imprimir-les fàcilment.

Per crear la carta:

1.  Aneu a **Cerca > Cerca contactes o Cerca > Cerca avançada**; si el que voleu és imprimir cartes per a membres o per algun grup, aneu a **Contactes > Gestiona grups** i cliqueu a "Contactes" al costat del grup en qüestió.
2.  Inseriu el criteri de cerca i cliqueu Cerca (no és aplicable si utilitzeu un grup).
3.  Seleccioneu els contactes que voleu que rebin la carta.
4.  Des de les accions del menú desplegable, escolliu "Imprimeix una carta PDF per als contactes".
5.  Reviseu les seleccions al Format de pàgina i realitzeu els ajustos necessaris. Aquí és on definireu la mida de la pàgina, els marges i l'orientació de la pàgina.
6.  Inseriu el text i realitzeu Enter your text and make formatting adjustments in the WYSIWYG
    editor. You can also insert image files such as your organisation's
    logo, or a signature. Click in the body of the letter where you want
    the image to appear and click the Image icon. 
7.  You can personalise the letter by using tokens; for example, Postal
    Greeting is a commonly used token in this situation. Click in the
    body of the letter where you want to enter the token. Then click on
    "Insert Tokens" located above the letter at the top right and select
    the desired token.

    ![PostalGreetingToken](../img/CiviCRM_update-CiviCore-PostalGreetingToken-en.png "PostalGreetingToken")

8.  Before you move to the next screen, decide whether the format of
    this letter could be used again. If so, check the Save As New
    Template box and enter a name in the Template Title field.
9.  When your letter is finished, scroll to the bottom and click Make
    PDF Letters.
10. A pop-up window will offer the option of opening or saving the PDF
    (this is the same notification your browser will give you for any
    download). Open the file, review your letters, and then print them,
    or save the PDF and review it at your leisure.

You can use this feature for any kind of document, not only letters. For
example, you could use it to print attendance certificates for a
workshop.

Generate mailing labels
-----------------------

Generating mailing labels is a very easy and useful function.

1.  Perform the search to select the contacts you want to target.
2.  Choose **Mailing Labels** from the **Actions** dropdown menu and
    click Go.
3.  Select the mailing label style
4.  Determine if you want to exclude people with "do not mail" checked
    in their privacy options (checked by default and recommended), and
    whether you want to merge any records with the same mailing address
    into one label.

This last option is very useful when sending a mailing to a households
or organisations where you don't want them to receive duplicate
mailings. When the records are merged, each name at that address is
listed on a separate line on the label.

Your system administrator can configure the fields included in mailing
labels. Read the information on configuring address settings in the
Contacts chapter to learn more about the options.
