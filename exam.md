# FOP WiSe 2022/2023 (20-00-0004)
## Informationen
- Bearbeitungszeit: 2,5 Stunden
## Frage 1
Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie ein generisches Functional public-Interface X mit einem generischen Typparameter A und mit zwei Methoden. Der generischeTypparameter A ist sowohl auf die Klasse Canvas und alle Subtypen von Canvas als auch auf das Interface IntPredicate und alle Subtypen von IntPredicate beschränkt.

Default-Methode def: ist generisch mit einem generischen Typparameter B, der auf Component und die Subtypen von Component beschränkt ist; liefert true oder false zurück; hat einen Parameter x vom generischen Typ LinkedList, wobei der generische Typparameter von LinkedList auf Integer und alle Supertypen von Integer beschränkt ist; hat einen zweiten Parameter y vom Typ B. Die Rückgabe ist genau dann true, wenn x auf ein Objekt verweist. Falls x auf ein Objekt verweist, soll def zudem Folgendes tun: Falls der dynamische Typ von y gleich Canvas oder ein Subtyp von Canvas ist, soll +1 in x eingefügt werden, andernfalls -1.

Funktionale Methode fct: hat einen Parameter op vom formalen Typ "BiFunction von A und Integer nach Double", einen Parameter a mit formalem Typ A sowie Rückgabetyp Double.

Hinweis: Sie müssen hier Restricted Genericity von Wildcards unterscheiden.

Erinnerung: Methode add von LinkeldList fügt ihren Parameter ein; Sie können add als void-Methode verwenden. Interface BiFunction hat drei generische Typparameter A, B und C (in dieser Reihenfolge) und repräsentiert mathematische Funktionen A×
B→C.
## Frage 2
Wiederholung aus Teilaufgabe (a): Der generische Typparameter von Interface X heißt A und ist sowohl auf Canvas als auch auf IntPredicate sowie deren beider Subtypen beschränkt. Methode fct von X hat einen Parameter op vom formalen Typ "BiFunction von A und Integer nach Double", einen Parameter a vom formalen Typ A sowie Rückgabetyp Double.


Ab hier neue Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie eine public-Klasse Y, die das Interface X mit denselben Einschränkungen von A wie bei X sowie außerdem das generische funktionale Interface Consumer aus der Java-Standardbibliothek implementiert, wobei der generische Typparameter von Consumer mit A instanziiert sein soll.

Methode fct von Y wendet Methode apply von op auf a und +2 an und liefert das Ergebnis zurück. Methode accept von Consumer ist in Y nicht implementiert.
## Frage 3
Wiederholung aus Teilaufgabe (a): Der generische Typparameter von X heißt A und ist auf Canvas und IntPredicate sowie deren beider Subtypen beschränkt.


Ab hier neue Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie eine public-Klasse Z, die direkt von Y\<A> abgeleitet ist mit denselben Einschränkungen von A wie bei X. Klasse Z hat ein private-Objektattribut a vom Typ A. Implementieren Sie die Methode accept von Consumer so, dass sie ihren aktualen Parameter dem Objektattribut a zuweist.

Erinnerung: Methode accept von Consumer hat einen Parameter mit seinem generischen Typ als formalem Parametertyp und keine Rückgabe.
## Frage 4
Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Gegeben seien eine direkt von Klasse Exception abgeleitete Klasse Exc1 und eine von Exc1 direkt abgeleitete Klasse Exc2. Dabei habe Exc1 einen public-Konstruktor mit einem Parameter vom formalen Typ int; Exc2 habe einen public-Konstruktor mit einem Parameter vom formalen Typ char.


Ab hier Aufgabe:

Schreiben Sie eine public-Klasse Exc3, die direkt von Exc1 abgeleitet ist. Klasse Exc3 soll einen public-Konstruktor mit einem Parameter supp vom formalen Typ Supplier\<String> haben. Falls supp gleich null ist oder -- im Fall ungleich null -- die parameterlose Methode get von supp den Wert null zurückliefert, soll der Konstruktor von Exc3 den Konstruktor von Exc1 mit 0 aufrufen, andernfalls mit 1.

Hinweis: Wie Sie wissen, darf super nur einmal aufgerufen werden. Sie müssen also die Fallunterscheidung in den aktualen Parameter von super integrieren.
## Frage 5
Wiederholung aus Teilaufgabe (a): Exc1 ist direkt von Exception, und Exc2 und Exc3 sind direkt von Exc1 abgeleitet. Klasse Exc1 hat einen  public-Konstruktor mit einem Parameter vom formalen Typ int, Exc2 einen mit einem Parameter vom formalen Typ char und Exc3 einen mit einem Parameter vom formalen Typ Supplier\<String>.


