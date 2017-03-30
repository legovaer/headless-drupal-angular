# Headless Drupal + AngularJS
A working "Headless Drupal" example implementation - an AngularJS app set up to talk to Drupal 8 vis the rest.module.

# Features
* SASS support including sourceMaps
* Minimal CSS styling of the view
* Gulp watch, build and local server tasks
* Responsive navigation
* Owl slider directive
* localStorage service for set, get, remove data
* queryService $http wrapper to handle calls
* Clear folder structure
* Less than 10 request in build version
* Minified CSS and JS build files
* Google analytics snippet
* Interaction with your Drupal 8 back-end

## Download

```bash
git clone https://github.com/joshkoenig/headless-drupal-angular.git
```

## 1. Setup
```bash
npm install
```
- install all npm and bower dependencies

**Note:** If `npm install` fails during dependency installation it will be likely caused by `gulp-imagemin`. In that case remove `gulp-imagemin` dependency from `package.json`, run `npm install` again and then install `gulp-imagemin` separately with following command: `npm install gulp-imagemin --save-dev`

## 2. Watch files
```bash
gulp
```
- all SCSS/HTML will be watched for changes and injected into browser thanks to BrowserSync

## 3. Build production version
```bash
gulp build
```
- this will process following tasks:
* clean _build folder
* compile SASS files, minify and uncss compiled css
* copy and optimize images
* minify and copy all HTML files into $templateCache
* build index.html
* minify and copy all JS files
* copy fonts
* show build folder size

## 4. Start webserver without watch task
```bash
gulp server
```

## 5. Start webserver from build folder
```bash
gulp server-build
```

## See a demonstration online:
### http://dev-headless-drupal-8.gotpantheon.com/

This is a quick and dirty demo, intended as a starting place for discussion, and to help others get hacking quickly. There's a _lot_ of work TODO.

Pull requests are welcome.

## Running it w/your own Drupal Install

Going beyond the most basic demo, you will likely want to customize the back-end a little bit as well. Getting your own up and running is pretty simple:

1. Start with a fresh Drupal 8 instance. [Use Pantheon if you like](https://www.getpantheon.com/d8)
2. Enable all the core REST Services module.
3. Copy in the provided rest.settings.yml configuration.
4. Change the ```mySite``` variable at the top of ```app.js``` or ```alt.js``` to point to your own site.
5. ???
6. Profit!


## TODO:
- Expand this Readme.md to explain how it works.
- Fixing whatever I've done n00bishly in Angular
- Better packaging/documentation of how to configure Drupal.
- Extend DEMO to include CRUD for nodes.
- Add custom routes to the demo.

## Changelog
### 1.0.1
- added gulpfile to simplify build process
- added npm integration
- changed project structure to make stuff easier
- updated the README with the updated changes

### 1.0.0
- Initial release
