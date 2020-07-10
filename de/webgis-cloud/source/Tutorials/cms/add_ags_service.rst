ArcGIS Server Dienst einbinden
==============================

Dazu im CMS Baum auf ``Dienste/ArcGIS Server/MapServer Dienst`` wechseln:

.. image:: img/image120.png

Auf ``Neuen Dienst einbinden`` klicken:

.. image:: img/image121.png

Danach auf ``Services Aktualisieren`` klicken, einen Namen vergeben und auf ``Übernehmen`` klicken

**Hinweis:** Wird der Name im Falle von AGS in der MXD gepflegt, wir auch dieser schon automatisch übernommen. Wird dieser nicht gepflegt, seht als Name im Dienst Layer oder Layers => wird nicht ins CMS übernommen => zu Allgemein


Das Übernehmen kann einige Sekunden dauern. Danach kann man in der Ansicht auf den Dienst klicken und kann so noch weitere Eigenschaften des Dienstes bearbeiten:

.. image:: img/image123.png

.. image:: img/image124.png


**Export Map Format:**
Im Normalfall liefert der AGS das Ergebnis eines Kartenrequest im JSON Format zurück. Darin steht dann die Url zum eigentlichen Bild im Output Verzeichnis. In unserem Fall wird das Bild im Outputverzeichnis hinter unserer Filewall abgelegt und ist NICHT über das Internet erreichbar. Das Kartenbild würde somit zwar erstellt werden, ist aber für den Browser nicht erreichbar.
Abhilfe für dieses Problem schafft der Wert „Image“. Dabei kommt das Ergebnis vom AGS nicht als JSON sondern als Bild (Bytes). Dieses nimmt WebGIS direkt in Empfang und legt es ins „Cloud“ – Output verzeichnis ab, das über das Internet verfügbar ist.
Diese Methode hat in der Cloud auch den Vorteil, dass über das Internet nicht nachvollzogen werden kann, woher der Kartendienst kommt. 
Client (Broser) <-> WebGIS <-> ArcGIS Server



**Achtung:** Für eine beim Kunden installierte WebGIS Instanz sollte dieser Werte in der Regel leer bzw auf JSON gestellt werden, weil ein Client meistens Zugriff auf das Output Verzeichnis hat. So folgt in der Regel weniger Trafik:
1.	Client (Browser) <-> WebGIS <-> ArcGIS Server (ImageRequest/JSON)
2.	Client (Browser)            <->           Output Verzeichnis


