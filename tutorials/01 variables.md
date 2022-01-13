
## How to declare variables in SASS
- always prefix with `$`
- followed by letters and numbers
- but no special characters as it can lead to errors
- then to assign a value put a `:` followed by the value
- don't forget to end by a `;`
- This allows to declare multiple variables in a single line
- The values can be any valid css units or strings enclosed in single/double quotes or no quotes like `no-repeat`


## String Selector to target elements
- supposed you declared a variable say
```scss
$divRow1: row_1;
```
- suppose you want to target a div with a class of row_1 then you can use the above declared variable as
```scss
div.#{$divRow1} {
    background: grey;
}
```
- basically you have to write in this expression: `#{name_of_variable}`
- it is similar to using variable in a string literal in es6.

## Other data types
- you can have list of values
- you can also have boolean and null as values of variables
- Finally you have have map of values
- You define map as key value pair separated by commas and key value pairs are enclosed inside parenthesis

## Maps
- Maps holds key value pairs.
- The keys must be unique but values can be duplicated
- The key value pairs are seperated by comma
- All the key value pairs are enclosed in parenthesis
- To retrieve values using the key follow this syntax: `map.get($your_map, "your_key")`
```scss
$myList: 1px solid green;

.card{
    width: $card_width;
    font-size: $card_font_size;
    border: $myList;
    background-color: white;
    border-radius: 3px;
    padding: 0.5rem;
}

$myMap: (
    "regular": 400,
    "medium": 500,
    "bold": 700
);

@debug map.get($myMap, "medium");

```