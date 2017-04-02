# api documentation for  [htmlparser2 (v3.9.2)](https://github.com/fb55/htmlparser2#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-htmlparser2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-htmlparser2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-htmlparser2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-htmlparser2)
#### Fast & forgiving HTML/XML/RSS parser

[![NPM](https://nodei.co/npm/htmlparser2.png?downloads=true)](https://www.npmjs.com/package/htmlparser2)

[![apidoc](https://npmdoc.github.io/node-npmdoc-htmlparser2/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-htmlparser2_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-htmlparser2/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-htmlparser2/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Felix Boehm",
        "email": "me@feedic.com"
    },
    "browser": {
        "readable-stream": false
    },
    "bugs": {
        "url": "http://github.com/fb55/htmlparser2/issues"
    },
    "dependencies": {
        "domelementtype": "^1.3.0",
        "domhandler": "^2.3.0",
        "domutils": "^1.5.1",
        "entities": "^1.1.1",
        "inherits": "^2.0.1",
        "readable-stream": "^2.0.2"
    },
    "description": "Fast & forgiving HTML/XML/RSS parser",
    "devDependencies": {
        "coveralls": "^2.11.4",
        "eslint": "^2.12.0",
        "istanbul": "^0.4.3",
        "mocha": "^2.2.5",
        "mocha-lcov-reporter": "^1.2.0"
    },
    "directories": {
        "lib": "lib/"
    },
    "dist": {
        "shasum": "1bdf87acca0f3f9e53fa4fcceb0f4b4cbb00b338",
        "tarball": "https://registry.npmjs.org/htmlparser2/-/htmlparser2-3.9.2.tgz"
    },
    "files": [
        "lib"
    ],
    "gitHead": "e1f12f626f65cf4a082f89bdde89081b54187818",
    "homepage": "https://github.com/fb55/htmlparser2#readme",
    "keywords": [
        "html",
        "parser",
        "streams",
        "xml",
        "dom",
        "rss",
        "feed",
        "atom"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "feedic",
            "email": "me@feedic.com"
        }
    ],
    "name": "htmlparser2",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/fb55/htmlparser2.git"
    },
    "scripts": {
        "coveralls": "npm run lint && npm run lcov && (cat coverage/lcov.info | coveralls || exit 0)",
        "lcov": "istanbul cover _mocha --report lcovonly -- -R spec",
        "lint": "eslint lib test",
        "test": "mocha && npm run lint"
    },
    "version": "3.9.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module htmlparser2](#apidoc.module.htmlparser2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>CollectingHandler (cbs)](#apidoc.element.htmlparser2.CollectingHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>DefaultHandler (callback, options, elementCB)](#apidoc.element.htmlparser2.DefaultHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>DomHandler (callback, options, elementCB)](#apidoc.element.htmlparser2.DomHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>FeedHandler (callback, options)](#apidoc.element.htmlparser2.FeedHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>Parser (cbs, options)](#apidoc.element.htmlparser2.Parser)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>ProxyHandler (cbs)](#apidoc.element.htmlparser2.ProxyHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>RssHandler (callback, options)](#apidoc.element.htmlparser2.RssHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>Stream (options)](#apidoc.element.htmlparser2.Stream)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>Tokenizer (options, cbs)](#apidoc.element.htmlparser2.Tokenizer)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>WritableStream (cbs, options)](#apidoc.element.htmlparser2.WritableStream)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>createDomStream (cb, options, elementCb)](#apidoc.element.htmlparser2.createDomStream)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>parseDOM (data, options)](#apidoc.element.htmlparser2.parseDOM)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>parseFeed (feed, options)](#apidoc.element.htmlparser2.parseFeed)
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>CollectingHandler.prototype
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>DomHandler.prototype
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>DomUtils
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>EVENTS
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>ElementType
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>FeedHandler.prototype
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>Parser.prototype
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>ProxyHandler.prototype
1.  object <span class="apidocSignatureSpan">htmlparser2.</span>Tokenizer.prototype

#### [module htmlparser2.CollectingHandler](#apidoc.module.htmlparser2.CollectingHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>CollectingHandler (cbs)](#apidoc.element.htmlparser2.CollectingHandler.CollectingHandler)

#### [module htmlparser2.CollectingHandler.prototype](#apidoc.module.htmlparser2.CollectingHandler.prototype)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onattribute (a, b)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onattribute)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncdataend ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncdataend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncdatastart ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncdatastart)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onclosetag (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onclosetag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncomment (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncomment)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncommentend ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncommentend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.onend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onerror (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onerror)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onopentag (a, b)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onopentag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onopentagname (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onopentagname)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onprocessinginstruction (a, b)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onprocessinginstruction)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onreset ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.onreset)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>ontext (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.ontext)
1.  [function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>restart ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.restart)

#### [module htmlparser2.DomHandler](#apidoc.module.htmlparser2.DomHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>DomHandler (callback, options, elementCB)](#apidoc.element.htmlparser2.DomHandler.DomHandler)

#### [module htmlparser2.DomHandler.prototype](#apidoc.module.htmlparser2.DomHandler.prototype)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>_addDomElement (element)](#apidoc.element.htmlparser2.DomHandler.prototype._addDomElement)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>_handleCallback (error)](#apidoc.element.htmlparser2.DomHandler.prototype._handleCallback)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncdataend ()](#apidoc.element.htmlparser2.DomHandler.prototype.oncdataend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncdatastart ()](#apidoc.element.htmlparser2.DomHandler.prototype.oncdatastart)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onclosetag ()](#apidoc.element.htmlparser2.DomHandler.prototype.onclosetag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncomment (data)](#apidoc.element.htmlparser2.DomHandler.prototype.oncomment)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncommentend ()](#apidoc.element.htmlparser2.DomHandler.prototype.oncommentend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.DomHandler.prototype.onend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onerror (error)](#apidoc.element.htmlparser2.DomHandler.prototype.onerror)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onopentag (name, attribs)](#apidoc.element.htmlparser2.DomHandler.prototype.onopentag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onparserinit (parser)](#apidoc.element.htmlparser2.DomHandler.prototype.onparserinit)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onprocessinginstruction (name, data)](#apidoc.element.htmlparser2.DomHandler.prototype.onprocessinginstruction)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onreset ()](#apidoc.element.htmlparser2.DomHandler.prototype.onreset)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>ontext (data)](#apidoc.element.htmlparser2.DomHandler.prototype.ontext)

#### [module htmlparser2.DomUtils](#apidoc.module.htmlparser2.DomUtils)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>append ()](#apidoc.element.htmlparser2.DomUtils.append)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>appendChild ()](#apidoc.element.htmlparser2.DomUtils.appendChild)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>compareDocumentPosition ()](#apidoc.element.htmlparser2.DomUtils.compareDocumentPosition)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>existsOne ()](#apidoc.element.htmlparser2.DomUtils.existsOne)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>filter ()](#apidoc.element.htmlparser2.DomUtils.filter)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>find ()](#apidoc.element.htmlparser2.DomUtils.find)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>findAll ()](#apidoc.element.htmlparser2.DomUtils.findAll)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>findOne ()](#apidoc.element.htmlparser2.DomUtils.findOne)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>findOneChild ()](#apidoc.element.htmlparser2.DomUtils.findOneChild)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getAttributeValue ()](#apidoc.element.htmlparser2.DomUtils.getAttributeValue)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getChildren ()](#apidoc.element.htmlparser2.DomUtils.getChildren)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElementById ()](#apidoc.element.htmlparser2.DomUtils.getElementById)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElements ()](#apidoc.element.htmlparser2.DomUtils.getElements)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElementsByTagName ()](#apidoc.element.htmlparser2.DomUtils.getElementsByTagName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElementsByTagType ()](#apidoc.element.htmlparser2.DomUtils.getElementsByTagType)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getInnerHTML ()](#apidoc.element.htmlparser2.DomUtils.getInnerHTML)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getName ()](#apidoc.element.htmlparser2.DomUtils.getName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getOuterHTML ()](#apidoc.element.htmlparser2.DomUtils.getOuterHTML)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getParent ()](#apidoc.element.htmlparser2.DomUtils.getParent)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getSiblings ()](#apidoc.element.htmlparser2.DomUtils.getSiblings)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getText ()](#apidoc.element.htmlparser2.DomUtils.getText)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>hasAttrib ()](#apidoc.element.htmlparser2.DomUtils.hasAttrib)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>isTag ()](#apidoc.element.htmlparser2.DomUtils.isTag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>prepend ()](#apidoc.element.htmlparser2.DomUtils.prepend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>removeElement ()](#apidoc.element.htmlparser2.DomUtils.removeElement)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>removeSubsets ()](#apidoc.element.htmlparser2.DomUtils.removeSubsets)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>replaceElement ()](#apidoc.element.htmlparser2.DomUtils.replaceElement)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>testElement ()](#apidoc.element.htmlparser2.DomUtils.testElement)
1.  [function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>uniqueSort ()](#apidoc.element.htmlparser2.DomUtils.uniqueSort)

#### [module htmlparser2.ElementType](#apidoc.module.htmlparser2.ElementType)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>isTag (elem)](#apidoc.element.htmlparser2.ElementType.isTag)
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>CDATA
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>Comment
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>Directive
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>Doctype
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>Script
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>Style
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>Tag
1.  string <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>Text

#### [module htmlparser2.FeedHandler](#apidoc.module.htmlparser2.FeedHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>FeedHandler (callback, options)](#apidoc.element.htmlparser2.FeedHandler.FeedHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.FeedHandler.</span>super_ (callback, options, elementCB)](#apidoc.element.htmlparser2.FeedHandler.super_)

#### [module htmlparser2.FeedHandler.prototype](#apidoc.module.htmlparser2.FeedHandler.prototype)
1.  [function <span class="apidocSignatureSpan">htmlparser2.FeedHandler.prototype.</span>init (callback, options, elementCB)](#apidoc.element.htmlparser2.FeedHandler.prototype.init)
1.  [function <span class="apidocSignatureSpan">htmlparser2.FeedHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.FeedHandler.prototype.onend)

#### [module htmlparser2.Parser](#apidoc.module.htmlparser2.Parser)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>Parser (cbs, options)](#apidoc.element.htmlparser2.Parser.Parser)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.</span>super_ ()](#apidoc.element.htmlparser2.Parser.super_)

#### [module htmlparser2.Parser.prototype](#apidoc.module.htmlparser2.Parser.prototype)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>_closeCurrentTag ()](#apidoc.element.htmlparser2.Parser.prototype._closeCurrentTag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>_getInstructionName (value)](#apidoc.element.htmlparser2.Parser.prototype._getInstructionName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>_updatePosition (initialOffset)](#apidoc.element.htmlparser2.Parser.prototype._updatePosition)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>done (chunk)](#apidoc.element.htmlparser2.Parser.prototype.done)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>end (chunk)](#apidoc.element.htmlparser2.Parser.prototype.end)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onattribdata (value)](#apidoc.element.htmlparser2.Parser.prototype.onattribdata)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onattribend ()](#apidoc.element.htmlparser2.Parser.prototype.onattribend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onattribname (name)](#apidoc.element.htmlparser2.Parser.prototype.onattribname)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>oncdata (value)](#apidoc.element.htmlparser2.Parser.prototype.oncdata)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onclosetag (name)](#apidoc.element.htmlparser2.Parser.prototype.onclosetag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>oncomment (value)](#apidoc.element.htmlparser2.Parser.prototype.oncomment)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>ondeclaration (value)](#apidoc.element.htmlparser2.Parser.prototype.ondeclaration)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onend ()](#apidoc.element.htmlparser2.Parser.prototype.onend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onerror (err)](#apidoc.element.htmlparser2.Parser.prototype.onerror)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onopentagend ()](#apidoc.element.htmlparser2.Parser.prototype.onopentagend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onopentagname (name)](#apidoc.element.htmlparser2.Parser.prototype.onopentagname)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onprocessinginstruction (value)](#apidoc.element.htmlparser2.Parser.prototype.onprocessinginstruction)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onselfclosingtag ()](#apidoc.element.htmlparser2.Parser.prototype.onselfclosingtag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>ontext (data)](#apidoc.element.htmlparser2.Parser.prototype.ontext)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>parseChunk (chunk)](#apidoc.element.htmlparser2.Parser.prototype.parseChunk)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>parseComplete (data)](#apidoc.element.htmlparser2.Parser.prototype.parseComplete)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>pause ()](#apidoc.element.htmlparser2.Parser.prototype.pause)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>reset ()](#apidoc.element.htmlparser2.Parser.prototype.reset)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>resume ()](#apidoc.element.htmlparser2.Parser.prototype.resume)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>write (chunk)](#apidoc.element.htmlparser2.Parser.prototype.write)

#### [module htmlparser2.ProxyHandler](#apidoc.module.htmlparser2.ProxyHandler)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>ProxyHandler (cbs)](#apidoc.element.htmlparser2.ProxyHandler.ProxyHandler)

#### [module htmlparser2.ProxyHandler.prototype](#apidoc.module.htmlparser2.ProxyHandler.prototype)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onattribute (a, b)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onattribute)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncdataend ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncdataend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncdatastart ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncdatastart)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onclosetag (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onclosetag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncomment (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncomment)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncommentend ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncommentend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.onend)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onerror (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onerror)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onopentag (a, b)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onopentag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onopentagname (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onopentagname)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onprocessinginstruction (a, b)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onprocessinginstruction)
1.  [function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>ontext (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.ontext)

#### [module htmlparser2.Stream](#apidoc.module.htmlparser2.Stream)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>Stream (options)](#apidoc.element.htmlparser2.Stream.Stream)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Stream.</span>super_ (cbs, options)](#apidoc.element.htmlparser2.Stream.super_)

#### [module htmlparser2.Tokenizer](#apidoc.module.htmlparser2.Tokenizer)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>Tokenizer (options, cbs)](#apidoc.element.htmlparser2.Tokenizer.Tokenizer)

#### [module htmlparser2.Tokenizer.prototype](#apidoc.module.htmlparser2.Tokenizer.prototype)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_cleanup ()](#apidoc.element.htmlparser2.Tokenizer.prototype._cleanup)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_decodeNumericEntity (offset, base)](#apidoc.element.htmlparser2.Tokenizer.prototype._decodeNumericEntity)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_emitPartial (value)](#apidoc.element.htmlparser2.Tokenizer.prototype._emitPartial)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_emitToken (name)](#apidoc.element.htmlparser2.Tokenizer.prototype._emitToken)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_finish ()](#apidoc.element.htmlparser2.Tokenizer.prototype._finish)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_getSection ()](#apidoc.element.htmlparser2.Tokenizer.prototype._getSection)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_handleTrailingData ()](#apidoc.element.htmlparser2.Tokenizer.prototype._handleTrailingData)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_parse ()](#apidoc.element.htmlparser2.Tokenizer.prototype._parse)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_parseLegacyEntity ()](#apidoc.element.htmlparser2.Tokenizer.prototype._parseLegacyEntity)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_parseNamedEntityStrict ()](#apidoc.element.htmlparser2.Tokenizer.prototype._parseNamedEntityStrict)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterAttributeName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterAttributeName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterCdata1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCdata1)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterCdata2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCdata2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterCloseingTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCloseingTagName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterComment1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterComment1)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterComment2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterComment2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript1)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript3)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript4)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript5 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript5)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle1)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle3)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle4)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeAttributeName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeAttributeName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeAttributeValue (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeAttributeValue)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata1)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata3)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata4)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata5 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata5)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata6 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata6)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCloseingTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCloseingTagName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeComment (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeComment)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeDeclaration (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeDeclaration)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeEntity)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeNumericEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeNumericEntity)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript1)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript3)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript4)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript5 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript5)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeSpecial (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeSpecial)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeSpecialEnd (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeSpecialEnd)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle1)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle2)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle3)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle4)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeTagName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeValueDoubleQuotes (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueDoubleQuotes)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeValueNoQuotes (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueNoQuotes)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeValueSingleQuotes (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueSingleQuotes)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInCdata (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInCdata)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInCloseingTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInCloseingTagName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInComment (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInComment)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInDeclaration (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInDeclaration)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInHexEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInHexEntity)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInNamedEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInNamedEntity)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInNumericEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInNumericEntity)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInProcessingInstruction (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInProcessingInstruction)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInSelfClosingTag (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInSelfClosingTag)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInTagName)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateText (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateText)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>end (chunk)](#apidoc.element.htmlparser2.Tokenizer.prototype.end)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>getAbsoluteIndex ()](#apidoc.element.htmlparser2.Tokenizer.prototype.getAbsoluteIndex)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>pause ()](#apidoc.element.htmlparser2.Tokenizer.prototype.pause)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>reset ()](#apidoc.element.htmlparser2.Tokenizer.prototype.reset)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>resume ()](#apidoc.element.htmlparser2.Tokenizer.prototype.resume)
1.  [function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>write (chunk)](#apidoc.element.htmlparser2.Tokenizer.prototype.write)

#### [module htmlparser2.WritableStream](#apidoc.module.htmlparser2.WritableStream)
1.  [function <span class="apidocSignatureSpan">htmlparser2.</span>WritableStream (cbs, options)](#apidoc.element.htmlparser2.WritableStream.WritableStream)
1.  [function <span class="apidocSignatureSpan">htmlparser2.WritableStream.</span>super_ (options)](#apidoc.element.htmlparser2.WritableStream.super_)



# <a name="apidoc.module.htmlparser2"></a>[module htmlparser2](#apidoc.module.htmlparser2)

#### <a name="apidoc.element.htmlparser2.CollectingHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>CollectingHandler (cbs)](#apidoc.element.htmlparser2.CollectingHandler)
- description and source-code
```javascript
function CollectingHandler(cbs){
	this._cbs = cbs || {};
	this.events = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DefaultHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>DefaultHandler (callback, options, elementCB)](#apidoc.element.htmlparser2.DefaultHandler)
- description and source-code
```javascript
function DomHandler(callback, options, elementCB){
	if(typeof callback === "object"){
		elementCB = options;
		options = callback;
		callback = null;
	} else if(typeof options === "function"){
		elementCB = options;
		options = defaultOpts;
	}
	this._callback = callback;
	this._options = options || defaultOpts;
	this._elementCB = elementCB;
	this.dom = [];
	this._done = false;
	this._tagStack = [];
	this._parser = this._parser || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>DomHandler (callback, options, elementCB)](#apidoc.element.htmlparser2.DomHandler)
- description and source-code
```javascript
function DomHandler(callback, options, elementCB){
	if(typeof callback === "object"){
		elementCB = options;
		options = callback;
		callback = null;
	} else if(typeof options === "function"){
		elementCB = options;
		options = defaultOpts;
	}
	this._callback = callback;
	this._options = options || defaultOpts;
	this._elementCB = elementCB;
	this.dom = [];
	this._done = false;
	this._tagStack = [];
	this._parser = this._parser || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.FeedHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>FeedHandler (callback, options)](#apidoc.element.htmlparser2.FeedHandler)
- description and source-code
```javascript
function FeedHandler(callback, options){
	this.init(callback, options);
}
```
- example usage
```shell
...
The 'DomHandler' (known as 'DefaultHandler' in the original 'htmlparser' module) produces a DOM (document object model) that can
 be manipulated using the ['DomUtils'](https://github.com/fb55/DomUtils) helper.

The 'DomHandler', while still bundled with this module, was moved to its [own module](https://github.com/fb55/domhandler). Have
a look at it for further information.

## Parsing RSS/RDF/Atom Feeds

'''javascript
new htmlparser.FeedHandler(function(<error> error, <object> feed){
    ...
});
'''

Note: While the provided feed handler works for most feeds, you might want to use  [danmactough/node-feedparser](https://github.
com/danmactough/node-feedparser), which is much better tested and actively maintained.

## Performance
...
```

#### <a name="apidoc.element.htmlparser2.Parser"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>Parser (cbs, options)](#apidoc.element.htmlparser2.Parser)
- description and source-code
```javascript
function Parser(cbs, options){
	this._options = options || {};
	this._cbs = cbs || {};

	this._tagname = "";
	this._attribname = "";
	this._attribvalue = "";
	this._attribs = null;
	this._stack = [];

	this.startIndex = 0;
	this.endIndex = null;

	this._lowerCaseTagNames = "lowerCaseTags" in this._options ?
									!!this._options.lowerCaseTags :
									!this._options.xmlMode;
	this._lowerCaseAttributeNames = "lowerCaseAttributeNames" in this._options ?
									!!this._options.lowerCaseAttributeNames :
									!this._options.xmlMode;

	if(this._options.Tokenizer) {
		Tokenizer = this._options.Tokenizer;
	}
	this._tokenizer = new Tokenizer(this._options, this);

	if(this._cbs.onparserinit) this._cbs.onparserinit(this);
}
```
- example usage
```shell
...

A live demo of htmlparser2 is available [here](http://demos.forbeslindesay.co.uk/htmlparser2/).

## Usage

'''javascript
var htmlparser = require("htmlparser2");
var parser = new htmlparser.Parser({
	onopentag: function(name, attribs){
		if(name === "script" && attribs.type === "text/javascript"){
			console.log("JS! Hooray!");
		}
	},
	ontext: function(text){
		console.log("-->", text);
...
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>ProxyHandler (cbs)](#apidoc.element.htmlparser2.ProxyHandler)
- description and source-code
```javascript
function ProxyHandler(cbs){
	this._cbs = cbs || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.RssHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>RssHandler (callback, options)](#apidoc.element.htmlparser2.RssHandler)
- description and source-code
```javascript
function FeedHandler(callback, options){
	this.init(callback, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Stream"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>Stream (options)](#apidoc.element.htmlparser2.Stream)
- description and source-code
```javascript
function Stream(options){
	Parser.call(this, new Cbs(this), options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>Tokenizer (options, cbs)](#apidoc.element.htmlparser2.Tokenizer)
- description and source-code
```javascript
function Tokenizer(options, cbs){
	this._state = TEXT;
	this._buffer = "";
	this._sectionStart = 0;
	this._index = 0;
	this._bufferOffset = 0; //chars removed from _buffer
	this._baseState = TEXT;
	this._special = SPECIAL_NONE;
	this._cbs = cbs;
	this._running = true;
	this._ended = false;
	this._xmlMode = !!(options && options.xmlMode);
	this._decodeEntities = !!(options && options.decodeEntities);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.WritableStream"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>WritableStream (cbs, options)](#apidoc.element.htmlparser2.WritableStream)
- description and source-code
```javascript
function Stream(cbs, options){
	var parser = this._parser = new Parser(cbs, options);
	var decoder = this._decoder = new StringDecoder();

	WritableStream.call(this, {decodeStrings: false});

	this.once("finish", function(){
		parser.end(decoder.end());
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.createDomStream"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>createDomStream (cb, options, elementCb)](#apidoc.element.htmlparser2.createDomStream)
- description and source-code
```javascript
createDomStream = function (cb, options, elementCb){
		var handler = new DomHandler(cb, options, elementCb);
		return new Parser(handler, options);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.parseDOM"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>parseDOM (data, options)](#apidoc.element.htmlparser2.parseDOM)
- description and source-code
```javascript
parseDOM = function (data, options){
		var handler = new DomHandler(options);
		new Parser(handler, options).end(data);
		return handler.dom;
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.parseFeed"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>parseFeed (feed, options)](#apidoc.element.htmlparser2.parseFeed)
- description and source-code
```javascript
parseFeed = function (feed, options){
		var handler = new module.exports.FeedHandler(options);
		new Parser(handler, options).end(feed);
		return handler.dom;
	}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.CollectingHandler"></a>[module htmlparser2.CollectingHandler](#apidoc.module.htmlparser2.CollectingHandler)

#### <a name="apidoc.element.htmlparser2.CollectingHandler.CollectingHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>CollectingHandler (cbs)](#apidoc.element.htmlparser2.CollectingHandler.CollectingHandler)
- description and source-code
```javascript
function CollectingHandler(cbs){
	this._cbs = cbs || {};
	this.events = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.CollectingHandler.prototype"></a>[module htmlparser2.CollectingHandler.prototype](#apidoc.module.htmlparser2.CollectingHandler.prototype)

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onattribute"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onattribute (a, b)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onattribute)
- description and source-code
```javascript
onattribute = function (a, b){
			this.events.push([name, a, b]);
			if(this._cbs[name]) this._cbs[name](a, b);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.oncdataend"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncdataend ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncdataend)
- description and source-code
```javascript
oncdataend = function (){
			this.events.push([name]);
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.oncdatastart"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncdatastart ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncdatastart)
- description and source-code
```javascript
oncdatastart = function (){
			this.events.push([name]);
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onclosetag"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onclosetag (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onclosetag)
- description and source-code
```javascript
onclosetag = function (a){
			this.events.push([name, a]);
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.oncomment"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncomment (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncomment)
- description and source-code
```javascript
oncomment = function (a){
			this.events.push([name, a]);
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.oncommentend"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>oncommentend ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.oncommentend)
- description and source-code
```javascript
oncommentend = function (){
			this.events.push([name]);
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onend"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.onend)
- description and source-code
```javascript
onend = function (){
			this.events.push([name]);
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onerror"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onerror (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onerror)
- description and source-code
```javascript
onerror = function (a){
			this.events.push([name, a]);
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onopentag"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onopentag (a, b)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onopentag)
- description and source-code
```javascript
onopentag = function (a, b){
			this.events.push([name, a, b]);
			if(this._cbs[name]) this._cbs[name](a, b);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onopentagname"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onopentagname (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onopentagname)
- description and source-code
```javascript
onopentagname = function (a){
			this.events.push([name, a]);
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onprocessinginstruction"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onprocessinginstruction (a, b)](#apidoc.element.htmlparser2.CollectingHandler.prototype.onprocessinginstruction)
- description and source-code
```javascript
onprocessinginstruction = function (a, b){
			this.events.push([name, a, b]);
			if(this._cbs[name]) this._cbs[name](a, b);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.onreset"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>onreset ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.onreset)
- description and source-code
```javascript
onreset = function (){
	this.events = [];
	if(this._cbs.onreset) this._cbs.onreset();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.ontext"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>ontext (a)](#apidoc.element.htmlparser2.CollectingHandler.prototype.ontext)
- description and source-code
```javascript
ontext = function (a){
			this.events.push([name, a]);
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.CollectingHandler.prototype.restart"></a>[function <span class="apidocSignatureSpan">htmlparser2.CollectingHandler.prototype.</span>restart ()](#apidoc.element.htmlparser2.CollectingHandler.prototype.restart)
- description and source-code
```javascript
restart = function (){
	if(this._cbs.onreset) this._cbs.onreset();

	for(var i = 0, len = this.events.length; i < len; i++){
		if(this._cbs[this.events[i][0]]){

			var num = this.events[i].length;

			if(num === 1){
				this._cbs[this.events[i][0]]();
			} else if(num === 2){
				this._cbs[this.events[i][0]](this.events[i][1]);
			} else {
				this._cbs[this.events[i][0]](this.events[i][1], this.events[i][2]);
			}
		}
	}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.DomHandler"></a>[module htmlparser2.DomHandler](#apidoc.module.htmlparser2.DomHandler)

#### <a name="apidoc.element.htmlparser2.DomHandler.DomHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>DomHandler (callback, options, elementCB)](#apidoc.element.htmlparser2.DomHandler.DomHandler)
- description and source-code
```javascript
function DomHandler(callback, options, elementCB){
	if(typeof callback === "object"){
		elementCB = options;
		options = callback;
		callback = null;
	} else if(typeof options === "function"){
		elementCB = options;
		options = defaultOpts;
	}
	this._callback = callback;
	this._options = options || defaultOpts;
	this._elementCB = elementCB;
	this.dom = [];
	this._done = false;
	this._tagStack = [];
	this._parser = this._parser || null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.DomHandler.prototype"></a>[module htmlparser2.DomHandler.prototype](#apidoc.module.htmlparser2.DomHandler.prototype)

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype._addDomElement"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>_addDomElement (element)](#apidoc.element.htmlparser2.DomHandler.prototype._addDomElement)
- description and source-code
```javascript
_addDomElement = function (element){
	var parent = this._tagStack[this._tagStack.length - 1];
	var siblings = parent ? parent.children : this.dom;
	var previousSibling = siblings[siblings.length - 1];

	element.next = null;

	if(this._options.withStartIndices){
		element.startIndex = this._parser.startIndex;
	}

	if (this._options.withDomLvl1) {
		element.__proto__ = element.type === "tag" ? ElementPrototype : NodePrototype;
	}

	if(previousSibling){
		element.prev = previousSibling;
		previousSibling.next = element;
	} else {
		element.prev = null;
	}

	siblings.push(element);
	element.parent = parent || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype._handleCallback"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>_handleCallback (error)](#apidoc.element.htmlparser2.DomHandler.prototype._handleCallback)
- description and source-code
```javascript
_handleCallback = function (error){
	if(typeof this._callback === "function"){
		this._callback(error, this.dom);
	} else {
		if(error) throw error;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.oncdataend"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncdataend ()](#apidoc.element.htmlparser2.DomHandler.prototype.oncdataend)
- description and source-code
```javascript
oncdataend = function (){
	this._tagStack.pop();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.oncdatastart"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncdatastart ()](#apidoc.element.htmlparser2.DomHandler.prototype.oncdatastart)
- description and source-code
```javascript
oncdatastart = function (){
	var element = {
		children: [{
			data: "",
			type: ElementType.Text
		}],
		type: ElementType.CDATA
	};

	this._addDomElement(element);
	this._tagStack.push(element);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.onclosetag"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onclosetag ()](#apidoc.element.htmlparser2.DomHandler.prototype.onclosetag)
- description and source-code
```javascript
onclosetag = function (){
	//if(this._tagStack.pop().name !== name) this._handleCallback(Error("Tagname didn't match!"));
	var elem = this._tagStack.pop();
	if(this._elementCB) this._elementCB(elem);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.oncomment"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncomment (data)](#apidoc.element.htmlparser2.DomHandler.prototype.oncomment)
- description and source-code
```javascript
oncomment = function (data){
	var lastTag = this._tagStack[this._tagStack.length - 1];

	if(lastTag && lastTag.type === ElementType.Comment){
		lastTag.data += data;
		return;
	}

	var element = {
		data: data,
		type: ElementType.Comment
	};

	this._addDomElement(element);
	this._tagStack.push(element);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.oncommentend"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>oncommentend ()](#apidoc.element.htmlparser2.DomHandler.prototype.oncommentend)
- description and source-code
```javascript
oncommentend = function (){
	this._tagStack.pop();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.onend"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.DomHandler.prototype.onend)
- description and source-code
```javascript
onend = function (){
	if(this._done) return;
	this._done = true;
	this._parser = null;
	this._handleCallback(null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.onerror"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onerror (error)](#apidoc.element.htmlparser2.DomHandler.prototype.onerror)
- description and source-code
```javascript
onerror = function (error){
	if(typeof this._callback === "function"){
		this._callback(error, this.dom);
	} else {
		if(error) throw error;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.onopentag"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onopentag (name, attribs)](#apidoc.element.htmlparser2.DomHandler.prototype.onopentag)
- description and source-code
```javascript
onopentag = function (name, attribs){
	var element = {
		type: name === "script" ? ElementType.Script : name === "style" ? ElementType.Style : ElementType.Tag,
		name: name,
		attribs: attribs,
		children: []
	};

	this._addDomElement(element);

	this._tagStack.push(element);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.onparserinit"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onparserinit (parser)](#apidoc.element.htmlparser2.DomHandler.prototype.onparserinit)
- description and source-code
```javascript
onparserinit = function (parser){
	this._parser = parser;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.onprocessinginstruction"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onprocessinginstruction (name, data)](#apidoc.element.htmlparser2.DomHandler.prototype.onprocessinginstruction)
- description and source-code
```javascript
onprocessinginstruction = function (name, data){
	this._addDomElement({
		name: name,
		data: data,
		type: ElementType.Directive
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.onreset"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>onreset ()](#apidoc.element.htmlparser2.DomHandler.prototype.onreset)
- description and source-code
```javascript
onreset = function (){
	DomHandler.call(this, this._callback, this._options, this._elementCB);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomHandler.prototype.ontext"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomHandler.prototype.</span>ontext (data)](#apidoc.element.htmlparser2.DomHandler.prototype.ontext)
- description and source-code
```javascript
ontext = function (data){
	//the ignoreWhitespace is officially dropped, but for now,
	//it's an alias for normalizeWhitespace
	var normalize = this._options.normalizeWhitespace || this._options.ignoreWhitespace;

	var lastTag;

	if(!this._tagStack.length && this.dom.length && (lastTag = this.dom[this.dom.length-1]).type === ElementType.Text){
		if(normalize){
			lastTag.data = (lastTag.data + data).replace(re_whitespace, " ");
		} else {
			lastTag.data += data;
		}
	} else {
		if(
			this._tagStack.length &&
			(lastTag = this._tagStack[this._tagStack.length - 1]) &&
			(lastTag = lastTag.children[lastTag.children.length - 1]) &&
			lastTag.type === ElementType.Text
		){
			if(normalize){
				lastTag.data = (lastTag.data + data).replace(re_whitespace, " ");
			} else {
				lastTag.data += data;
			}
		} else {
			if(normalize){
				data = data.replace(re_whitespace, " ");
			}

			this._addDomElement({
				data: data,
				type: ElementType.Text
			});
		}
	}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.DomUtils"></a>[module htmlparser2.DomUtils](#apidoc.module.htmlparser2.DomUtils)

#### <a name="apidoc.element.htmlparser2.DomUtils.append"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>append ()](#apidoc.element.htmlparser2.DomUtils.append)
- description and source-code
```javascript
append = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.appendChild"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>appendChild ()](#apidoc.element.htmlparser2.DomUtils.appendChild)
- description and source-code
```javascript
appendChild = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.compareDocumentPosition"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>compareDocumentPosition ()](#apidoc.element.htmlparser2.DomUtils.compareDocumentPosition)
- description and source-code
```javascript
compareDocumentPosition = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.existsOne"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>existsOne ()](#apidoc.element.htmlparser2.DomUtils.existsOne)
- description and source-code
```javascript
existsOne = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.filter"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>filter ()](#apidoc.element.htmlparser2.DomUtils.filter)
- description and source-code
```javascript
filter = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.find"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>find ()](#apidoc.element.htmlparser2.DomUtils.find)
- description and source-code
```javascript
find = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.findAll"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>findAll ()](#apidoc.element.htmlparser2.DomUtils.findAll)
- description and source-code
```javascript
findAll = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.findOne"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>findOne ()](#apidoc.element.htmlparser2.DomUtils.findOne)
- description and source-code
```javascript
findOne = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.findOneChild"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>findOneChild ()](#apidoc.element.htmlparser2.DomUtils.findOneChild)
- description and source-code
```javascript
findOneChild = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getAttributeValue"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getAttributeValue ()](#apidoc.element.htmlparser2.DomUtils.getAttributeValue)
- description and source-code
```javascript
getAttributeValue = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getChildren"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getChildren ()](#apidoc.element.htmlparser2.DomUtils.getChildren)
- description and source-code
```javascript
getChildren = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getElementById"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElementById ()](#apidoc.element.htmlparser2.DomUtils.getElementById)
- description and source-code
```javascript
getElementById = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getElements"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElements ()](#apidoc.element.htmlparser2.DomUtils.getElements)
- description and source-code
```javascript
getElements = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getElementsByTagName"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElementsByTagName ()](#apidoc.element.htmlparser2.DomUtils.getElementsByTagName)
- description and source-code
```javascript
getElementsByTagName = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getElementsByTagType"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getElementsByTagType ()](#apidoc.element.htmlparser2.DomUtils.getElementsByTagType)
- description and source-code
```javascript
getElementsByTagType = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getInnerHTML"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getInnerHTML ()](#apidoc.element.htmlparser2.DomUtils.getInnerHTML)
- description and source-code
```javascript
getInnerHTML = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getName"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getName ()](#apidoc.element.htmlparser2.DomUtils.getName)
- description and source-code
```javascript
getName = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getOuterHTML"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getOuterHTML ()](#apidoc.element.htmlparser2.DomUtils.getOuterHTML)
- description and source-code
```javascript
getOuterHTML = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getParent"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getParent ()](#apidoc.element.htmlparser2.DomUtils.getParent)
- description and source-code
```javascript
getParent = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getSiblings"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getSiblings ()](#apidoc.element.htmlparser2.DomUtils.getSiblings)
- description and source-code
```javascript
getSiblings = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.getText"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>getText ()](#apidoc.element.htmlparser2.DomUtils.getText)
- description and source-code
```javascript
getText = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.hasAttrib"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>hasAttrib ()](#apidoc.element.htmlparser2.DomUtils.hasAttrib)
- description and source-code
```javascript
hasAttrib = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.isTag"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>isTag ()](#apidoc.element.htmlparser2.DomUtils.isTag)
- description and source-code
```javascript
isTag = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.prepend"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>prepend ()](#apidoc.element.htmlparser2.DomUtils.prepend)
- description and source-code
```javascript
prepend = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.removeElement"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>removeElement ()](#apidoc.element.htmlparser2.DomUtils.removeElement)
- description and source-code
```javascript
removeElement = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.removeSubsets"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>removeSubsets ()](#apidoc.element.htmlparser2.DomUtils.removeSubsets)
- description and source-code
```javascript
removeSubsets = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.replaceElement"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>replaceElement ()](#apidoc.element.htmlparser2.DomUtils.replaceElement)
- description and source-code
```javascript
replaceElement = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.testElement"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>testElement ()](#apidoc.element.htmlparser2.DomUtils.testElement)
- description and source-code
```javascript
testElement = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.DomUtils.uniqueSort"></a>[function <span class="apidocSignatureSpan">htmlparser2.DomUtils.</span>uniqueSort ()](#apidoc.element.htmlparser2.DomUtils.uniqueSort)
- description and source-code
```javascript
uniqueSort = function () { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.ElementType"></a>[module htmlparser2.ElementType](#apidoc.module.htmlparser2.ElementType)

#### <a name="apidoc.element.htmlparser2.ElementType.isTag"></a>[function <span class="apidocSignatureSpan">htmlparser2.ElementType.</span>isTag (elem)](#apidoc.element.htmlparser2.ElementType.isTag)
- description and source-code
```javascript
isTag = function (elem){
		return elem.type === "tag" || elem.type === "script" || elem.type === "style";
	}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.FeedHandler"></a>[module htmlparser2.FeedHandler](#apidoc.module.htmlparser2.FeedHandler)

#### <a name="apidoc.element.htmlparser2.FeedHandler.FeedHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>FeedHandler (callback, options)](#apidoc.element.htmlparser2.FeedHandler.FeedHandler)
- description and source-code
```javascript
function FeedHandler(callback, options){
	this.init(callback, options);
}
```
- example usage
```shell
...
The 'DomHandler' (known as 'DefaultHandler' in the original 'htmlparser' module) produces a DOM (document object model) that can
 be manipulated using the ['DomUtils'](https://github.com/fb55/DomUtils) helper.

The 'DomHandler', while still bundled with this module, was moved to its [own module](https://github.com/fb55/domhandler). Have
a look at it for further information.

## Parsing RSS/RDF/Atom Feeds

'''javascript
new htmlparser.FeedHandler(function(<error> error, <object> feed){
    ...
});
'''

Note: While the provided feed handler works for most feeds, you might want to use  [danmactough/node-feedparser](https://github.
com/danmactough/node-feedparser), which is much better tested and actively maintained.

## Performance
...
```

#### <a name="apidoc.element.htmlparser2.FeedHandler.super_"></a>[function <span class="apidocSignatureSpan">htmlparser2.FeedHandler.</span>super_ (callback, options, elementCB)](#apidoc.element.htmlparser2.FeedHandler.super_)
- description and source-code
```javascript
function DomHandler(callback, options, elementCB){
	if(typeof callback === "object"){
		elementCB = options;
		options = callback;
		callback = null;
	} else if(typeof options === "function"){
		elementCB = options;
		options = defaultOpts;
	}
	this._callback = callback;
	this._options = options || defaultOpts;
	this._elementCB = elementCB;
	this.dom = [];
	this._done = false;
	this._tagStack = [];
	this._parser = this._parser || null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.FeedHandler.prototype"></a>[module htmlparser2.FeedHandler.prototype](#apidoc.module.htmlparser2.FeedHandler.prototype)

#### <a name="apidoc.element.htmlparser2.FeedHandler.prototype.init"></a>[function <span class="apidocSignatureSpan">htmlparser2.FeedHandler.prototype.</span>init (callback, options, elementCB)](#apidoc.element.htmlparser2.FeedHandler.prototype.init)
- description and source-code
```javascript
function DomHandler(callback, options, elementCB){
	if(typeof callback === "object"){
		elementCB = options;
		options = callback;
		callback = null;
	} else if(typeof options === "function"){
		elementCB = options;
		options = defaultOpts;
	}
	this._callback = callback;
	this._options = options || defaultOpts;
	this._elementCB = elementCB;
	this.dom = [];
	this._done = false;
	this._tagStack = [];
	this._parser = this._parser || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.FeedHandler.prototype.onend"></a>[function <span class="apidocSignatureSpan">htmlparser2.FeedHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.FeedHandler.prototype.onend)
- description and source-code
```javascript
onend = function (){
	var feed = {},
	    feedRoot = getOneElement(isValidFeed, this.dom),
	    tmp, childs;

	if(feedRoot){
		if(feedRoot.name === "feed"){
			childs = feedRoot.children;

			feed.type = "atom";
			addConditionally(feed, "id", "id", childs);
			addConditionally(feed, "title", "title", childs);
			if((tmp = getOneElement("link", childs)) && (tmp = tmp.attribs) && (tmp = tmp.href)) feed.link = tmp;
			addConditionally(feed, "description", "subtitle", childs);
			if((tmp = fetch("updated", childs))) feed.updated = new Date(tmp);
			addConditionally(feed, "author", "email", childs, true);

			feed.items = getElements("entry", childs).map(function(item){
				var entry = {}, tmp;

				item = item.children;

				addConditionally(entry, "id", "id", item);
				addConditionally(entry, "title", "title", item);
				if((tmp = getOneElement("link", item)) && (tmp = tmp.attribs) && (tmp = tmp.href)) entry.link = tmp;
				if((tmp = fetch("summary", item) || fetch("content", item))) entry.description = tmp;
				if((tmp = fetch("updated", item))) entry.pubDate = new Date(tmp);
				return entry;
			});
		} else {
			childs = getOneElement("channel", feedRoot.children).children;

			feed.type = feedRoot.name.substr(0, 3);
			feed.id = "";
			addConditionally(feed, "title", "title", childs);
			addConditionally(feed, "link", "link", childs);
			addConditionally(feed, "description", "description", childs);
			if((tmp = fetch("lastBuildDate", childs))) feed.updated = new Date(tmp);
			addConditionally(feed, "author", "managingEditor", childs, true);

			feed.items = getElements("item", feedRoot.children).map(function(item){
				var entry = {}, tmp;

				item = item.children;

				addConditionally(entry, "id", "guid", item);
				addConditionally(entry, "title", "title", item);
				addConditionally(entry, "link", "link", item);
				addConditionally(entry, "description", "description", item);
				if((tmp = fetch("pubDate", item))) entry.pubDate = new Date(tmp);
				return entry;
			});
		}
	}
	this.dom = feed;
	DomHandler.prototype._handleCallback.call(
		this, feedRoot ? null : Error("couldn't find root of feed")
	);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.Parser"></a>[module htmlparser2.Parser](#apidoc.module.htmlparser2.Parser)

#### <a name="apidoc.element.htmlparser2.Parser.Parser"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>Parser (cbs, options)](#apidoc.element.htmlparser2.Parser.Parser)
- description and source-code
```javascript
function Parser(cbs, options){
	this._options = options || {};
	this._cbs = cbs || {};

	this._tagname = "";
	this._attribname = "";
	this._attribvalue = "";
	this._attribs = null;
	this._stack = [];

	this.startIndex = 0;
	this.endIndex = null;

	this._lowerCaseTagNames = "lowerCaseTags" in this._options ?
									!!this._options.lowerCaseTags :
									!this._options.xmlMode;
	this._lowerCaseAttributeNames = "lowerCaseAttributeNames" in this._options ?
									!!this._options.lowerCaseAttributeNames :
									!this._options.xmlMode;

	if(this._options.Tokenizer) {
		Tokenizer = this._options.Tokenizer;
	}
	this._tokenizer = new Tokenizer(this._options, this);

	if(this._cbs.onparserinit) this._cbs.onparserinit(this);
}
```
- example usage
```shell
...

A live demo of htmlparser2 is available [here](http://demos.forbeslindesay.co.uk/htmlparser2/).

## Usage

'''javascript
var htmlparser = require("htmlparser2");
var parser = new htmlparser.Parser({
	onopentag: function(name, attribs){
		if(name === "script" && attribs.type === "text/javascript"){
			console.log("JS! Hooray!");
		}
	},
	ontext: function(text){
		console.log("-->", text);
...
```

#### <a name="apidoc.element.htmlparser2.Parser.super_"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.</span>super_ ()](#apidoc.element.htmlparser2.Parser.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.Parser.prototype"></a>[module htmlparser2.Parser.prototype](#apidoc.module.htmlparser2.Parser.prototype)

#### <a name="apidoc.element.htmlparser2.Parser.prototype._closeCurrentTag"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>_closeCurrentTag ()](#apidoc.element.htmlparser2.Parser.prototype._closeCurrentTag)
- description and source-code
```javascript
_closeCurrentTag = function (){
	var name = this._tagname;

	this.onopentagend();

	//self-closing tags will be on the top of the stack
	//(cheaper check than in onclosetag)
	if(this._stack[this._stack.length - 1] === name){
		if(this._cbs.onclosetag){
			this._cbs.onclosetag(name);
		}
		this._stack.pop();
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype._getInstructionName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>_getInstructionName (value)](#apidoc.element.htmlparser2.Parser.prototype._getInstructionName)
- description and source-code
```javascript
_getInstructionName = function (value){
	var idx = value.search(re_nameEnd),
	    name = idx < 0 ? value : value.substr(0, idx);

	if(this._lowerCaseTagNames){
		name = name.toLowerCase();
	}

	return name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype._updatePosition"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>_updatePosition (initialOffset)](#apidoc.element.htmlparser2.Parser.prototype._updatePosition)
- description and source-code
```javascript
_updatePosition = function (initialOffset){
	if(this.endIndex === null){
		if(this._tokenizer._sectionStart <= initialOffset){
			this.startIndex = 0;
		} else {
			this.startIndex = this._tokenizer._sectionStart - initialOffset;
		}
	}
	else this.startIndex = this.endIndex + 1;
	this.endIndex = this._tokenizer.getAbsoluteIndex();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.done"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>done (chunk)](#apidoc.element.htmlparser2.Parser.prototype.done)
- description and source-code
```javascript
done = function (chunk){
	this._tokenizer.end(chunk);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.end"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>end (chunk)](#apidoc.element.htmlparser2.Parser.prototype.end)
- description and source-code
```javascript
end = function (chunk){
	this._tokenizer.end(chunk);
}
```
- example usage
```shell
...
	onclosetag: function(tagname){
		if(tagname === "script"){
			console.log("That's it?!");
		}
	}
}, {decodeEntities: true});
parser.write("Xyz <script type='text/javascript'>var foo = '<<bar>>';</ script>");
parser.end();
'''

Output (simplified):

'''
--> Xyz
JS! Hooray!
...
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onattribdata"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onattribdata (value)](#apidoc.element.htmlparser2.Parser.prototype.onattribdata)
- description and source-code
```javascript
onattribdata = function (value){
	this._attribvalue += value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onattribend"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onattribend ()](#apidoc.element.htmlparser2.Parser.prototype.onattribend)
- description and source-code
```javascript
onattribend = function (){
	if(this._cbs.onattribute) this._cbs.onattribute(this._attribname, this._attribvalue);
	if(
		this._attribs &&
		!Object.prototype.hasOwnProperty.call(this._attribs, this._attribname)
	){
		this._attribs[this._attribname] = this._attribvalue;
	}
	this._attribname = "";
	this._attribvalue = "";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onattribname"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onattribname (name)](#apidoc.element.htmlparser2.Parser.prototype.onattribname)
- description and source-code
```javascript
onattribname = function (name){
	if(this._lowerCaseAttributeNames){
		name = name.toLowerCase();
	}
	this._attribname = name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.oncdata"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>oncdata (value)](#apidoc.element.htmlparser2.Parser.prototype.oncdata)
- description and source-code
```javascript
oncdata = function (value){
	this._updatePosition(1);

	if(this._options.xmlMode || this._options.recognizeCDATA){
		if(this._cbs.oncdatastart) this._cbs.oncdatastart();
		if(this._cbs.ontext) this._cbs.ontext(value);
		if(this._cbs.oncdataend) this._cbs.oncdataend();
	} else {
		this.oncomment("[CDATA[" + value + "]]");
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onclosetag"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onclosetag (name)](#apidoc.element.htmlparser2.Parser.prototype.onclosetag)
- description and source-code
```javascript
onclosetag = function (name){
	this._updatePosition(1);

	if(this._lowerCaseTagNames){
		name = name.toLowerCase();
	}

	if(this._stack.length && (!(name in voidElements) || this._options.xmlMode)){
		var pos = this._stack.lastIndexOf(name);
		if(pos !== -1){
			if(this._cbs.onclosetag){
				pos = this._stack.length - pos;
				while(pos--) this._cbs.onclosetag(this._stack.pop());
			}
			else this._stack.length = pos;
		} else if(name === "p" && !this._options.xmlMode){
			this.onopentagname(name);
			this._closeCurrentTag();
		}
	} else if(!this._options.xmlMode && (name === "br" || name === "p")){
		this.onopentagname(name);
		this._closeCurrentTag();
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.oncomment"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>oncomment (value)](#apidoc.element.htmlparser2.Parser.prototype.oncomment)
- description and source-code
```javascript
oncomment = function (value){
	this._updatePosition(4);

	if(this._cbs.oncomment) this._cbs.oncomment(value);
	if(this._cbs.oncommentend) this._cbs.oncommentend();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.ondeclaration"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>ondeclaration (value)](#apidoc.element.htmlparser2.Parser.prototype.ondeclaration)
- description and source-code
```javascript
ondeclaration = function (value){
	if(this._cbs.onprocessinginstruction){
		var name = this._getInstructionName(value);
		this._cbs.onprocessinginstruction("!" + name, "!" + value);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onend"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onend ()](#apidoc.element.htmlparser2.Parser.prototype.onend)
- description and source-code
```javascript
onend = function (){
	if(this._cbs.onclosetag){
		for(
			var i = this._stack.length;
			i > 0;
			this._cbs.onclosetag(this._stack[--i])
		);
	}
	if(this._cbs.onend) this._cbs.onend();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onerror"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onerror (err)](#apidoc.element.htmlparser2.Parser.prototype.onerror)
- description and source-code
```javascript
onerror = function (err){
	if(this._cbs.onerror) this._cbs.onerror(err);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onopentagend"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onopentagend ()](#apidoc.element.htmlparser2.Parser.prototype.onopentagend)
- description and source-code
```javascript
onopentagend = function (){
	this._updatePosition(1);

	if(this._attribs){
		if(this._cbs.onopentag) this._cbs.onopentag(this._tagname, this._attribs);
		this._attribs = null;
	}

	if(!this._options.xmlMode && this._cbs.onclosetag && this._tagname in voidElements){
		this._cbs.onclosetag(this._tagname);
	}

	this._tagname = "";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onopentagname"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onopentagname (name)](#apidoc.element.htmlparser2.Parser.prototype.onopentagname)
- description and source-code
```javascript
onopentagname = function (name){
	if(this._lowerCaseTagNames){
		name = name.toLowerCase();
	}

	this._tagname = name;

	if(!this._options.xmlMode && name in openImpliesClose) {
		for(
			var el;
			(el = this._stack[this._stack.length - 1]) in openImpliesClose[name];
			this.onclosetag(el)
		);
	}

	if(this._options.xmlMode || !(name in voidElements)){
		this._stack.push(name);
	}

	if(this._cbs.onopentagname) this._cbs.onopentagname(name);
	if(this._cbs.onopentag) this._attribs = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onprocessinginstruction"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onprocessinginstruction (value)](#apidoc.element.htmlparser2.Parser.prototype.onprocessinginstruction)
- description and source-code
```javascript
onprocessinginstruction = function (value){
	if(this._cbs.onprocessinginstruction){
		var name = this._getInstructionName(value);
		this._cbs.onprocessinginstruction("?" + name, "?" + value);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.onselfclosingtag"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>onselfclosingtag ()](#apidoc.element.htmlparser2.Parser.prototype.onselfclosingtag)
- description and source-code
```javascript
onselfclosingtag = function (){
	if(this._options.xmlMode || this._options.recognizeSelfClosing){
		this._closeCurrentTag();
	} else {
		this.onopentagend();
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.ontext"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>ontext (data)](#apidoc.element.htmlparser2.Parser.prototype.ontext)
- description and source-code
```javascript
ontext = function (data){
	this._updatePosition(1);
	this.endIndex--;

	if(this._cbs.ontext) this._cbs.ontext(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.parseChunk"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>parseChunk (chunk)](#apidoc.element.htmlparser2.Parser.prototype.parseChunk)
- description and source-code
```javascript
parseChunk = function (chunk){
	this._tokenizer.write(chunk);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.parseComplete"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>parseComplete (data)](#apidoc.element.htmlparser2.Parser.prototype.parseComplete)
- description and source-code
```javascript
parseComplete = function (data){
	this.reset();
	this.end(data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.pause"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>pause ()](#apidoc.element.htmlparser2.Parser.prototype.pause)
- description and source-code
```javascript
pause = function (){
	this._tokenizer.pause();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.reset"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>reset ()](#apidoc.element.htmlparser2.Parser.prototype.reset)
- description and source-code
```javascript
reset = function (){
	if(this._cbs.onreset) this._cbs.onreset();
	this._tokenizer.reset();

	this._tagname = "";
	this._attribname = "";
	this._attribs = null;
	this._stack = [];

	if(this._cbs.onparserinit) this._cbs.onparserinit(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.resume"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>resume ()](#apidoc.element.htmlparser2.Parser.prototype.resume)
- description and source-code
```javascript
resume = function (){
	this._tokenizer.resume();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Parser.prototype.write"></a>[function <span class="apidocSignatureSpan">htmlparser2.Parser.prototype.</span>write (chunk)](#apidoc.element.htmlparser2.Parser.prototype.write)
- description and source-code
```javascript
write = function (chunk){
	this._tokenizer.write(chunk);
}
```
- example usage
```shell
...
	},
	onclosetag: function(tagname){
		if(tagname === "script"){
			console.log("That's it?!");
		}
	}
}, {decodeEntities: true});
parser.write("Xyz <script type='text/javascript'>var foo = '<<bar>>';</ script>");
parser.end();
'''

Output (simplified):

'''
--> Xyz
...
```



# <a name="apidoc.module.htmlparser2.ProxyHandler"></a>[module htmlparser2.ProxyHandler](#apidoc.module.htmlparser2.ProxyHandler)

#### <a name="apidoc.element.htmlparser2.ProxyHandler.ProxyHandler"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>ProxyHandler (cbs)](#apidoc.element.htmlparser2.ProxyHandler.ProxyHandler)
- description and source-code
```javascript
function ProxyHandler(cbs){
	this._cbs = cbs || {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.ProxyHandler.prototype"></a>[module htmlparser2.ProxyHandler.prototype](#apidoc.module.htmlparser2.ProxyHandler.prototype)

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.onattribute"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onattribute (a, b)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onattribute)
- description and source-code
```javascript
onattribute = function (a, b){
			if(this._cbs[name]) this._cbs[name](a, b);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.oncdataend"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncdataend ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncdataend)
- description and source-code
```javascript
oncdataend = function (){
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.oncdatastart"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncdatastart ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncdatastart)
- description and source-code
```javascript
oncdatastart = function (){
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.onclosetag"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onclosetag (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onclosetag)
- description and source-code
```javascript
onclosetag = function (a){
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.oncomment"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncomment (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncomment)
- description and source-code
```javascript
oncomment = function (a){
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.oncommentend"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>oncommentend ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.oncommentend)
- description and source-code
```javascript
oncommentend = function (){
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.onend"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onend ()](#apidoc.element.htmlparser2.ProxyHandler.prototype.onend)
- description and source-code
```javascript
onend = function (){
			if(this._cbs[name]) this._cbs[name]();
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.onerror"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onerror (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onerror)
- description and source-code
```javascript
onerror = function (a){
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.onopentag"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onopentag (a, b)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onopentag)
- description and source-code
```javascript
onopentag = function (a, b){
			if(this._cbs[name]) this._cbs[name](a, b);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.onopentagname"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onopentagname (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onopentagname)
- description and source-code
```javascript
onopentagname = function (a){
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.onprocessinginstruction"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>onprocessinginstruction (a, b)](#apidoc.element.htmlparser2.ProxyHandler.prototype.onprocessinginstruction)
- description and source-code
```javascript
onprocessinginstruction = function (a, b){
			if(this._cbs[name]) this._cbs[name](a, b);
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.ProxyHandler.prototype.ontext"></a>[function <span class="apidocSignatureSpan">htmlparser2.ProxyHandler.prototype.</span>ontext (a)](#apidoc.element.htmlparser2.ProxyHandler.prototype.ontext)
- description and source-code
```javascript
ontext = function (a){
			if(this._cbs[name]) this._cbs[name](a);
		}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.Stream"></a>[module htmlparser2.Stream](#apidoc.module.htmlparser2.Stream)

#### <a name="apidoc.element.htmlparser2.Stream.Stream"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>Stream (options)](#apidoc.element.htmlparser2.Stream.Stream)
- description and source-code
```javascript
function Stream(options){
	Parser.call(this, new Cbs(this), options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Stream.super_"></a>[function <span class="apidocSignatureSpan">htmlparser2.Stream.</span>super_ (cbs, options)](#apidoc.element.htmlparser2.Stream.super_)
- description and source-code
```javascript
function Stream(cbs, options){
	var parser = this._parser = new Parser(cbs, options);
	var decoder = this._decoder = new StringDecoder();

	WritableStream.call(this, {decodeStrings: false});

	this.once("finish", function(){
		parser.end(decoder.end());
	});
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.Tokenizer"></a>[module htmlparser2.Tokenizer](#apidoc.module.htmlparser2.Tokenizer)

#### <a name="apidoc.element.htmlparser2.Tokenizer.Tokenizer"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>Tokenizer (options, cbs)](#apidoc.element.htmlparser2.Tokenizer.Tokenizer)
- description and source-code
```javascript
function Tokenizer(options, cbs){
	this._state = TEXT;
	this._buffer = "";
	this._sectionStart = 0;
	this._index = 0;
	this._bufferOffset = 0; //chars removed from _buffer
	this._baseState = TEXT;
	this._special = SPECIAL_NONE;
	this._cbs = cbs;
	this._running = true;
	this._ended = false;
	this._xmlMode = !!(options && options.xmlMode);
	this._decodeEntities = !!(options && options.decodeEntities);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.htmlparser2.Tokenizer.prototype"></a>[module htmlparser2.Tokenizer.prototype](#apidoc.module.htmlparser2.Tokenizer.prototype)

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._cleanup"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_cleanup ()](#apidoc.element.htmlparser2.Tokenizer.prototype._cleanup)
- description and source-code
```javascript
_cleanup = function (){
	if(this._sectionStart < 0){
		this._buffer = "";
		this._bufferOffset += this._index;
		this._index = 0;
	} else if(this._running){
		if(this._state === TEXT){
			if(this._sectionStart !== this._index){
				this._cbs.ontext(this._buffer.substr(this._sectionStart));
			}
			this._buffer = "";
			this._bufferOffset += this._index;
			this._index = 0;
		} else if(this._sectionStart === this._index){
			//the section just started
			this._buffer = "";
			this._bufferOffset += this._index;
			this._index = 0;
		} else {
			//remove everything unnecessary
			this._buffer = this._buffer.substr(this._sectionStart);
			this._index -= this._sectionStart;
			this._bufferOffset += this._sectionStart;
		}

		this._sectionStart = 0;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._decodeNumericEntity"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_decodeNumericEntity (offset, base)](#apidoc.element.htmlparser2.Tokenizer.prototype._decodeNumericEntity)
- description and source-code
```javascript
_decodeNumericEntity = function (offset, base){
	var sectionStart = this._sectionStart + offset;

	if(sectionStart !== this._index){
		//parse entity
		var entity = this._buffer.substring(sectionStart, this._index);
		var parsed = parseInt(entity, base);

		this._emitPartial(decodeCodePoint(parsed));
		this._sectionStart = this._index;
	} else {
		this._sectionStart--;
	}

	this._state = this._baseState;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._emitPartial"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_emitPartial (value)](#apidoc.element.htmlparser2.Tokenizer.prototype._emitPartial)
- description and source-code
```javascript
_emitPartial = function (value){
	if(this._baseState !== TEXT){
		this._cbs.onattribdata(value); //TODO implement the new event
	} else {
		this._cbs.ontext(value);
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._emitToken"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_emitToken (name)](#apidoc.element.htmlparser2.Tokenizer.prototype._emitToken)
- description and source-code
```javascript
_emitToken = function (name){
	this._cbs[name](this._getSection());
	this._sectionStart = -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._finish"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_finish ()](#apidoc.element.htmlparser2.Tokenizer.prototype._finish)
- description and source-code
```javascript
_finish = function (){
	//if there is remaining data, emit it in a reasonable way
	if(this._sectionStart < this._index){
		this._handleTrailingData();
	}

	this._cbs.onend();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._getSection"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_getSection ()](#apidoc.element.htmlparser2.Tokenizer.prototype._getSection)
- description and source-code
```javascript
_getSection = function (){
	return this._buffer.substring(this._sectionStart, this._index);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._handleTrailingData"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_handleTrailingData ()](#apidoc.element.htmlparser2.Tokenizer.prototype._handleTrailingData)
- description and source-code
```javascript
_handleTrailingData = function (){
	var data = this._buffer.substr(this._sectionStart);

	if(this._state === IN_CDATA || this._state === AFTER_CDATA_1 || this._state === AFTER_CDATA_2){
		this._cbs.oncdata(data);
	} else if(this._state === IN_COMMENT || this._state === AFTER_COMMENT_1 || this._state === AFTER_COMMENT_2){
		this._cbs.oncomment(data);
	} else if(this._state === IN_NAMED_ENTITY && !this._xmlMode){
		this._parseLegacyEntity();
		if(this._sectionStart < this._index){
			this._state = this._baseState;
			this._handleTrailingData();
		}
	} else if(this._state === IN_NUMERIC_ENTITY && !this._xmlMode){
		this._decodeNumericEntity(2, 10);
		if(this._sectionStart < this._index){
			this._state = this._baseState;
			this._handleTrailingData();
		}
	} else if(this._state === IN_HEX_ENTITY && !this._xmlMode){
		this._decodeNumericEntity(3, 16);
		if(this._sectionStart < this._index){
			this._state = this._baseState;
			this._handleTrailingData();
		}
	} else if(
		this._state !== IN_TAG_NAME &&
		this._state !== BEFORE_ATTRIBUTE_NAME &&
		this._state !== BEFORE_ATTRIBUTE_VALUE &&
		this._state !== AFTER_ATTRIBUTE_NAME &&
		this._state !== IN_ATTRIBUTE_NAME &&
		this._state !== IN_ATTRIBUTE_VALUE_SQ &&
		this._state !== IN_ATTRIBUTE_VALUE_DQ &&
		this._state !== IN_ATTRIBUTE_VALUE_NQ &&
		this._state !== IN_CLOSING_TAG_NAME
	){
		this._cbs.ontext(data);
	}
	//else, ignore remaining data
	//TODO add a way to remove current tag
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._parse"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_parse ()](#apidoc.element.htmlparser2.Tokenizer.prototype._parse)
- description and source-code
```javascript
_parse = function (){
	while(this._index < this._buffer.length && this._running){
		var c = this._buffer.charAt(this._index);
		if(this._state === TEXT) {
			this._stateText(c);
		} else if(this._state === BEFORE_TAG_NAME){
			this._stateBeforeTagName(c);
		} else if(this._state === IN_TAG_NAME) {
			this._stateInTagName(c);
		} else if(this._state === BEFORE_CLOSING_TAG_NAME){
			this._stateBeforeCloseingTagName(c);
		} else if(this._state === IN_CLOSING_TAG_NAME){
			this._stateInCloseingTagName(c);
		} else if(this._state === AFTER_CLOSING_TAG_NAME){
			this._stateAfterCloseingTagName(c);
		} else if(this._state === IN_SELF_CLOSING_TAG){
			this._stateInSelfClosingTag(c);
		}

		<span class="apidocCodeCommentSpan">/*
		*	attributes
		*/
</span>		else if(this._state === BEFORE_ATTRIBUTE_NAME){
			this._stateBeforeAttributeName(c);
		} else if(this._state === IN_ATTRIBUTE_NAME){
			this._stateInAttributeName(c);
		} else if(this._state === AFTER_ATTRIBUTE_NAME){
			this._stateAfterAttributeName(c);
		} else if(this._state === BEFORE_ATTRIBUTE_VALUE){
			this._stateBeforeAttributeValue(c);
		} else if(this._state === IN_ATTRIBUTE_VALUE_DQ){
			this._stateInAttributeValueDoubleQuotes(c);
		} else if(this._state === IN_ATTRIBUTE_VALUE_SQ){
			this._stateInAttributeValueSingleQuotes(c);
		} else if(this._state === IN_ATTRIBUTE_VALUE_NQ){
			this._stateInAttributeValueNoQuotes(c);
		}

		/*
		*	declarations
		*/
		else if(this._state === BEFORE_DECLARATION){
			this._stateBeforeDeclaration(c);
		} else if(this._state === IN_DECLARATION){
			this._stateInDeclaration(c);
		}

		/*
		*	processing instructions
		*/
		else if(this._state === IN_PROCESSING_INSTRUCTION){
			this._stateInProcessingInstruction(c);
		}

		/*
		*	comments
		*/
		else if(this._state === BEFORE_COMMENT){
			this._stateBeforeComment(c);
		} else if(this._state === IN_COMMENT){
			this._stateInComment(c);
		} else if(this._state === AFTER_COMMENT_1){
			this._stateAfterComment1(c);
		} else if(this._state === AFTER_COMMENT_2){
			this._stateAfterComment2(c);
		}

		/*
		*	cdata
		*/
		else if(this._state === BEFORE_CDATA_1){
			this._stateBeforeCdata1(c);
		} else if(this._state === BEFORE_CDATA_2){
			this._stateBeforeCdata2(c);
		} else if(this._state === BEFORE_CDATA_3){
			this._stateBeforeCdata3(c);
		} else if(this._state === BEFORE_CDATA_4){
			this._stateBeforeCdata4(c);
		} else if(this._state === BEFORE_CDATA_5){
			this._stateBeforeCdata5(c);
		} else if(this._state === BEFORE_CDATA_6){
			this._stateBeforeCdata6(c);
		} else if(this._state === IN_CDATA){
			this._stateInCdata(c);
		} else if(this._state === AFTER_CDATA_1){
			this._stateAfterCdata1(c);
		} else if(this._state === AFTER_CDATA_2){
			this._stateAfterCdata2(c);
		}

		/*
		* special tags
		*/
		else if(this._state === BEFORE_SPECIAL){
			this._stateBeforeSpecial(c);
		} else if(this._state === BEFORE_SPECIAL_END){
			this._stateBeforeSpecialEnd(c);
		}

		/*
		* script
		*/
		else if(this._state === BEFORE_SCRIPT_1){
			this._stateBeforeScript1(c);
		} else if(this._state === BEFORE_SCRIPT_2){
			this._stateBeforeScript2(c);
		} else if(this._state === BEFORE_SCRIPT_3){
			this._stateBeforeScript3(c);
		} else if(this._state === BEFORE_SCRIPT_4){
			this._stateBeforeScript4(c);
		} else if(this._state === BEFORE_SCRIPT_5){
			this._stateBeforeScript5(c);
		}

		else if(this._state === AFTER_SCRIPT_1){
			this._stateAfterScript1(c);
		} else if(this._state === AFTER_SCRIPT_2){
			this._stateAfterScript2(c);
		} else if(this._state === AFTER_SCRIPT_3){
			this._stateAfterScript3(c);
		} else if(this._state === AFTER_SCRIPT_4){
			this._stateAfterScript4(c);
		} else if(this._state === AFTER_SCRIPT_5){
			this._stateAfterScript5(c);
		}

		/*
		* style
		*/
		else if(this._state === BEFORE_STYLE_1){
			this._stateBeforeStyle1(c);
		} else if(this._state === BEFORE_STYLE_2){
			this._stateBeforeStyle2(c);
		} else if(this._state === BEFORE_STYLE_3){
			this._stateBeforeStyle3(c);
		} else if(this._state === BEFORE_STYLE_4){
			this._stateBeforeStyle4(c);
		}

		else if(this._state === AFTER_STYLE_1){
			this._stateAfterStyle1(c);
		} e ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._parseLegacyEntity"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_parseLegacyEntity ()](#apidoc.element.htmlparser2.Tokenizer.prototype._parseLegacyEntity)
- description and source-code
```javascript
_parseLegacyEntity = function (){
	var start = this._sectionStart + 1,
	    limit = this._index - start;

	if(limit > 6) limit = 6; //the max length of legacy entities is 6

	while(limit >= 2){ //the min length of legacy entities is 2
		var entity = this._buffer.substr(start, limit);

		if(legacyMap.hasOwnProperty(entity)){
			this._emitPartial(legacyMap[entity]);
			this._sectionStart += limit + 1;
			return;
		} else {
			limit--;
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._parseNamedEntityStrict"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_parseNamedEntityStrict ()](#apidoc.element.htmlparser2.Tokenizer.prototype._parseNamedEntityStrict)
- description and source-code
```javascript
_parseNamedEntityStrict = function (){
	//offset = 1
	if(this._sectionStart + 1 < this._index){
		var entity = this._buffer.substring(this._sectionStart + 1, this._index),
		    map = this._xmlMode ? xmlMap : entityMap;

		if(map.hasOwnProperty(entity)){
			this._emitPartial(map[entity]);
			this._sectionStart = this._index + 1;
		}
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterAttributeName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterAttributeName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterAttributeName)
- description and source-code
```javascript
_stateAfterAttributeName = function (c){
	if(c === "="){
		this._state = BEFORE_ATTRIBUTE_VALUE;
	} else if(c === "/" || c === ">"){
		this._cbs.onattribend();
		this._state = BEFORE_ATTRIBUTE_NAME;
		this._index--;
	} else if(!whitespace(c)){
		this._cbs.onattribend();
		this._state = IN_ATTRIBUTE_NAME;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCdata1"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterCdata1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCdata1)
- description and source-code
```javascript
_stateAfterCdata1 = function (c){
		if(c === char) this._state = SUCCESS;
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCdata2"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterCdata2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCdata2)
- description and source-code
```javascript
_stateAfterCdata2 = function (c){
	if(c === ">"){
		//remove 2 trailing chars
		this._cbs.oncdata(this._buffer.substring(this._sectionStart, this._index - 2));
		this._state = TEXT;
		this._sectionStart = this._index + 1;
	} else if(c !== "]") {
		this._state = IN_CDATA;
	}
	//else: stay in AFTER_CDATA_2 (']]]>')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCloseingTagName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterCloseingTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterCloseingTagName)
- description and source-code
```javascript
_stateAfterCloseingTagName = function (c){
	//skip everything until ">"
	if(c === ">"){
		this._state = TEXT;
		this._sectionStart = this._index + 1;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterComment1"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterComment1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterComment1)
- description and source-code
```javascript
_stateAfterComment1 = function (c){
	if(c === "-"){
		this._state = AFTER_COMMENT_2;
	} else {
		this._state = IN_COMMENT;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterComment2"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterComment2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterComment2)
- description and source-code
```javascript
_stateAfterComment2 = function (c){
	if(c === ">"){
		//remove 2 trailing chars
		this._cbs.oncomment(this._buffer.substring(this._sectionStart, this._index - 2));
		this._state = TEXT;
		this._sectionStart = this._index + 1;
	} else if(c !== "-"){
		this._state = IN_COMMENT;
	}
	// else: stay in AFTER_COMMENT_2 ('--->')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript1"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript1)
- description and source-code
```javascript
_stateAfterScript1 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript2"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript2)
- description and source-code
```javascript
_stateAfterScript2 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript3"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript3)
- description and source-code
```javascript
_stateAfterScript3 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript4"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript4)
- description and source-code
```javascript
_stateAfterScript4 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript5"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterScript5 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterScript5)
- description and source-code
```javascript
_stateAfterScript5 = function (c){
	if(c === ">" || whitespace(c)){
		this._special = SPECIAL_NONE;
		this._state = IN_CLOSING_TAG_NAME;
		this._sectionStart = this._index - 6;
		this._index--; //reconsume the token
	}
	else this._state = TEXT;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle1"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle1)
- description and source-code
```javascript
_stateAfterStyle1 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle2"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle2)
- description and source-code
```javascript
_stateAfterStyle2 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle3"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle3)
- description and source-code
```javascript
_stateAfterStyle3 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle4"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateAfterStyle4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateAfterStyle4)
- description and source-code
```javascript
_stateAfterStyle4 = function (c){
	if(c === ">" || whitespace(c)){
		this._special = SPECIAL_NONE;
		this._state = IN_CLOSING_TAG_NAME;
		this._sectionStart = this._index - 5;
		this._index--; //reconsume the token
	}
	else this._state = TEXT;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeAttributeName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeAttributeName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeAttributeName)
- description and source-code
```javascript
_stateBeforeAttributeName = function (c){
	if(c === ">"){
		this._cbs.onopentagend();
		this._state = TEXT;
		this._sectionStart = this._index + 1;
	} else if(c === "/"){
		this._state = IN_SELF_CLOSING_TAG;
	} else if(!whitespace(c)){
		this._state = IN_ATTRIBUTE_NAME;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeAttributeValue"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeAttributeValue (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeAttributeValue)
- description and source-code
```javascript
_stateBeforeAttributeValue = function (c){
	if(c === "\""){
		this._state = IN_ATTRIBUTE_VALUE_DQ;
		this._sectionStart = this._index + 1;
	} else if(c === "'"){
		this._state = IN_ATTRIBUTE_VALUE_SQ;
		this._sectionStart = this._index + 1;
	} else if(!whitespace(c)){
		this._state = IN_ATTRIBUTE_VALUE_NQ;
		this._sectionStart = this._index;
		this._index--; //reconsume token
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata1"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata1)
- description and source-code
```javascript
_stateBeforeCdata1 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata2"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata2)
- description and source-code
```javascript
_stateBeforeCdata2 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata3"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata3)
- description and source-code
```javascript
_stateBeforeCdata3 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata4"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata4)
- description and source-code
```javascript
_stateBeforeCdata4 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata5"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata5 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata5)
- description and source-code
```javascript
_stateBeforeCdata5 = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata6"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCdata6 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCdata6)
- description and source-code
```javascript
_stateBeforeCdata6 = function (c){
	if(c === "["){
		this._state = IN_CDATA;
		this._sectionStart = this._index + 1;
	} else {
		this._state = IN_DECLARATION;
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCloseingTagName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeCloseingTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeCloseingTagName)
- description and source-code
```javascript
_stateBeforeCloseingTagName = function (c){
	if(whitespace(c));
	else if(c === ">"){
		this._state = TEXT;
	} else if(this._special !== SPECIAL_NONE){
		if(c === "s" || c === "S"){
			this._state = BEFORE_SPECIAL_END;
		} else {
			this._state = TEXT;
			this._index--;
		}
	} else {
		this._state = IN_CLOSING_TAG_NAME;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeComment"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeComment (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeComment)
- description and source-code
```javascript
_stateBeforeComment = function (c){
	if(c === "-"){
		this._state = IN_COMMENT;
		this._sectionStart = this._index + 1;
	} else {
		this._state = IN_DECLARATION;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeDeclaration"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeDeclaration (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeDeclaration)
- description and source-code
```javascript
_stateBeforeDeclaration = function (c){
	this._state = c === "[" ? BEFORE_CDATA_1 :
					c === "-" ? BEFORE_COMMENT :
						IN_DECLARATION;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeEntity"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeEntity)
- description and source-code
```javascript
_stateBeforeEntity = function (c){
			if(c === lower){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeNumericEntity"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeNumericEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeNumericEntity)
- description and source-code
```javascript
_stateBeforeNumericEntity = function (c){
			if(c === lower || c === upper){
				this._state = SUCCESS;
			} else {
				this._state = FAILURE;
				this._index--;
			}
		}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript1"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript1)
- description and source-code
```javascript
_stateBeforeScript1 = function (c){
		if(c === lower || c === upper){
			this._state = NEXT_STATE;
		} else {
			this._state = IN_TAG_NAME;
			this._index--; //consume the token again
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript2"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript2)
- description and source-code
```javascript
_stateBeforeScript2 = function (c){
		if(c === lower || c === upper){
			this._state = NEXT_STATE;
		} else {
			this._state = IN_TAG_NAME;
			this._index--; //consume the token again
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript3"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript3)
- description and source-code
```javascript
_stateBeforeScript3 = function (c){
		if(c === lower || c === upper){
			this._state = NEXT_STATE;
		} else {
			this._state = IN_TAG_NAME;
			this._index--; //consume the token again
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript4"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript4)
- description and source-code
```javascript
_stateBeforeScript4 = function (c){
		if(c === lower || c === upper){
			this._state = NEXT_STATE;
		} else {
			this._state = IN_TAG_NAME;
			this._index--; //consume the token again
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript5"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeScript5 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeScript5)
- description and source-code
```javascript
_stateBeforeScript5 = function (c){
	if(c === "/" || c === ">" || whitespace(c)){
		this._special = SPECIAL_SCRIPT;
	}
	this._state = IN_TAG_NAME;
	this._index--; //consume the token again
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeSpecial"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeSpecial (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeSpecial)
- description and source-code
```javascript
_stateBeforeSpecial = function (c){
	if(c === "c" || c === "C"){
		this._state = BEFORE_SCRIPT_1;
	} else if(c === "t" || c === "T"){
		this._state = BEFORE_STYLE_1;
	} else {
		this._state = IN_TAG_NAME;
		this._index--; //consume the token again
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeSpecialEnd"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeSpecialEnd (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeSpecialEnd)
- description and source-code
```javascript
_stateBeforeSpecialEnd = function (c){
	if(this._special === SPECIAL_SCRIPT && (c === "c" || c === "C")){
		this._state = AFTER_SCRIPT_1;
	} else if(this._special === SPECIAL_STYLE && (c === "t" || c === "T")){
		this._state = AFTER_STYLE_1;
	}
	else this._state = TEXT;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle1"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle1 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle1)
- description and source-code
```javascript
_stateBeforeStyle1 = function (c){
		if(c === lower || c === upper){
			this._state = NEXT_STATE;
		} else {
			this._state = IN_TAG_NAME;
			this._index--; //consume the token again
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle2"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle2 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle2)
- description and source-code
```javascript
_stateBeforeStyle2 = function (c){
		if(c === lower || c === upper){
			this._state = NEXT_STATE;
		} else {
			this._state = IN_TAG_NAME;
			this._index--; //consume the token again
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle3"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle3 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle3)
- description and source-code
```javascript
_stateBeforeStyle3 = function (c){
		if(c === lower || c === upper){
			this._state = NEXT_STATE;
		} else {
			this._state = IN_TAG_NAME;
			this._index--; //consume the token again
		}
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle4"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeStyle4 (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeStyle4)
- description and source-code
```javascript
_stateBeforeStyle4 = function (c){
	if(c === "/" || c === ">" || whitespace(c)){
		this._special = SPECIAL_STYLE;
	}
	this._state = IN_TAG_NAME;
	this._index--; //consume the token again
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeTagName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateBeforeTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateBeforeTagName)
- description and source-code
```javascript
_stateBeforeTagName = function (c){
	if(c === "/"){
		this._state = BEFORE_CLOSING_TAG_NAME;
	} else if(c === "<"){
		this._cbs.ontext(this._getSection());
		this._sectionStart = this._index;
	} else if(c === ">" || this._special !== SPECIAL_NONE || whitespace(c)) {
		this._state = TEXT;
	} else if(c === "!"){
		this._state = BEFORE_DECLARATION;
		this._sectionStart = this._index + 1;
	} else if(c === "?"){
		this._state = IN_PROCESSING_INSTRUCTION;
		this._sectionStart = this._index + 1;
	} else {
		this._state = (!this._xmlMode && (c === "s" || c === "S")) ?
						BEFORE_SPECIAL : IN_TAG_NAME;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeName)
- description and source-code
```javascript
_stateInAttributeName = function (c){
	if(c === "=" || c === "/" || c === ">" || whitespace(c)){
		this._cbs.onattribname(this._getSection());
		this._sectionStart = -1;
		this._state = AFTER_ATTRIBUTE_NAME;
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueDoubleQuotes"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeValueDoubleQuotes (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueDoubleQuotes)
- description and source-code
```javascript
_stateInAttributeValueDoubleQuotes = function (c){
	if(c === "\""){
		this._emitToken("onattribdata");
		this._cbs.onattribend();
		this._state = BEFORE_ATTRIBUTE_NAME;
	} else if(this._decodeEntities && c === "&"){
		this._emitToken("onattribdata");
		this._baseState = this._state;
		this._state = BEFORE_ENTITY;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueNoQuotes"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeValueNoQuotes (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueNoQuotes)
- description and source-code
```javascript
_stateInAttributeValueNoQuotes = function (c){
	if(whitespace(c) || c === ">"){
		this._emitToken("onattribdata");
		this._cbs.onattribend();
		this._state = BEFORE_ATTRIBUTE_NAME;
		this._index--;
	} else if(this._decodeEntities && c === "&"){
		this._emitToken("onattribdata");
		this._baseState = this._state;
		this._state = BEFORE_ENTITY;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueSingleQuotes"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInAttributeValueSingleQuotes (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInAttributeValueSingleQuotes)
- description and source-code
```javascript
_stateInAttributeValueSingleQuotes = function (c){
	if(c === "'"){
		this._emitToken("onattribdata");
		this._cbs.onattribend();
		this._state = BEFORE_ATTRIBUTE_NAME;
	} else if(this._decodeEntities && c === "&"){
		this._emitToken("onattribdata");
		this._baseState = this._state;
		this._state = BEFORE_ENTITY;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInCdata"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInCdata (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInCdata)
- description and source-code
```javascript
_stateInCdata = function (c){
	if(c === "]") this._state = AFTER_CDATA_1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInCloseingTagName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInCloseingTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInCloseingTagName)
- description and source-code
```javascript
_stateInCloseingTagName = function (c){
	if(c === ">" || whitespace(c)){
		this._emitToken("onclosetag");
		this._state = AFTER_CLOSING_TAG_NAME;
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInComment"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInComment (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInComment)
- description and source-code
```javascript
_stateInComment = function (c){
	if(c === "-") this._state = AFTER_COMMENT_1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInDeclaration"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInDeclaration (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInDeclaration)
- description and source-code
```javascript
_stateInDeclaration = function (c){
	if(c === ">"){
		this._cbs.ondeclaration(this._getSection());
		this._state = TEXT;
		this._sectionStart = this._index + 1;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInHexEntity"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInHexEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInHexEntity)
- description and source-code
```javascript
_stateInHexEntity = function (c){
	if(c === ";"){
		this._decodeNumericEntity(3, 16);
		this._sectionStart++;
	} else if((c < "a" || c > "f") && (c < "A" || c > "F") && (c < "0" || c > "9")){
		if(!this._xmlMode){
			this._decodeNumericEntity(3, 16);
		} else {
			this._state = this._baseState;
		}
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInNamedEntity"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInNamedEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInNamedEntity)
- description and source-code
```javascript
_stateInNamedEntity = function (c){
	if(c === ";"){
		this._parseNamedEntityStrict();
		if(this._sectionStart + 1 < this._index && !this._xmlMode){
			this._parseLegacyEntity();
		}
		this._state = this._baseState;
	} else if((c < "a" || c > "z") && (c < "A" || c > "Z") && (c < "0" || c > "9")){
		if(this._xmlMode);
		else if(this._sectionStart + 1 === this._index);
		else if(this._baseState !== TEXT){
			if(c !== "="){
				this._parseNamedEntityStrict();
			}
		} else {
			this._parseLegacyEntity();
		}

		this._state = this._baseState;
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInNumericEntity"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInNumericEntity (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInNumericEntity)
- description and source-code
```javascript
_stateInNumericEntity = function (c){
	if(c === ";"){
		this._decodeNumericEntity(2, 10);
		this._sectionStart++;
	} else if(c < "0" || c > "9"){
		if(!this._xmlMode){
			this._decodeNumericEntity(2, 10);
		} else {
			this._state = this._baseState;
		}
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInProcessingInstruction"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInProcessingInstruction (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInProcessingInstruction)
- description and source-code
```javascript
_stateInProcessingInstruction = function (c){
	if(c === ">"){
		this._cbs.onprocessinginstruction(this._getSection());
		this._state = TEXT;
		this._sectionStart = this._index + 1;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInSelfClosingTag"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInSelfClosingTag (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInSelfClosingTag)
- description and source-code
```javascript
_stateInSelfClosingTag = function (c){
	if(c === ">"){
		this._cbs.onselfclosingtag();
		this._state = TEXT;
		this._sectionStart = this._index + 1;
	} else if(!whitespace(c)){
		this._state = BEFORE_ATTRIBUTE_NAME;
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateInTagName"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateInTagName (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateInTagName)
- description and source-code
```javascript
_stateInTagName = function (c){
	if(c === "/" || c === ">" || whitespace(c)){
		this._emitToken("onopentagname");
		this._state = BEFORE_ATTRIBUTE_NAME;
		this._index--;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype._stateText"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>_stateText (c)](#apidoc.element.htmlparser2.Tokenizer.prototype._stateText)
- description and source-code
```javascript
_stateText = function (c){
	if(c === "<"){
		if(this._index > this._sectionStart){
			this._cbs.ontext(this._getSection());
		}
		this._state = BEFORE_TAG_NAME;
		this._sectionStart = this._index;
	} else if(this._decodeEntities && this._special === SPECIAL_NONE && c === "&"){
		if(this._index > this._sectionStart){
			this._cbs.ontext(this._getSection());
		}
		this._baseState = TEXT;
		this._state = BEFORE_ENTITY;
		this._sectionStart = this._index;
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype.end"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>end (chunk)](#apidoc.element.htmlparser2.Tokenizer.prototype.end)
- description and source-code
```javascript
end = function (chunk){
	if(this._ended) this._cbs.onerror(Error(".end() after done!"));
	if(chunk) this.write(chunk);

	this._ended = true;

	if(this._running) this._finish();
}
```
- example usage
```shell
...
	onclosetag: function(tagname){
		if(tagname === "script"){
			console.log("That's it?!");
		}
	}
}, {decodeEntities: true});
parser.write("Xyz <script type='text/javascript'>var foo = '<<bar>>';</ script>");
parser.end();
'''

Output (simplified):

'''
--> Xyz
JS! Hooray!
...
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype.getAbsoluteIndex"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>getAbsoluteIndex ()](#apidoc.element.htmlparser2.Tokenizer.prototype.getAbsoluteIndex)
- description and source-code
```javascript
getAbsoluteIndex = function (){
	return this._bufferOffset + this._index;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype.pause"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>pause ()](#apidoc.element.htmlparser2.Tokenizer.prototype.pause)
- description and source-code
```javascript
pause = function (){
	this._running = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype.reset"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>reset ()](#apidoc.element.htmlparser2.Tokenizer.prototype.reset)
- description and source-code
```javascript
reset = function (){
	Tokenizer.call(this, {xmlMode: this._xmlMode, decodeEntities: this._decodeEntities}, this._cbs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype.resume"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>resume ()](#apidoc.element.htmlparser2.Tokenizer.prototype.resume)
- description and source-code
```javascript
resume = function (){
	this._running = true;

	if(this._index < this._buffer.length){
		this._parse();
	}
	if(this._ended){
		this._finish();
	}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.Tokenizer.prototype.write"></a>[function <span class="apidocSignatureSpan">htmlparser2.Tokenizer.prototype.</span>write (chunk)](#apidoc.element.htmlparser2.Tokenizer.prototype.write)
- description and source-code
```javascript
write = function (chunk){
	if(this._ended) this._cbs.onerror(Error(".write() after done!"));

	this._buffer += chunk;
	this._parse();
}
```
- example usage
```shell
...
	},
	onclosetag: function(tagname){
		if(tagname === "script"){
			console.log("That's it?!");
		}
	}
}, {decodeEntities: true});
parser.write("Xyz <script type='text/javascript'>var foo = '<<bar>>';</ script>");
parser.end();
'''

Output (simplified):

'''
--> Xyz
...
```



# <a name="apidoc.module.htmlparser2.WritableStream"></a>[module htmlparser2.WritableStream](#apidoc.module.htmlparser2.WritableStream)

#### <a name="apidoc.element.htmlparser2.WritableStream.WritableStream"></a>[function <span class="apidocSignatureSpan">htmlparser2.</span>WritableStream (cbs, options)](#apidoc.element.htmlparser2.WritableStream.WritableStream)
- description and source-code
```javascript
function Stream(cbs, options){
	var parser = this._parser = new Parser(cbs, options);
	var decoder = this._decoder = new StringDecoder();

	WritableStream.call(this, {decodeStrings: false});

	this.once("finish", function(){
		parser.end(decoder.end());
	});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.htmlparser2.WritableStream.super_"></a>[function <span class="apidocSignatureSpan">htmlparser2.WritableStream.</span>super_ (options)](#apidoc.element.htmlparser2.WritableStream.super_)
- description and source-code
```javascript
function Writable(options) {
  // Writable ctor is applied to Duplexes, too.
  // 'realHasInstance' is necessary because using plain 'instanceof'
  // would return false, as no '_writableState' property is attached.

  // Trying to use the custom 'instanceof' for Writable here will also break the
  // Node.js LazyTransform implementation, which has a non-trivial getter for
  // '_writableState' that would lead to infinite recursion.
  if (!(realHasInstance.call(Writable, this)) &&
      !(this instanceof Stream.Duplex)) {
    return new Writable(options);
  }

  this._writableState = new WritableState(options, this);

  // legacy.
  this.writable = true;

  if (options) {
    if (typeof options.write === 'function')
      this._write = options.write;

    if (typeof options.writev === 'function')
      this._writev = options.writev;
  }

  Stream.call(this);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
