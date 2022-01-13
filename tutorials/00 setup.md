## Project Setup
- We will setup a simple vanilla web project - I mean we will have an index.html
- For SCSS compilation we can use vs code extention Live SASS Compiler
- Or we can install dart sass and compile, we will use this approach

## Package installation
- To include it in the project
```sh
npm i sass -D
```
- Or better install it globally `npm install -g sass` then you will get sass as a nodejs command

## Compile sass files
```sh
npx sass --watch scss:css
```
- if installed globally run this command: `sass --watch scss:css` 
- create a folder `scss` and keep your sass files in there.
- after compilation you will get your css files in `css` folder
- Create an `index.html`
- Refer the stylesheet that got generated in `css` folder
- Start writing scss in style.scss
- Serve the index.html using Live Server