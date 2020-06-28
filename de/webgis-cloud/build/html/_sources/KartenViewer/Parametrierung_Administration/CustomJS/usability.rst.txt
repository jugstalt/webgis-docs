Usability
=========

Einige Features aus API lassen sich sogenannte Usability-Konstante steuern. Diese können natürlich auch über die custom.js für einzelne Karte oder komplette Portalseiten gesetzt werden.

Die ClickBubble dient zur besseren Bedienbarkeit des Viewers auf Touch Geräten. Werkezeuge, die einen Klick in die Karte voraussetzen, (z.B. Identify) sind oft schwer zu bedienen, weil ein Klick mit dem Finger meist zu genau ist. Aktiviert man die ClickBubble erscheint diese bei jedem Werkzeug, das Klick-Interaktion voraussetzt:
 
.. image:: img/image4.png
 
Der Anwender kann jetzt nicht mehr wie gewohnt in die Karte klicken, sondern zieht die Bubble an den gewünschten Ort um eine Aktion auszulösen. Die Spitze markiert dabei den Punkt, für den die Aktion ausgelöst werden soll. Ist die Bubble am gewünschten Ort, kann sie einfach wieder losgelassen werden und kehrt automatisch an den rechten oberen Rand zurück und die Aktion (z.B. Identify) wird gestartet.

Klickt der Anwender auf die Bubble (ohne ziehen) öffnet sich eine Beschreibung, wie diese bedient werden kann.

Manche Werkezuge setzen auch die Möglichkeit einer rechten Maustaste voraus (z.B. das Kontextmenü für den Sketch beim Messen oder Editieren). Dafür gibt es eine weitere Bubble, die aktiviert werden kann. Auf diese kann der Anwender Klicken, um das Kontextmenü zu öffnen. Ebenso kann man diese an eine bestimmte Stelle ziehen, um genau für einen bestimmten Ort das Kontextmenü zu öffnen (z.B. einen bestimmten Vertex verschieben oder löschen, rechtwinklig zu Kante konstruieren, usw.).

.. image:: img/image5.png

Mit diesen Werkzeugen stehen einem versierten Anwender alle Möglichkeiten des Konstruierens (inkl. Snapping) auch auf mobilen Geräten zur Verfügung.

Diese Werkzeuge stehen normalerweise nicht zur Verfügung, sondern müssen über die custom.js  aktiviert werden.

.. code-block :: JavaScript

    // ClickBubble aktiviern 
    webgis.usability.clickBubble = true;
    // ContextMenu Bubble aktiviern
    webgis.usability.contextMenuBubble = true;

Da die Werkzeuge nur Geräten mit Touch Bedienung praktisch sind, kann anstelle von true/false auch die Methode isTouchDevice() verwendet werden:

.. code-block :: JavaScript

    webgis.usability.clickBubble =
    webgis.usability.contextMenuBubble = webgis.isTouchDevice();

Beim Sketch bestand bisher für den Anwender die Möglichkeit, auf einen Vertex zu klicken und so ein Popup Menü zu öffnen:

.. image:: img/image6.png

Dieses ist allerdings nicht mehr notwendig, wenn eine rechte Maustaste bzw. die ContextMenu Bubble zur Verfügung steht. Mit folgender Variable kann dieses Menü trotzdem wieder aktivieren:

.. code-block :: JavaScript

    webgis.usability.sketchMarkerPopup = true;  // Empfehlung: false!!

Ebenfalls ist es oft wünschenswert, dem Anwender weniger Werkzeuge beim Zeichnen anzubieten. So sind die Konstruktionswerkzeuge eher für versierte Anwender und nicht in jeder Karte sinnvoll. Mit folgender Variabel können die Konstruktionswerkzeuge deaktiviert werden:

.. code-block :: JavaScript

    webgis.usability.constructionTools = false;

Das komplette Kontextmenü beim Zeichnen kann man mit:

.. code-block :: JavaScript

    webgis.usability.sketchContextMenu = false;


