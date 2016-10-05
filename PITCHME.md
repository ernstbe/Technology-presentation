## Entwicklung einer Front-End 
### 

#HSLIDE

## Grundstein des Ganzen <img style="width: 50%; margin-top: 50px; border: none; background: none; box-shadow: none;" src="http://www.scala-js.org/assets/img/scala-js-site-logo.svg" />


#VSLIDE

### Im Kern ist Scala.js ein Compiler.
![Scalajs-how-it-works](images/scalajs-how-it-works.png)

#VSLIDE

Ökosystem ?

#VSLIDE

## JavaScript Bibliotheken
![JSFrameworks](images/jsUiFrameworks.png)
 
#VSLIDE

## Scala Bibliotheken
![ScalaFrameworks](images/scalaFrameworks.png)  

#VSLIDE

![AngularJS](images/noAngular.jpg)

#HSLIDE

![React-Logo](images/react-logo-colored.png)

## React(.JS)

#VSLIDE

## Warum React ?

-  Nahe an Bekannter Syntax <!-- .element: class="fragment" -->
-  Re-Render bei jeder Änderung  <!-- .element: class="fragment" -->
-  Htmlcontent wird als Komponenten erzeugt  <!-- .element: class="fragment" -->
-  Templates sind Debugfähig <!-- .element: class="fragment" -->
-  Geschwindigkeit durch Virutellen DOM <!-- .element: class="fragment" -->
-  Server Seitiges Rendering <!-- .element: class="fragment" -->
-  Gute Fehlermeldungen <!-- .element: class="fragment" -->
-  Gute Tesbarkeit durch JavaScript <!-- .element: class="fragment" -->

#VSLIDE

## Was spricht gegen React?

- Benötigt eine Umgebung um eine Vollwertige App zu erstellen <!-- .element: class="fragment" -->
- Sehr steile Lernkurve für Einsteiger <!-- .element: class="fragment" -->


#VSLIDE

![Reactjs](images/reactJS.jpg)

#HSLIDE

Was bietet React.js ?

#VSLIDE

## JSX

(<span style="color:#e49436">J</span>ava<span style="color:#e49436">S</span>cript<span style="color:#e49436">X</span>ML)

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

#VSLIDE

## Virtueller DOM

 Nie wieder ein _"echtes" **DOM**_-Element erstellen
 
 **React übernimmt das! <!-- .element: class="fragment" -->**
 

#VSLIDE

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

#VSLIDE

## Gute Fehlermeldungen
![errorMessages](images/great-error-messages.png)

#VSLIDE

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

#VSLIDE

### Eine **benötigt** Methode :

***<span class="fragment" style="color:#e49436">render()</span>*** 

#VSLIDE

## Props

Das _"externe Interface"_ zu den Komponenten.

**propTypes** erlauben die Validierung des Input

#VSLIDE

## State
Der Interne Komponenten Zustand

 ***<span class="fragment" style="color:#e49436">setState()</span>*** 

Führt zu einem Re-Renderen der Komponenten <!-- .element: class="fragment" -->

#HSLIDE

<img style="width: 30%; border: none; background: none; box-shadow: none;" src="https://facebook.github.io/flux/img/flux_logo.svg" /> 

## Die Flux Struktur 


#VSLIDE

Daten in Flux Apps fließen in eine Richtung

![Flux](images/flux-diagram.png)

#VSLIDE

Die Views lösen bei Userinteraktionen Actions aus

![Flux-with-client-action](images/flux-diagram-with-client-action.png)

#VSLIDE

![Flux-with-background](images/flux-diagram-with-background.png)

#VSLIDE

## Testbarkeit

#HSLIDE

## Danke für Ihre Aufmerksamkeit!
![React-is-the-Force](images/let-the-reactjs.jpg)