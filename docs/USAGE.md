This file contains basic *usage information* for the **Mermaid** extension. See also the [readme].

The `#mermaid` parser function allows to add [mermaid][mermaid] typed content to a wiki article. Copying,
[example syntax][examplemjs] is as easy as:

```
{{#mermaid:sequenceDiagram
participant Alice
participant Bob
  Alice->John: Hello John, how are you?
  loop Healthcheck
       John->John: Fight against hypochondria
  end
  Note right of John: Rational thoughts <br/>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
}}
```
![image](https://user-images.githubusercontent.com/1245473/34535703-14a32100-f106-11e7-9201-ea90a6286c58.png)

This extension now supports all configuration options of MermaidJS

* Reference - https://mermaid-js.github.io/mermaid/#/Setup?id=configuration

It is passed to the parser function like shown:
```
{{#mermaid:graph LR;
 ...
 |
 config.theme = default
 config.flowchart.useMaxWidth = false
 config.flowchart.curve = basis
}}
```
Note that is is also possible to further adapt the graph using CSS, e.g. to add a scrollbar:

```
.ext-mermaid > div {
	overflow: scroll;
}
```

Further [examples][examplesmw] have been created on wiki. See also [Drawing Diagrams and Charts with Mermaid](https://www.pro.wiki/help/draw-mermaid-diagrams-charts-in-mediawiki)


[readme]: https://github.com/SemanticMediaWiki/Mermaid/blob/master/README.md
[mermaid]: https://github.com/knsv/mermaid
[examplemjs]: https://mermaidjs.github.io/
[examplesmw]: https://sandbox.semantic-mediawiki.org/wiki/Mermaid
