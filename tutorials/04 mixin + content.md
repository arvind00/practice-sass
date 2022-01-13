## Learning Objective
- [] Learn the usage of mixin with the `@content` directive


## Scenario Briefing
- suppose we want to create and animation that will be supported in all browsers
- we can achieve this with mixin and content directive as follows
```scss
/* mixin + content */
@mixin animation($name){
  @-webkit-keyframes #{$name} {
      @content;
  }

  @-moz-keyframes #{$name} {
    @content;
  }

  @-o-keyframes #{$name} {
    @content;
  }

  @keyframes #{$name} {
    @content;
  }
}

@include animation(ani1){
    0% {opacity: 0}
    100% {opacity: 1;}
}

````
- the above scss will generate the below css
```css
/* mixin + content */
@-webkit-keyframes ani1 {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@-moz-keyframes ani1 {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@-o-keyframes ani1 {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
@keyframes ani1 {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
```