Ab hier neue Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie eine public-Klassenmethode m mit Rückgabetyp char, einem Parameter ch vom formalen Typ Optional\<Character> und einem Parameter supp vom formalen Typ Supplier\<String>. Die Klasse, zu der m gehört, müssen Sie nicht schreiben.

Falls ch oder supp nicht auf ein Objekt verweist (inklusiv-oder), soll m eine Exc1 mit aktualem Parameterwert 3 für den Konstruktor werfen. Andernfalls: Falls ch leer ist, wirft m eine Exc2, wobei der Konstruktor von Exc2 mit 'a' aufgerufen wird. Im verbliebenen Fall soll Folgendes passieren: Falls ch das Zeichen 'b' einkapselt, soll m eine Exc3 mit supp werfen; andernfalls liefert m das in ch enthaltene Zeichen zurück.

Erinnerung: Klasse Optional\<T> hat eine parameterlose boolesche Methode isEmpty sowie eine parameterlose Methode get, die bei einem nichtleeren Optional-Objekt einen Verweis auf das enthaltene T-Objekt zurückliefert. Die parameterlose Methode charValue von Character liefert das eingekapselte Zeichen zurück.
## Frage 6
Wiederholung aus Teilaufgabe (a) und (b): Exc1 ist direkt von Exception, und Exc2 und Exc3 sind direkt von Exc1 abgeleitet. Klasse Exc1 hat einen public-Konstruktor mit einem Parameter vom formalen Typ int, Exc2 einen mit einem Parameter vom formalen Typ char und Exc3 einen mit einem Parameter vom formalen Typ Supplier\<String>. Die Klassenmethode m aus Teilaufgabe (b) hat Rückgabetyp char, einen Parameter vom formalen Typ Optional\<Character> und einen zweiten Parameter vom formalen Typ Supplier\<String>.


Ab hier neue Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie eine public-Objektmethode m2, die keine Rückgabe und einen Parameter supp vom formalen Typ Supplier\<String> hat. Methode m2 gehört nicht zur selben Klasse wie Methode m. Die Klasse, zu der m gehört, heiße Y. Die Klasse, zu der m2 gehört, müssen Sie nicht schreiben.

In m2 wird die Methode m aus Teilaufgabe (b) aufgerufen. Der erste aktuale Parameter bei diesem Aufruf ist nicht leer und enthält 'c'; der zweite aktuale Parameter ist einfach supp. Falls m bei diesem Aufruf eine Exc2 wirft, soll m2 eine Exc3 mit supp werfen.  Falls hingegen m eine Exc3 wirft, soll m2 eine Exc2 mit 'd' werfen.  Falls m schließlich eine Exc1 wirft, soll diese von m2 weitergereicht werden, ohne dass m2 sie fängt. Die Rückgabe von m wird nicht verwendet und darf ignoriert werden.

Erinnerung: Klassenmethode ofNullable von Optional\<T> erzeugt ein Optional\<T>-Objekt mit ihren Parameter vom formalen Typ T.
## Frage 7
Folgende Funktion foo in Racket erstellt eine bestimmte Konkatenation von lst1 und lst2. Konkret kommen in der Ergebnisliste zuerst alle Elemente von lst1 in derselben Reihenfolge wie in lst1. Danach kommen alle Elemente von lst2, aber in umgekehrter Reihenfolge gegenüber lst2.
```
  ( define ( bar lst lst-reversed )
       ( cond
            [  ( empty? lst )  lst-reversed  ]
            [  else  ( bar ( rest lst ) ( cons ( first lst )  lst-reversed ) )  ]  ) )

  ( define  ( foo lst1 lst2 )
       ( cond
           [  ( empty? lst1 )  ( bar lst2 empty )  ]
           [  else  ( cons ( first lst1 ) ( foo ( rest lst1 ) lst2 ) )  ]  ) )
```
Folgende Klasse kennen Sie aus der Vorlesung und den Übungen:
```
     public class ListItem <T> {
        public T key;
        public ListItem<T> next;
     }
```
Ab hier Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie in Java public-Objektmethoden foo und bar analog zum Racket-Code oben. Diese beiden Methoden gehören zur selben Klasse, und diese Klasse ist generisch mit generischem Typparameter T (diese Klasse müssen Sie nicht selbst schreiben). Die formalen Parametertypen sowie die Rückgabetypen von foo und bar sind allesamt ListItem\<T>.  Sie können davon ausgehen, dass die beiden aktualen Parameter von foo auf korrekt gebildete lineare Listen verweisen (die auch leer, also gleich null sein können).

