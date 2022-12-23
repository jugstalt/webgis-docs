Tabelle
-------

Hier wird angeführt, welche Felder in der Ergebnisliste angezeigt werden. Damit die Abfrage 
funktioniert, müssen hier Werte eingetragen werden. Eine Ausnahme stellen hier WMS Dienste dar, 
wo das Schema der Daten nicht über die *Capabilities* bekannt ist. Hier kann in der 
Regel keine Tabelle definiert werden.

Hat man beim Erstellen der Abfrage (siehe oben) unter Tabelle ``Felder dynamisch importieren`` 
ausgewählt, befindet sich unter ``Tabelle`` bereits eine *Spalte*:

.. image:: img/queries6.png

Hierbei handelt es sich um einen Sonderfall: Als Feld wird hier ``*`` angeführt, was 
bedeutet, dass die Felder automatisch zur Laufzeit bestimmt werden. Alle Attribute, die von 
einer Abfrage vom *Kartendienst* zurückgeliefert werden können, werden angezeigt.

.. note::
   Diese Option kann auch verwendet werden, wenn bei einem WMS Dienst als ``GetFeatures Type`` 
   beispielsweise ``application/geojson`` oder ``txt/xml`` eingestellt wird. Dann werden auch 
   hier alle Felder in die Tabelle übernommen. Alternativ könnten hier auch die einzelnen 
   Felder manuell angelegt werden.

Möchte man mehr Kontrolle über die Tabelle haben, können hier Felder auch einzeln angeben werden.
Dazu kann der Button ``Mehrere Spalten hinzufügen`` und ``Spalte hinzufügen`` verwendet werden.
Der erste Punkt funktioniert allerdings nur, wenn der zugrunde liegende Dienste auch Auskunft 
über das Datenschema der einzelnen Themen liefert (AGS, IMS, ...).

Wurden Spalten hinzugefügt, kann die Eigenschaften weiter bearbeitet werden:

.. image:: img/queries7.png

Der ``Spalten Typ`` gibt an, was in der Tabellenspalte angezeigt wird. Der Standardwert ist 
hier ``Field``, was bedeutet, dass in der Spalte der Wert eines Attributes des Geo-Objektes angezeigt 
wird. Unter ``Definition / Quelle`` muss für diesen Typ ein Feld aus den Abfragethema angeführt 
werden:

.. image:: img/queries8.png

Wählt man als ``Spalten Typ`` beispielsweise ``Hotlink`` erscheint in der Tabelle ein *Hotlink*, über 
den der Anwender auf eine neue Seite weitergeleitet werden kann. Unter ``Definition / Quelle`` 
kann hier eine ``Hotlink Url`` angegeben werden. In dieser Url können Felder aus dem 
entsprechen Geo-Objekt als Platzhalter (in eckigen Klammern) angeführt werden:

.. image:: img/queries9.png

Unter ``Name / Bezeichnung des Hotlinks`` kann eingetragen werden, mit welchem Text der Hotlink in der 
Tabelle angezeigt wird.

``1:n`` gibt an, ob der Link für alle Zeilen einer Tabelle aufgerufen werden kann. Dabei kann auch ein 
Trennzeichen angegeben werden, mit dem die einzelnen Werte in der Url getrennt werden.

Weiter Spalten Typen sind beispielsweise:

* **Expression:**
  Hier kann ein *Ausdruck* bestehenden aus (mehreren) Feldern und freiem Text angeben werden.
  Die Platzhalter für die Felder werden wieder in eckigen Klammern angegeben, z.B.: ``Fläche: [THE_AREA_FIELD]m²``.

* **ImageExpression:** 
  Wie Hotlink, nur muss die Ziel Url eine Bilddatei sein. Das Bild wird in der Ergebnistabelle 
  angezeigt. Die Größe kann eingestellt werden.

* **EmailAddress, PhoneNumber:** Das Ergebnis wird als anklickbare E-Mail Adresse oder Telefonnummer 
  in der Tabelle dargestellt.

* **DateTime:** Das Ergebnis wird als Datum dargestellt. Unter Definition kann dabei eingestellt 
  werden, wie das Datum formatiert werden soll.

