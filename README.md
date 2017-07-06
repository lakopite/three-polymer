# \<three-polymer\>
[![slack](http://slackin-xfuuoewxii.now.sh/badge.svg)](https://slackin-xfuuoewxii.now.sh)

Polymer web components for rendering 3D geometry in the browser

## Element \<three-model\>
### Properties
##### data: Array
An array of objects that compose the model. The objects must include `vertices` as well as `metadata` (e.g.
`{"vertices":[[0, 0, 0],[0, 0, 10]], "metadata": {"axial": 10, "flexure": 40}}`)

##### contour-by: String
The `metadata` field from which contours will be calculated. This field may be any of the fields within `metadataFields`

##### geometry-filter: Object = `{}`
A bounding box object to filter which model elements are visible to the user.  
It may contain any number of fields `xMax`,`xMin`,`yMax`,`yMin`,`zMax`,`zMin` with values of type `Number` 

##### is-loading: Boolean _computed_
Indicates whether or not the model is in the process of stamping out or removing any of its children

##### metadata-fields: Array _computed_
The set of fields of which you can specify to contour the model

##### object: Object _computed_
The `THREE.Group()` object associated with the model

##### boundaries: Object _computed_
The bounding box computed from `data`. This will not update based on any filters applied to the model.

##### position: Array _computed_
The center of the model's bounding box

##### radius: Number _computed_
The radius of the model's bounding box

##### stroke: Number _computed_
The width of the lines in the model

##### _lines: Array _protected_
        

## Development
### Setup
Install dependencies:
```
$ bower i
```
Install the [Polymer CLI](https://www.npmjs.com/package/polymer-cli)

### Running Tests
```
$ polymer test -l chrome
```

### Demo
```
$ polymer serve
```
navigate to http://localhost:8081/components/three-polymer/