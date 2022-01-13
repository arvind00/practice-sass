
## Share CSS rules using a placeholder
- define a placeholder by prefixing with % followed by placeholder name
- Then we can re-use the content of placeholder somewhere else using the @extend
- The syntax is `@extend %placeholder_name;`
  
```scss
%shared {
    background: green;
    font-size: 1.5rem;
    color: white;
}

.someClass { 
    @extend %shared;
    line-height: 1.4; 
}

.someOther1, .someOther2 {
    @extend %shared;
}

```