Verbindliche Anforderungen:

- Die Methoden foo und bar sind rein rekursiv, das heißt, Schleifen sind nicht erlaubt.
- Übersetzungen in andere Datenstrukturen (Arrays, Streams etc.) sind nicht erlaubt.
- Die Eingabelisten lst1 und lst2 von foo dürfen in foo und bar nicht verändert werden, das heißt, Sie müssen die ListItem\<T>-Objekte in der Ergebnisliste mit Operator new erzeugen (die key-Werte dürfen Sie hingegen mit "=" zuweisen).
## Frage 8
Wiederholung aus Teilaufgabe (a): Folgende Funktion foo in Racket erstellt eine bestimmte Konkatenation von lst1 und lst2. Konkret kommen in der Ergebnisliste zuerst alle Elemente von lst1 in derselben Reihenfolge wie in lst1. Danach kommen alle Elemente von lst2, aber in umgekehrter Reihenfolge gegenüber lst2.
```
  ( define ( bar lst lst-reversed )
       ( cond
            [  ( empty? lst )  lst-reversed  ]
            [  else  ( bar ( rest lst ) ( cons ( first lst )  lst-reversed ) )  ]  ) )

  ( define  ( foo lst1 lst2 )
       ( cond
          [  ( empty? lst1 )  ( bar lst2 empty )  ]
          [  else  ( cons ( first lst1 ) ( foo ( rest lst1 ) lst2 ) )  ]  ) )
```
Folgende Klasse kennen Sie aus der Vorlesung und den Übungen:
```
public class ListItem <T> {
    public T key;
    public ListItem<T> next;
}
```

Ab hier neue Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie in Java public-Objektmethoden foo und bar analog zum Racket-Code oben. Beachten Sie, dass, abweichend vom Racket-Code, kein zweiter Parameter lstReversed für bar notwendig ist und daher auch nicht sein soll (lstReversed richten Sie stattdessen als leere Liste in bar ein). Die beiden Methoden foo und bar gehören zur selben Klasse, und diese Klasse ist generisch mit Typparameter T (diese Klasse müssen Sie nicht selbst schreiben). Die formalen Parametertypen sowie die Rückgabetypen von foo und bar sind allesamt ListItem\<T>.  In foo verwalten Sie zwei Verweise, head und tail, auf Anfang und Ende der Ergebnisliste (natürlich nur, falls die Ergebnisliste nicht leer ist). Sie können davon ausgehen, dass die beiden aktualen Parameter von foo auf korrekt gebildete lineare Listen verweisen (die auch leer, also gleich null sein können).

Verbindliche Anforderungen:

- Die Methoden foo und bar sind rein iterativ, das heißt, Rekursion ist nicht erlaubt.
- Übersetzungen in andere Datenstrukturen (Arrays, Streams etc.) sind nicht erlaubt.
- Die Eingabelisten lst1 und lst2 von foo dürfen in foo und bar nicht verändert werden, das heißt, Sie müssen die ListItem\<T>-Objekte in der Ergebnisliste mit Operator new erzeugen (die key-Werte dürfen Sie hingegen mit "=" zuweisen).
## Frage 9
Wiederholung aus Teilaufgabe (a)+(b): Folgende Funktion foo in Racket erstellt eine bestimmte Konkatenation von lst1 und lst2. Konkret kommen in der Ergebnisliste zuerst alle Elemente von lst1 in derselben Reihenfolge wie in lst1. Danach kommen alle Elemente von lst2, aber in umgekehrter Reihenfolge gegenüber lst2.
```
  ( define ( bar lst lst-reversed )
       ( cond
            [  ( empty? lst )  lst-reversed  ]
            [  else  ( bar ( rest lst ) ( cons ( first lst )  lst-reversed ) )  ]  ) )

  ( define  ( foo lst1 lst2 )
       ( cond
           [  ( empty? lst1 )  ( bar lst2 empty )  ]
           [  else  ( cons ( first lst1 ) ( foo ( rest lst1 ) lst2 ) )  ]  ) )
```
Ab hier neue Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie in Java public-Objektmethoden foo und bar analog zum Racket-Code oben. Beachten Sie, dass, abweichend vom Racket-Code, bar keine Rückgabe benötigt und daher auch keine haben soll, denn der zweite aktuale Parameter soll schon bei Aufruf von bar die Kopie von lst1 enthalten. Diese Kopie von lst1 wird in foo vor Aufruf von bar erstellt. Zum Einfügen an der richtigen Position im zweiten Parameter richten Sie in bar als erstes eine Konstante lengthOfLst1 ein, die - wie der Name schon sagt - die Länge von lst1 enthalten soll. Die beiden Methoden foo und bar gehören zur selben Klasse (diese Klasse müssen Sie nicht selbst schreiben). Die formalen Parametertypen von foo und bar sowie der Rückgabetyp von foo sind allesamt List\<T> (gemeint ist java.util.List). Der dynamische Typ der Rückgabe von foo soll LinkedList\<T> sein (java.util.LinkedList). Sie können davon ausgehen, dass die beiden aktualen Parameter von foo nicht null sind (aber auf leere Listen verweisen können).

