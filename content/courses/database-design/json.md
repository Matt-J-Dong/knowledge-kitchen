---
title: Javascript Object Notation (JSON)
---

JavaScript Object Notation (JSON) is a shorthand syntax for representing data in plain text. Data is represented as Javascript objects, in a slight variation of normal Javascript syntax, even though JSON is now used to represent data in programs of other langauges as well.

## What is an object?

If you are not familiar with [object-oriented programming](/content/courses/intro-to-computer-science/slides/object-orientation/), you can think of an object as a custom data type. You design your own custom data type by creating custom objects.

## Empty object

In JSON, all objects are represented between curly brackets. For example, you can indicate a blank object with the following code:

```json
{}
```

## Objects with properties

If you want to have a property stored in your object, use the following syntax to indicate the name of the property (i.e. its "key") and its value:

```json
{
  "first_name": "Foo"
}
```

Note: keys in JSON data must be surrounded by double quotes, whereas this is not generally necessary in Javascript code.

```javascript
{
  'note': 'Single quotes are not allowed in JSON, so this is invalid JSON!'
}
```

Multiple properties are simply key/value pairs separated by commas:

```json
{
  "first_name": "Foo",
  "last_name": "Barstein",
  "age": 40
}
```

## Properties that are objects

The values of properties can themselves be objects, as in the `address` field below:

```json
{
  "first_name": "Foo",
  "last_name": "Barstein",
  "age": 40,
  "address": {
    "street": "1329 Progress Way",
    "city": "Cedar Rapids",
    "state": "Iowa",
    "zip": 52401
  }
}
```

## Properties that are arrays

The value of any given property can be an array (a.k.a. list). Arrays are indicated by a comma-separated group of values surrounded by square brackets `[ ... ]`, as in the `lucky_numbers` field below:

```json
{
  "first_name": "Foo",
  "last_name": "Barstein",
  "age": 40,
  "address": {
    "street": "1329 Progress Way",
    "city": "Cedar Rapids",
    "state": "Iowa",
    "zip": 52401
  },
  "lucky_numbers": [22, 109, 5, 13]
}
```

The values of a Javascript array can be of any type, including objects.

```json
{
  "my_best_friends": [
    {
      "first_name": "Foo",
      "last_name": "Barstein",
      "age": 40
    },
    {
      "first_name": "Bar",
      "last_name": "Foostein",
      "age": 12
    }
  ]
}
```

## Comments - not allowed

Comments are not allowed in JSON, whereas they are valid in regular Javascript.

```json
{
  // this comment invalidates this otherwise beautiful JSON data
  "foo": "bar"
}
```

Some people try to get around this problem by writing comments as valid fields, e.g.:

```json
{
  "comment": "this is a sort of comment in valid JSON, although you can only do one field with the name 'comment'. "
  "foo": "bar"
  "comment-2": "so any further comments have to have different field names... silliness."
}
```

## Objects with functions - not allowed

In regular Javascript, it is possible to embed functions within objects.

```json
{
  first_name: "Foo",
  last_name: "Barstein",
  age: 40,
  address: {
    street: "1329 Progress Way",
    city: "Cedar Rapids",
    state: "Iowa",
    zip: 52401
  },
  // a function within an object definitino
  do_something: function() {
      var x = 10;
      var y = "twenty";
      var z = 20.1
      var z = true;
  }
}
```

However, adding functions to JSON data is not valid:

```javascript
{
  "first_name": "Foo",
  "last_name": "Barstein",
  "age": 40,
  "address": {
    "street": "1329 Progress Way",
    "city": "Cedar Rapids",
    "state": "Iowa",
    "zip": 52401
  },
  // !!!the following is invalid JSON, as is this comment itself!!!
  "do_something": function() {
      var x = 10;
      var y = "twenty";
      var z = 20.1
      var z = true;
  }
}
```

## Arrays

Objects in JSON can be bunded up into arrays:

```json
[
  {
    "foo": "bar"
  },
  {
    "foo": "baz"
  }
]
```
