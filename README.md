# QuickText
## Framer Module to make working with TextLayers a snap

QuickText automatically converts any text created in Framer Design to a TextLayer. 
It can also convert any Layer into a TextLayer.

## Installation
Include the `QuickText.coffee` file in your project's module directory, then add the following lines to the top of your file
```coffee
QuickText = require "QuickText"
QuickText.init()
```

## Usage
#### Layer.toTextLayer()
```coffee
layerA = new Layer
layerA = layerA.toTextLayer()
layerA.text = "Hello world!"
```
#### QuickText.toTextLayer(layer)
```coffee
layerA = new Layer
layerA = QuickText.toTextLayer(layerA)
layerA.text = "Hello world!"
```


## Configuration
If you'd like to modify the behavior of QuickText, the init method accepts a few options
```coffee
QuickText = require "QuickText"
QuickText.init
    autoConvert: true    # <boolean> Toggles automatic conversion of Framer Design text into TextLayers
    layerConvert: true   # <boolean> Toggles adding a new toTextLayer() method to instances of Layer
```

Alternatively, to manually use QuickText on any Layer, you can import just the `ToTextLayer` method.

```coffee
{ ToTextLayer } = require "QuickText"

layerA = new Layer
ToTextLayer(layerA)
layerA.text = "Hello world!"
```