Verbindliche Anforderungen:

- Auf die Elemente von lst1 und lst2 wird ausschließlich mit Iteratoren zugegriffen, auch clone o.ä. ist nicht erlaubt.
- Listen dürfen nicht in andere Datenstrukturen kopiert werden (z.B. mit Methode toArray oder Methode stream).

Erinnerung: Interface List\<T> hat eine parameterlose Objektmethode size, eine parameterlose Objektmethode iterator mit Rückgabetyp Iterator\<T>, eine Objektmethode add mit einem Parameter vom Typ T sowie eine weitere Objektmethode add mit einem Parameter vom formalen Typ int (der Index) und einen zweiten Parameter vom formalen Typ T. Die erste Methode add fügt ihren Parameter hinten an die Liste an. Die zweite Methode add fügt ihren zweiten aktualen Parameter am Index ein, wobei sich die Indizes (=Positionen) aller nachfolgenden Elemente um 1 erhöhen. Klasse Iterator\<T> hat zwei parameterlose Methoden hasNext und next, wobei hasNext Rückgabetyp boolean und next Rückgabetyp T hat. Klasse LinkedList\<T> hat einen parameterlosen Konstruktor.
## Frage 10
Gegeben sei folgende Funktion in Racket:
```
        ( define ( foobar bar foo t1 t2 )
               ( lambda ( x y ) ( bar ( foo x y ) t1 t2 ) ) )
```
Wie Sie sehen, sind foo und bar Funktionen. Gegeben sei zudem der folgende beispielhafte Aufruf von foobar:
```
     ( ( foobar ( lambda ( c d e ) ( and ( < c d ) ( < c e ) ) )
                    ( lambda ( a b ) ( * ( first a ) ( first b ) ) )
                    3 5 )
       lst1 lst2 )
```
Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie in Java ein nichtgenerisches funktionales public-Interface Foo mit funktionaler Methode apply, das auf foo passt, wobei Integer der Zahlentyp und List\<Integer> der Listentyp ist.

Schreiben Sie zudem eine nichtgenerische public-Klasse MyFoo, die Foo implementiert und dasselbe Ergebnis zurückliefert wie der Lambda-Ausdruck für foo im obigen beispielhaften Aufruf.

Erinnerung: Klasse Integer hat eine parameterlose Methode intValue. Methode get von List liefert das Listenelement an der im aktualen Parameter angegebenen Position zurück, wobei Positionen wie üblich mit 0 beginnen.
## Frage 11
Wiederholung aus Teilaufgabe (a):

Gegeben sei folgende Funktion in Racket:
```
    ( define ( foobar bar foo t1 t2 )
          ( lambda ( x y ) ( bar ( foo x y ) t1 t2 ) ) )
```
Wie Sie sehen, sind foo und bar Funktionen. Gegeben sei zudem der folgende beispielhafte Aufruf von foobar:
```
    ( ( foobar ( lambda ( c d e ) ( and ( < c d ) ( < c e ) ) )
                   ( lambda ( a b ) ( * ( first a ) ( first b ) ) )
                   3 5 )
      lst1 lst2 )
```
Ab hier Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie in Java ein generisches funktionales public-Interface Bar mit generischem Typparameter T, das auf bar passt, wobei die funktionale Methode test heißen soll. Alle Parameter von test sind vom formalen Typ T, und Rückgabetyp von test ist boolean.

