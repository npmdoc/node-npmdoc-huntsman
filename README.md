# api documentation for  [huntsman (v0.3.0)](https://github.com/missinglink/huntsman#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-huntsman.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-huntsman) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-huntsman.svg)](https://travis-ci.org/npmdoc/node-npmdoc-huntsman)
#### Super configurable async web spider

[![NPM](https://nodei.co/npm/huntsman.png?downloads=true)](https://www.npmjs.com/package/huntsman)

[![apidoc](https://npmdoc.github.io/node-npmdoc-huntsman/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-huntsman_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-huntsman/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-huntsman/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-huntsman/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Peter Johnson",
        "email": "@insertcoffee",
        "url": "https://github.com/missinglink/"
    },
    "bugs": {
        "url": "http://github.com/missinglink/huntsman/issues"
    },
    "dependencies": {
        "async": "0.7.0",
        "cheerio": "^0.19.0",
        "regexemitter": "0.2.3",
        "semver": "3.0.1",
        "superagent": "0.18.0"
    },
    "description": "Super configurable async web spider",
    "devDependencies": {
        "breakdown": "*",
        "coffee-script": "*",
        "mocha": "*",
        "should": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "f11858152c6e5f3b5c6bee51da2c901e3968681c",
        "tarball": "https://registry.npmjs.org/huntsman/-/huntsman-0.3.0.tgz"
    },
    "engines": {
        "node": ">0.10.0",
        "npm": ">1.1.x"
    },
    "gitHead": "38ef6b92a1f14bd761a5de5b2612283d7b3f6ded",
    "homepage": "https://github.com/missinglink/huntsman#readme",
    "keywords": [
        "spider",
        "crawler",
        "crawl",
        "huntsman",
        "robot",
        "aync"
    ],
    "license": "MIT",
    "licenses": [
        {
            "type": "MIT",
            "url": "http://www.opensource.org/licenses/MIT"
        }
    ],
    "maintainers": [
        {
            "name": "missinglink",
            "email": "peter@missinglink.co.nz"
        }
    ],
    "name": "huntsman",
    "optionalDependencies": {},
    "preferGlobal": false,
    "private": false,
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/missinglink/huntsman.git"
    },
    "scripts": {
        "test": "node node_modules/mocha/bin/mocha --recursive --reporter spec --compilers coffee:coffee-script/register test"
    },
    "version": "0.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module huntsman](#apidoc.module.huntsman)
1.  [function <span class="apidocSignatureSpan">huntsman.</span>Queue ( isUnique )](#apidoc.element.huntsman.Queue)
1.  [function <span class="apidocSignatureSpan">huntsman.</span>extension ()](#apidoc.element.huntsman.extension)
1.  [function <span class="apidocSignatureSpan">huntsman.</span>proxy ()](#apidoc.element.huntsman.proxy)
1.  [function <span class="apidocSignatureSpan">huntsman.</span>spider ( options )](#apidoc.element.huntsman.spider)
1.  [function <span class="apidocSignatureSpan">huntsman.</span>storage ()](#apidoc.element.huntsman.storage)
1.  object <span class="apidocSignatureSpan">huntsman.</span>Queue.prototype
1.  object <span class="apidocSignatureSpan">huntsman.</span>link

#### [module huntsman.Queue](#apidoc.module.huntsman.Queue)
1.  [function <span class="apidocSignatureSpan">huntsman.</span>Queue ( isUnique )](#apidoc.element.huntsman.Queue.Queue)

#### [module huntsman.Queue.prototype](#apidoc.module.huntsman.Queue.prototype)
1.  [function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>add ( key )](#apidoc.element.huntsman.Queue.prototype.add)
1.  [function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>count ()](#apidoc.element.huntsman.Queue.prototype.count)
1.  [function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>has ( key )](#apidoc.element.huntsman.Queue.prototype.has)
1.  [function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>pop ()](#apidoc.element.huntsman.Queue.prototype.pop)
1.  [function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>remove ( key )](#apidoc.element.huntsman.Queue.prototype.remove)
1.  [function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>shift ()](#apidoc.element.huntsman.Queue.prototype.shift)

#### [module huntsman.link](#apidoc.module.huntsman.link)
1.  [function <span class="apidocSignatureSpan">huntsman.link.</span>extractor ( uri, body, options )](#apidoc.element.huntsman.link.extractor)
1.  [function <span class="apidocSignatureSpan">huntsman.link.</span>normaliser ( uri )](#apidoc.element.huntsman.link.normaliser)
1.  [function <span class="apidocSignatureSpan">huntsman.link.</span>resolver ( uri, baseUri )](#apidoc.element.huntsman.link.resolver)



# <a name="apidoc.module.huntsman"></a>[module huntsman](#apidoc.module.huntsman)

#### <a name="apidoc.element.huntsman.Queue"></a>[function <span class="apidocSignatureSpan">huntsman.</span>Queue ( isUnique )](#apidoc.element.huntsman.Queue)
- description and source-code
```javascript
function Queue( isUnique ){
  this.data = [];
  this.complete = [];
  this.isUnique = ( 'boolean' === typeof isUnique ) ? isUnique : true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.huntsman.extension"></a>[function <span class="apidocSignatureSpan">huntsman.</span>extension ()](#apidoc.element.huntsman.extension)
- description and source-code
```javascript
extension = function (){
  var args = Array.prototype.slice.call( arguments, 0 );
  var module = require( './lib/' + mod + '/' + args.shift() );
  return module.apply( module, args );
}
```
- example usage
```shell
...
'''javascript
/** Crawl wikipedia and use jquery syntax to extract information from the page **/

var huntsman = require('huntsman');
var spider = huntsman.spider();

spider.extensions = [
huntsman.extension( 'recurse' ), // load recurse extension & follow anchor links
huntsman.extension( 'cheerio' ) // load cheerio extension
];

// follow pages which match this uri regex
spider.on( /http:\/\/en\.wikipedia\.org\/wiki\/\w+:\w+$/, function ( err, res ){

// use jquery-style selectors & functions
...
```

#### <a name="apidoc.element.huntsman.proxy"></a>[function <span class="apidocSignatureSpan">huntsman.</span>proxy ()](#apidoc.element.huntsman.proxy)
- description and source-code
```javascript
proxy = function (){
  var args = Array.prototype.slice.call( arguments, 0 );
  var module = require( './lib/' + mod + '/' + args.shift() );
  return module.apply( module, args );
}
```
- example usage
```shell
...
  });
});

huntsman.next = function( isSeed ){
  var uri = huntsman.queue.shift();
  if( 'string' === typeof( uri ) ){
    if( true === isSeed || huntsman.match( uri ) ){
      huntsman.proxy( uri, function( err, res ){
        huntsman.emit( 'HUNTSMAN_RESPONSE', err, res );
      });
    }
    else console.log( '[skip] uri cannot be matched to callback', uri );
  } else if (( new Date().getTime() - huntsman.options.timeout ) > huntsman.updated ){
    huntsman.stop();
  }
...
```

#### <a name="apidoc.element.huntsman.spider"></a>[function <span class="apidocSignatureSpan">huntsman.</span>spider ( options )](#apidoc.element.huntsman.spider)
- description and source-code
```javascript
spider = function ( options ){

  var huntsman = new EventEmitter();

  // Allow undefined callbacks
  // @todo add unit test for this
  huntsman.on = function( event, cb ){
    EventEmitter.prototype.on.call( this, event, cb || function(){} );
  }

  huntsman.options = options || {};
  huntsman.options.throttle = huntsman.options.throttle || 10;
  huntsman.options.timeout = huntsman.options.timeout || 5000;
  huntsman.proxy = huntsman.options.proxy || new (require('./proxy/http'))();
  huntsman.queue = huntsman.options.queue || new (require('./Queue'))();
  huntsman.extensions = [];
  huntsman.loop = function(){};
  huntsman.updated = new Date().getTime() + huntsman.options.timeout;

  // Extensions
  huntsman.on( 'HUNTSMAN_RESPONSE', function( err, res ){
    if( err ) huntsman.emit( 'HUNTSMAN_ERROR', 'response error' + err.toString('utf8') );
    huntsman.updated = new Date().getTime();
    async.parallel( huntsman.extensions.map( function( extension ){
      return async.apply( extension, huntsman, err, res );
    }), function( err, results ){
      if( err ) huntsman.emit( 'HUNTSMAN_ERROR', 'extension error' + err.toString('utf8') );
      res.extension = {};
      if( Array.isArray( results ) ){
        results.forEach( function( result ){
          for( var key in result ){ res.extension[ key ] = result[ key ]; }
        });
      }
      huntsman.emit.call( huntsman, res.uri, err, res );
    });
  });

  huntsman.next = function( isSeed ){
    var uri = huntsman.queue.shift();
    if( 'string' === typeof( uri ) ){
      if( true === isSeed || huntsman.match( uri ) ){
        huntsman.proxy( uri, function( err, res ){
          huntsman.emit( 'HUNTSMAN_RESPONSE', err, res );
        });
      }
      else console.log( '[skip] uri cannot be matched to callback', uri );
    } else if (( new Date().getTime() - huntsman.options.timeout ) > huntsman.updated ){
      huntsman.stop();
    }
  };

  huntsman.wait = function( waitms ){
    huntsman.stop();
    setTimeout( huntsman.start, waitms );
    console.error( 'waiting: ' + waitms + ' ms' );
  };

  huntsman.stop = function(){
    console.error( 'spider stop' );
    clearInterval( huntsman.loop );
    huntsman.emit( 'HUNTSMAN_EXIT' );
  };

  huntsman.start = function(){
    if( huntsman.queue.count() === 0 ) return console.error( 'no uri in queue' );
    huntsman.loop = setInterval( huntsman.next, 1000 / huntsman.options.throttle );
    huntsman.next( true );
  };

  return huntsman;
}
```
- example usage
```shell
...

### Example Script

'''javascript
/** Crawl wikipedia and use jquery syntax to extract information from the page **/

var huntsman = require('huntsman');
var spider = huntsman.spider();

spider.extensions = [
  huntsman.extension( 'recurse' ), // load recurse extension & follow anchor links
  huntsman.extension( 'cheerio' ) // load cheerio extension
];

// follow pages which match this uri regex
...
```

#### <a name="apidoc.element.huntsman.storage"></a>[function <span class="apidocSignatureSpan">huntsman.</span>storage ()](#apidoc.element.huntsman.storage)
- description and source-code
```javascript
storage = function (){
  var args = Array.prototype.slice.call( arguments, 0 );
  var module = require( './lib/' + mod + '/' + args.shift() );
  return module.apply( module, args );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.huntsman.Queue"></a>[module huntsman.Queue](#apidoc.module.huntsman.Queue)

#### <a name="apidoc.element.huntsman.Queue.Queue"></a>[function <span class="apidocSignatureSpan">huntsman.</span>Queue ( isUnique )](#apidoc.element.huntsman.Queue.Queue)
- description and source-code
```javascript
function Queue( isUnique ){
  this.data = [];
  this.complete = [];
  this.isUnique = ( 'boolean' === typeof isUnique ) ? isUnique : true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.huntsman.Queue.prototype"></a>[module huntsman.Queue.prototype](#apidoc.module.huntsman.Queue.prototype)

#### <a name="apidoc.element.huntsman.Queue.prototype.add"></a>[function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>add ( key )](#apidoc.element.huntsman.Queue.prototype.add)
- description and source-code
```javascript
add = function ( key ){
  if( !this.isUnique || ( -1 === this.complete.indexOf( key ) && !this.has( key ) ) ){
    this.data.push( key );
    return true;
  }
  return false;
}
```
- example usage
```shell
...
    body: $('div#mw-content-text p').text().trim()
  };

  console.log( wikipedia );

});

spider.queue.add( 'http://en.wikipedia.org/wiki/Huntsman_spider' );
spider.start();
'''

### Example Output

'''bash
peter@edgy:/tmp$ node examples/html.js
...
```

#### <a name="apidoc.element.huntsman.Queue.prototype.count"></a>[function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>count ()](#apidoc.element.huntsman.Queue.prototype.count)
- description and source-code
```javascript
count = function (){
  return this.data.length;
}
```
- example usage
```shell
...
  huntsman.stop = function(){
    console.error( 'spider stop' );
    clearInterval( huntsman.loop );
    huntsman.emit( 'HUNTSMAN_EXIT' );
  };

  huntsman.start = function(){
    if( huntsman.queue.count() === 0 ) return console.error( 'no uri in queue' );
    huntsman.loop = setInterval( huntsman.next, 1000 / huntsman.options.throttle );
    huntsman.next( true );
  };

  return huntsman;
};
...
```

#### <a name="apidoc.element.huntsman.Queue.prototype.has"></a>[function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>has ( key )](#apidoc.element.huntsman.Queue.prototype.has)
- description and source-code
```javascript
has = function ( key ){
  return( 0 <= this.data.indexOf( key ) );
}
```
- example usage
```shell
...
};

Queue.prototype.count = function(){
  return this.data.length;
};

Queue.prototype.add = function( key ){
  if( !this.isUnique || ( -1 === this.complete.indexOf( key ) && !this.has( key ) ) ){
    this.data.push( key );
    return true;
  }
  return false;
};

Queue.prototype.remove = function( key ){
...
```

#### <a name="apidoc.element.huntsman.Queue.prototype.pop"></a>[function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>pop ()](#apidoc.element.huntsman.Queue.prototype.pop)
- description and source-code
```javascript
pop = function (){
  val = this.data.pop();
  if( val ) this.complete.push( val );
  return val;
}
```
- example usage
```shell
...
Queue.prototype.shift = function(){
  val = this.data.shift();
  if( val ) this.complete.push( val );
  return val;
};

Queue.prototype.pop = function(){
  val = this.data.pop();
  if( val ) this.complete.push( val );
  return val;
};

module.exports = Queue;
...
```

#### <a name="apidoc.element.huntsman.Queue.prototype.remove"></a>[function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>remove ( key )](#apidoc.element.huntsman.Queue.prototype.remove)
- description and source-code
```javascript
remove = function ( key ){
  if( this.isUnique ){
    this.data = this.data.filter( function( elem ){
      return( elem !== key );
    });
  }
  else {
    var i = this.data.indexOf( key );
    if( i > -1 ){
      this.data.splice( i, 1 );
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.huntsman.Queue.prototype.shift"></a>[function <span class="apidocSignatureSpan">huntsman.Queue.prototype.</span>shift ()](#apidoc.element.huntsman.Queue.prototype.shift)
- description and source-code
```javascript
shift = function (){
  val = this.data.shift();
  if( val ) this.complete.push( val );
  return val;
}
```
- example usage
```shell
...




function loadModule( mod ){
return function(){
  var args = Array.prototype.slice.call( arguments, 0 );
  var module = require( './lib/' + mod + '/' + args.shift() );
  return module.apply( module, args );
};
}

module.exports = {
spider: require( './lib/huntsman' ),
proxy: loadModule( 'proxy' ),
...
```



# <a name="apidoc.module.huntsman.link"></a>[module huntsman.link](#apidoc.module.huntsman.link)

#### <a name="apidoc.element.huntsman.link.extractor"></a>[function <span class="apidocSignatureSpan">huntsman.link.</span>extractor ( uri, body, options )](#apidoc.element.huntsman.link.extractor)
- description and source-code
```javascript
extractor = function ( uri, body, options ) {

  var links = [];

  // accept a list of regex patterns to match & allow custom link normaliser
  if( !options ) options = {};
  if( !options.pattern ) options.pattern = {};
  if( !options.pattern.search ) options.pattern.search = pattern.search;
  if( !options.pattern.refine ) options.pattern.refine = pattern.refine;
  if( !options.pattern.filter ) options.pattern.filter = pattern.filter;
  if( !options.resolver ) options.resolver = module.exports.resolver;
  if( !options.normaliser ) options.normaliser = module.exports.normaliser;
  if( 'boolean' !== typeof options.unique ) options.unique = true;

  // match all patterns and extract links
  var matches = body.match( options.pattern.search );
  if( Array.isArray( matches ) ){
    links = links.concat( matches.filter( String ).map( function( link ){
      return link.match( options.pattern.refine )[1];
    }));
  }

  // resolve links
  if( options.resolver ){
    links = links.map( function( link ){
      return options.resolver( link, uri );
    });
  }

  // normalise links
  if( options.normaliser ){
    links = links.map( function( link ){
      return options.normaliser( link );
    });
  }

  // filter domains
  if( options.pattern.filter ){
    links = links.filter( function( link ){
      return link.match( options.pattern.filter );
    });
  }

  // remove duplicates
  if( options.unique ){
    links = links.filter( function( value, index ) {
      return links.indexOf( value ) === index;
    });
  }

  return links;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.huntsman.link.normaliser"></a>[function <span class="apidocSignatureSpan">huntsman.link.</span>normaliser ( uri )](#apidoc.element.huntsman.link.normaliser)
- description and source-code
```javascript
normaliser = function ( uri ) {
  if( ( 'string' !== typeof uri ) || !uri.length ) throw new Error( 'invalid uri' );
  return uri.replace( '/?', '?' )
            .replace( '/#', '#' )
            .replace( /\/$/, '' );
}
```
- example usage
```shell
...
    return options.resolver( link, uri );
  });
}

// normalise links
if( options.normaliser ){
  links = links.map( function( link ){
    return options.normaliser( link );
  });
}

// filter domains
if( options.pattern.filter ){
  links = links.filter( function( link ){
    return link.match( options.pattern.filter );
...
```

#### <a name="apidoc.element.huntsman.link.resolver"></a>[function <span class="apidocSignatureSpan">huntsman.link.</span>resolver ( uri, baseUri )](#apidoc.element.huntsman.link.resolver)
- description and source-code
```javascript
resolver = function ( uri, baseUri ) {
  if( ( 'string' !== typeof uri ) || !uri.length ) throw new Error( 'invalid uri' );
  return baseUri ? resolve( baseUri, uri ) : uri;
}
```
- example usage
```shell
...
    return link.match( options.pattern.refine )[1];
  }));
}

// resolve links
if( options.resolver ){
  links = links.map( function( link ){
    return options.resolver( link, uri );
  });
}

// normalise links
if( options.normaliser ){
  links = links.map( function( link ){
    return options.normaliser( link );
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
