UI mit Scala.JS
Welches Framework? 

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scala-js.png" />
<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/add.png" width="200" />
<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/fragezeichen.png" width="200" />


#HSLIDE

In Verbindung mit Scala.Js stehen eine Menge Frameworks zur Auswahl

#HSLIDE
 
 Erstemal stellte sich die Frage :
  
  Ein JavaScript oder eine Scala Library ? 

#VSLIDE
 
 Schaut man sich die Dokumentation von Scala.js an sieht man wie viele es gibt aber welches ist das richtige?
 
#VSLIDE
 
 <h2>JavaScript Libaries</h2> 
 
 ![JSFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/jsUiFrameworks.png)
 
#VSLIDE

 <h2>Scala Libaries</h2>
 
 ![ScalaFrameworks](https://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/scalaFrameworks.png) 

#HSLIDE

Ich entschied mich für eine 2013 von Facebook ins Leben gerufene <i>Javascript-Bibliothek</i>

#HSLIDE

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/react-logo-colored.png" width="420"/>

<h1>React(.JS)</h1>

#VSLIDE

Warum ich mich für React entschieden habe?

<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/reactJS.jpg" />
<img src="http://raw.githubusercontent.com/ernstbe/Technology-presentation/add-presentation/images/noAngular.jpg" />

#VSLIDE 

<ol>
    <li> Re-Render bei jeder Änderung </li>
    <li> Sehr Komponenten basiert </li>
    <li> Geschwindigkeit durch Virutellen DOM</li>
    <li> Server Seitiges Rendering</li>
    <li> Gute Fehlermeldungen</li>
</ol>

#VSLIDE

<JSX />
Vereinfacht die erstellung der 'Komponenten'

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

#VSLIDE

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

Thanks!
