# Siyavula Website

## Installation

1. Install jekyll: `sudo gem install jekyll`
2. Install gulp-cli globally: `sudo npm install -g gulp-cli`
3. Clone the git repository: `git clone git@github.com:Siyavula/Siyavula.github.io.git`
4. Go to the repository directory and install dependencies locally: `cd Siyavula.github.io && npm install`

### Failure

If jekyll fails to build in step 1 with error `mkmf.rb can't find header files`, then install ruby dev package:

* Ubuntu/Debian: `sudo apt-get install ruby-dev`
* Red Hat/RPM-based distro: `sudo apt-get install ruby-devel`

Run step 1 again.


## Development

### Working with Static Resources

The main css for the website will be managed through a SASS file at '_sass/style.scss'. For those
familiar with the benefits of SCSS, this supports all of them. For those not quite comfortable with
SCSSS, the file can be continued to be used like a normal CSS file, however Jekyll will
automatically minify the file for you.

### Compressing static resources

To manually minify resources, install the minifier as such:

`npm install -g minifier`

CSS files can be minified as follows:

* Individually: `minify my_styles.css`  (this will create my_styles.min.css)

* Combining them: `minify --output combined.min.css styles1.css styles2.css`  (this
    will take the contents of both styles1.css and styles2.css and combine (and minify) them into
    one css file).

For this project, fontello.css and font-awesome.css have been combined into fonts.min.css.

The same can be done for javascript. In this case, the app.js has been minified and the jquery
plugins minified into a single file:

`minify --output jquery_plugins.min.js jquery.countTo.js jquery.appear.js jquery.validate.js jquery.sequence-min.js jquery.easing.1.3.js`

## Running the Website

You can run the website using:

`jekyll serve --host 0.0.0.0`

This will run on port 4000 by default and will automatically restart on all changes. You can access
the website in the browser at:

`localhost:4000`

To access the site over a network, find your IP address:

`ifconfig -a`

and open in a browser:

`192.168.xxx.xxx:4000`
