# SCSS FRAMEWORK
## file structures
>base  
-- fonts.scss  
-- reset.scss  
components  
-- btn.scss  
config  
-- colors.scss  
-- keyframes.scss  
-- mixins.scss  
-- variables.scss  
globals  
-- anim.scss  
-- text.scss  
-- util.scss  
pages  
-- page-example.scss  
config.scss  
main.scss

### base
>The *base* directory contains all our base rules. _(e.g. fonts, reset)_.

### components
>The *components* directory contains all our component scss rules.

### config
>The *config* directory contains all the configuration within our framework.
__colors.scss__ - We define all our applications color schema inside the `$colors` map. During compilation __utility classes__ will be generated accordingly. 
__keyframes.scss__ - We define all our animation keyframes inside this file.
__mixins.scss__ - We define all our mixins inside this file.
__variables.scss__ - We define all our variables inside this file.

### globals
>We *globals* directory contains all our global modifiers.
__anim.scss__ - We define all our animation classes inside this file.
__text.scss__ - We define all our text classes inside this file.
__util.scss__ - We define all our utility classes inside this file.

### pages
>The *pages* directory contains all our page rules. We __do not__ include our page files inside the __main.scss__ because we want the rules defined inside to be accessible only to a specific page and not globally.
__page-example.scss__ - example template for page. 

### config.scss
>The config.scss contains all the files inside the __config directory__. We include this file on top of our main modules (e.g. main.scss, page.scss).

### main.scss
>The main.scss contains all our files besides our page files as explained previously. We include this file for every document of our application.

## Coding style
### File naming
>Our file names must follow the **prefix-module** convention in order to make sure that our classes do not collide with our vendors. The value of our prefix must be the same with our app prefix and the value of our module must be the same with our block-element [See BEM documentation](http://getbem.com/).
```
// app-foo.scss - This is the file name.
app-foo {
    // style goes here..
}
```

### BEM + Global Modifiers
>Our codes must strictly follow the [BEM](http://getbem.com) standards for development it provides us with a clean and robust markup for our application. While BEM is good for structuring our application it lacks code reusability for this we use __global modifiers__.

### Global Modifiers
> A good example of global modifiers are [Bootstrap](https://getbootstrap.com/) classes where you can define the class names inside your element and it will apply the necesarry styling.
```
<div class="app-foo">
    <p class="app-foo__text app-text-white">Foo bar</p>
</div>
```
>On the code above, the `app-text-white` is not part of the `app-foo` component, it is a global modifier. What it does is it modifies the text elements color to white. 

Generally we apply single responsibility for all our classes. Always keep in mind that if a rules does not belong in its __default state__ it must fall under the __modified state__.