Schreiben Sie zudem in Java eine nichtgenerische public-Klasse MyBar, die Bar mit Instanziierung Integer implementiert und dasselbe Ergebnis zurückliefert wie der Lambda-Ausdruck für bar im obigen beispielhaften Aufruf.

Erinnerung: Klasse Integer hat eine parameterlose Methode intValue.
## Frage 12
Wiederholung aus Teilaufgabe (a)+(b):

Gegeben sei folgende Funktion in Racket:
```
    ( define ( foobar bar foo t1 t2 )
          ( lambda ( x y ) ( bar ( foo x y ) t1 t2 ) ) )
```
Wie Sie sehen, sind foo und bar Funktionen. Gegeben sei zudem der folgende beispielhafte Aufruf von foobar:
```
    ( ( foobar ( lambda ( c d e ) ( and ( < c d ) ( < c e ) ) )
                   ( lambda ( a b ) ( * ( first a ) ( first b ) ) )
                   3 5 )
      lst1 lst2 )
```
Ab hier Aufgabe:

Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie in Java eine public-Klassenmethode foobar, die auf Basis von Foo und  Bar die obige Racket-Funktion foobar eins-zu-eins nach Java übersetzt. Die Klasse, zu der foobar gehört, heißt X, die müssen Sie aber nicht schreiben. Weder X noch foobar ist generisch. Rückgabetyp von foobar ist BiFunction mit passenden Typparametern (gemeint ist java.util.function.BiFunction). Zahlentyp ist Integer und Listentyp ist List\<Integer>.

Schließlich übersetzen Sie den obigen beispielhaften Racket-Ausdruck nach Java.

Verbindliche Anforderung: Alle drei Lambda-Ausdrücke im obigen Racket-Code müssen in Lambda-Ausdrücke in Java übersetzt werden.

Erinnerung: Die Java-Interfaces Foo und Bar aus den Teilaufgaben (a) und (b) passen auf foo und bar im obigen beispielhaften Aufruf. Die funktionalen Methoden von Foo und Bar heißen apply bzw. test. Zahlentyp ist Integer und Listentyp ist List\<Integer>. Methode get von List liefert das Listenelement an der im aktualen Parameter angegebenen Position zurück, wobei Positionen wie üblich mit 0 beginnen. Interface BiFunction hat drei generische Typparameter A, B und C (in dieser Reihenfolge) und repräsentiert mathematische Funktionen A×B→C. Die funktionale Methode von BiFunction heißt apply. Klasse Integer hat eine parameterlose Methode intValue.
## Frage 13
Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie eine public-Klassenmethode foobar, die zwei Parameter a und b vom Typ "Array von String" und Rückgabetyp "Array von char" hat (die Klasse, zu der foobar gehört, müssen Sie nicht schreiben). Ihre Methode foobar kann ohne Prüfung davon ausgehen, dass a und b auf String-Arrays mit Länge größer 0 verweisen und dass jede Komponente von a und b auf jeweils einen String mit Länge größer 0 verweist.

Für jeden Index i in der Schnittmenge der Indexbereiche von a und b (also für jedes i ∈{0,…,min{
a.length,b.length}}), an dem das erste Zeichen dieser beiden Strings dasselbe ist, enthält das zurückgelieferte Array eine Komponente mit diesem Zeichen als Inhalt. Die Reihenfolge dieser Komponenten ist dieselbe wie in a und b. Darüber hinaus enthält das zurückgelieferte Array keine Komponenten.

Beispiel: a=[vw,wx,xy,wx,z], b=[vz,xw,xy,w,vz,zx,yv]⟶[v,x,w]



Verbindliche Anforderungen:

- Lösen Sie die oben genannte Aufgabe rein iterativ, das heißt, Rekursion ist nicht erlaubt.
- Sie müssen auf Arrays arbeiten. Streams, Listen usw. sind nicht erlaubt.

Erinnerung: Arraytypen haben eine Klassenkonstante length. Klasse String hat eine Objektmethode charAt, die einen Index des Strings (wie üblich beginnend mit 0) als Parameter haben soll und das Zeichen an diesem Index als char zurückliefert.
## Frage 14
Sie brauchen keine import- oder package-Anweisungen zu schreiben.

