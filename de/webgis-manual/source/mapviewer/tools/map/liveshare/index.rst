Live Share (Karte *live* teilen)
================================

Mit diesem Werkzeug können Karten in Echtzeit (*live*) geteilt werden. 
Das macht Sinn, wenn alle Teilnehmer gleichzeitig eine WebGIS Karte geöffnet haben und dabei per Telefon/Chat miteinader kommunizieren.

Bei LiveShare Session gibt es zwei unterschiedliche Anwendergruppen:

* **Session Eigentümer:** Der Anwender, die die LiveShare Session startet. Diese kann kann Links und/oder SessionIds verteilen und so anderer Anwender einladen. Bevor ein neuer Anwender der Session beitreten möchte, kann der Session-Eigentümer den Zutritt bestätigen oder ablehnen. Der Session-Eigentümer kann die Session auch wieder beenden. Pro Session gibt es genau einen Eigentümer.

* **Session Teilnehmer:** Session Teilnehmer bekommen von Session Eigentümer einen Link oder eine SessionId. Mit dieses können sie an eine Session Teilnehmen. Pro Session kann es beliebig viele Teilnehmer geben.

Geteilt werden:

* Kartenausschnitt
* Positionsmarker (jeder Teilnehmer kann einen für alle anderen sichtbaren Marker in die Karte setzten, zB die eigene Position)
* Darstellungs-/Themenebenen
* Zeichnungen (Redlining): Alle Teilnehmer können die Zeichnungen des Session-Eigentümers sehen/bearbeiten/ergänzen.

.. note::
   Verteilt der *Session Eigentümer* einen Link zur Session, steigen alle Teilnehmer in der Regel mit die gleiche Karte in die Session ein. Das bedeutet auch, dass alle Eigentümer (abhängig von der Berechtigung) die gleiche Themenebenen sehen.
   Für LiveShare ist es allerdings nicht notwendig, dass alle Teilnehmer in die gleiche Karte einsteigen. Es kann vorkommen, dass nicht alle Teilnehmer zugriff auf die Karte des Session Eigentümers haben (diese kann beispielsweise nur über
   ein Intranet aufgerufen werden). Teilnehmer können dann trotzdem in eine beliebige, für sie zugängliche WebGIS Karte einsteigen (zB unter https://maps.webgiscloud.com) und dort mit der entsprechenden SessionId an der *Live Share Session*
   teilnehmen. In diesem Fall kann dann nur noch der Ausschnitt, Positionsmarker und Zeichnungen (Redlining) geteilt werden (Keine Themenebenen)

.. note::
   LiveShare kann nicht nur von unterschiedlichen Teilnehmern genutzt werden. Manchmal macht es auch Sinn, eine Session nur für den eigenen Gebrauch zu machen. Arbeitet man beispielsweise mit mehreren Bildschirmen, dann man auf jedem
   Bildschirm einen Kartenviewer (eventuell mit unterschiedlichen Kartenebenen) öffnen. Damit beide Kartenviewer immer den gleichen Ausschnitt anzeigen, kann dafür eine "lokale" LiveShare Session verwendet werden.
