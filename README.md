# api documentation for  [critical (v0.8.4)](https://github.com/addyosmani/critical#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-critical.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-critical) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-critical.svg)](https://travis-ci.org/npmdoc/node-npmdoc-critical)
#### Extract & Inline Critical-path CSS from HTML

[![NPM](https://nodei.co/npm/critical.png?downloads=true)](https://www.npmjs.com/package/critical)

[![apidoc](https://npmdoc.github.io/node-npmdoc-critical/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-critical_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-critical/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-critical/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Addy Osmani"
    },
    "bin": {
        "critical": "cli.js"
    },
    "bugs": {
        "url": "https://github.com/addyosmani/critical/issues"
    },
    "dependencies": {
        "bluebird": "^3.4.7",
        "chalk": "^1.1.3",
        "cheerio": "^0.22.0",
        "clean-css": "^4.0.6",
        "cli": "^1.0.1",
        "debug": "^2.6.1",
        "filter-css": "^0.1.2",
        "finalhandler": "^0.5.1",
        "fs-extra": "^2.0.0",
        "get-port": "^2.1.0",
        "get-stdin": "^5.0.1",
        "gulp-util": "^3.0.8",
        "imageinliner": "^0.2.4",
        "indent-string": "^3.1.0",
        "inline-critical": "^2.4.0",
        "lodash": "^4.17.4",
        "meow": "^3.7.0",
        "mime-types": "^2.1.14",
        "oust": "^0.3.0",
        "parseurl": "^1.3.1",
        "penthouse": "^0.10.9",
        "postcss": "^5.2.12",
        "postcss-image-inliner": "^1.0.4",
        "request": "^2.79.0",
        "serve-static": "^1.11.2",
        "slash": "^1.0.0",
        "tempfile": "^1.1.1",
        "through2": "^2.0.3",
        "tmp": "^0.0.31",
        "vinyl": "^2.0.1"
    },
    "description": "Extract & Inline Critical-path CSS from HTML",
    "devDependencies": {
        "async": "^2.1.4",
        "chai": "^3.5.0",
        "connect": "^3.5.0",
        "mocha": "^3.2.0",
        "mockery": "^2.0.0",
        "normalize-newline": "^3.0.0",
        "read-package-json": "^2.0.4",
        "stream-array": "^1.1.2",
        "stream-assert": "^2.0.3",
        "vinyl-source-stream": "^1.1.0",
        "xo": "^0.17.1"
    },
    "directories": {},
    "dist": {
        "shasum": "beb716afa221a84c4ed216719c18e25a8ac8a3c2",
        "tarball": "https://registry.npmjs.org/critical/-/critical-0.8.4.tgz"
    },
    "engines": {
        "node": ">=4.0"
    },
    "files": [
        "cli.js",
        "index.js",
        "lib"
    ],
    "gitHead": "24465c459830e06af4a4fd593c0c287ee21c197c",
    "homepage": "https://github.com/addyosmani/critical#readme",
    "keywords": [
        "critical",
        "path",
        "css",
        "optimization"
    ],
    "license": "Apache-2.0",
    "maintainers": [
        {
            "name": "addyosmani",
            "email": "addyosmani@gmail.com"
        },
        {
            "name": "sindresorhus",
            "email": "sindresorhus@gmail.com"
        },
        {
            "name": "bezoerb",
            "email": "ben@sommerlaune.com"
        }
    ],
    "name": "critical",
    "optionalDependencies": {},
    "preferGlobal": true,
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/addyosmani/critical.git"
    },
    "scripts": {
        "test": "xo && mocha test/*.js --timeout 100000"
    },
    "version": "0.8.4",
    "xo": {
        "space": 4
    }
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module critical](#apidoc.module.critical)
1.  [function <span class="apidocSignatureSpan">critical.</span>generate (opts, cb)](#apidoc.element.critical.generate)
1.  [function <span class="apidocSignatureSpan">critical.</span>generateInline (opts, cb)](#apidoc.element.critical.generateInline)
1.  [function <span class="apidocSignatureSpan">critical.</span>inline (opts, cb)](#apidoc.element.critical.inline)
1.  [function <span class="apidocSignatureSpan">critical.</span>stream (opts)](#apidoc.element.critical.stream)
1.  [function <span class="apidocSignatureSpan">critical.</span>vinyl_remote (file)](#apidoc.element.critical.vinyl_remote)
1.  object <span class="apidocSignatureSpan">critical.</span>core
1.  object <span class="apidocSignatureSpan">critical.</span>file_helper
1.  object <span class="apidocSignatureSpan">critical.</span>gc
1.  object <span class="apidocSignatureSpan">critical.</span>vinyl_remote.prototype

#### [module critical.core](#apidoc.module.critical.core)
1.  [function <span class="apidocSignatureSpan">critical.core.</span>generate (opts)](#apidoc.element.critical.core.generate)

#### [module critical.file_helper](#apidoc.module.critical.file_helper)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>assertLocal (opts)](#apidoc.element.critical.file_helper.assertLocal)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>getPenthouseUrl (opts, file, port)](#apidoc.element.critical.file_helper.getPenthouseUrl)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>getVinylPromise (opts)](#apidoc.element.critical.file_helper.getVinylPromise)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>guessBasePath (opts)](#apidoc.element.critical.file_helper.guessBasePath)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>isExternal (href)](#apidoc.element.critical.file_helper.isExternal)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>isVinyl (file)](#apidoc.element.critical.file_helper.isVinyl)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>replaceAssetPaths (html, opts)](#apidoc.element.critical.file_helper.replaceAssetPaths)
1.  [function <span class="apidocSignatureSpan">critical.file_helper.</span>resourcePath (htmlfile, opts)](#apidoc.element.critical.file_helper.resourcePath)

#### [module critical.gc](#apidoc.module.critical.gc)
1.  [function <span class="apidocSignatureSpan">critical.gc.</span>addFile (file)](#apidoc.element.critical.gc.addFile)

#### [module critical.vinyl_remote](#apidoc.module.critical.vinyl_remote)
1.  [function <span class="apidocSignatureSpan">critical.</span>vinyl_remote (file)](#apidoc.element.critical.vinyl_remote.vinyl_remote)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.</span>isCustomProp (key)](#apidoc.element.critical.vinyl_remote.isCustomProp)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.</span>isVinyl (file)](#apidoc.element.critical.vinyl_remote.isVinyl)

#### [module critical.vinyl_remote.prototype](#apidoc.module.critical.vinyl_remote.prototype)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>clone (opt)](#apidoc.element.critical.vinyl_remote.prototype.clone)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>inspect ()](#apidoc.element.critical.vinyl_remote.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isBuffer ()](#apidoc.element.critical.vinyl_remote.prototype.isBuffer)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isDirectory ()](#apidoc.element.critical.vinyl_remote.prototype.isDirectory)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isNull ()](#apidoc.element.critical.vinyl_remote.prototype.isNull)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isStream ()](#apidoc.element.critical.vinyl_remote.prototype.isStream)
1.  [function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isSymbolic ()](#apidoc.element.critical.vinyl_remote.prototype.isSymbolic)



# <a name="apidoc.module.critical"></a>[module critical](#apidoc.module.critical)

#### <a name="apidoc.element.critical.generate"></a>[function <span class="apidocSignatureSpan">critical.</span>generate (opts, cb)](#apidoc.element.critical.generate)
- description and source-code
```javascript
generate = function (opts, cb) {
    opts = prepareOptions(opts);

    // generate critical css
    var corePromise = core.generate(opts);

    // @deprecated
    // should be removed in next major release
    if (opts.styleTarget) {
        corePromise.then(function (output) {
            var file = path.resolve(opts.styleTarget);
            var dir = path.dirname(file);
            return fs.ensureDirAsync(dir).then(function () {
                return fs.writeFileAsync(path.resolve(opts.styleTarget), output);
            });
        });
    }

    // inline
    if (opts.inline) {
        corePromise = Bluebird.props({
            file: file.getVinylPromise(opts),
            css: corePromise
        }).then(function (result) {
            return sourceInliner(result.file.contents.toString(), result.css, {
                minify: opts.minify || false,
                extract: opts.extract || false,
                basePath: opts.base || process.cwd()
            });
        });
    }

    // save to file
    if (opts.dest) {
        corePromise = corePromise.then(function (output) {
            var file = path.resolve(opts.dest);
            var dir = path.dirname(file);
            return fs.ensureDirAsync(dir).then(function () {
                return fs.writeFileAsync(path.resolve(opts.dest), output);
            }).then(function () {
                return output;
            });
        });
    }

    // return promise if callback is not defined
    if (_.isFunction(cb)) {
        corePromise.catch(function (err) {
            cb(err);
            throw new Bluebird.CancellationError();
        }).then(function (output) {
            cb(null, output.toString());
        }).catch(Bluebird.CancellationError, function () {
        }).done();
    } else {
        return corePromise;
    }
}
```
- example usage
```shell
...
'''js
var critical = require('critical');
'''

Full blown example with available options:

'''js
critical.generate({
// Inline the generated critical-path CSS
// - true generates HTML
// - false generates CSS
inline: true,

// Your base directory
base: 'dist/',
...
```

#### <a name="apidoc.element.critical.generateInline"></a>[function <span class="apidocSignatureSpan">critical.</span>generateInline (opts, cb)](#apidoc.element.critical.generateInline)
- description and source-code
```javascript
generateInline = function (opts, cb) {
    opts.inline = true;
    if (opts.htmlTarget) {
        opts.dest = opts.htmlTarget;
    } else if (opts.styleTarget) {
        // return error
    }

    return exports.generate(opts, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.inline"></a>[function <span class="apidocSignatureSpan">critical.</span>inline (opts, cb)](#apidoc.element.critical.inline)
- description and source-code
```javascript
inline = function (opts, cb) {
    opts = opts || {};
    cb = cb || function () {};

    if (!opts.src || !opts.base) {
        throw new Error('A valid source and base path are required.');
    }

    // Inline the critical path CSS
    fs.readFile(path.join(opts.base, opts.src), function (err, data) {
        if (err) {
            cb(err);
            return;
        }

        var out = inliner(data, opts);

        if (opts.dest) {
            // Write HTML with inlined CSS to dest
            fs.writeFile(path.resolve(opts.dest), out, function (err) {
                if (err) {
                    cb(err);
                    return;
                }

                cb(null, out.toString());
            });
        } else {
            cb(null, out.toString());
        }
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.stream"></a>[function <span class="apidocSignatureSpan">critical.</span>stream (opts)](#apidoc.element.critical.stream)
- description and source-code
```javascript
stream = function (opts) {
    // return stream
    return through2.obj(function (file, enc, cb) {
        if (file.isNull()) {
            return cb(null, file);
        }

        if (file.isStream()) {
            return this.emit('error', new PluginError('critical', 'Streaming not supported'));
        }

        var options = _.assign(opts || {}, {
            src: file
        });

        exports.generate(options, function (err, data) {
            if (err) {
                return cb(new PluginError('critical', err.message));
            }

            // rename file if not inlined
            if (!opts.inline) {
                file.path = replaceExtension(file.path, '.css');
            }

            file.contents = new Buffer(data);
            cb(err, file);
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.vinyl_remote"></a>[function <span class="apidocSignatureSpan">critical.</span>vinyl_remote (file)](#apidoc.element.critical.vinyl_remote)
- description and source-code
```javascript
function File(file) {
  var self = this;

  if (!file) {
    file = {};
  }

  // Stat = files stats object
  this.stat = file.stat || null;

  // Contents = stream, buffer, or null if not read
  this.contents = file.contents || null;

  // Replay path history to ensure proper normalization and trailing sep
  var history = Array.prototype.slice.call(file.history || []);
  if (file.path) {
    history.push(file.path);
  }
  this.history = [];
  history.forEach(function(path) {
    self.path = path;
  });

  this.cwd = file.cwd || process.cwd();
  this.base = file.base;

  this._isVinyl = true;

  this._symlink = null;

  // Set custom properties
  Object.keys(file).forEach(function(key) {
    if (self.constructor.isCustomProp(key)) {
      self[key] = file[key];
    }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.critical.core"></a>[module critical.core](#apidoc.module.critical.core)

#### <a name="apidoc.element.critical.core.generate"></a>[function <span class="apidocSignatureSpan">critical.core.</span>generate (opts)](#apidoc.element.critical.core.generate)
- description and source-code
```javascript
function generate(opts) {
    opts = opts || {};

    if (!opts.src && !opts.html) {
        return Bluebird.reject(new Error('A valid source is required.'));
    }

    if (!opts.dimensions) {
        opts.dimensions = [{
            height: opts.height || 900,
            width: opts.width || 1300
        }];
    }

    debug('Start with the following options');
    debug(opts);

    return Bluebird.map(opts.dimensions, function (dimensions) {
        // use content to fetch used css files
        return file.getVinylPromise(opts)
            .then(appendStylesheets(opts))
            .then(processStylesheets(opts))
            .then(computeCritical(dimensions, opts));
    }).then(function (criticalCSS) {
        criticalCSS = combineCss(criticalCSS);

        if (opts.ignore) {
            debug('generate', 'Applying filter', opts.ignore);
            criticalCSS = filterCss(criticalCSS, opts.ignore, opts.ignoreOptions || {});
        }

        if (opts.minify === true) {
            debug('generate', 'Minify css');
            criticalCSS = new CleanCSS().minify(criticalCSS).styles;
        }

        debug('generate', 'Done');
        return criticalCSS;
    });
}
```
- example usage
```shell
...
'''js
var critical = require('critical');
'''

Full blown example with available options:

'''js
critical.generate({
// Inline the generated critical-path CSS
// - true generates HTML
// - false generates CSS
inline: true,

// Your base directory
base: 'dist/',
...
```



# <a name="apidoc.module.critical.file_helper"></a>[module critical.file_helper](#apidoc.module.critical.file_helper)

#### <a name="apidoc.element.critical.file_helper.assertLocal"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>assertLocal (opts)](#apidoc.element.critical.file_helper.assertLocal)
- description and source-code
```javascript
function assertLocal(opts) {
    return function (filePath) {
        if (!isExternal(filePath)) {
            return new Bluebird(function (resolve) {
                resolve(filePath);
            });
        }
        return requestAsync(filePath)
            .then(temp({
                dir: opts.base
            }));
    };
}
```
- example usage
```shell
...
            return htmlfile;
        }

        // Oust extracts a list of your stylesheets
        var stylesheets = oust(htmlfile.contents.toString(), 'stylesheets');
        debug('appendStylesheets', stylesheets);
        stylesheets = stylesheets.map(file.resourcePath(htmlfile, opts));
        return Bluebird.map(stylesheets, file.assertLocal(opts)).then(function (stylesheets) {
            htmlfile.stylesheets = stylesheets;
            return htmlfile;
        });
    };
}

/**
...
```

#### <a name="apidoc.element.critical.file_helper.getPenthouseUrl"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>getPenthouseUrl (opts, file, port)](#apidoc.element.critical.file_helper.getPenthouseUrl)
- description and source-code
```javascript
function getPenthouseUrl(opts, file, port) {
    if (opts.src && isExternal(opts.src)) {
        return opts.src;
    }

    return 'http://127.0.0.1:' + port + '/' + normalizePath(path.relative(path.resolve(file.base), file.path));
}
```
- example usage
```shell
...
 * @returns {function}
 */
function computeCritical(dimensions, opts) {
return function (htmlfile) {
    return startServer(opts).then(function (server) {
        debug('Processing: ' + htmlfile.path + ' [' + dimensions.width + 'x' + dimensions.height + ']');
        return penthouseAsync({
            url: file.getPenthouseUrl(opts, htmlfile, server.port),
            css: htmlfile.cssPath,
            forceInclude: opts.include || [],
            timeout: opts.timeout,
            maxEmbeddedBase64Length: opts.maxImageFileSize || 10240,
            width: dimensions.width,
            height: dimensions.height
        }).finally(function () {
...
```

#### <a name="apidoc.element.critical.file_helper.getVinylPromise"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>getVinylPromise (opts)](#apidoc.element.critical.file_helper.getVinylPromise)
- description and source-code
```javascript
function getVinylPromise(opts) {
    if (!(opts.src || opts.html) || !opts.base) {
        return Bluebird.reject(new Error('A valid source and base path are required.'));
    }

    if (isVinyl(opts.src)) {
        return new Bluebird(function (resolve) {
            resolve(opts.src);
        });
    }

    var file = new File({
        base: opts.base
    });

    if (opts.src && isExternal(opts.src)) {
        file.remotePath = opts.src;
    } else if (opts.src) {
        file.path = opts.src;
    }

    if (opts.html) {
        var folder = generateSourcePath(opts);
        debug('hacky source path folder', folder);

        // html passed in directly -> create tmp file
        return tmp.fileAsync({dir: opts.base, postfix: '.html'})
            .then(getFirst)
            .then(function (filepath) {
                file.path = filepath;
                file.path = path.join(folder, path.basename(filepath));
                file.base = folder;
                file.contents = new Buffer(opts.html);
                gc.addFile(filepath);
                return fs.writeFileAsync(filepath, file.contents).then(function () {
                    return file;
                });
            });
    }

    // use src file provided, fetch content and return vinyl
    return assertLocal(opts)(opts.src)
        .then(function (data) {
            // src can either be absolute or relative to opts.base
            if (opts.src !== path.resolve(data) && !isExternal(opts.src)) {
                file.path = path.join(opts.base, opts.src);
            } else {
                file.path = path.relative(process.cwd(), data);
            }

            return fs.readFileAsync(file.path).then(function (contents) {
                file.contents = contents;
                return file;
            });
        });
}
```
- example usage
```shell
...
        });
    });
}

// inline
if (opts.inline) {
    corePromise = Bluebird.props({
        file: file.getVinylPromise(opts),
        css: corePromise
    }).then(function (result) {
        return sourceInliner(result.file.contents.toString(), result.css, {
            minify: opts.minify || false,
            extract: opts.extract || false,
            basePath: opts.base || process.cwd()
        });
...
```

#### <a name="apidoc.element.critical.file_helper.guessBasePath"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>guessBasePath (opts)](#apidoc.element.critical.file_helper.guessBasePath)
- description and source-code
```javascript
function guessBasePath(opts) {
    if (opts.src && !isExternal(opts.src) && !isVinyl(opts.src)) {
        return path.dirname(opts.src);
    } else if (opts.src && isVinyl(opts.src)) {
        return opts.src.dirname;
    }

    return process.cwd();
}
```
- example usage
```shell
...
 */
function prepareOptions(opts) {
if (!opts) {
    opts = {};
}

var options = _.defaults(opts, {
    base: file.guessBasePath(opts),
    dimensions: [{
        height: opts.height || 900,
        width: opts.width || 1300
    }]
});

// set dest relative to base if isn't specivied absolute
...
```

#### <a name="apidoc.element.critical.file_helper.isExternal"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>isExternal (href)](#apidoc.element.critical.file_helper.isExternal)
- description and source-code
```javascript
function isExternal(href) {
    return /(^\/\/)|(:\/\/)/.test(href);
}
```
- example usage
```shell
...
            var assetPaths = opts.assetPaths || [];

            // Add some suitable fallbacks for convinience if nothing is set.
            // Otherwise don't add them to keep the user in control
            if (assetPaths.length === 0) {
assetPaths.push(path.dirname(vinyl.path));
// Add domain as asset source for external domains
if (file.isExternal(opts.src)) {
    var urlObj = url.parse(opts.src);
    var domain = urlObj.protocol + '//' + urlObj.host;
    assetPaths.push(domain, domain + path.dirname(urlObj.pathname));
}

if (opts.base) {
    assetPaths.push(opts.base);
...
```

#### <a name="apidoc.element.critical.file_helper.isVinyl"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>isVinyl (file)](#apidoc.element.critical.file_helper.isVinyl)
- description and source-code
```javascript
function isVinyl(file) {
    return File.isVinyl(file) ||
        file instanceof File ||
        (file && /function File\(/.test(file.constructor.toString()) && file.contents && file.path);
}
```
- example usage
```shell
...

/**
* Wrapper for File.isVinyl to detect vinyl objects generated by gulp (vinyl < v0.5.6)
* @param {*} file
* @returns {string}
*/
function isVinyl(file) {
   return File.isVinyl(file) ||
       file instanceof File ||
       (file && /function File\(/.test(file.constructor.toString()) && file.contents && file.path);
}

/**
* Returns a promise to a local file
* @param {object} opts Options passed to critical
...
```

#### <a name="apidoc.element.critical.file_helper.replaceAssetPaths"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>replaceAssetPaths (html, opts)](#apidoc.element.critical.file_helper.replaceAssetPaths)
- description and source-code
```javascript
function replaceAssetPaths(html, opts) {
    // set dest path with fallback to html path
    var destPath = opts.destFolder || (opts.dest && path.dirname(opts.dest)) || path.dirname(html.path);
    var destPathResolved = path.resolve(destPath);
    var baseResolved = path.resolve(opts.base);

<span class="apidocCodeCommentSpan">    /**
     * the resulting function should get passed an vinyl object with the css file
     */
</span>    return function (stylesheet) {
        // normalize relative paths
        var css = stylesheet.contents.toString().replace(/url\(['"]?([^'"\\)]+)['"]?\)/g, function (match, assetPath) {
            // skip absolute paths, urls and data-uris
            if (/^data:/.test(assetPath) || /(?:^\/)|(?::\/\/)/.test(assetPath)) {
                return match;
            }

            // create asset path relative to opts.base
            var stylesheetPath = path.dirname(stylesheet.path);
            var assetRelative = path.relative(baseResolved, path.resolve(path.join(stylesheetPath, assetPath)));

            // compute path prefix default relative to html
            var pathPrefixDefault = path.relative(destPathResolved, baseResolved);

            var pathPrefix = (typeof opts.pathPrefix === 'undefined') ? pathPrefixDefault : opts.pathPrefix;

            return normalizePath(match.replace(assetPath, path.join(pathPrefix, assetRelative)));
        });

        stylesheet.contents = new Buffer(css);
        return stylesheet;
    };
}
```
- example usage
```shell
...
 * @returns {function}
 */
function processStylesheets(opts) {
return function (htmlfile) {
    debug('processStylesheets', htmlfile.stylesheets);
    return Bluebird.map(htmlfile.stylesheets, vinylize(opts))
        .map(inlineImages(opts))
        .map(file.replaceAssetPaths(htmlfile, opts))
        .reduce(function (total, stylesheet) {
            return total + os.EOL + stylesheet.contents.toString('utf8');
        }, '')
        .then(function (css) {
            htmlfile.cssPath = tempfile('.css');
            // add file to garbage collector so it get's removed on exit
            gc.addFile(htmlfile.cssPath);
...
```

#### <a name="apidoc.element.critical.file_helper.resourcePath"></a>[function <span class="apidocSignatureSpan">critical.file_helper.</span>resourcePath (htmlfile, opts)](#apidoc.element.critical.file_helper.resourcePath)
- description and source-code
```javascript
function resourcePath(htmlfile, opts) {
    return function (filepath) {
        if (isExternal(filepath)) {
            debug('resourcePath - remote', filepath);
            return filepath;
        }

        if (isExternal(htmlfile.history[0])) {
            debug('resourcePath - remote', htmlfile.history[0]);
            return url.resolve(htmlfile.history[0], filepath);
        }

        if (/(?:^\/)/.test(filepath)) {
            return path.join(opts.base, filepath.split('?')[0]);
        }
        var folder = path.relative(opts.base, path.dirname(htmlfile.path));
        if (folder) {
            debug('resourcePath - folder', folder);
        }
        return path.join(path.dirname(htmlfile.path), filepath.split('?')[0]);
    };
}
```
- example usage
```shell
...
            htmlfile.stylesheets = typeof opts.css === 'string' ? [opts.css] : opts.css;
            return htmlfile;
        }

        // Oust extracts a list of your stylesheets
        var stylesheets = oust(htmlfile.contents.toString(), 'stylesheets');
        debug('appendStylesheets', stylesheets);
        stylesheets = stylesheets.map(file.resourcePath(htmlfile, opts));
        return Bluebird.map(stylesheets, file.assertLocal(opts)).then(function (stylesheets) {
            htmlfile.stylesheets = stylesheets;
            return htmlfile;
        });
    };
}
...
```



# <a name="apidoc.module.critical.gc"></a>[module critical.gc](#apidoc.module.critical.gc)

#### <a name="apidoc.element.critical.gc.addFile"></a>[function <span class="apidocSignatureSpan">critical.gc.</span>addFile (file)](#apidoc.element.critical.gc.addFile)
- description and source-code
```javascript
addFile = function (file) {
    files.push(file);
}
```
- example usage
```shell
...
            .map(file.replaceAssetPaths(htmlfile, opts))
            .reduce(function (total, stylesheet) {
                return total + os.EOL + stylesheet.contents.toString('utf8');
            }, '')
            .then(function (css) {
                htmlfile.cssPath = tempfile('.css');
                // add file to garbage collector so it get's removed on exit
                gc.addFile(htmlfile.cssPath);

                return fs.writeFileAsync(htmlfile.cssPath, css).then(function () {
                    return htmlfile;
                });
            });
    };
}
...
```



# <a name="apidoc.module.critical.vinyl_remote"></a>[module critical.vinyl_remote](#apidoc.module.critical.vinyl_remote)

#### <a name="apidoc.element.critical.vinyl_remote.vinyl_remote"></a>[function <span class="apidocSignatureSpan">critical.</span>vinyl_remote (file)](#apidoc.element.critical.vinyl_remote.vinyl_remote)
- description and source-code
```javascript
function File(file) {
  var self = this;

  if (!file) {
    file = {};
  }

  // Stat = files stats object
  this.stat = file.stat || null;

  // Contents = stream, buffer, or null if not read
  this.contents = file.contents || null;

  // Replay path history to ensure proper normalization and trailing sep
  var history = Array.prototype.slice.call(file.history || []);
  if (file.path) {
    history.push(file.path);
  }
  this.history = [];
  history.forEach(function(path) {
    self.path = path;
  });

  this.cwd = file.cwd || process.cwd();
  this.base = file.base;

  this._isVinyl = true;

  this._symlink = null;

  // Set custom properties
  Object.keys(file).forEach(function(key) {
    if (self.constructor.isCustomProp(key)) {
      self[key] = file[key];
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.vinyl_remote.isCustomProp"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.</span>isCustomProp (key)](#apidoc.element.critical.vinyl_remote.isCustomProp)
- description and source-code
```javascript
isCustomProp = function (key) {
  return builtInFields.indexOf(key) === -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.vinyl_remote.isVinyl"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.</span>isVinyl (file)](#apidoc.element.critical.vinyl_remote.isVinyl)
- description and source-code
```javascript
isVinyl = function (file) {
  return (file && file._isVinyl === true) || false;
}
```
- example usage
```shell
...

/**
* Wrapper for File.isVinyl to detect vinyl objects generated by gulp (vinyl < v0.5.6)
* @param {*} file
* @returns {string}
*/
function isVinyl(file) {
   return File.isVinyl(file) ||
       file instanceof File ||
       (file && /function File\(/.test(file.constructor.toString()) && file.contents && file.path);
}

/**
* Returns a promise to a local file
* @param {object} opts Options passed to critical
...
```



# <a name="apidoc.module.critical.vinyl_remote.prototype"></a>[module critical.vinyl_remote.prototype](#apidoc.module.critical.vinyl_remote.prototype)

#### <a name="apidoc.element.critical.vinyl_remote.prototype.clone"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>clone (opt)](#apidoc.element.critical.vinyl_remote.prototype.clone)
- description and source-code
```javascript
clone = function (opt) {
  var self = this;

  if (typeof opt === 'boolean') {
    opt = {
      deep: opt,
      contents: true,
    };
  } else if (!opt) {
    opt = {
      deep: true,
      contents: true,
    };
  } else {
    opt.deep = opt.deep === true;
    opt.contents = opt.contents !== false;
  }

  // Clone our file contents
  var contents;
  if (this.isStream()) {
    contents = this.contents.clone();
  } else if (this.isBuffer()) {
    contents = opt.contents ? cloneBuffer(this.contents) : this.contents;
  }

  var file = new this.constructor({
    cwd: this.cwd,
    base: this.base,
    stat: (this.stat ? cloneStats(this.stat) : null),
    history: this.history.slice(),
    contents: contents,
  });

  // Clone our custom properties
  Object.keys(this).forEach(function(key) {
    if (self.constructor.isCustomProp(key)) {
      file[key] = opt.deep ? clone(self[key], true) : self[key];
    }
  });
  return file;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.vinyl_remote.prototype.inspect"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>inspect ()](#apidoc.element.critical.vinyl_remote.prototype.inspect)
- description and source-code
```javascript
inspect = function () {
  var inspect = [];

  // Use relative path if possible
  var filePath = this.path ? this.relative : null;

  if (filePath) {
    inspect.push('"' + filePath + '"');
  }

  if (this.isBuffer()) {
    inspect.push(this.contents.inspect());
  }

  if (this.isStream()) {
    inspect.push(inspectStream(this.contents));
  }

  return '<File ' + inspect.join(' ') + '>';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.vinyl_remote.prototype.isBuffer"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isBuffer ()](#apidoc.element.critical.vinyl_remote.prototype.isBuffer)
- description and source-code
```javascript
isBuffer = function () {
  return isBuffer(this.contents);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.vinyl_remote.prototype.isDirectory"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isDirectory ()](#apidoc.element.critical.vinyl_remote.prototype.isDirectory)
- description and source-code
```javascript
isDirectory = function () {
  if (!this.isNull()) {
    return false;
  }

  if (this.stat && typeof this.stat.isDirectory === 'function') {
    return this.stat.isDirectory();
  }

  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.critical.vinyl_remote.prototype.isNull"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isNull ()](#apidoc.element.critical.vinyl_remote.prototype.isNull)
- description and source-code
```javascript
isNull = function () {
  return (this.contents === null);
}
```
- example usage
```shell
...
 *
 * @param {object} opts
 * @returns {*}
 */
exports.stream = function (opts) {
    // return stream
    return through2.obj(function (file, enc, cb) {
if (file.isNull()) {
    return cb(null, file);
}

if (file.isStream()) {
    return this.emit('error', new PluginError('critical', 'Streaming not supported'));
}
...
```

#### <a name="apidoc.element.critical.vinyl_remote.prototype.isStream"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isStream ()](#apidoc.element.critical.vinyl_remote.prototype.isStream)
- description and source-code
```javascript
isStream = function () {
  return isStream(this.contents);
}
```
- example usage
```shell
...
exports.stream = function (opts) {
    // return stream
    return through2.obj(function (file, enc, cb) {
if (file.isNull()) {
    return cb(null, file);
}

if (file.isStream()) {
    return this.emit('error', new PluginError('critical', 'Streaming not supported'));
}

var options = _.assign(opts || {}, {
    src: file
});
...
```

#### <a name="apidoc.element.critical.vinyl_remote.prototype.isSymbolic"></a>[function <span class="apidocSignatureSpan">critical.vinyl_remote.prototype.</span>isSymbolic ()](#apidoc.element.critical.vinyl_remote.prototype.isSymbolic)
- description and source-code
```javascript
isSymbolic = function () {
  if (!this.isNull()) {
    return false;
  }

  if (this.stat && typeof this.stat.isSymbolicLink === 'function') {
    return this.stat.isSymbolicLink();
  }

  return false;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
