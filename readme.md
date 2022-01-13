
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
- if installed globally `sass --watch scss:css` create a folder `scss` and keep your sass files in there.
- after compilation you will get your css files in `css` folder
  
## Reference
> https://www.udemy.com/course/sass-workflow/learn/lecture/2162788?start=0#overview
> usage of @use over @import https://www.youtube.com/watch?v=CR-a8upNjJ0


## Issues
- while using map.get you might get error. check out https://stackoverflow.com/questions/64210390/sass-map-get-doesnt-work-map-get-does-what-gives
- for we have to have this statement in the beginning of the file: `@use "sass:map";`