# Starting a WebApp with Angular2, Webpack and Semantic-UI

## Prerequisites

- npm
- typings
- gulp

## Step 0: Initialising the application

- Create the directory
- Do nothing else (you might want to do npm init, but this is not necessary though we will create a package.json by copying it from the angular tutorial)

## Step 1: Creating sample application with Angular2 tutorial (Webpack)

- Follow the tutorial: https://angular.io/docs/ts/latest/guide/webpack.html
- Or you might simply check out the code from this repository: https://github.com/cbeulke/tutorial-angular2-webpack-semantic

## Step 2: Installing jQuery

- npm install jquery --save
- vendor.ts => add "import 'jquery';"
- webpack.common.js => add ProvidePlugin:

```
plugins: [
	...,

	new webpack.ProvidePlugin({
		jQuery: 'jquery',
		$: 'jquery',
		jquery: 'jquery'
	})
]
```

## Step 3: Installing Semantic-UI

- http://semantic-ui.com/introduction/getting-started.html
- npm install semantic-ui --save
- cd semantic/
- gulp build
- vendor.ts => add "import '../semantic/dist/semantic.min.js';"
- vendor.ts => add "import '../semantic/dist/semantic.min.css';"

## Step 4: Installing ngSemantic

- https://github.com/vladotesanovic/ngSemantic
- npm install ng-semantic --save
- vendor.ts => add "import 'ng-semantic';"
- app.module.ts => add "import { NgSemanticModule } from 'ng-semantic';"
- app.module.ts => add NgSemanticModule to imports

## Step 5: Testing

- Use components / tags in your template (https://ng-semantic.herokuapp.com/#/)
