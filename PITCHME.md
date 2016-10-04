## Frontend Framework mit Scala.Js
### Eine Tour durch die möglichkeiten

#HSLIDE

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scala-js.png" />

## Grundstein des Ganzen ist _**Scala.js**_

#VSLIDE

### Im Kern ist Scala.js ein Scala zu JavaScript Compiler.

Er Compiliert _`.scala`_ Dateien in einzeln optimierte und minimierte _`.js`_ Dateien pro Anwendung

#VSLIDE

Was dem Entwickler die möglichkeit gibt die mächtigen Sprachfunktionen von Scala zu nutzen. 

#VSLIDE

Ein Compiler wäre aber nichts ohne ein EcoSystem aus Biblioteken und Werkzeugen

Zum Glück deckt Scala.js auch das ab!

#VSLIDE

Bei Scala.js gibt es die möglichkeit Scala oder ein Javascript Frameworks einzubinden

#VSLIDE
 
Da es hier um die erstellung einer UI geht
hier nur die Relevanten ausschnitte der JS und Scala Bibliotheken aus den Scala.js Docs

## JavaScript Libaries
![JSFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/jsUiFrameworks.png)
 
#VSLIDE

## Scala Libaries
![ScalaFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scalaFrameworks.png) 


#VSLIDE

**AngularJS** wurde durch Vorgaben aus der Auswahl ausgeschloßen 

![AngularJS](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/noAngular.jpg)


#HSLIDE

Die Entscheidung fiel auf die, 2013 von Facebook ins Leben gerufene <i>Javascript-Bibliothek</i>

#HSLIDE

![ReactLogo](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/react-logo-colored.png)

## React(.JS)

#VSLIDE

## Warum React ?

-  Nahe an Bekannter Syntax 
-  Leichte Handhabung
-  Re-Render bei jeder Änderung 
-  Htmlcontent wird als Komponenten erzeugt 
-  Templates sind Debugfähig
-  Geschwindigkeit durch Virutellen DOM
-  Server Seitiges Rendering
-  Gute Fehlermeldungen

#VSLIDE

![ReactJS](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/reactJS.jpg)

#HSLIDE

Ein näherer Blick auf die Möglichkeiten die React bietet:

#VSLIDE

## JSX

(Eine JavaScript Syntax erweiterung welche wie XML aussieht)

Vereinfacht die erstellung der 'Komponenten'

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
![errorMessages](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/great-error-messages.png)

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

#### setState() <!-- .element: class="fragment" -->

Führt zu einem Re-Renderen der Komponenten <!-- .element: class="fragment" -->

#HSLIDE

## Danke für Ihre Aufmerksamkeit!
