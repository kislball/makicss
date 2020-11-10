# MakiCSS
> Utility-first frontend framework that just exists
## Warning 
**This project is under development, not production ready**
## Usage
MakiCSS is available as npm package. Install it via:
```shell script
$ npm install makicss
```
Then, import css or scss styles:
```js
// for css
import 'makicss/dist/maki.css';
// or
import 'makicss/dist/maki.min.css';

// for scss
import 'makicss/src/maki.scss';
```
### Importing modules
MakiCSS consists of two parts: `utils`, `grid`. You can import them independently:
```js
// for grid(css)
import 'makicss/dist/maki-grid.css';
// or
import 'makicss/dist/maki-grid.min.css';

// for utils(css)
import 'makicss/dist/maki-utils.css';
// or
import 'makicss/dist/maki-utils.min.css'


// for scss
import 'makicss/src/grid.scss';
import 'makicss/src/utils.scss';
```
## Building
MakiCSS uses npm scripts for building in favour of Webpack, Parcel etc.  
```shell script
# build whole framework
$ npm run build 
# build scss only
$ npm run build:scss
# build only grid system
$ npm run build:scss-grid
# see others in package.json
```
## License
The code is licensed under MIT-license