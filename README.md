# generator-essentials
<img src="https://img.shields.io/npm/v/generator-essentials.svg">
<img src="https://david-dm.org/S3B4S/generator-essentials.svg">

## Table of contents
- [Description](#description)
- [Get started](#getstarted)
- [Tasks](#tasks)
- [What does this include?](#include)
- [What does this generate?](#generate)
- [Philosophy behind scss structure and BEM](#scss)
- [Planned features](#features)

<a name="description"/>

## Description

So, I really like using very specific packages which do their job very well, [Jeet](http://jeet.gs/) and [Typi](https://github.com/zellwk/typi) for example. As I kept expanding my library of must-have small tools that make my life so much easier I started noticing that setting up the project took longer than I wanted it to be. Wouldn't it be great if I could use templates and have everything generated and installed with the command line? Yes, it would be, and that's why `generator-essentials` has been created. And it's all yours to use aswell! :smile:

- No bloated stuff, only code that you actually use will be deployed.
- A scss structure that follows a philosophy, to keep all your projects consistent.
- Flexible, responsive grid (but really).
- Responsive typography.

<a name="getstarted"/>

## Get started

### prerequisites

Tool                         | If it's not installed yet
:--------------------------- | :---------- 
[npm](https://www.npmjs.com/)| https://docs.npmjs.com/getting-started/installing-node
[Yeoman](http://yeoman.io/)  | `npm install -g yo`
[Gulp](https://gulpjs.com/)  | `npm install gulp-cli -g`

You can check your installed global packages with `npm ls -g --depth=0`.

### Installing generator-essentials

`npm install -g generator-essentials`

### Generating the project
Unfortunately, at the moment `npm init` hasn't been configured within the generator itself. So for now this has to happen manually.

1. Create a new directory that contains your project, this is the root directory.

2. Navigate inside this directory from terminal.

3. Run `npm init`.

4. Run `yo essentials`.
    - By default, your directory name will be the project name, but you can set a new one.

`npm install` isn't necessary, this is taken care of by the generator.

5. Happy coding!

<a name="tasks"/>

## Tasks
Task  | Description
:---- | :---------- 
`gulp`| Launces your project in browser. Auto-refresh & scss compiles to css on save.

<a name="include"/>

## What does this include?
- [Jeet](http://jeet.gs/)
- [Typi](https://github.com/zellwk/typi)

<a name="generate"/>

## What does this generate?
```
├── node_modules/
├─┬ src/
│ ├── js/
│ ├─┬ scss/
│ | ├── base/
│ | ├── components/
│ | ├── utils/
│ | ├── layout/
│ | └── vendor/
│ └── index.html
└── gulpfile.js
```

<a name="scss"/>

## Philosophy behind scss structure and BEM
When working with scss, you really want to keep it mantained, this makes it easier for other developers to read your code, or if you have to come back to your project later on. After looking into multiple structures I went with the one that's heavily insipred from [sitepoint.com](https://www.sitepoint.com/architecture-sass-project/).

One thing that's also *very* useful, is using [BEM](https://en.bem.info/methodology/css/). I recommend you to seperate the css that you use for each component and the css that you use to display (the space between) each component. This way, you can easily reuse the components in later projects and all you have to do is write the css code to create the spacing in between or place them at the correct position on your site. This follows the BEM philosophy.

In short:

Directory     | Purpose
:------------ | :---------- 
`base`        | This is where css which will apply 'globally' will end up, think of typography.
`components`  | The css for each component, best to keep each seperated in its own file.
`utils`       | This is where variables, mixins etc will end up, the utilities that come along with scss.
`layout`      | Grid, margins and paddings between components.
`vendor`      | Third-party code, keep it seperated so you can keep track of updates etc easily.

<a name="features"/>

## Planned features
- Let the generator execute `npm init` in the way it's supposed to be.
- Provide options and be able to pass these as flags.
  - Other preprocessor options beside SCSS.
  - Include comments in code.
- Choose which npm packages you want.
- Let Yeoman generate empty directories

## Thanks
Thanks MacMeep for testing the package! :tada:
