# Library Kata "CLI Table"

Entwickeln sie eine Bibliothek, mit der man auf der Console Daten in einer Tabelle ausgeben kann.

## Anforderungen

* Spalten sollen einen Titel besitzen der vom User festgelegt werden kann
* Spalten sollen eine feste Breite haben. Es gibt eine standard Breite, die aber auch vom User überschrieben werden kann
* Sollte ein Wert die Spaltenbreite überschreiten soll der Wert einfach abgeschnitten werden (siehe Beispiel)
* Die Daten sollen Zeilweisen geliefert werden können
* Die Tabelle soll am Schluss von einer Methode als String zurückgegeben werden
* OPTIONAL: Die Daten sollen Spaltenweise geliefert werden können (siehe Beispiel 2)

## Beispiel

So könnte eine Tabelle dann aussehen

    |--------------|----------------|
    | Spalte 1     | Spalte 2       |
    |--------------|----------------|
    | Wert1        | Wert 2         |
    | zu langer we | wert 4         |
    |--------------|----------------|

## Beispiel 2: Daten Spaltenweise liefern

    $col1 = array('Wert1', 'zu langer wert');
    $col2 = array('Wert 2', 'Wert 4');

    $table->addColumn($col1);
    $table->addColumn($col2);
    echo $table->generate_table();