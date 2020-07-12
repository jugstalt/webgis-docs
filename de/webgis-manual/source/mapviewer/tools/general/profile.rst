Höhenprofil
===========

Mit diesem Werkzeug keine ein Höhenprofil entlang einer gezeichneten (Poly) Linie erstellt werden.
Im Werkzeugdialog muss bestimmt werden, für welchen Fall (Maßstab/Überhöhung) das Profil erstellt werden sollte.

.. image:: img/profile1.png

.. note::
   Der Maßstab bestimmt dabei in der Regel, wie viele Zwischenpunkte abgefragt werden sollte. Wählt man
   beispielsweise einen sehr großen Maßstab für einen sehr langen Linienzug, kann die Erstellung des Profils sehr lange
   dauern, weil dann sehr viele Zwischenpunkte abgefragt werden. Im schlimmsten Fall ist die Abfrage gar nicht möglich

In der kann jetzt eine Linie mit mehreren Zwischenpunkte erstellt werden.

.. image:: img/profile2.png

Klickt man danach im Werkzeugdialog auf Profil erstellen, wird nach kurzer Berechnungszeit das Höhenprofil
angezeigt:

.. image:: img/profile3.png

.. note:: 
   Ist das Profile zu "ungenau" (hat zu wenige Zwischenpunkte) kann der Profiltype geändert und das Profil neu erstellt werden.

.. note::
   Das im Viewer angezeigte Höhenprofil ist interaktiv. Bewegt man die Maus auf einer der *Höhenpunkte* wird die 
   Höhe als Tooltip angezeigt. Gleichzeigt wir an der entsprechenden Stelle in der Karte auf der gezeichneten 
   Profillinie ein Marker dargestellt.

Über den *Drucken* Button im Werkzeugdialog kann das Profile auch als PDF ausgegeben werden.
Dazu erscheint noch einmal ein Dialog, in dem der Zielmaßstab und die genaue Überhöhung des Profils angegeben 
werden kann:

.. image:: img/profile4.png

Nach erfolgreichem Erstellen der PDF Datei, erscheint eine Vorschau im Druckaufträge Dialog und das Höhenprofil kann
herunter geladen werden:

.. image:: img/profile5.png
