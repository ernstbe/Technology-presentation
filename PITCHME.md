#Frontend Framework mit Scala.Js
###Eine Tour durch die möglichkeiten
   
#HSLIDE

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scala-js.png" />

##Grundstein des Ganzen ist Scala.js

#VSLIDE 

Im Kern ist Scala.js ein Scala zu JavaScript Compiler.
Er Compiliert `.scala` Dateien in einzeln optimierte und minimierte `.js` Dateien pro Anwendung

#VSlide

Was dem Entwickler die möglichkeit gibt die mächtigen Sprachfunktionen von Scala zu nutzen. 

#VSLIDE

Bei Scala JS gibt es die möglichkeit ein Scala oder ein Javascript Framework zu verwenden

#VSLIDE 

Ein Compiler wäre aber nichts ohne ein EcoSystem aus Biblioteken und Werkzeugen
Zum Glück deckt Scala.js auch das ab!


#VSLIDE
 
 Da es hier um die erstellung einer Benutzer Oberfläche geht, nur die Relevanten ausschnitte der JS und Scala Bibliotheken aus den Scala.js Docs
 ##JavaScript Libaries
 
 ![JSFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/jsUiFrameworks.png)
 
#VSLIDE

 ##Scala Libaries
 
 ![ScalaFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scalaFrameworks.png) 


#VSLIDE


AngularJS wurde durch Vorgaben aus der Auswahl entfernt 

![AngularJS](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/noAngular.jpg)

#HSLIDE

Die Entscheidung fiel auf die, 2013 von Facebook ins Leben gerufene <i>Javascript-Bibliothek</i>

#HSLIDE

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/react-logo-colored.png" width="420"/>

#React(.JS)

#VSLIDE

Warum React ?

    -  Nahe an Bekannter Syntax
    -  Leichte Handhabung
    -  Re-Render bei jeder Änderung 
    -  Htmlcontent wird als Komponenten erzeugt 
    -  Templates sind Debugfähig
    -  Geschwindigkeit durch Virutellen DOM
    -  Server Seitiges Rendering
    -  Gute Fehlermeldungen

#VSLIDE

Desweiteren :
 
![ReactJS](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/reactJS.jpg)


#HSLIDE

Die möglichkeiten die React bietet:

#VSLIDE

#JSX
(Eine JavaScript Syntax erweiterung welche wie XML aussieht)

Vereinfacht die erstellung der 'Komponenten'

bsp:

#VSLIDE

##Vanilla JS

```
render: function() {
    React.DOM.div({ className: 'my-thing' },
        React.DOM.a({ href: '/path' },
            'Link: ' + this.props.linkText
        )
    );
}
```

##JSX

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

Danke für die Aufmerksamkeit!
