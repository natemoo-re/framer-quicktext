# QuickText
## Framer Module that makes working with TextLayers a breeze

QuickText automatically converts any text created in Framer Design to a TextLayer. 
It can also convert any Layer into a TextLayer.

## Usage
Include 'QuickText.coffee' in your project's module directory, then add the following at the top of your file.
'''coffee
QuickText = require "QuickText"
QuickText.init()
'''

## Configuration
If you'd like to modify the behavior of QuickText, the init function accepts a few options:
'''coffee
QuickText = require "QuickText"
QuickText.init
    autoConvert: true    # <boolean>
    layerConvert: true   # <boolean>
'''

Alternatively, to manually use QuickText on any Layer, you can import just the 'toTextLayer' method.

'''coffee
{ ToTextLayer } = require "QuickText"

layerA = new Layer
ToTextLayer(layerA)
layerA.text = "Hello world!"
'''


changes in wording can be done from Framer Code  Target.text = "New Text!"
