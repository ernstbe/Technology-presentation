UI mit Scala.JS und ?

Welches Framework? 

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scala-js.png" />
<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/fragezeichen.png" width="200" />


#HSLIDE

In Verbindung mit Scala.Js stehen eine Menge Frameworks zur Auswahl

#HSLIDE
 
 Erstemal stellt sich die Frage :
  
  Eine JavaScript oder eine Scala Library ? 

#VSLIDE
 
 In der Dokumentation von Scala.js findet man einige beispiele 
 
#VSLIDE
 
 <h2>JavaScript Libaries</h2> 
 
 ![JSFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/jsUiFrameworks.png)
 
#VSLIDE

 <h2>Scala Libaries</h2>
 
 ![ScalaFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scalaFrameworks.png) 


#VSLIDE

AngularJS wurde durch Vorgaben aus der Auswahl entfernt 

![AngularJS](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/noAngular.jpg)

#HSLIDE

Ich entschied mich für eine 2013 von Facebook ins Leben gerufene <i>Javascript-Bibliothek</i>

#HSLIDE

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/react-logo-colored.png" width="420"/>

<h1>React(.JS)</h1>

#VSLIDE

Warum ich mich für React entschieden habe?

<ol>
<li> Nahe an Bekannter Syntax </li>
<li> Leichte 
    <li> Re-Render bei jeder Änderung </li>
    <li> Htmlcontetn wird als Komponenten erzeugt </li>
    <li> Templates sind Debugfähig</li>
    <li> Geschwindigkeit durch Virutellen DOM</li>
    <li> Server Seitiges Rendering</li>
    <li> Gute Fehlermeldungen</li>
</ol>

#VSLIDE

Desweiteren :
 
![ReactJS](http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/reactJS.jpg)


#HSLIDE

Die möglichkeiten die React bietet:

#VSLIDE

<h1>JSX</h1>
Vereinfacht die erstellung der 'Komponenten'

bsp:

#VSLIDE

<h2>Vanilla JS</h2>

```
render: function() {
    React.DOM.div({ className: 'my-thing' },
        React.DOM.a({ href: '/path' },
            'Link: ' + this.props.linkText
        )
    );
}
```

<h2>JSX</h2>

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
