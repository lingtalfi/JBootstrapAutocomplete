JBootstrapAutocomplete
===========
2019-11-15



A port of the [bootstrap-autocomplete](https://www.jqueryscript.net/form/jQuery-Bootstrap-4-Typeahead-Plugin.html) plugin for the universe framework.


This is part of the [universe framework](https://github.com/karayabin/universe-snapshot).


Install
==========
Using the [uni](https://github.com/lingtalfi/universe-naive-importer) command.
```bash
uni import Ling/JBootstrapAutocomplete
```

Or just download it and place it where you want otherwise.






Summary
===========
- [JBootstrapAutocomplete api](https://github.com/lingtalfi/JBootstrapAutocomplete/blob/master/doc/api/Ling/JBootstrapAutocomplete.md) (generated with [DocTools](https://github.com/lingtalfi/DocTools))





What is this
=============

This planet is a port from the [bootstrap autocomplete plugin found on jqueryscript.net](https://www.jqueryscript.net/form/jQuery-Bootstrap-4-Typeahead-Plugin.html) 
to the [universe](https://github.com/karayabin/universe-snapshot).

I host it as a planet for dependency resolution convenience inside my universe framework, but all credits
goes to the guy who wrote this plugin and posted it on jqueryscript.net.



How to use
==========

First type your html:

```html
<input class="typeahead form-control">
```


Then define your sources.

You can either:

- define sources directly
- load the data from an external JSON file 


Define sources directly
---------
```js
$(".typeahead").typeahead({
  source: [
    {id: "id1", name: "jQuery"},
    {id: "id2", name: "Script"},
    {id: "id3", name: "Net"}
  ]
});

```

Load the data from an external JSON file
---------

```js
$.get("data.json", function(data){
  $(".typeahead").typeahead({ 
    source:data 
  });
},'json');


```



Then call the plugin:

```js
$(".typeahead").typeahead({ 

  // data source
  source: [],

  // how many items to show
  items: 8,

  // default template
  menu: '<ul class="typeahead dropdown-menu" role="listbox"></ul>',
  item: '<li><a class="dropdown-item" href="#" role="option"></a></li>',
  headerHtml: '<li class="dropdown-header"></li>',
  headerDivider: '<li class="divider" role="separator"></li>',
  itemContentSelector:'a',

  // min length to trigger the suggestion list
  minLength: 1,

  // number of pixels the scrollable parent container scrolled down
  scrollHeight: 0,

  // auto selects the first item
  autoSelect: true,

  // callbacks
  afterSelect: $.noop,
  afterEmptySelect: $.noop,

  // adds an item to the end of the list
  addItem: false,

  // delay between lookups
  delay: 0,
  
});


```









History Log
=============

- 1.0.0 -- 2019-11-15

    - initial commit