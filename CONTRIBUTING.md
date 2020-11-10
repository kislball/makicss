# MakiCSS Contributing guide
Hi there and first of all thanks for being intersted in contributing to MakiCSS! In this guide, you can see code styles we use and repository organization.
## Code
MakiCSS uses SCSS for its implementation. We **do not** use indented syntax. In further sections, you will see the code style
### Style
```scss
// comment style is double slash, so they can be omitted on the build
@use 'sass:map'; // blank line between: @use sections, @import sections and .selectors

@import '../_colors.scss'; // always put extensions and _ as well

.my-super-selector { // selectors are splitted via - and first curly bracket is on selector's line. selectors should be readble(see next chapter)
  color: map.get($maki-colors, "black"); // MakiCSS uses two-spaces for tabs
  &:hover {
    color: map.get($maki-colors, "white"); // use & wheter possible
  }
} 

// Other notable features:
// If you feel it is configurable and it is global, put in variables/_configuration.scss
// If you feel it is configurable but not global, create a variable and prefix it
```
### Selectors
MakiCSS is inspired by Bulma in terms of readability.  
The entities are: `border`, `text`, `background` etc. This is common syntax:
`{entity}-is-{description}-{breakpoint?}`.
However, `display-is-block` isn't readble. So, we use `as` for verbs:
`{verbs}-as-{type}-{breakpoint?}`.
One of the most important thesises is:
**DO NOT USE ABBREVIATIONS**
*except breakpoints
### Building
MakiCSS uses npm-script for building. There are most important:
```sh
# start a build
$ npm run build
# dev mode
$ npm run dev
```
## Repostitory
Repository has two branches: `master` and `dev`. All contributions should go to dev branch.
### Commit style
Commits are following this schema:
`[PREFIX] {what have you changed}`
Available prefixes: `UTILS`, `GRID`, `STYLE`, `BUILD`, `README`
