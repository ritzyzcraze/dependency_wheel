Dependency Wheel
================

This is a fork from the MooWheel Class version 0.2 from unwieldy studios <http://unwieldy.net>. Written by Augusto Becciu. You can get more information to MooWheel here <http://unwieldy.net/web/moowheel>
   
This fork is customized to visualize dependencies for software libraries. 
It is used on <https://www.versioneye.com> to show recursive dependencies for Java and Ruby Projects. 

This fork is very strongly customized for VersionEye. But anyway! Feel free to take a look and get some inspiration :-) 

Images
==
Some of the dependency wheels created at VersionEye are on [Pinterest.com](http://pinterest.com/versioneye/pins/). This image below is one example.

![](http://media-cache-ec5.pinterest.com/upload/72620612711867522_GUQiokvU_c.jpg "Dependency Wheel")

Code Example
==
It is very to use the library. All you need is HTML div. 

```html
<div id="canvas-container"></div>
```

And a little bit JavaScript. 

```JavaScript
<script type="text/javascript">
  function render_wheel(){
    canvas_container = document.getElementById("canvas-container")
    if (canvas_container){
      var wheel = new DependencyWheel.Remote(false, canvas_container, { 
        url: 'YOUR_RESOURCE_RETURNING_JSON.json',
        width: "605", 
        height: "605",
        infoBox: "infoBox",
        infoNumber: "runtime_recursive_number",
        canvas_id: "canvas",
        canvas_hover_id: "canvas_hover",
        product_key: "PRODUCT_KEY`", 
        product_version: "PRODUCT_VERSION",
        product_name: "PRODUCT_NAME", 
        version: "VERSION",
        data_border: 70,
        show_label: false,
        resize: false,
        scope: "SCOPE",
        container_id: "canvas-container",
        onItemClick: function(item, event){
          window.location.href = "YOUR_NEW_RESOURCE";
        }
      } );
    }
  }
</script>
```

License
==
MIT License <http://www.opensource.org/licenses/MIT>