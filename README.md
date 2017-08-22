# \<three-polymer\>
[![webcomponents](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/lakopite/three-polymer)
[![slack](http://slackin-xfuuoewxii.now.sh/badge.svg)](https://slackin-xfuuoewxii.now.sh)

Polymer web components for rendering 3D geometry in the browser. 
`<three-view>` is a viewport to render and manipulate a `<three-model>`. 

## Example:
<!--
```
<custom-element-demo>
  <template>
	<script src="https://rawgit.com/mrdoob/stats.js/master/build/stats.min.js"></script>
	<link rel="import" href="three-view/three-view.html">
	<link rel="import" href="three-model/three-model.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<div style="height: 500px; width: 100%">
  <three-view
    show-stats="true"
    scene-background-color="#F5F5F5">
    <three-model
      slot="model"
      contour-by="id"
      data='[
        {"vertices":[[0, 0, 0],[0, 0, 10]], "metadata": {"id": 1, "section_property_name": "W14X257"}},
        {"vertices":[[0, 0, 10],[10, 0, 10]], "metadata": {"id": 2, "section_property_name": "W27X84"}},
        {"vertices":[[10, 0, 0],[10, 0, 10]], "metadata": {"id": 3, "section_property_name": "W14X257"}}
      ]'>
    </three-model>
  </three-view>
</div>
```        

## Development:
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