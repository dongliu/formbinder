formbinder
==========

A small JavaScript library for two-direction HTML form data binding.

You can find the original version from https://code.google.com/p/js-binding/

My changes include

* serialize '' as null instead of undefined

null is more easily processed by a storage back end like mongodb. undefined properties of an object is disregarded by mongo. I have also tried not serializing '' at all, but that caused problem when the value in an input was removed.
* stringArray type support

This type is used for tags that separated by ',' and represented by a JavaScript string array. Note that this is different from the array used to represent the value of checkbox or select-multiple input types.
