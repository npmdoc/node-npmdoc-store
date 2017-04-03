# api documentation for  [store (v2.0.4)](https://github.com/marcuswestin/store.js#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-store.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-store) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-store.svg)](https://travis-ci.org/npmdoc/node-npmdoc-store)
#### A localStorage wrapper for all browsers without using cookies or flash. Uses localStorage, globalStorage, and userData behavior under the hood

[![NPM](https://nodei.co/npm/store.png?downloads=true)](https://www.npmjs.com/package/store)

[![apidoc](https://npmdoc.github.io/node-npmdoc-store/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-store_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-store/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-store/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-store/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Marcus Westin",
        "email": "narcvs@gmail.com"
    },
    "bugs": {
        "url": "http://github.com/marcuswestin/store.js/issues"
    },
    "dependencies": {},
    "description": "A localStorage wrapper for all browsers without using cookies or flash. Uses localStorage, globalStorage, and userData behavior under the hood",
    "devDependencies": {
        "babel-preset-es2015": "^6.22.0",
        "babelify": "^7.3.0",
        "browserify": "^14.1.0",
        "budo": "^7.1.0",
        "eslint": "^3.12.2",
        "lodash": "^3.10.1",
        "ngrok": "^2.2.6",
        "node-localstorage": "^0.6.0",
        "request": "^2.67.0",
        "tinytest": "^1.1.3",
        "uglify-js": "^2.7.5"
    },
    "directories": {
        "lib": "."
    },
    "dist": {
        "shasum": "6c6819602a5497166ade85db2442cc64ebcc5761",
        "tarball": "https://registry.npmjs.org/store/-/store-2.0.4.tgz"
    },
    "engines": {
        "node": "*"
    },
    "eslintConfig": {
        "env": {
            "browser": true,
            "commonjs": true,
            "es6": true,
            "node": true
        },
        "extends": "eslint:recommended",
        "parserOptions": {
            "sourceType": "module"
        },
        "globals": {
            "test": false,
            "assert": false,
            "print": false
        },
        "rules": {
            "no-unused-vars": [
                "error",
                {
                    "vars": "all",
                    "args": "none",
                    "varsIgnorePattern": "^_$"
                }
            ],
            "indent": [
                "error",
                "tab"
            ],
            "linebreak-style": [
                "error",
                "unix"
            ],
            "semi": [
                "error",
                "never"
            ]
        }
    },
    "gitHead": "4fbbc9692ceaf16824ac2b11008a878caedffd85",
    "homepage": "https://github.com/marcuswestin/store.js#readme",
    "license": "MIT",
    "main": "dist/store.legacy.js",
    "maintainers": [
        {
            "name": "marcuswestin",
            "email": "narcvs@gmail.com"
        }
    ],
    "name": "store",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/marcuswestin/store.js.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "2.0.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module store](#apidoc.module.store)
1.  boolean <span class="apidocSignatureSpan">store.</span>enabled
1.  [function <span class="apidocSignatureSpan">store.</span>addPlugin (plugin)](#apidoc.element.store.addPlugin)
1.  [function <span class="apidocSignatureSpan">store.</span>addStorage (storage)](#apidoc.element.store.addStorage)
1.  [function <span class="apidocSignatureSpan">store.</span>clearAll ()](#apidoc.element.store.clearAll)
1.  [function <span class="apidocSignatureSpan">store.</span>createStore (storages, plugins)](#apidoc.element.store.createStore)
1.  [function <span class="apidocSignatureSpan">store.</span>each (callback)](#apidoc.element.store.each)
1.  [function <span class="apidocSignatureSpan">store.</span>get (key, optionalDefaultValue)](#apidoc.element.store.get)
1.  [function <span class="apidocSignatureSpan">store.</span>hasNamespace (namespace)](#apidoc.element.store.hasNamespace)
1.  [function <span class="apidocSignatureSpan">store.</span>namespace (namespace)](#apidoc.element.store.namespace)
1.  [function <span class="apidocSignatureSpan">store.</span>remove (key)](#apidoc.element.store.remove)
1.  [function <span class="apidocSignatureSpan">store.</span>set (key, value)](#apidoc.element.store.set)
1.  object <span class="apidocSignatureSpan">store.</span>all
1.  object <span class="apidocSignatureSpan">store.</span>cookieStorage
1.  object <span class="apidocSignatureSpan">store.</span>localStorage
1.  object <span class="apidocSignatureSpan">store.</span>memoryStorage
1.  object <span class="apidocSignatureSpan">store.</span>observe
1.  object <span class="apidocSignatureSpan">store.</span>oldFF_globalStorage
1.  object <span class="apidocSignatureSpan">store.</span>oldIE_userDataStorage
1.  object <span class="apidocSignatureSpan">store.</span>operations
1.  object <span class="apidocSignatureSpan">store.</span>sessionStorage
1.  object <span class="apidocSignatureSpan">store.</span>store_engine
1.  object <span class="apidocSignatureSpan">store.</span>util
1.  object <span class="apidocSignatureSpan">store.</span>v1_backcompat
1.  string <span class="apidocSignatureSpan">store.</span>storage
1.  string <span class="apidocSignatureSpan">store.</span>version

#### [module store.all](#apidoc.module.store.all)
1.  [function <span class="apidocSignatureSpan">store.all.</span>defaults ()](#apidoc.element.store.all.defaults)
1.  [function <span class="apidocSignatureSpan">store.all.</span>dump ()](#apidoc.element.store.all.dump)
1.  [function <span class="apidocSignatureSpan">store.all.</span>events ()](#apidoc.element.store.all.events)
1.  [function <span class="apidocSignatureSpan">store.all.</span>expire ()](#apidoc.element.store.all.expire)
1.  [function <span class="apidocSignatureSpan">store.all.</span>json2 ()](#apidoc.element.store.all.json2)
1.  [function <span class="apidocSignatureSpan">store.all.</span>update ()](#apidoc.element.store.all.update)
1.  object <span class="apidocSignatureSpan">store.all.</span>observe
1.  object <span class="apidocSignatureSpan">store.all.</span>operations
1.  object <span class="apidocSignatureSpan">store.all.</span>v1-backcompat

#### [module store.cookieStorage](#apidoc.module.store.cookieStorage)
1.  [function <span class="apidocSignatureSpan">store.cookieStorage.</span>clearAll ()](#apidoc.element.store.cookieStorage.clearAll)
1.  [function <span class="apidocSignatureSpan">store.cookieStorage.</span>each (callback)](#apidoc.element.store.cookieStorage.each)
1.  [function <span class="apidocSignatureSpan">store.cookieStorage.</span>read (key)](#apidoc.element.store.cookieStorage.read)
1.  [function <span class="apidocSignatureSpan">store.cookieStorage.</span>remove (key)](#apidoc.element.store.cookieStorage.remove)
1.  [function <span class="apidocSignatureSpan">store.cookieStorage.</span>write (key, data)](#apidoc.element.store.cookieStorage.write)
1.  string <span class="apidocSignatureSpan">store.cookieStorage.</span>name

#### [module store.localStorage](#apidoc.module.store.localStorage)
1.  [function <span class="apidocSignatureSpan">store.localStorage.</span>clearAll ()](#apidoc.element.store.localStorage.clearAll)
1.  [function <span class="apidocSignatureSpan">store.localStorage.</span>each (fn)](#apidoc.element.store.localStorage.each)
1.  [function <span class="apidocSignatureSpan">store.localStorage.</span>read (key)](#apidoc.element.store.localStorage.read)
1.  [function <span class="apidocSignatureSpan">store.localStorage.</span>remove (key)](#apidoc.element.store.localStorage.remove)
1.  [function <span class="apidocSignatureSpan">store.localStorage.</span>write (key, data)](#apidoc.element.store.localStorage.write)
1.  string <span class="apidocSignatureSpan">store.localStorage.</span>name

#### [module store.memoryStorage](#apidoc.module.store.memoryStorage)
1.  [function <span class="apidocSignatureSpan">store.memoryStorage.</span>clearAll (key)](#apidoc.element.store.memoryStorage.clearAll)
1.  [function <span class="apidocSignatureSpan">store.memoryStorage.</span>each (callback)](#apidoc.element.store.memoryStorage.each)
1.  [function <span class="apidocSignatureSpan">store.memoryStorage.</span>read (key)](#apidoc.element.store.memoryStorage.read)
1.  [function <span class="apidocSignatureSpan">store.memoryStorage.</span>remove (key)](#apidoc.element.store.memoryStorage.remove)
1.  [function <span class="apidocSignatureSpan">store.memoryStorage.</span>write (key, data)](#apidoc.element.store.memoryStorage.write)
1.  string <span class="apidocSignatureSpan">store.memoryStorage.</span>name

#### [module store.observe](#apidoc.module.store.observe)
1.  [function <span class="apidocSignatureSpan">store.observe.</span>0 ()](#apidoc.element.store.observe.0)
1.  [function <span class="apidocSignatureSpan">store.observe.</span>1 ()](#apidoc.element.store.observe.1)

#### [module store.oldFF_globalStorage](#apidoc.module.store.oldFF_globalStorage)
1.  [function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>clearAll ()](#apidoc.element.store.oldFF_globalStorage.clearAll)
1.  [function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>each (fn)](#apidoc.element.store.oldFF_globalStorage.each)
1.  [function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>read (key)](#apidoc.element.store.oldFF_globalStorage.read)
1.  [function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>remove (key)](#apidoc.element.store.oldFF_globalStorage.remove)
1.  [function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>write (key, data)](#apidoc.element.store.oldFF_globalStorage.write)
1.  string <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>name

#### [module store.oldIE_userDataStorage](#apidoc.module.store.oldIE_userDataStorage)
1.  [function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>clearAll ()](#apidoc.element.store.oldIE_userDataStorage.clearAll)
1.  [function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>each (callback)](#apidoc.element.store.oldIE_userDataStorage.each)
1.  [function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>read (unfixedKey)](#apidoc.element.store.oldIE_userDataStorage.read)
1.  [function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>remove (unfixedKey)](#apidoc.element.store.oldIE_userDataStorage.remove)
1.  [function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>write (unfixedKey, data)](#apidoc.element.store.oldIE_userDataStorage.write)
1.  string <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>name

#### [module store.operations](#apidoc.module.store.operations)
1.  [function <span class="apidocSignatureSpan">store.operations.</span>0 ()](#apidoc.element.store.operations.0)
1.  [function <span class="apidocSignatureSpan">store.operations.</span>1 ()](#apidoc.element.store.operations.1)

#### [module store.sessionStorage](#apidoc.module.store.sessionStorage)
1.  [function <span class="apidocSignatureSpan">store.sessionStorage.</span>clearAll ()](#apidoc.element.store.sessionStorage.clearAll)
1.  [function <span class="apidocSignatureSpan">store.sessionStorage.</span>each (fn)](#apidoc.element.store.sessionStorage.each)
1.  [function <span class="apidocSignatureSpan">store.sessionStorage.</span>read (key)](#apidoc.element.store.sessionStorage.read)
1.  [function <span class="apidocSignatureSpan">store.sessionStorage.</span>remove (key)](#apidoc.element.store.sessionStorage.remove)
1.  [function <span class="apidocSignatureSpan">store.sessionStorage.</span>write (key, data)](#apidoc.element.store.sessionStorage.write)
1.  string <span class="apidocSignatureSpan">store.sessionStorage.</span>name

#### [module store.store_engine](#apidoc.module.store.store_engine)
1.  [function <span class="apidocSignatureSpan">store.store_engine.</span>createStore (storages, plugins)](#apidoc.element.store.store_engine.createStore)

#### [module store.util](#apidoc.module.store.util)
1.  [function <span class="apidocSignatureSpan">store.util.</span>assign ()](#apidoc.element.store.util.assign)
1.  [function <span class="apidocSignatureSpan">store.util.</span>bind (obj, fn)](#apidoc.element.store.util.bind)
1.  [function <span class="apidocSignatureSpan">store.util.</span>create (obj, assignProps1, assignProps2, etc)](#apidoc.element.store.util.create)
1.  [function <span class="apidocSignatureSpan">store.util.</span>each (obj, fn)](#apidoc.element.store.util.each)
1.  [function <span class="apidocSignatureSpan">store.util.</span>isFunction (val)](#apidoc.element.store.util.isFunction)
1.  [function <span class="apidocSignatureSpan">store.util.</span>isList (val)](#apidoc.element.store.util.isList)
1.  [function <span class="apidocSignatureSpan">store.util.</span>isObject (val)](#apidoc.element.store.util.isObject)
1.  [function <span class="apidocSignatureSpan">store.util.</span>map (obj, fn)](#apidoc.element.store.util.map)
1.  [function <span class="apidocSignatureSpan">store.util.</span>pluck (obj, fn)](#apidoc.element.store.util.pluck)
1.  [function <span class="apidocSignatureSpan">store.util.</span>slice (arr, index)](#apidoc.element.store.util.slice)
1.  [function <span class="apidocSignatureSpan">store.util.</span>trim (str)](#apidoc.element.store.util.trim)
1.  object <span class="apidocSignatureSpan">store.util.</span>Global

#### [module store.v1_backcompat](#apidoc.module.store.v1_backcompat)
1.  [function <span class="apidocSignatureSpan">store.v1_backcompat.</span>0 ()](#apidoc.element.store.v1_backcompat.0)
1.  [function <span class="apidocSignatureSpan">store.v1_backcompat.</span>1 ()](#apidoc.element.store.v1_backcompat.1)
1.  [function <span class="apidocSignatureSpan">store.v1_backcompat.</span>2 ()](#apidoc.element.store.v1_backcompat.2)



# <a name="apidoc.module.store"></a>[module store](#apidoc.module.store)

#### <a name="apidoc.element.store.addPlugin"></a>[function <span class="apidocSignatureSpan">store.</span>addPlugin (plugin)](#apidoc.element.store.addPlugin)
- description and source-code
```javascript
addPlugin = function (plugin) {
		var self = this

		// If the plugin is an array, then add all plugins in the array.
		// This allows for a plugin to depend on other plugins.
		if (isList(plugin)) {
			each(plugin, function(plugin) {
				self.addPlugin(plugin)
			})
			return
		}

		// Keep track of all plugins we've seen so far, so that we
		// don't add any of them twice.
		var seenPlugin = pluck(this._seenPlugins, function(seenPlugin) { return (plugin === seenPlugin) })
		if (seenPlugin) {
			return
		}
		this._seenPlugins.push(plugin)

		// Check that the plugin is properly formed
		if (!isFunction(plugin)) {
			throw new Error('Plugins must be function values that return objects')
		}

		var pluginProperties = plugin.call(this)
		if (!isObject(pluginProperties)) {
			throw new Error('Plugins must return an object of function properties')
		}

		// Add the plugin function properties to this store instance.
		each(pluginProperties, function(pluginFnProp, propName) {
			if (!isFunction(pluginFnProp)) {
				throw new Error('Bad plugin property: '+propName+' from plugin '+plugin.name+'. Plugins should only return functions.')
			}
			self._assignPluginFnProp(pluginFnProp, propName)
		})
	}
```
- example usage
```shell
...
### Using Plugins

With npm:

'''js
// Example plugin usage:
var expirePlugin = require('store/plugins/expire')
store.addPlugin(expirePlugin)
'''

If you're using script tags, you can either use [store.everything.min.js](dist/store.everything.min.js) (which
has all plugins built-in), or clone this repo to add or modify a build and run 'make build'.

### Write your own plugin
...
```

#### <a name="apidoc.element.store.addStorage"></a>[function <span class="apidocSignatureSpan">store.</span>addStorage (storage)](#apidoc.element.store.addStorage)
- description and source-code
```javascript
addStorage = function (storage) {
		if (this.enabled) { return }
		if (this._testStorage(storage)) {
			this._storage.resolved = storage
			this.enabled = true
			this.storage = storage.name
		}
	}
```
- example usage
```shell
...
	name: 'myStorage',
	read: function(key) { ... },
	write: function(key, value) { ... },
	each: function(fn) { ... },
	remove: function(key) { ... },
	clearAll: function() { ... }
}
store.addStorage(storage)
'''
...
```

#### <a name="apidoc.element.store.clearAll"></a>[function <span class="apidocSignatureSpan">store.</span>clearAll ()](#apidoc.element.store.clearAll)
- description and source-code
```javascript
clearAll = function () {
		this._storage().clearAll()
	}
```
- example usage
```shell
...
// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''
...
```

#### <a name="apidoc.element.store.createStore"></a>[function <span class="apidocSignatureSpan">store.</span>createStore (storages, plugins)](#apidoc.element.store.createStore)
- description and source-code
```javascript
createStore = function (storages, plugins) {
		return createStore(storages, plugins)
	}
```
- example usage
```shell
...
	require('store/storages/localStorage'),
	require('store/storages/cookieStorage')
]
var plugins = [
	require('store/plugins/defaults'),
	require('store/plugins/expire')
]
var store = engine.createStore(storages, plugins)
store.set('foo', 'bar', new Date().getTime() + 3000) // Using expire plugin to expire in 3 seconds
'''




Storages
...
```

#### <a name="apidoc.element.store.each"></a>[function <span class="apidocSignatureSpan">store.</span>each (callback)](#apidoc.element.store.each)
- description and source-code
```javascript
each = function (callback) {
		var self = this
		this._storage().each(function(val, namespacedKey) {
			callback(self._deserialize(val), namespacedKey.replace(self._namespaceRegexp, ''))
		})
	}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.get"></a>[function <span class="apidocSignatureSpan">store.</span>get (key, optionalDefaultValue)](#apidoc.element.store.get)
- description and source-code
```javascript
get = function (key, optionalDefaultValue) {
		var data = this._storage().read(this._namespacePrefix + key)
		return this._deserialize(data, optionalDefaultValue)
	}
```
- example usage
```shell
...
<script>
	init()
	function init() {
		if (!store.enabled) {
			alert('Local storage is not supported by your browser. Please disable "Private Mode", or upgrade to a modern browser.')
			return
		}
		var user = store.get('user')
		// ... and so on ...
	}
</script>
'''

LocalStorage may sometimes appear to be available but throw an error when used. An example is Safari's private browsing mode. Other
 browsers allow the user to temporarily disable localStorage. Store.js detects these conditions and sets the 'store.enabled' flag
 appropriately.
...
```

#### <a name="apidoc.element.store.hasNamespace"></a>[function <span class="apidocSignatureSpan">store.</span>hasNamespace (namespace)](#apidoc.element.store.hasNamespace)
- description and source-code
```javascript
hasNamespace = function (namespace) {
		return (this._namespacePrefix == '__storejs_'+namespace+'_')
	}
```
- example usage
```shell
...
	return {
		set: expire_set,
		get: expire_get,
		remove: expire_remove
	}
	
	function expire_set(super_fn, key, val, expiration) {
		if (!this.hasNamespace(namespace)) {
			expirations.set(key, expiration)
		}
		return super_fn()
	}
	
	function expire_get(super_fn, key) {
		if (!this.hasNamespace(namespace)) {
...
```

#### <a name="apidoc.element.store.namespace"></a>[function <span class="apidocSignatureSpan">store.</span>namespace (namespace)](#apidoc.element.store.namespace)
- description and source-code
```javascript
namespace = function (namespace) {
		if (!this._legalNamespace.test(namespace)) {
			throw new Error('store.js namespaces can only have alhpanumerics + underscores and dashes')
		}
		// create a prefix that is very unlikely to collide with un-namespaced keys
		var namespacePrefix = '__storejs_'+namespace+'_'
		return create(this, {
			_namespacePrefix: namespacePrefix,
			_namespaceRegexp: namespacePrefix ? new RegExp('^'+namespacePrefix) : null
		})
	}
```
- example usage
```shell
...
A store.js plugin is a function that returns an object that gets added to the store.
If any of the plugin functions overrides existing functions, the plugin function can still call
the original function using the first argument (super_fn).

'''js
// Example plugin that stores a version history of every value
var versionHistoryPlugin = function() {
	var historyStore = this.namespace('history')
	return {
		set: function(super_fn, key, value) {
			var history = historyStore.get(key) || []
			history.push(value)
			historyStore.set(key, history)
			return super_fn()
		},
...
```

#### <a name="apidoc.element.store.remove"></a>[function <span class="apidocSignatureSpan">store.</span>remove (key)](#apidoc.element.store.remove)
- description and source-code
```javascript
remove = function (key) {
		this._storage().remove(this._namespacePrefix + key)
	}
```
- example usage
```shell
...
// Store current user
store.set('user', { name:'Marcus' })

// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
...
```

#### <a name="apidoc.element.store.set"></a>[function <span class="apidocSignatureSpan">store.</span>set (key, value)](#apidoc.element.store.set)
- description and source-code
```javascript
set = function (key, value) {
		if (value === undefined) {
			return this.remove(key)
		}
		this._storage().write(this._namespacePrefix + key, this._serialize(value))
		return value
	}
```
- example usage
```shell
...
In node.js
----------
store.js works as expected in node.js, assuming that global.localStorage has been set:

'''
global.localStorage = require('localStorage')
var store = require('./store')
store.set('foo', 1)
console.log(store.get('foo'))
'''


Supported browsers
------------------
- Tested in iOS 4+
...
```



# <a name="apidoc.module.store.all"></a>[module store.all](#apidoc.module.store.all)

#### <a name="apidoc.element.store.all.defaults"></a>[function <span class="apidocSignatureSpan">store.all.</span>defaults ()](#apidoc.element.store.all.defaults)
- description and source-code
```javascript
function defaultsPlugin() {
	var defaultValues = {}
	
	return {
		defaults: defaults,
		get: get
	}
	
	function defaults(_, values) {
		defaultValues = values
	}
	
	function get(super_fn, key) {
		var val = super_fn()
		return (val !== undefined ? val : defaultValues[key])
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.all.dump"></a>[function <span class="apidocSignatureSpan">store.all.</span>dump ()](#apidoc.element.store.all.dump)
- description and source-code
```javascript
function dumpPlugin() {
	return {
		dump: dump
	}
	
	function dump(_) {
		var res = {}
		this.each(function(val, key) {
			res[key] = val
		})
		return res
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.all.events"></a>[function <span class="apidocSignatureSpan">store.all.</span>events ()](#apidoc.element.store.all.events)
- description and source-code
```javascript
function eventsPlugin() {
	var pubsub = _newPubSub()

	return {
		watch: watch,
		unwatch: unwatch,
		once: once,

		set: set,
		remove: remove,
		clearAll: clearAll
	}

	// new pubsub functions
	function watch(_, key, listener) {
		return pubsub.on(key, bind(this, listener))
	}
	function unwatch(_, subId) {
		pubsub.off(subId)
	}
	function once(_, key, listener) {
		pubsub.once(key, bind(this, listener))
	}

	// overwrite function to fire when appropriate
	function set(super_fn, key, val) {
		var oldVal = this.get(key)
		super_fn()
		pubsub.fire(key, val, oldVal)
	}
	function remove(super_fn, key) {
		var oldVal = this.get(key)
		super_fn()
		pubsub.fire(key, undefined, oldVal)
	}
	function clearAll(super_fn) {
		var oldVals = {}
		this.each(function(val, key) {
			oldVals[key] = val
		})
		super_fn()
		each(oldVals, function(oldVal, key) {
			pubsub.fire(key, undefined, oldVal)
		})
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.all.expire"></a>[function <span class="apidocSignatureSpan">store.all.</span>expire ()](#apidoc.element.store.all.expire)
- description and source-code
```javascript
function expirePlugin() {
	var expirations = this.namespace(namespace)
	
	return {
		set: expire_set,
		get: expire_get,
		remove: expire_remove
	}
	
	function expire_set(super_fn, key, val, expiration) {
		if (!this.hasNamespace(namespace)) {
			expirations.set(key, expiration)
		}
		return super_fn()
	}
	
	function expire_get(super_fn, key) {
		if (!this.hasNamespace(namespace)) {
			var expiration = expirations.get(key, Number.MAX_VALUE)
			if (expiration <= new Date().getTime()) {
				this.remove(key)
			}
		}
		return super_fn()
	}
	
	function expire_remove(super_fn, key) {
		if (!this.hasNamespace(namespace)) {
			expirations.remove(key)
		}
		return super_fn()
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.all.json2"></a>[function <span class="apidocSignatureSpan">store.all.</span>json2 ()](#apidoc.element.store.all.json2)
- description and source-code
```javascript
function json2Plugin() {
	require('./lib/json2')
	return {}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.all.update"></a>[function <span class="apidocSignatureSpan">store.all.</span>update ()](#apidoc.element.store.all.update)
- description and source-code
```javascript
function updatePlugin() {
	return {
		update: update
	}
	
	function update(_, key, optDefaultVal, updateFn) {
		if (arguments.length == 3) {
			updateFn = optDefaultVal
			optDefaultVal = undefined
		}
		var val = this.get(key, optDefaultVal)
		var retVal = updateFn(val)
		this.set(key, retVal != undefined ? retVal : val)
	}
}
```
- example usage
```shell
...
	function unshift(_, key, val1, val2, val3, etc) {
		return _arrayOp.call(this, 'unshift', arguments)
	}

	// obj
	function assign_(_, key, props1, props2, props3, etc) {
		var varArgs = slice(arguments, 2)
		return this.update(key, {}, function(val) {
			if (typeof val != 'object') {
				throw new Error('store.assign called for non-object value with key "'+key+'"')
			}
			varArgs.unshift(val)
			return assign.apply(Object, varArgs)
		})
	}
...
```



# <a name="apidoc.module.store.cookieStorage"></a>[module store.cookieStorage](#apidoc.module.store.cookieStorage)

#### <a name="apidoc.element.store.cookieStorage.clearAll"></a>[function <span class="apidocSignatureSpan">store.cookieStorage.</span>clearAll ()](#apidoc.element.store.cookieStorage.clearAll)
- description and source-code
```javascript
function clearAll() {
	each(function(_, key) {
		remove(key)
	})
}
```
- example usage
```shell
...
// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''
...
```

#### <a name="apidoc.element.store.cookieStorage.each"></a>[function <span class="apidocSignatureSpan">store.cookieStorage.</span>each (callback)](#apidoc.element.store.cookieStorage.each)
- description and source-code
```javascript
function each(callback) {
	var cookies = doc.cookie.split(/; ?/g)
	for (var i = cookies.length - 1; i >= 0; i--) {
		if (!trim(cookies[i])) {
			continue
		}
		var kvp = cookies[i].split('=')
		var key = unescape(kvp[0])
		var val = unescape(kvp[1])
		callback(val, key)
	}
}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.cookieStorage.read"></a>[function <span class="apidocSignatureSpan">store.cookieStorage.</span>read (key)](#apidoc.element.store.cookieStorage.read)
- description and source-code
```javascript
function read(key) {
	if (!key || !_has(key)) { return null }
	var regexpStr = "(?:^|.*;\\s*)" +
		escape(key).replace(/[\-\.\+\*]/g, "\\$&") +
		"\\s*\\=\\s*((?:[^;](?!;))*[^;]?).*"
	return unescape(doc.cookie.replace(new RegExp(regexpStr), "$1"))
}
```
- example usage
```shell
...
			self._assignPluginFnProp(pluginFnProp, propName)
		})
	},

	// get returns the value of the given key. If that value
	// is undefined, it returns optionalDefaultValue instead.
	get: function(key, optionalDefaultValue) {
		var data = this._storage().read(this._namespacePrefix + key)
		return this._deserialize(data, optionalDefaultValue)
	},

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
...
```

#### <a name="apidoc.element.store.cookieStorage.remove"></a>[function <span class="apidocSignatureSpan">store.cookieStorage.</span>remove (key)](#apidoc.element.store.cookieStorage.remove)
- description and source-code
```javascript
function remove(key) {
	if (!key || !_has(key)) {
		return
	}
	doc.cookie = escape(key) + "=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/"
}
```
- example usage
```shell
...
// Store current user
store.set('user', { name:'Marcus' })

// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
...
```

#### <a name="apidoc.element.store.cookieStorage.write"></a>[function <span class="apidocSignatureSpan">store.cookieStorage.</span>write (key, data)](#apidoc.element.store.cookieStorage.write)
- description and source-code
```javascript
function write(key, data) {
	if(!key) { return }
	doc.cookie = escape(key) + "=" + escape(data) + "; expires=Tue, 19 Jan 2038 03:14:07 GMT; path=/"
}
```
- example usage
```shell
...

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
			return this.remove(key)
		}
		this._storage().write(this._namespacePrefix + key, this._serialize(value))
		return value
	},

	// remove deletes the key and value stored at the given key.
	remove: function(key) {
		this._storage().remove(this._namespacePrefix + key)
	},
...
```



# <a name="apidoc.module.store.localStorage"></a>[module store.localStorage](#apidoc.module.store.localStorage)

#### <a name="apidoc.element.store.localStorage.clearAll"></a>[function <span class="apidocSignatureSpan">store.localStorage.</span>clearAll ()](#apidoc.element.store.localStorage.clearAll)
- description and source-code
```javascript
function clearAll() {
	return localStorage().clear()
}
```
- example usage
```shell
...
// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''
...
```

#### <a name="apidoc.element.store.localStorage.each"></a>[function <span class="apidocSignatureSpan">store.localStorage.</span>each (fn)](#apidoc.element.store.localStorage.each)
- description and source-code
```javascript
function each(fn) {
	for (var i = localStorage().length - 1; i >= 0; i--) {
		var key = localStorage().key(i)
		fn(read(key), key)
	}
}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.localStorage.read"></a>[function <span class="apidocSignatureSpan">store.localStorage.</span>read (key)](#apidoc.element.store.localStorage.read)
- description and source-code
```javascript
function read(key) {
	return localStorage().getItem(key)
}
```
- example usage
```shell
...
			self._assignPluginFnProp(pluginFnProp, propName)
		})
	},

	// get returns the value of the given key. If that value
	// is undefined, it returns optionalDefaultValue instead.
	get: function(key, optionalDefaultValue) {
		var data = this._storage().read(this._namespacePrefix + key)
		return this._deserialize(data, optionalDefaultValue)
	},

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
...
```

#### <a name="apidoc.element.store.localStorage.remove"></a>[function <span class="apidocSignatureSpan">store.localStorage.</span>remove (key)](#apidoc.element.store.localStorage.remove)
- description and source-code
```javascript
function remove(key) {
	return localStorage().removeItem(key)
}
```
- example usage
```shell
...
// Store current user
store.set('user', { name:'Marcus' })

// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
...
```

#### <a name="apidoc.element.store.localStorage.write"></a>[function <span class="apidocSignatureSpan">store.localStorage.</span>write (key, data)](#apidoc.element.store.localStorage.write)
- description and source-code
```javascript
function write(key, data) {
	return localStorage().setItem(key, data)
}
```
- example usage
```shell
...

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
			return this.remove(key)
		}
		this._storage().write(this._namespacePrefix + key, this._serialize(value))
		return value
	},

	// remove deletes the key and value stored at the given key.
	remove: function(key) {
		this._storage().remove(this._namespacePrefix + key)
	},
...
```



# <a name="apidoc.module.store.memoryStorage"></a>[module store.memoryStorage](#apidoc.module.store.memoryStorage)

#### <a name="apidoc.element.store.memoryStorage.clearAll"></a>[function <span class="apidocSignatureSpan">store.memoryStorage.</span>clearAll (key)](#apidoc.element.store.memoryStorage.clearAll)
- description and source-code
```javascript
function clearAll(key) {
	memoryStorage = {}
}
```
- example usage
```shell
...
// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''
...
```

#### <a name="apidoc.element.store.memoryStorage.each"></a>[function <span class="apidocSignatureSpan">store.memoryStorage.</span>each (callback)](#apidoc.element.store.memoryStorage.each)
- description and source-code
```javascript
function each(callback) {
	for (var key in memoryStorage) {
		if (memoryStorage.hasOwnProperty(key)) {
			callback(memoryStorage[key], key)
		}
	}
}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.memoryStorage.read"></a>[function <span class="apidocSignatureSpan">store.memoryStorage.</span>read (key)](#apidoc.element.store.memoryStorage.read)
- description and source-code
```javascript
function read(key) {
	return memoryStorage[key]
}
```
- example usage
```shell
...
			self._assignPluginFnProp(pluginFnProp, propName)
		})
	},

	// get returns the value of the given key. If that value
	// is undefined, it returns optionalDefaultValue instead.
	get: function(key, optionalDefaultValue) {
		var data = this._storage().read(this._namespacePrefix + key)
		return this._deserialize(data, optionalDefaultValue)
	},

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
...
```

#### <a name="apidoc.element.store.memoryStorage.remove"></a>[function <span class="apidocSignatureSpan">store.memoryStorage.</span>remove (key)](#apidoc.element.store.memoryStorage.remove)
- description and source-code
```javascript
function remove(key) {
	delete memoryStorage[key]
}
```
- example usage
```shell
...
// Store current user
store.set('user', { name:'Marcus' })

// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
...
```

#### <a name="apidoc.element.store.memoryStorage.write"></a>[function <span class="apidocSignatureSpan">store.memoryStorage.</span>write (key, data)](#apidoc.element.store.memoryStorage.write)
- description and source-code
```javascript
function write(key, data) {
	memoryStorage[key] = data
}
```
- example usage
```shell
...

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
			return this.remove(key)
		}
		this._storage().write(this._namespacePrefix + key, this._serialize(value))
		return value
	},

	// remove deletes the key and value stored at the given key.
	remove: function(key) {
		this._storage().remove(this._namespacePrefix + key)
	},
...
```



# <a name="apidoc.module.store.observe"></a>[module store.observe](#apidoc.module.store.observe)

#### <a name="apidoc.element.store.observe.0"></a>[function <span class="apidocSignatureSpan">store.observe.</span>0 ()](#apidoc.element.store.observe.0)
- description and source-code
```javascript
function eventsPlugin() {
	var pubsub = _newPubSub()

	return {
		watch: watch,
		unwatch: unwatch,
		once: once,

		set: set,
		remove: remove,
		clearAll: clearAll
	}

	// new pubsub functions
	function watch(_, key, listener) {
		return pubsub.on(key, bind(this, listener))
	}
	function unwatch(_, subId) {
		pubsub.off(subId)
	}
	function once(_, key, listener) {
		pubsub.once(key, bind(this, listener))
	}

	// overwrite function to fire when appropriate
	function set(super_fn, key, val) {
		var oldVal = this.get(key)
		super_fn()
		pubsub.fire(key, val, oldVal)
	}
	function remove(super_fn, key) {
		var oldVal = this.get(key)
		super_fn()
		pubsub.fire(key, undefined, oldVal)
	}
	function clearAll(super_fn) {
		var oldVals = {}
		this.each(function(val, key) {
			oldVals[key] = val
		})
		super_fn()
		each(oldVals, function(oldVal, key) {
			pubsub.fire(key, undefined, oldVal)
		})
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.observe.1"></a>[function <span class="apidocSignatureSpan">store.observe.</span>1 ()](#apidoc.element.store.observe.1)
- description and source-code
```javascript
function observePlugin() {
	return {
		observe: observe,
		unobserve: unobserve
	}

	function observe(_, key, callback) {
		var subId = this.watch(key, callback)
		callback(this.get(key))
		return subId
	}
	function unobserve(_, subId) {
		this.unwatch(subId)
	}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.store.oldFF_globalStorage"></a>[module store.oldFF_globalStorage](#apidoc.module.store.oldFF_globalStorage)

#### <a name="apidoc.element.store.oldFF_globalStorage.clearAll"></a>[function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>clearAll ()](#apidoc.element.store.oldFF_globalStorage.clearAll)
- description and source-code
```javascript
function clearAll() {
	each(function(key, _) {
		delete globalStorage[key]
	})
}
```
- example usage
```shell
...
// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''
...
```

#### <a name="apidoc.element.store.oldFF_globalStorage.each"></a>[function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>each (fn)](#apidoc.element.store.oldFF_globalStorage.each)
- description and source-code
```javascript
function each(fn) {
	for (var i = globalStorage.length - 1; i >= 0; i--) {
		var key = globalStorage.key(i)
		fn(globalStorage[key], key)
	}
}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.oldFF_globalStorage.read"></a>[function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>read (key)](#apidoc.element.store.oldFF_globalStorage.read)
- description and source-code
```javascript
function read(key) {
	return globalStorage[key]
}
```
- example usage
```shell
...
			self._assignPluginFnProp(pluginFnProp, propName)
		})
	},

	// get returns the value of the given key. If that value
	// is undefined, it returns optionalDefaultValue instead.
	get: function(key, optionalDefaultValue) {
		var data = this._storage().read(this._namespacePrefix + key)
		return this._deserialize(data, optionalDefaultValue)
	},

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
...
```

#### <a name="apidoc.element.store.oldFF_globalStorage.remove"></a>[function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>remove (key)](#apidoc.element.store.oldFF_globalStorage.remove)
- description and source-code
```javascript
function remove(key) {
	return globalStorage.removeItem(key)
}
```
- example usage
```shell
...
// Store current user
store.set('user', { name:'Marcus' })

// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
...
```

#### <a name="apidoc.element.store.oldFF_globalStorage.write"></a>[function <span class="apidocSignatureSpan">store.oldFF_globalStorage.</span>write (key, data)](#apidoc.element.store.oldFF_globalStorage.write)
- description and source-code
```javascript
function write(key, data) {
	globalStorage[key] = data
}
```
- example usage
```shell
...

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
			return this.remove(key)
		}
		this._storage().write(this._namespacePrefix + key, this._serialize(value))
		return value
	},

	// remove deletes the key and value stored at the given key.
	remove: function(key) {
		this._storage().remove(this._namespacePrefix + key)
	},
...
```



# <a name="apidoc.module.store.oldIE_userDataStorage"></a>[module store.oldIE_userDataStorage](#apidoc.module.store.oldIE_userDataStorage)

#### <a name="apidoc.element.store.oldIE_userDataStorage.clearAll"></a>[function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>clearAll ()](#apidoc.element.store.oldIE_userDataStorage.clearAll)
- description and source-code
```javascript
function clearAll() {
	_withStorageEl(function(storageEl) {
		var attributes = storageEl.XMLDocument.documentElement.attributes
		storageEl.load(storageName)
		for (var i=attributes.length-1; i>=0; i--) {
			storageEl.removeAttribute(attributes[i].name)
		}
		storageEl.save(storageName)
	})
}
```
- example usage
```shell
...
// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''
...
```

#### <a name="apidoc.element.store.oldIE_userDataStorage.each"></a>[function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>each (callback)](#apidoc.element.store.oldIE_userDataStorage.each)
- description and source-code
```javascript
function each(callback) {
	_withStorageEl(function(storageEl) {
		var attributes = storageEl.XMLDocument.documentElement.attributes
		for (var i=attributes.length-1; i>=0; i--) {
			var attr = attributes[i]
			callback(storageEl.getAttribute(attr.name), attr.name)
		}
	})
}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.oldIE_userDataStorage.read"></a>[function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>read (unfixedKey)](#apidoc.element.store.oldIE_userDataStorage.read)
- description and source-code
```javascript
function read(unfixedKey) {
	if (disable) { return }
	var fixedKey = fixKey(unfixedKey)
	var res = null
	_withStorageEl(function(storageEl) {
		res = storageEl.getAttribute(fixedKey)
	})
	return res
}
```
- example usage
```shell
...
			self._assignPluginFnProp(pluginFnProp, propName)
		})
	},

	// get returns the value of the given key. If that value
	// is undefined, it returns optionalDefaultValue instead.
	get: function(key, optionalDefaultValue) {
		var data = this._storage().read(this._namespacePrefix + key)
		return this._deserialize(data, optionalDefaultValue)
	},

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
...
```

#### <a name="apidoc.element.store.oldIE_userDataStorage.remove"></a>[function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>remove (unfixedKey)](#apidoc.element.store.oldIE_userDataStorage.remove)
- description and source-code
```javascript
function remove(unfixedKey) {
	var fixedKey = fixKey(unfixedKey)
	_withStorageEl(function(storageEl) {
		storageEl.removeAttribute(fixedKey)
		storageEl.save(storageName)
	})
}
```
- example usage
```shell
...
// Store current user
store.set('user', { name:'Marcus' })

// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
...
```

#### <a name="apidoc.element.store.oldIE_userDataStorage.write"></a>[function <span class="apidocSignatureSpan">store.oldIE_userDataStorage.</span>write (unfixedKey, data)](#apidoc.element.store.oldIE_userDataStorage.write)
- description and source-code
```javascript
function write(unfixedKey, data) {
	if (disable) { return }
	var fixedKey = fixKey(unfixedKey)
	_withStorageEl(function(storageEl) {
		storageEl.setAttribute(fixedKey, data)
		storageEl.save(storageName)
	})
}
```
- example usage
```shell
...

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
			return this.remove(key)
		}
		this._storage().write(this._namespacePrefix + key, this._serialize(value))
		return value
	},

	// remove deletes the key and value stored at the given key.
	remove: function(key) {
		this._storage().remove(this._namespacePrefix + key)
	},
...
```



# <a name="apidoc.module.store.operations"></a>[module store.operations](#apidoc.module.store.operations)

#### <a name="apidoc.element.store.operations.0"></a>[function <span class="apidocSignatureSpan">store.operations.</span>0 ()](#apidoc.element.store.operations.0)
- description and source-code
```javascript
function updatePlugin() {
	return {
		update: update
	}
	
	function update(_, key, optDefaultVal, updateFn) {
		if (arguments.length == 3) {
			updateFn = optDefaultVal
			optDefaultVal = undefined
		}
		var val = this.get(key, optDefaultVal)
		var retVal = updateFn(val)
		this.set(key, retVal != undefined ? retVal : val)
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.operations.1"></a>[function <span class="apidocSignatureSpan">store.operations.</span>1 ()](#apidoc.element.store.operations.1)
- description and source-code
```javascript
function operationsPlugin() {
	return {
		// array
		push: push,
		pop: pop,
		shift: shift,
		unshift: unshift,

		// obj
		assign: assign_,
	}

	// array
	function push(_, key, val1, val2, val3, etc) {
		return _arrayOp.call(this, 'push', arguments)
	}
	function pop(_, key) {
		return _arrayOp.call(this, 'pop', arguments)
	}
	function shift(_, key) {
		return _arrayOp.call(this, 'shift', arguments)
	}
	function unshift(_, key, val1, val2, val3, etc) {
		return _arrayOp.call(this, 'unshift', arguments)
	}

	// obj
	function assign_(_, key, props1, props2, props3, etc) {
		var varArgs = slice(arguments, 2)
		return this.update(key, {}, function(val) {
			if (typeof val != 'object') {
				throw new Error('store.assign called for non-object value with key "'+key+'"')
			}
			varArgs.unshift(val)
			return assign.apply(Object, varArgs)
		})
	}

	// internal
	///////////
	function _arrayOp(arrayFn, opArgs) {
		var res
		var key = opArgs[1]
		var rest = slice(opArgs, 2)
		this.update(key, [], function(arrVal) {
			res = Array.prototype[arrayFn].apply(arrVal, rest)
		})
		return res
	}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.store.sessionStorage"></a>[module store.sessionStorage](#apidoc.module.store.sessionStorage)

#### <a name="apidoc.element.store.sessionStorage.clearAll"></a>[function <span class="apidocSignatureSpan">store.sessionStorage.</span>clearAll ()](#apidoc.element.store.sessionStorage.clearAll)
- description and source-code
```javascript
function clearAll() {
	return sessionStorage().clear()
}
```
- example usage
```shell
...
// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''
...
```

#### <a name="apidoc.element.store.sessionStorage.each"></a>[function <span class="apidocSignatureSpan">store.sessionStorage.</span>each (fn)](#apidoc.element.store.sessionStorage.each)
- description and source-code
```javascript
function each(fn) {
	for (var i = sessionStorage().length - 1; i >= 0; i--) {
		var key = sessionStorage().key(i)
		fn(read(key), key)
	}
}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.sessionStorage.read"></a>[function <span class="apidocSignatureSpan">store.sessionStorage.</span>read (key)](#apidoc.element.store.sessionStorage.read)
- description and source-code
```javascript
function read(key) {
	return sessionStorage().getItem(key)
}
```
- example usage
```shell
...
			self._assignPluginFnProp(pluginFnProp, propName)
		})
	},

	// get returns the value of the given key. If that value
	// is undefined, it returns optionalDefaultValue instead.
	get: function(key, optionalDefaultValue) {
		var data = this._storage().read(this._namespacePrefix + key)
		return this._deserialize(data, optionalDefaultValue)
	},

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
...
```

#### <a name="apidoc.element.store.sessionStorage.remove"></a>[function <span class="apidocSignatureSpan">store.sessionStorage.</span>remove (key)](#apidoc.element.store.sessionStorage.remove)
- description and source-code
```javascript
function remove(key) {
	return sessionStorage().removeItem(key)
}
```
- example usage
```shell
...
// Store current user
store.set('user', { name:'Marcus' })

// Get current user
store.get('user')

// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
...
```

#### <a name="apidoc.element.store.sessionStorage.write"></a>[function <span class="apidocSignatureSpan">store.sessionStorage.</span>write (key, data)](#apidoc.element.store.sessionStorage.write)
- description and source-code
```javascript
function write(key, data) {
	return sessionStorage().setItem(key, data)
}
```
- example usage
```shell
...

	// set will store the given value at key and returns value.
	// Calling set with value === undefined is equivalent to calling remove.
	set: function(key, value) {
		if (value === undefined) {
			return this.remove(key)
		}
		this._storage().write(this._namespacePrefix + key, this._serialize(value))
		return value
	},

	// remove deletes the key and value stored at the given key.
	remove: function(key) {
		this._storage().remove(this._namespacePrefix + key)
	},
...
```



# <a name="apidoc.module.store.store_engine"></a>[module store.store_engine](#apidoc.module.store.store_engine)

#### <a name="apidoc.element.store.store_engine.createStore"></a>[function <span class="apidocSignatureSpan">store.store_engine.</span>createStore (storages, plugins)](#apidoc.element.store.store_engine.createStore)
- description and source-code
```javascript
function createStore(storages, plugins) {
	var _privateStoreProps = {
		_seenPlugins: [],
		_namespacePrefix: '',
		_namespaceRegexp: null,
		_legalNamespace: /^[a-zA-Z0-9_\-]+$/, // alpha-numeric + underscore and dash

		_storage: function() {
			if (!this.enabled) {
				throw new Error("store.js: No supported storage has been added! "+
					"Add one (e.g store.addStorage(require('store/storages/cookieStorage')) "+
					"or use a build with more built-in storages (e.g "+
					"https://github.com/marcuswestin/store.js/tree/master/dist/store.legacy.min.js)")
			}
			return this._storage.resolved
		},

		_testStorage: function(storage) {
			try {
				var testStr = '__storejs__test__'
				storage.write(testStr, testStr)
				var ok = (storage.read(testStr) === testStr)
				storage.remove(testStr)
				return ok
			} catch(e) {
				return false
			}
		},

		_assignPluginFnProp: function(pluginFnProp, propName) {
			var oldFn = this[propName]
			this[propName] = function pluginFn() {
				var args = slice(arguments, 0)
				var self = this

				// super_fn calls the old function which was overwritten by
				// this mixin.
				function super_fn() {
					if (!oldFn) { return }
					each(arguments, function(arg, i) {
						args[i] = arg
					})
					return oldFn.apply(self, args)
				}

				// Give mixing function access to super_fn by prefixing all mixin function
				// arguments with super_fn.
				var newFnArgs = [super_fn].concat(args)

				return pluginFnProp.apply(self, newFnArgs)
			}
		},

		_serialize: function(obj) {
			return JSON.stringify(obj)
		},

		_deserialize: function(strVal, defaultVal) {
			if (!strVal) { return defaultVal }
			// It is possible that a raw string value has been previously stored
			// in a storage without using store.js, meaning it will be a raw
			// string value instead of a JSON serialized string. By defaulting
			// to the raw string value in case of a JSON parse error, we allow
			// for past stored values to be forwards-compatible with store.js
			var val = ''
			try { val = JSON.parse(strVal) }
			catch(e) { val = strVal }

			return (val !== undefined ? val : defaultVal)
		},
	}

	var store = create(_privateStoreProps, storeAPI)
	each(storages, function(storage) {
		store.addStorage(storage)
	})
	each(plugins, function(plugin) {
		store.addPlugin(plugin)
	})
	return store
}
```
- example usage
```shell
...
	require('store/storages/localStorage'),
	require('store/storages/cookieStorage')
]
var plugins = [
	require('store/plugins/defaults'),
	require('store/plugins/expire')
]
var store = engine.createStore(storages, plugins)
store.set('foo', 'bar', new Date().getTime() + 3000) // Using expire plugin to expire in 3 seconds
'''




Storages
...
```



# <a name="apidoc.module.store.util"></a>[module store.util](#apidoc.module.store.util)

#### <a name="apidoc.element.store.util.assign"></a>[function <span class="apidocSignatureSpan">store.util.</span>assign ()](#apidoc.element.store.util.assign)
- description and source-code
```javascript
function assign() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.bind"></a>[function <span class="apidocSignatureSpan">store.util.</span>bind (obj, fn)](#apidoc.element.store.util.bind)
- description and source-code
```javascript
function bind(obj, fn) {
	return function() {
		return fn.apply(obj, Array.prototype.slice.call(arguments, 0))
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.create"></a>[function <span class="apidocSignatureSpan">store.util.</span>create (obj, assignProps1, assignProps2, etc)](#apidoc.element.store.util.create)
- description and source-code
```javascript
function create(obj, assignProps1, assignProps2, etc) {
			var assignArgsList = slice(arguments, 1)
			return assign.apply(this, [Object.create(obj)].concat(assignArgsList))
		}
```
- example usage
```shell
...
	}
}

function make_create() {
	if (Object.create) {
		return function create(obj, assignProps1, assignProps2, etc) {
			var assignArgsList = slice(arguments, 1)
			return assign.apply(this, [Object.create(obj)].concat(assignArgsList))
		}
	} else {
		function F() {} // eslint-disable-line no-inner-declarations
		return function create(obj, assignProps1, assignProps2, etc) {
			var assignArgsList = slice(arguments, 1)
			F.prototype = obj
			return assign.apply(this, [new F()].concat(assignArgsList))
...
```

#### <a name="apidoc.element.store.util.each"></a>[function <span class="apidocSignatureSpan">store.util.</span>each (obj, fn)](#apidoc.element.store.util.each)
- description and source-code
```javascript
function each(obj, fn) {
	pluck(obj, function(key, val) {
		fn(key, val)
		return false
	})
}
```
- example usage
```shell
...
// Remove current user
store.remove('user')

// Clear all keys
store.clearAll()

// Loop over all stored values
store.each(function(value, key) {
	console.log(key, '==', value)
})
'''

### Installation

Using npm:
...
```

#### <a name="apidoc.element.store.util.isFunction"></a>[function <span class="apidocSignatureSpan">store.util.</span>isFunction (val)](#apidoc.element.store.util.isFunction)
- description and source-code
```javascript
function isFunction(val) {
	return val && {}.toString.call(val) === '[object Function]'
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.isList"></a>[function <span class="apidocSignatureSpan">store.util.</span>isList (val)](#apidoc.element.store.util.isList)
- description and source-code
```javascript
function isList(val) {
	return (val != null && typeof val != 'function' && typeof val.length == 'number')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.isObject"></a>[function <span class="apidocSignatureSpan">store.util.</span>isObject (val)](#apidoc.element.store.util.isObject)
- description and source-code
```javascript
function isObject(val) {
	return val && {}.toString.call(val) === '[object Object]'
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.map"></a>[function <span class="apidocSignatureSpan">store.util.</span>map (obj, fn)](#apidoc.element.store.util.map)
- description and source-code
```javascript
function map(obj, fn) {
	var res = (isList(obj) ? [] : {})
	pluck(obj, function(v, k) {
		res[k] = fn(v, k)
		return false
	})
	return res
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.pluck"></a>[function <span class="apidocSignatureSpan">store.util.</span>pluck (obj, fn)](#apidoc.element.store.util.pluck)
- description and source-code
```javascript
function pluck(obj, fn) {
	if (isList(obj)) {
		for (var i=0; i<obj.length; i++) {
			if (fn(obj[i], i)) {
				return obj[i]
			}
		}
	} else {
		for (var key in obj) {
			if (obj.hasOwnProperty(key)) {
				if (fn(obj[key], key)) {
					return obj[key]
				}
			}
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.slice"></a>[function <span class="apidocSignatureSpan">store.util.</span>slice (arr, index)](#apidoc.element.store.util.slice)
- description and source-code
```javascript
function slice(arr, index) {
	return Array.prototype.slice.call(arr, index || 0)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.util.trim"></a>[function <span class="apidocSignatureSpan">store.util.</span>trim (str)](#apidoc.element.store.util.trim)
- description and source-code
```javascript
function trim(str) {
			return String.prototype.trim.call(str)
		}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.store.v1_backcompat"></a>[module store.v1_backcompat](#apidoc.module.store.v1_backcompat)

#### <a name="apidoc.element.store.v1_backcompat.0"></a>[function <span class="apidocSignatureSpan">store.v1_backcompat.</span>0 ()](#apidoc.element.store.v1_backcompat.0)
- description and source-code
```javascript
function dumpPlugin() {
	return {
		dump: dump
	}
	
	function dump(_) {
		var res = {}
		this.each(function(val, key) {
			res[key] = val
		})
		return res
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.v1_backcompat.1"></a>[function <span class="apidocSignatureSpan">store.v1_backcompat.</span>1 ()](#apidoc.element.store.v1_backcompat.1)
- description and source-code
```javascript
function json2Plugin() {
	require('./lib/json2')
	return {}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.store.v1_backcompat.2"></a>[function <span class="apidocSignatureSpan">store.v1_backcompat.</span>2 ()](#apidoc.element.store.v1_backcompat.2)
- description and source-code
```javascript
function v1BackcompatPlugin() {
	this.disabled = !this.enabled
	return {
		has: backcompat_has,
		transact: backcompat_transact,
		clear: backcompat_clear,
		forEach: backcompat_forEach,
		getAll: backcompat_getAll,
		serialize: backcompat_serialize,
		deserialize: backcompat_deserialize,
	}
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
