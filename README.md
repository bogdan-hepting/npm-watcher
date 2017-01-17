# ThemeKit
A starter Drupal subtheme reliant on the Drupal 8 core Classy theme.
 
## Setup 

### Recommended
Run
```
npm run build
```
That's it, you now have all of the node modules required, basic Drupal theme files, scss/js files and `watch`er.



## Npm commands
We use npm scripts instead of Gulp or Grunt.

### Build styles
```
npm run build:css
```
Compile all sass files to css. Take files from `./sass` folder and output to `./css`.

### Build scripts
```
npm run build:js
```
Take files from `./js/src` folder, grouping and output to `./js/dist/theme.bundle.js`.

**Note:** if you want separate js files - you have to create files in `./js/dist` folder.

### Build all
```
npm run build:all
```
Compiles all JavaScript and CSS. This essentially just calls `npm run build:js` and `npm run build:css`.

### Watcher
```
npm run watch
```
Watches for any JavaScript or Scss changes and compiles them to css and js. This is similar to `npm run build:all` but with a
file watcher.

**Note:** also you can ran watcher for js or scss only using commands `npm run watch:js` or `npm run watch:css`. 



## Foundation
Foundation already included to `package.json` file and used by `scss`.

All you need is edit two files  `./sass/base/_settings.scss` and `./sass/base/_app.scss`. The last one partial contains the settings import and all of the foundation components imports. You can include all or include only what you like.

Lastly, if you are using any javascript components, you must initialize foundation on DOM ready.
```
$(document).foundation();
```

## Legacy Breakpoints
Foundation 6 has a great system for breakpoints which allows you to define them in sass and use them in javascript. The downside to Foundation in general is that there is no support for legacy browsers like IE8. [ResponseKit](https://github.com/tandroid1/ResponseKit) is a library that was created to provide very similar breakpoint functionality but with support for no-query fallbacks. 

