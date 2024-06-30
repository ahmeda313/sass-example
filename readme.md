# Sass
## Preprocessing
```
sass -watch input-filename output-filename
```
or
```
sass -w input-folder output-folder
```
## important aspects
1. variables ```$color```

2. partials ```_functions.scss```
```
@import 'functions'
```

3. nesting 
```
{ 
    &-a{
      background-color:$color;   
    }
}
```


4. inheritance ```@extends %something```
```
%btn{
    padding: 0.5rem ,1rem;
}

Btns{ 
    &-a{
      @extend %btn;   
    }
}
```

5. functions ```function-name(var);```
```
@function setColor($var){
    @if(lightness($var)>50){
        @return #fff
    } @else{
        @return #000
    }
}
```
6. mixin ```@include mixin-name(var);```
```
@mixin transform($property) {
  --webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}
```