# WP Gulp
A ready-made gulpfile for WordPress Theme & Plugin development

[![Code Climate](https://codeclimate.com/repos/58cd6b61ac2b9a753f000813/badges/e1c504fb8004cf46b792/gpa.svg)](https://codeclimate.com/repos/58cd6b61ac2b9a753f000813/feed)
[![Test Coverage](https://codeclimate.com/repos/58cd6b61ac2b9a753f000813/badges/e1c504fb8004cf46b792/coverage.svg)](https://codeclimate.com/repos/58cd6b61ac2b9a753f000813/coverage)
[![Issue Count](https://codeclimate.com/repos/58cd6b61ac2b9a753f000813/badges/e1c504fb8004cf46b792/issue_count.svg)](https://codeclimate.com/repos/58cd6b61ac2b9a753f000813/feed)

## Installation
#### Manual
Download both the gulpfile.js and package.json files and place them at the base directory of the plugin or theme you are developing. 
 - i.e) wordpress/wp-content/plugins/your-plugin/{place-files-here}
 - i.e) wordpress/wp-content/themes/your-theme/{place-files-here}
 
#### CLI Tool
Install the imforza-cli tool by running `npm install imforza-cli -g`. Then traverse into the base directory of your plugin or theme and run `imforza gulp install` or `imforza -G install`.
  - More info on [imforza-cli](https://www.npmjs.com/package/imforza-cli)

## Usage

- `gulp` - Proxies your local development site through [browsersync](https://browsersync.io/).
- `gulp init` - Initializes local environment, Install composer, wp-enforcer, and the pre-commit & post-merge hooks.
- `gulp build-sass` - Compiles & minifies sass files.
- `gulp build-js` - Minifies Javascript files.
- `gulp build-img` - Compresses image files
- `gulp translate` - Creates a .pot file of translatable strings found in the source code.
- `gulp phpcs` - Runs PHP Code Sniffer on all recently modified files.
- `gulp phpcbf` - Runs PHP Code Beautifier on all recently modified files.
- `gulp build` - An alias for running  the 'translate', 'build-sass', 'build-js', 'build-img', 'phpcbf',  & 'phpcs' gulp tasks all at once.
- `gulp composer-install` - Runs the `composer install` command.
- `gulp composer-update` - Runs the `composer update` command.
- `gulp wp-enforcer` - Installs wp-enforcer on your project.
- `gulp clean` - Deletes the `pre-commit` & `post-merge` git hooks as well as the contents of the `./dist/` directory.
- `gulp tag` - Creates a tag of the current project state on GitHub.
- `gulp zip` - Creates a zip file of your plugin or theme so that it can be manually installed on WordPress. Output is located in the `./dist/` directory
- `gulp release` - Tags the code, updates the version number and uploads a release to GitHub. 
    - **NOTE**: For releases to work, you will need to create [GitHub Access Token](https://github.com/blog/1509-personal-api-tokens) and export it to your local environment by placing it in your `.profile`, `.bash_profile`, or `.bashrc` file.
    -  i.e) `export GITHUB_TOKEN="f941e0..."`
