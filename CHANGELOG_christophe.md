In genrepo folder
- I create my own canvas draw plugin, search for HACK to get changes

dragnodes plugin
- no right click

sigma source code:
- I adapt mouseover to detect square nodes
- I comment out node hover drawings in sigma.misc.drawHovers
- nodeRenderers[defaultNodeType] || missing in the sane function = sigma bug ( 4 times)
- check for node exsitance if unhovering or trying to draw node
OK - isPointOnSegment add epsilon to final comparison if between x12x y1y2
OK - arrow edge and edgehover, change start and end point
- give all nodes to node detection on hover

Tooltips angular
- have my own plugin

Edgelabels plugin
changed two lines

My imports:
script(src='/vendor/sigmajs/sigma.require.js')
script(src='/vendor/sigmajs/plugins/sigma.plugins.dragNodes.js')
script(src='/vendor/sigmajs/plugins/sigma.plugins.tooltips-angular.js')
script(src='/vendor/sigmajs/plugins/edgeLabels/settings.js')
script(src='/vendor/sigmajs/plugins/edgeLabels/sigma.canvas.edges.labels.curve.js')
script(src='/vendor/sigmajs/plugins/edgeLabels/sigma.canvas.edges.labels.curvedArrow.js')
script(src='/vendor/sigmajs/plugins/edgeLabels/sigma.canvas.edges.labels.def.js')

Converted into new code:
- my canvas plugin into renderers/sigma.renderers.canvas.js
- my sigma plugins added es6 part
- put my drag node hack into plugins/sigma.plugins.dragNodes/sigma.plugins.dragNodes.js
- edge labels changes into plugins/sigma.renderers.edges.labels.curve.js


TODO:
delete old sigma.renderes.canvas in my genseqhub dir
put my plugins into my sigma fork ?
put tooltip plugin into sigma fork?
