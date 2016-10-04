## Front End mit Scala.Js
### 

#HSLIDE

![Scala-Js](images/scala-js.png)

## Grundstein des Ganzen ist _**Scala.js**_

#VSLIDE

### Im Kern ist Scala.js ein Scala zu JavaScript Compiler.

Er Compiliert _.scala_ Dateien in einzeln optimierte und minimierte _.js_ Dateien pro Anwendung

#VSLIDE

Was dem Entwickler die Möglichkeit gibt die mächtigen Sprachfunktionen von Scala zu nutzen

#VSLIDE

Ein Compiler wäre aber nichts ohne ein Ökosystem aus Bibliotheken und Werkzeugen

Zum Glück deckt Scala.js auch das ab!

#VSLIDE

Bei Scala.js gibt es die Möglichkeit Scala oder ein Javascript Libraries einzubinden

#VSLIDE
 
Da es hier um die Erstellung einer UI geht
hier nur die Relevanten Ausschnitte der JS und Scala Bibliotheken aus den Scala.js Docs

## JavaScript Libraries
![JSFrameworks](images/jsUiFrameworks.png)
 
#VSLIDE

## Scala Libraries
![ScalaFrameworks](images/scalaFrameworks.png)  

#VSLIDE

**AngularJS** wurde durch Vorgaben aus der Auswahl ausgeschlossen 

![AngularJS](images/noAngular.jpg)

#HSLIDE

Die Entscheidung fiel auf die, 2013 von Facebook ins Leben gerufene <i>Javascript-Bibliothek</i>

#HSLIDE

![React-Logo](images/react-logo-colored.png)

## React(.JS)

#VSLIDE

## Warum React ?

-  Nahe an Bekannter Syntax 
-  Re-Render bei jeder Änderung 
-  Htmlcontent wird als Komponenten erzeugt 
-  Templates sind Debugfähig
-  Geschwindigkeit durch Virutellen DOM
-  Server Seitiges Rendering
-  Gute Fehlermeldungen

#VSLIDE

![ReactJS](images/reactJS.jpg)

#HSLIDE

Ein näherer Blick auf die Möglichkeiten die React bietet:

#VSLIDE

## JSX

(Eine JavaScript Syntax Erweiterung welche wie XML aussieht)

Vereinfacht die Erstellung der 'Komponenten'

#VSLIDE

### Vanilla JS
```
render: function() {
    React.DOM.div({ className: 'my-thing' },
        React.DOM.a({ href: '/path' },
            'Link: ' + this.props.linkText
        )
    );
}
```

### JSX
```
render: function() {
    return (
        <div className="my-thing">
            <a href="/path">
                Link: {this.props.linkText}
            </a>
        </div>
    );
}
```

#HSLIDE

## Virtueller DOM

 Nie wieder eine _"echtes" **DOM**_-Element erstellen
 
 React übernimmt das! <!-- .element: class="fragment" -->

#VSLIDE

### "VDOM"-abgleich

Unterscheidet virtuelle Nodes

(vergleicht JS Objekte)


#VSLIDE

### "VDOM"-abgleich

Transparent für den Entwickler 

"Hier ist ein neuer Zustand , rendere ihn"

#HSLIDE

### Server-   <!-- .element: class="fragment" -->

### seitiges  <!-- .element: class="fragment" -->

### Rendering <!-- .element: class="fragment" -->

#VSLIDE

### Es ist alles Virtuell!
```
var EventList = require('path/to/event-list-component');
var SomeApi = require('path/to/some-api');
var Server = require('someHttpServer').listen(80);

Server.on('request', function(req, res) {

    SomeApi.getEvents(req.params.matchId)
        .then(function(err, events) {
            var html = React.renderComponentToString(
                new EventList({ events: events })
            );
    
            res.send(html);
        });
});
```

#HSLIDE

### Es ist alles Virtuell!

Die Client Seite kann nun den tree ändern
und damit fortfahren den Status bei Änderungen zu 
Aktualisierung

#HSLIDE

## Gute Fehlermeldungen
![errorMessages](images/great-error-messages.png)

#HSLIDE

## Automatisch gebundene Funktionen
```
React.createClass({
    onClick: function(e) {
        // "this" bezieht sich auf die Komponente
        this.setState({ clicked: true });
    },

    render: function() {
        return <button onClick={this.onClick} />;
    }
});
```

#HSLIDE

### Man **benötigt** nur **eine** Methode :

#### render() <!-- .element: class="fragment" -->

#HSLIDE

## Props

Das _"externe Interface"_ zu den Komponenten.

**propTypes** erlauben die Validierung des Input

#HSLIDE

## State
Der Interne Komponenten Zustand

#### <span class="fragment" style:="color:#e49436">setState()</span> 

Führt zu einem Re-Renderen der Komponenten <!-- .element: class="fragment" -->

#HSLIDE

## Was spricht gegen React?

- Benötigt Verständnis der Flux Struktur
- Benötigt zusätzliche Libraries um eine Vollwertige App zu erstellen
- Sehr steile Lernkurve für Einsteiger


#HSLIDE

## Danke für Ihre Aufmerksamkeit!