Schreiben Sie eine public-Klassenmethode foobar, die zwei Parameter a und b vom Typ "Array von String" und Rückgabetyp "Array von char" hat (die Klasse, zu der foobar gehört, müssen Sie nicht schreiben). Ihre Methode foobar kann ohne Prüfung davon ausgehen, dass a und b auf String-Arrays mit Länge größer 0 verweisen und dass jede Komponente von a und b auf jeweils einen String mit Länge größer 0 verweist.

Für jeden Index i in der Schnittmenge der Indexbereiche von a und b (also für jedes i ∈{0,…,min{
a.length-1,b.length-1}}), an dem das erste Zeichen dieser beiden Strings dasselbe ist, enthält das zurückgelieferte Array eine Komponente mit diesem Zeichen als Inhalt. Die Reihenfolge dieser Komponenten ist dieselbe wie in a und b. Darüber hinaus enthält das zurückgelieferte Array keine Komponenten.

Beispiel: a=[vw,wx,xy,wx,z], b=[vz,xw,xy,w,vz,zx,yv]⟶[v,x,w]



Verbindliche Anforderungen:

- Lösen Sie die oben genannte Aufgabe rein rekursiv, das heißt, Schleifen sind nicht erlaubt.
- Sie müssen auf Arrays arbeiten. Streams, Listen usw. sind nicht erlaubt.

Für die Länge des zurückzuliefernden Arrays schreiben Sie eine rekursive private-Hilfsmethode foo, die a und b sowie ein int namens index als Parameter hat und die Anzahl der Indizes größer/gleich index in a und b zurückliefert, von denen das erste Zeichen in das Ergebnisarray gemäß obiger Spezifikation zu übernehmen ist.

Für die Befüllung des zurückzuliefernden Arrays mit Zeichen schreiben Sie eine rückgabelose rekursive private-Hilfsmethode bar mit a und b, einem char-Array result sowie zwei int namens indexInAAndB und indexInResult als Parametern. Dabei soll indexInResult immer der jeweils nächste Index in result sein, an den ein Zeichen zu kopieren ist.

Erinnerung: Arraytypen haben eine Klassenkonstante length. Klasse String hat eine parameterlose Objektmethode charAt, die einen Index des Strings (wie üblich beginnend mit 0) als Parameter haben soll und das Zeichen an diesem Index als char zurückliefert.
## Frage 15
Aus der Vorlesung kennen Sie die Racket-Funktionen foldl und foldr sowie unseren Nachbau my-fold von foldr, alle drei vom Typ ( X Y -> Y ) Y ( list of X ) -> Y.

Ebenso haben Sie in der Vorlesung eine beispielhafte Anwendung von my-fold auf X = student und Y = natural gesehen, wobei student ein Struct mit einem natural-Attribut für die Studiengebührenhöhe dieses/dieser Studierenden ist und die Studiengebührenhöhen aller Studierenden durch my-fold aufsummiert werden.

Erläutern Sie in eigenen Worten, was der erste Parameter macht und welchen Wert der zweite Parameter hat, (i) am oben genannten Beispiel, (ii) in abstrakten Formulierungen unabhängig von allen Anwendungsbeispielen.
## Frage 16
Wie Sie aus der Vorlesung wissen, kann man eine Variable x im Kopf einer for-Schleife F1 definieren, nämlich vor dem ersten Semikolon in der runden Klammern nach Schlüsselwort for. Was ist der Scope dieser Definition von x? Unter welchen Umständen darf der Identifier x in einer anderen for-Schleife F2 aufgrund dieser Definition in F1 nicht nochmals definiert werden?
## Frage 17
Aus der Vorlesung kennen Sie BufferedReader und BufferedWriter in Package java.io. Was tragen diese beiden Klassen zum Einlesen aus bzw. Hinausschreiben in Textdateien bei? Das heißt, erläutern Sie konkret, was mit gepufferter Ein- bzw. Ausgabe gemeint ist.
 
Hinweis: Möglicherweise wird das Formulieren einfacher, wenn Sie Ihre Antwort für BufferedReader und BufferedWriter jeweils separat formulieren, auch wenn vielleicht einzelne Textbausteine dann doppelt vorkommen.
## Frage 18
Aus der Vorlesung kennen Sie die Idee, eine Klasse für Vögel zu schreiben, dieser Klasse Funktionalität für das Fliegen zu geben und für alle Arten, Gattungen, Familien usw. von Vögeln jeweils Klassen direkt oder indirekt von der Klasse für Vögel abzuleiten. Was ist das Problem dabei und warum ist das ein Verstoß gegen das Liskov Substitution Principle?
