Potential issue in Swagger Editor and empty "paths" object

To reproduce:
* Keep the browser's JavaScript console open (tested with Firefox)
* Load the "a.yaml" file in Swagger Editor by following the "Load a.yaml" link below (it contains an empty paths object; no errors are shown in the JS console)
* Load the "test.yaml" file in Swagger Editor by following the "Load test.yaml" link below (the content of this yaml file is irrelevant as long as it is a valid OpenAPI)
* See lots of errors in the console

[Load a.yaml](https://editor.swagger.io/?url=https://raw.githubusercontent.com/jdegre/jdegre.github.io/master/test/a.yaml)

[Load test.yaml](https://editor.swagger.io/?url=https://raw.githubusercontent.com/jdegre/jdegre.github.io/master/test/test.yaml)

The error is shonw in the JS console when test.yaml is loaded, but this file would have not caused any error at all, if it is loaded alone. Hoever, any yaml file loaded after a.yaml (due to the empty paths object) fails, and the error pops up in the JS console.
