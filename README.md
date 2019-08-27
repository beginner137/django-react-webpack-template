# django-react-webpack-template
A minimal template for hooking up Django, React, Webpack, with stateful react hot reload.



## 1: Setup the environment
Create python3 virtual environment and `pip install requirements.txt`

Initialize and install npm packages using `npm init` && `npm install -y`

Start Django server with `./manage.py runserver`


## 2: Run in production mode 
Run `npm run build` to output the minified files inside **'front-end/dist/js'** directory.


## 3: Run in development mode
`npm run dev` will start a front end dev server at http://localhost:3000/hmr which serves the local source files inside **'front-end/src/js'**

## 4: Load more custom javascript files inside Django templates
Create the new file inside **front-end/src/js** folder.

Register the entry inside **webpack.js**.

Run `npm run build` to output its minified version.

Use `{% load_hmr_js <file-name>.min.js %}` template tag to load it inside Django templates.
