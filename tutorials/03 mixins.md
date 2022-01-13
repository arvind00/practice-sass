
## Mixins - How to define it
- Mixins can be a block of style rules - can be standard css or scss or combination
- The main intention of mixins is to reuse that block of code of that mixins
- Mixins can also take arguments, which can be used inside the code block of the mixin
- To define a mixin use the keyword `@mixin`

```scss
// mixin - with single param example
@mixin mx2($bgColor) {
    background-color: $bgColor;
}
$c1_bgColor: teal;

.card-v1 {
    @include mx2($c1_bgColor);
    color: white;
}

// mixin - with multiple param example
@mixin bxShadow($s...){
    -webkit-box-shadow: $s;
    -moz-box-shadow: $s;
    -o-box-shadow: $s;
    box-shadow: $s;
}

$bx1: 1px 2px 3px rgba(0,0,0,0.3);
$bx2: 4px 3px 2px rgba(0,0,0,0.3);
.card-v2 {
    @include bxShadow($bx1, $bx2);
}
```
- To include a mixin use the keyword `@include` followed by a space and the mixin name