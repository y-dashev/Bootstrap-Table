# bootsrap-table
JQwidgets Test

The task of this code snippet is to make a boostrap table using the following:
1. CSS - CSS3 variables or SCSS or SaSS .
2. Javascript - vanilla javascript ES6 or VueJS.
3. Info icon - FontAwesome or Material Icons

And with the these functionalities:
1. Table with Bootstrap styles, Info button and Bootstrap Progress component
2. Clicking on the Info button should open a popover component with some details about the row
3. Double clicking on a Cell should open an Input to edit the cell value

My personal choice for this task was to use:
    Vuejs 2,
    Bootstrap 4,
    Bootstrap-Vue 2,
    Sass.

Progress bar and info icon components are from Bootsrap-Vue.

Also I choose to have the information in the ElementsTable.vue component to be set as props so whenever we need to use the component or we need to used it multiple times we just assign new values to these props.

## To run the code first run 
```
npm install
```

### Then to compile the code for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


