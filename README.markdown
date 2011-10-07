JSON Schema PHP Validator
=

JSON Schema
-

> *JSON Schema is a specification for a JSON-based format for defining the structure of JSON data. JSON Schema provides a contract for what JSON data is required for a given application and how it can be modified, much like what XML Schema provides for XML. JSON Schema is intended to provide validation, documentation, and interaction control of JSON data.* - [http://code.google.com/p/jsonschema/](http://code.google.com/p/jsonschema/)

JSON Schema Validator for PHP
-

> *Json schema validator in php. It is a PHP class that validates a json data structure against a schema definition. It is a simple class that returns an object containing the result and errors that happened.* - [http://sourceforge.net/projects/jsonschemaphpv/](http://sourceforge.net/projects/jsonschemaphpv/)

Usage Example
-

    $schema = json_decode('{ type : "object", properties : { a : { type : "string" }} }');
    $json = json_decode('{ a : 1 }');

    $result = JsonSchema::validate(
        $json,
        $schema
    );

    if (!$result->valid) {
        echo "Errors: \n";
        print_r($result->errors);
    }
