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