# project-html-template
Html template for project page

## Install
```shell
npm install --save-dev project-html-template
```

## Usage
make sure `html-webpack-plugin` is in used, and we use `project-html-template` like this:

```js
// in webpack.config.js
const ProjectHtmlTemplate = require('project-html-template');
const { name, description } = require('./package');

// ...
plugins: [
  new HtmlWebpackPlugin({
    title: name,
    desc: description,
    repository: `https://github.com/escX/${name}.git`,
    template: ProjectHtmlTemplate,
    favicon: './examples/src/favicon.ico'
  })
]
```