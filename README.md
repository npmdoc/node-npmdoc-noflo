# api documentation for  [noflo (v0.8.3)](http://noflojs.org/)  [![npm package](https://img.shields.io/npm/v/npmdoc-noflo.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-noflo) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-noflo.svg)](https://travis-ci.org/npmdoc/node-npmdoc-noflo)
#### Flow-Based Programming environment for JavaScript

[![NPM](https://nodei.co/npm/noflo.png?downloads=true)](https://www.npmjs.com/package/noflo)

[![apidoc](https://npmdoc.github.io/node-npmdoc-noflo/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-noflo_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-noflo/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-noflo/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-noflo/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Henri Bergius",
        "email": "henri.bergius@iki.fi"
    },
    "bin": {
        "noflo": "./bin/noflo",
        "noflo-cache-preheat": "./bin/noflo-cache-preheat"
    },
    "bugs": {
        "url": "https://github.com/noflo/noflo/issues"
    },
    "dependencies": {
        "coffee-script": "~1.12.0",
        "debug": "^2.5.2",
        "fbp": "~1.5.0",
        "fbp-graph": "^0.1.0",
        "fbp-manifest": "~0.1.13"
    },
    "description": "Flow-Based Programming environment for JavaScript",
    "devDependencies": {
        "chai": "^3.5.0",
        "coffee-loader": "^0.7.2",
        "fbp-loader": "^0.1.1",
        "grunt": "^1.0.1",
        "grunt-cli": "^1.2.0",
        "grunt-coffeelint": "^0.0.16",
        "grunt-contrib-coffee": "^1.0.0",
        "grunt-contrib-connect": "^1.0.1",
        "grunt-contrib-watch": "~1.0.0",
        "grunt-mocha-phantomjs": "^4.0.0",
        "grunt-mocha-test": "^0.13.2",
        "grunt-noflo-browser": "^1.1.4",
        "json-loader": "^0.5.4",
        "mocha": "^3.1.2"
    },
    "directories": {},
    "dist": {
        "shasum": "4237921da5159383ad1870701a9f005ef5fc0fe7",
        "tarball": "https://registry.npmjs.org/noflo/-/noflo-0.8.3.tgz"
    },
    "docco_husky": {
        "output_dir": "docs",
        "project_name": "NoFlo"
    },
    "engines": {
        "node": ">= 4"
    },
    "gitHead": "4be2f0c5cddcd6165640e4a656a2dd29ab6f40c5",
    "homepage": "http://noflojs.org/",
    "keywords": [
        "fbp",
        "workflow",
        "flow",
        "noflo"
    ],
    "license": "MIT",
    "main": "./lib/NoFlo",
    "maintainers": [
        {
            "name": "bergie",
            "email": "henri.bergius@iki.fi"
        }
    ],
    "name": "noflo",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/noflo/noflo.git"
    },
    "scripts": {
        "test": "grunt test"
    },
    "version": "0.8.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module noflo](#apidoc.module.noflo)
1.  [function <span class="apidocSignatureSpan">noflo.</span>ArrayPort (type)](#apidoc.element.noflo.ArrayPort)
1.  [function <span class="apidocSignatureSpan">noflo.</span>AsyncComponent (inPortName, outPortName, errPortName)](#apidoc.element.noflo.AsyncComponent)
1.  [function <span class="apidocSignatureSpan">noflo.</span>BasePort (options)](#apidoc.element.noflo.BasePort)
1.  [function <span class="apidocSignatureSpan">noflo.</span>Component (options)](#apidoc.element.noflo.Component)
1.  [function <span class="apidocSignatureSpan">noflo.</span>ComponentLoader (baseDir, options)](#apidoc.element.noflo.ComponentLoader)
1.  [function <span class="apidocSignatureSpan">noflo.</span>Graph (name1, options)](#apidoc.element.noflo.Graph)
1.  [function <span class="apidocSignatureSpan">noflo.</span>IP (type, data, options)](#apidoc.element.noflo.IP)
1.  [function <span class="apidocSignatureSpan">noflo.</span>InPort (options, process)](#apidoc.element.noflo.InPort)
1.  [function <span class="apidocSignatureSpan">noflo.</span>InPorts ()](#apidoc.element.noflo.InPorts)
1.  [function <span class="apidocSignatureSpan">noflo.</span>Journal (graph, metadata, store)](#apidoc.element.noflo.Journal)
1.  [function <span class="apidocSignatureSpan">noflo.</span>Network (graph, options)](#apidoc.element.noflo.Network)
1.  [function <span class="apidocSignatureSpan">noflo.</span>OutPort (options)](#apidoc.element.noflo.OutPort)
1.  [function <span class="apidocSignatureSpan">noflo.</span>OutPorts ()](#apidoc.element.noflo.OutPorts)
1.  [function <span class="apidocSignatureSpan">noflo.</span>Port (type)](#apidoc.element.noflo.Port)
1.  [function <span class="apidocSignatureSpan">noflo.</span>asCallback (component, options)](#apidoc.element.noflo.asCallback)
1.  [function <span class="apidocSignatureSpan">noflo.</span>createNetwork (graph, callback, options)](#apidoc.element.noflo.createNetwork)
1.  [function <span class="apidocSignatureSpan">noflo.</span>internalSocket.InternalSocket (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket)
1.  [function <span class="apidocSignatureSpan">noflo.</span>isBrowser ()](#apidoc.element.noflo.isBrowser)
1.  [function <span class="apidocSignatureSpan">noflo.</span>journal.JournalStore (graph1)](#apidoc.element.noflo.journal.JournalStore)
1.  [function <span class="apidocSignatureSpan">noflo.</span>journal.MemoryJournalStore (graph)](#apidoc.element.noflo.journal.MemoryJournalStore)
1.  [function <span class="apidocSignatureSpan">noflo.</span>loadFile (file, options, callback)](#apidoc.element.noflo.loadFile)
1.  [function <span class="apidocSignatureSpan">noflo.</span>saveFile (graph, file, callback)](#apidoc.element.noflo.saveFile)
1.  [function <span class="apidocSignatureSpan">noflo.</span>streams.IP (data1)](#apidoc.element.noflo.streams.IP)
1.  [function <span class="apidocSignatureSpan">noflo.</span>streams.StreamReceiver (port1, buffered, process)](#apidoc.element.noflo.streams.StreamReceiver)
1.  [function <span class="apidocSignatureSpan">noflo.</span>streams.StreamSender (port1, ordered)](#apidoc.element.noflo.streams.StreamSender)
1.  [function <span class="apidocSignatureSpan">noflo.</span>streams.Substream (key)](#apidoc.element.noflo.streams.Substream)
1.  object <span class="apidocSignatureSpan">noflo.</span>ArrayPort.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>AsCallback
1.  object <span class="apidocSignatureSpan">noflo.</span>AsyncComponent.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>Component.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>ComponentLoader.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>Graph.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>IP.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>InPort.__super__
1.  object <span class="apidocSignatureSpan">noflo.</span>InPort.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>InPorts.__super__
1.  object <span class="apidocSignatureSpan">noflo.</span>InPorts.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>Journal.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>Network.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>OutPort.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>OutPorts.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>Platform
1.  object <span class="apidocSignatureSpan">noflo.</span>Port.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>Ports
1.  object <span class="apidocSignatureSpan">noflo.</span>Utils
1.  object <span class="apidocSignatureSpan">noflo.</span>graph
1.  object <span class="apidocSignatureSpan">noflo.</span>helpers
1.  object <span class="apidocSignatureSpan">noflo.</span>internalSocket
1.  object <span class="apidocSignatureSpan">noflo.</span>internalSocket.InternalSocket.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>journal
1.  object <span class="apidocSignatureSpan">noflo.</span>journal.JournalStore.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>journal.MemoryJournalStore.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>streams
1.  object <span class="apidocSignatureSpan">noflo.</span>streams.IP.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>streams.StreamReceiver.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>streams.StreamSender.prototype
1.  object <span class="apidocSignatureSpan">noflo.</span>streams.Substream.prototype

#### [module noflo.ArrayPort](#apidoc.module.noflo.ArrayPort)
1.  boolean <span class="apidocSignatureSpan">noflo.ArrayPort.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>ArrayPort (type)](#apidoc.element.noflo.ArrayPort.ArrayPort)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.</span>EventEmitter ()](#apidoc.element.noflo.ArrayPort.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.</span>init ()](#apidoc.element.noflo.ArrayPort.init)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.ArrayPort.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.ArrayPort.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.ArrayPort.</span>__super__

#### [module noflo.ArrayPort.prototype](#apidoc.module.noflo.ArrayPort.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>attach (socket, socketId)](#apidoc.element.noflo.ArrayPort.prototype.attach)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>beginGroup (group, socketId)](#apidoc.element.noflo.ArrayPort.prototype.beginGroup)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>connect (socketId)](#apidoc.element.noflo.ArrayPort.prototype.connect)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>constructor (type)](#apidoc.element.noflo.ArrayPort.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>disconnect (socketId)](#apidoc.element.noflo.ArrayPort.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>endGroup (socketId)](#apidoc.element.noflo.ArrayPort.prototype.endGroup)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>isAddressable ()](#apidoc.element.noflo.ArrayPort.prototype.isAddressable)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>isAttached (socketId)](#apidoc.element.noflo.ArrayPort.prototype.isAttached)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>isConnected (socketId)](#apidoc.element.noflo.ArrayPort.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>send (data, socketId)](#apidoc.element.noflo.ArrayPort.prototype.send)

#### [module noflo.AsCallback](#apidoc.module.noflo.AsCallback)
1.  [function <span class="apidocSignatureSpan">noflo.AsCallback.</span>asCallback (component, options)](#apidoc.element.noflo.AsCallback.asCallback)

#### [module noflo.AsyncComponent](#apidoc.module.noflo.AsyncComponent)
1.  boolean <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>AsyncComponent (inPortName, outPortName, errPortName)](#apidoc.element.noflo.AsyncComponent.AsyncComponent)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>EventEmitter ()](#apidoc.element.noflo.AsyncComponent.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>init ()](#apidoc.element.noflo.AsyncComponent.init)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>listenerCount (emitter, type)](#apidoc.element.noflo.AsyncComponent.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>__super__

#### [module noflo.AsyncComponent.prototype](#apidoc.module.noflo.AsyncComponent.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>constructor (inPortName, outPortName, errPortName)](#apidoc.element.noflo.AsyncComponent.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>decrementLoad ()](#apidoc.element.noflo.AsyncComponent.prototype.decrementLoad)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>doAsync (data, callback)](#apidoc.element.noflo.AsyncComponent.prototype.doAsync)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>error (e, groups, errorPort)](#apidoc.element.noflo.AsyncComponent.prototype.error)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>incrementLoad ()](#apidoc.element.noflo.AsyncComponent.prototype.incrementLoad)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>processData (data)](#apidoc.element.noflo.AsyncComponent.prototype.processData)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>processQueue ()](#apidoc.element.noflo.AsyncComponent.prototype.processQueue)
1.  [function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>tearDown (callback)](#apidoc.element.noflo.AsyncComponent.prototype.tearDown)

#### [module noflo.BasePort](#apidoc.module.noflo.BasePort)
1.  boolean <span class="apidocSignatureSpan">noflo.BasePort.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>BasePort (options)](#apidoc.element.noflo.BasePort.BasePort)
1.  [function <span class="apidocSignatureSpan">noflo.BasePort.</span>EventEmitter ()](#apidoc.element.noflo.BasePort.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.BasePort.</span>init ()](#apidoc.element.noflo.BasePort.init)
1.  [function <span class="apidocSignatureSpan">noflo.BasePort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.BasePort.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.BasePort.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.BasePort.</span>__super__

#### [module noflo.Component](#apidoc.module.noflo.Component)
1.  boolean <span class="apidocSignatureSpan">noflo.Component.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>Component (options)](#apidoc.element.noflo.Component.Component)
1.  [function <span class="apidocSignatureSpan">noflo.Component.</span>EventEmitter ()](#apidoc.element.noflo.Component.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.Component.</span>init ()](#apidoc.element.noflo.Component.init)
1.  [function <span class="apidocSignatureSpan">noflo.Component.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Component.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.Component.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.Component.</span>__super__

#### [module noflo.Component.prototype](#apidoc.module.noflo.Component.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>activate (context)](#apidoc.element.noflo.Component.prototype.activate)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>addBracketForwards (result)](#apidoc.element.noflo.Component.prototype.addBracketForwards)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>addToResult (result, port, ip, before)](#apidoc.element.noflo.Component.prototype.addToResult)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>constructor (options)](#apidoc.element.noflo.Component.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>deactivate (context)](#apidoc.element.noflo.Component.prototype.deactivate)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>error (e, groups, errorPort, scope)](#apidoc.element.noflo.Component.prototype.error)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getBracketContext (type, port, scope, idx)](#apidoc.element.noflo.Component.prototype.getBracketContext)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getDescription ()](#apidoc.element.noflo.Component.prototype.getDescription)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getForwardableContexts (inport, outport, contexts)](#apidoc.element.noflo.Component.prototype.getForwardableContexts)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getIcon ()](#apidoc.element.noflo.Component.prototype.getIcon)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>handleIP (ip, port)](#apidoc.element.noflo.Component.prototype.handleIP)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isForwardingInport (port)](#apidoc.element.noflo.Component.prototype.isForwardingInport)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isForwardingOutport (inport, outport)](#apidoc.element.noflo.Component.prototype.isForwardingOutport)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isLegacy ()](#apidoc.element.noflo.Component.prototype.isLegacy)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isOrdered ()](#apidoc.element.noflo.Component.prototype.isOrdered)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isReady ()](#apidoc.element.noflo.Component.prototype.isReady)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isStarted ()](#apidoc.element.noflo.Component.prototype.isStarted)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isSubgraph ()](#apidoc.element.noflo.Component.prototype.isSubgraph)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>prepareForwarding ()](#apidoc.element.noflo.Component.prototype.prepareForwarding)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>process (handle)](#apidoc.element.noflo.Component.prototype.process)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>processOutputQueue ()](#apidoc.element.noflo.Component.prototype.processOutputQueue)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>setIcon (icon)](#apidoc.element.noflo.Component.prototype.setIcon)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>setUp (callback)](#apidoc.element.noflo.Component.prototype.setUp)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>shutdown (callback)](#apidoc.element.noflo.Component.prototype.shutdown)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>start (callback)](#apidoc.element.noflo.Component.prototype.start)
1.  [function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>tearDown (callback)](#apidoc.element.noflo.Component.prototype.tearDown)
1.  object <span class="apidocSignatureSpan">noflo.Component.prototype.</span>icon
1.  string <span class="apidocSignatureSpan">noflo.Component.prototype.</span>description

#### [module noflo.ComponentLoader](#apidoc.module.noflo.ComponentLoader)
1.  boolean <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>ComponentLoader (baseDir, options)](#apidoc.element.noflo.ComponentLoader.ComponentLoader)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>EventEmitter ()](#apidoc.element.noflo.ComponentLoader.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>init ()](#apidoc.element.noflo.ComponentLoader.init)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>listenerCount (emitter, type)](#apidoc.element.noflo.ComponentLoader.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>__super__

#### [module noflo.ComponentLoader.prototype](#apidoc.module.noflo.ComponentLoader.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>clear ()](#apidoc.element.noflo.ComponentLoader.prototype.clear)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>constructor (baseDir, options)](#apidoc.element.noflo.ComponentLoader.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>createComponent (name, component, metadata, callback)](#apidoc.element.noflo.ComponentLoader.prototype.createComponent)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>getLibraryIcon (prefix)](#apidoc.element.noflo.ComponentLoader.prototype.getLibraryIcon)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>getModulePrefix (name)](#apidoc.element.noflo.ComponentLoader.prototype.getModulePrefix)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>getSource (name, callback)](#apidoc.element.noflo.ComponentLoader.prototype.getSource)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>isGraph (cPath)](#apidoc.element.noflo.ComponentLoader.prototype.isGraph)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>listComponents (callback)](#apidoc.element.noflo.ComponentLoader.prototype.listComponents)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>load (name, callback, metadata)](#apidoc.element.noflo.ComponentLoader.prototype.load)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>loadGraph (name, component, callback, metadata)](#apidoc.element.noflo.ComponentLoader.prototype.loadGraph)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>normalizeName (packageId, name)](#apidoc.element.noflo.ComponentLoader.prototype.normalizeName)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>registerComponent (packageId, name, cPath, callback)](#apidoc.element.noflo.ComponentLoader.prototype.registerComponent)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>registerGraph (packageId, name, gPath, callback)](#apidoc.element.noflo.ComponentLoader.prototype.registerGraph)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>registerLoader (loader, callback)](#apidoc.element.noflo.ComponentLoader.prototype.registerLoader)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>setIcon (name, instance)](#apidoc.element.noflo.ComponentLoader.prototype.setIcon)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>setLibraryIcon (prefix, icon)](#apidoc.element.noflo.ComponentLoader.prototype.setLibraryIcon)
1.  [function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>setSource (packageId, name, source, language, callback)](#apidoc.element.noflo.ComponentLoader.prototype.setSource)

#### [module noflo.Graph](#apidoc.module.noflo.Graph)
1.  boolean <span class="apidocSignatureSpan">noflo.Graph.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>Graph (name1, options)](#apidoc.element.noflo.Graph.Graph)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.</span>EventEmitter ()](#apidoc.element.noflo.Graph.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.</span>init ()](#apidoc.element.noflo.Graph.init)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Graph.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.Graph.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.Graph.</span>__super__

#### [module noflo.Graph.prototype](#apidoc.module.noflo.Graph.prototype)
1.  boolean <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>caseSensitive
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addEdge (outNode, outPort, inNode, inPort, metadata)](#apidoc.element.noflo.Graph.prototype.addEdge)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addEdgeIndex (outNode, outPort, outIndex, inNode, inPort, inIndex, metadata)](#apidoc.element.noflo.Graph.prototype.addEdgeIndex)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addExport (publicPort, nodeKey, portKey, metadata)](#apidoc.element.noflo.Graph.prototype.addExport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addGraphInitial (data, node, metadata)](#apidoc.element.noflo.Graph.prototype.addGraphInitial)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addGraphInitialIndex (data, node, index, metadata)](#apidoc.element.noflo.Graph.prototype.addGraphInitialIndex)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addGroup (group, nodes, metadata)](#apidoc.element.noflo.Graph.prototype.addGroup)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addInitial (data, node, port, metadata)](#apidoc.element.noflo.Graph.prototype.addInitial)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addInitialIndex (data, node, port, index, metadata)](#apidoc.element.noflo.Graph.prototype.addInitialIndex)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addInport (publicPort, nodeKey, portKey, metadata)](#apidoc.element.noflo.Graph.prototype.addInport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addNode (id, component, metadata)](#apidoc.element.noflo.Graph.prototype.addNode)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addOutport (publicPort, nodeKey, portKey, metadata)](#apidoc.element.noflo.Graph.prototype.addOutport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>checkTransactionEnd ()](#apidoc.element.noflo.Graph.prototype.checkTransactionEnd)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>checkTransactionStart ()](#apidoc.element.noflo.Graph.prototype.checkTransactionStart)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>constructor (name1, options)](#apidoc.element.noflo.Graph.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>endTransaction (id, metadata)](#apidoc.element.noflo.Graph.prototype.endTransaction)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>getEdge (node, port, node2, port2)](#apidoc.element.noflo.Graph.prototype.getEdge)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>getNode (id)](#apidoc.element.noflo.Graph.prototype.getNode)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>getPortName (port)](#apidoc.element.noflo.Graph.prototype.getPortName)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeEdge (node, port, node2, port2)](#apidoc.element.noflo.Graph.prototype.removeEdge)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeExport (publicPort)](#apidoc.element.noflo.Graph.prototype.removeExport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeGraphInitial (node)](#apidoc.element.noflo.Graph.prototype.removeGraphInitial)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeGroup (groupName)](#apidoc.element.noflo.Graph.prototype.removeGroup)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeInitial (node, port)](#apidoc.element.noflo.Graph.prototype.removeInitial)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeInport (publicPort)](#apidoc.element.noflo.Graph.prototype.removeInport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeNode (id)](#apidoc.element.noflo.Graph.prototype.removeNode)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeOutport (publicPort)](#apidoc.element.noflo.Graph.prototype.removeOutport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameGroup (oldName, newName)](#apidoc.element.noflo.Graph.prototype.renameGroup)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameInport (oldPort, newPort)](#apidoc.element.noflo.Graph.prototype.renameInport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameNode (oldId, newId)](#apidoc.element.noflo.Graph.prototype.renameNode)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameOutport (oldPort, newPort)](#apidoc.element.noflo.Graph.prototype.renameOutport)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>save (file, callback)](#apidoc.element.noflo.Graph.prototype.save)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setEdgeMetadata (node, port, node2, port2, metadata)](#apidoc.element.noflo.Graph.prototype.setEdgeMetadata)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setGroupMetadata (groupName, metadata)](#apidoc.element.noflo.Graph.prototype.setGroupMetadata)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setInportMetadata (publicPort, metadata)](#apidoc.element.noflo.Graph.prototype.setInportMetadata)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setNodeMetadata (id, metadata)](#apidoc.element.noflo.Graph.prototype.setNodeMetadata)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setOutportMetadata (publicPort, metadata)](#apidoc.element.noflo.Graph.prototype.setOutportMetadata)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setProperties (properties)](#apidoc.element.noflo.Graph.prototype.setProperties)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>startTransaction (id, metadata)](#apidoc.element.noflo.Graph.prototype.startTransaction)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>toDOT ()](#apidoc.element.noflo.Graph.prototype.toDOT)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>toJSON ()](#apidoc.element.noflo.Graph.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>toYUML ()](#apidoc.element.noflo.Graph.prototype.toYUML)
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>edges
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>exports
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>groups
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>initializers
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>inports
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>nodes
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>outports
1.  object <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>properties
1.  string <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>name

#### [module noflo.IP](#apidoc.module.noflo.IP)
1.  [function <span class="apidocSignatureSpan">noflo.</span>IP (type, data, options)](#apidoc.element.noflo.IP.IP)
1.  [function <span class="apidocSignatureSpan">noflo.IP.</span>isIP (obj)](#apidoc.element.noflo.IP.isIP)
1.  object <span class="apidocSignatureSpan">noflo.IP.</span>types

#### [module noflo.IP.prototype](#apidoc.module.noflo.IP.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.IP.prototype.</span>clone ()](#apidoc.element.noflo.IP.prototype.clone)
1.  [function <span class="apidocSignatureSpan">noflo.IP.prototype.</span>drop ()](#apidoc.element.noflo.IP.prototype.drop)
1.  [function <span class="apidocSignatureSpan">noflo.IP.prototype.</span>move (owner)](#apidoc.element.noflo.IP.prototype.move)

#### [module noflo.InPort](#apidoc.module.noflo.InPort)
1.  boolean <span class="apidocSignatureSpan">noflo.InPort.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>InPort (options, process)](#apidoc.element.noflo.InPort.InPort)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.</span>EventEmitter ()](#apidoc.element.noflo.InPort.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.</span>init ()](#apidoc.element.noflo.InPort.init)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.InPort.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.InPort.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.InPort.</span>__super__

#### [module noflo.InPort.__super__](#apidoc.module.noflo.InPort.__super__)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>attach (socket, index)](#apidoc.element.noflo.InPort.__super__.attach)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>attachSocket ()](#apidoc.element.noflo.InPort.__super__.attachSocket)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>canAttach ()](#apidoc.element.noflo.InPort.__super__.canAttach)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>constructor (options)](#apidoc.element.noflo.InPort.__super__.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>detach (socket)](#apidoc.element.noflo.InPort.__super__.detach)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>getDataType ()](#apidoc.element.noflo.InPort.__super__.getDataType)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>getDescription ()](#apidoc.element.noflo.InPort.__super__.getDescription)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>getId ()](#apidoc.element.noflo.InPort.__super__.getId)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>handleOptions (options)](#apidoc.element.noflo.InPort.__super__.handleOptions)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isAddressable ()](#apidoc.element.noflo.InPort.__super__.isAddressable)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isAttached (socketId)](#apidoc.element.noflo.InPort.__super__.isAttached)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isBuffered ()](#apidoc.element.noflo.InPort.__super__.isBuffered)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isConnected (socketId)](#apidoc.element.noflo.InPort.__super__.isConnected)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isRequired ()](#apidoc.element.noflo.InPort.__super__.isRequired)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>listAttached ()](#apidoc.element.noflo.InPort.__super__.listAttached)

#### [module noflo.InPort.prototype](#apidoc.module.noflo.InPort.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>attachSocket (socket, localId)](#apidoc.element.noflo.InPort.prototype.attachSocket)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>clear ()](#apidoc.element.noflo.InPort.prototype.clear)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>constructor (options, process)](#apidoc.element.noflo.InPort.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>contains ()](#apidoc.element.noflo.InPort.prototype.contains)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>get (scope, idx)](#apidoc.element.noflo.InPort.prototype.get)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>getBuffer (scope, idx, initial)](#apidoc.element.noflo.InPort.prototype.getBuffer)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>getFromBuffer (scope, idx, initial)](#apidoc.element.noflo.InPort.prototype.getFromBuffer)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>handleIP (ip, id)](#apidoc.element.noflo.InPort.prototype.handleIP)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>handleSocketEvent (event, payload, id)](#apidoc.element.noflo.InPort.prototype.handleSocketEvent)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>has (scope, idx, validate)](#apidoc.element.noflo.InPort.prototype.has)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>hasDefault ()](#apidoc.element.noflo.InPort.prototype.hasDefault)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>hasIIP (idx, validate)](#apidoc.element.noflo.InPort.prototype.hasIIP)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>hasIPinBuffer (scope, idx, validate, initial)](#apidoc.element.noflo.InPort.prototype.hasIPinBuffer)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>length (scope, idx)](#apidoc.element.noflo.InPort.prototype.length)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>prepareBuffer ()](#apidoc.element.noflo.InPort.prototype.prepareBuffer)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>prepareBufferForIP (ip)](#apidoc.element.noflo.InPort.prototype.prepareBufferForIP)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>ready (scope, idx)](#apidoc.element.noflo.InPort.prototype.ready)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>receive ()](#apidoc.element.noflo.InPort.prototype.receive)
1.  [function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>validateData (data)](#apidoc.element.noflo.InPort.prototype.validateData)

#### [module noflo.InPorts](#apidoc.module.noflo.InPorts)
1.  boolean <span class="apidocSignatureSpan">noflo.InPorts.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>InPorts ()](#apidoc.element.noflo.InPorts.InPorts)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.</span>EventEmitter ()](#apidoc.element.noflo.InPorts.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.</span>init ()](#apidoc.element.noflo.InPorts.init)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.</span>listenerCount (emitter, type)](#apidoc.element.noflo.InPorts.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.InPorts.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.InPorts.</span>__super__

#### [module noflo.InPorts.__super__](#apidoc.module.noflo.InPorts.__super__)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>add (name, options, process)](#apidoc.element.noflo.InPorts.__super__.add)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>constructor (ports)](#apidoc.element.noflo.InPorts.__super__.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>model (options, process)](#apidoc.element.noflo.InPorts.__super__.model)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>remove (name)](#apidoc.element.noflo.InPorts.__super__.remove)

#### [module noflo.InPorts.prototype](#apidoc.module.noflo.InPorts.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.prototype.</span>constructor ()](#apidoc.element.noflo.InPorts.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.prototype.</span>on (name, event, callback)](#apidoc.element.noflo.InPorts.prototype.on)
1.  [function <span class="apidocSignatureSpan">noflo.InPorts.prototype.</span>once (name, event, callback)](#apidoc.element.noflo.InPorts.prototype.once)

#### [module noflo.Journal](#apidoc.module.noflo.Journal)
1.  boolean <span class="apidocSignatureSpan">noflo.Journal.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>Journal (graph, metadata, store)](#apidoc.element.noflo.Journal.Journal)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.</span>EventEmitter ()](#apidoc.element.noflo.Journal.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.</span>init ()](#apidoc.element.noflo.Journal.init)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Journal.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.Journal.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.Journal.</span>__super__

#### [module noflo.Journal.prototype](#apidoc.module.noflo.Journal.prototype)
1.  boolean <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>subscribed
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>appendCommand (cmd, args, rev)](#apidoc.element.noflo.Journal.prototype.appendCommand)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>canRedo ()](#apidoc.element.noflo.Journal.prototype.canRedo)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>canUndo ()](#apidoc.element.noflo.Journal.prototype.canUndo)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>constructor (graph, metadata, store)](#apidoc.element.noflo.Journal.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>endTransaction (id, meta)](#apidoc.element.noflo.Journal.prototype.endTransaction)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>executeEntry (entry)](#apidoc.element.noflo.Journal.prototype.executeEntry)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>executeEntryInversed (entry)](#apidoc.element.noflo.Journal.prototype.executeEntryInversed)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>moveToRevision (revId)](#apidoc.element.noflo.Journal.prototype.moveToRevision)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>redo ()](#apidoc.element.noflo.Journal.prototype.redo)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>save (file, success)](#apidoc.element.noflo.Journal.prototype.save)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>startTransaction (id, meta)](#apidoc.element.noflo.Journal.prototype.startTransaction)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>toJSON (startRev, endRev)](#apidoc.element.noflo.Journal.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>toPrettyString (startRev, endRev)](#apidoc.element.noflo.Journal.prototype.toPrettyString)
1.  [function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>undo ()](#apidoc.element.noflo.Journal.prototype.undo)
1.  object <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>entries
1.  object <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>graph

#### [module noflo.Network](#apidoc.module.noflo.Network)
1.  boolean <span class="apidocSignatureSpan">noflo.Network.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>Network (graph, options)](#apidoc.element.noflo.Network.Network)
1.  [function <span class="apidocSignatureSpan">noflo.Network.</span>EventEmitter ()](#apidoc.element.noflo.Network.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.Network.</span>init ()](#apidoc.element.noflo.Network.init)
1.  [function <span class="apidocSignatureSpan">noflo.Network.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Network.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.Network.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.Network.</span>__super__

#### [module noflo.Network.prototype](#apidoc.module.noflo.Network.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addDefaults (node, callback)](#apidoc.element.noflo.Network.prototype.addDefaults)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addEdge (edge, callback)](#apidoc.element.noflo.Network.prototype.addEdge)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addInitial (initializer, callback)](#apidoc.element.noflo.Network.prototype.addInitial)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addNode (node, callback)](#apidoc.element.noflo.Network.prototype.addNode)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>bufferedEmit (event, payload)](#apidoc.element.noflo.Network.prototype.bufferedEmit)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>checkIfFinished ()](#apidoc.element.noflo.Network.prototype.checkIfFinished)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>connect (done)](#apidoc.element.noflo.Network.prototype.connect)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>connectPort (socket, process, port, index, inbound)](#apidoc.element.noflo.Network.prototype.connectPort)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>constructor (graph, options)](#apidoc.element.noflo.Network.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>getActiveProcesses ()](#apidoc.element.noflo.Network.prototype.getActiveProcesses)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>getDebug ()](#apidoc.element.noflo.Network.prototype.getDebug)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>getNode (id)](#apidoc.element.noflo.Network.prototype.getNode)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>isRunning ()](#apidoc.element.noflo.Network.prototype.isRunning)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>isStarted ()](#apidoc.element.noflo.Network.prototype.isStarted)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>load (component, metadata, callback)](#apidoc.element.noflo.Network.prototype.load)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>removeEdge (edge, callback)](#apidoc.element.noflo.Network.prototype.removeEdge)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>removeInitial (initializer, callback)](#apidoc.element.noflo.Network.prototype.removeInitial)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>removeNode (node, callback)](#apidoc.element.noflo.Network.prototype.removeNode)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>renameNode (oldId, newId, callback)](#apidoc.element.noflo.Network.prototype.renameNode)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>sendDefaults (callback)](#apidoc.element.noflo.Network.prototype.sendDefaults)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>sendInitial (initial)](#apidoc.element.noflo.Network.prototype.sendInitial)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>sendInitials (callback)](#apidoc.element.noflo.Network.prototype.sendInitials)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>setDebug (active)](#apidoc.element.noflo.Network.prototype.setDebug)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>setStarted (started)](#apidoc.element.noflo.Network.prototype.setStarted)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>start (callback)](#apidoc.element.noflo.Network.prototype.start)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>startComponents (callback)](#apidoc.element.noflo.Network.prototype.startComponents)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>stop (callback)](#apidoc.element.noflo.Network.prototype.stop)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeGraph ()](#apidoc.element.noflo.Network.prototype.subscribeGraph)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeNode (node)](#apidoc.element.noflo.Network.prototype.subscribeNode)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeSocket (socket, source)](#apidoc.element.noflo.Network.prototype.subscribeSocket)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeSubgraph (node)](#apidoc.element.noflo.Network.prototype.subscribeSubgraph)
1.  [function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>uptime ()](#apidoc.element.noflo.Network.prototype.uptime)
1.  object <span class="apidocSignatureSpan">noflo.Network.prototype.</span>connections
1.  object <span class="apidocSignatureSpan">noflo.Network.prototype.</span>defaults
1.  object <span class="apidocSignatureSpan">noflo.Network.prototype.</span>graph
1.  object <span class="apidocSignatureSpan">noflo.Network.prototype.</span>initials
1.  object <span class="apidocSignatureSpan">noflo.Network.prototype.</span>processes
1.  object <span class="apidocSignatureSpan">noflo.Network.prototype.</span>startupDate

#### [module noflo.OutPort](#apidoc.module.noflo.OutPort)
1.  boolean <span class="apidocSignatureSpan">noflo.OutPort.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>OutPort (options)](#apidoc.element.noflo.OutPort.OutPort)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.</span>EventEmitter ()](#apidoc.element.noflo.OutPort.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.</span>init ()](#apidoc.element.noflo.OutPort.init)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.OutPort.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.OutPort.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.OutPort.</span>__super__

#### [module noflo.OutPort.prototype](#apidoc.module.noflo.OutPort.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>attach (socket, index)](#apidoc.element.noflo.OutPort.prototype.attach)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>beginGroup (group, socketId)](#apidoc.element.noflo.OutPort.prototype.beginGroup)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>checkRequired (sockets)](#apidoc.element.noflo.OutPort.prototype.checkRequired)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>closeBracket (data, options, socketId)](#apidoc.element.noflo.OutPort.prototype.closeBracket)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>connect (socketId)](#apidoc.element.noflo.OutPort.prototype.connect)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>constructor (options)](#apidoc.element.noflo.OutPort.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>data (data, options, socketId)](#apidoc.element.noflo.OutPort.prototype.data)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>disconnect (socketId)](#apidoc.element.noflo.OutPort.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>endGroup (socketId)](#apidoc.element.noflo.OutPort.prototype.endGroup)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>getSockets (socketId)](#apidoc.element.noflo.OutPort.prototype.getSockets)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>isCaching ()](#apidoc.element.noflo.OutPort.prototype.isCaching)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>openBracket (data, options, socketId)](#apidoc.element.noflo.OutPort.prototype.openBracket)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>send (data, socketId)](#apidoc.element.noflo.OutPort.prototype.send)
1.  [function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>sendIP (type, data, options, socketId, autoConnect)](#apidoc.element.noflo.OutPort.prototype.sendIP)

#### [module noflo.OutPorts](#apidoc.module.noflo.OutPorts)
1.  boolean <span class="apidocSignatureSpan">noflo.OutPorts.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>OutPorts ()](#apidoc.element.noflo.OutPorts.OutPorts)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.</span>EventEmitter ()](#apidoc.element.noflo.OutPorts.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.</span>init ()](#apidoc.element.noflo.OutPorts.init)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.</span>listenerCount (emitter, type)](#apidoc.element.noflo.OutPorts.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.OutPorts.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.OutPorts.</span>__super__

#### [module noflo.OutPorts.prototype](#apidoc.module.noflo.OutPorts.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>beginGroup (name, group, socketId)](#apidoc.element.noflo.OutPorts.prototype.beginGroup)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>connect (name, socketId)](#apidoc.element.noflo.OutPorts.prototype.connect)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>constructor ()](#apidoc.element.noflo.OutPorts.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>disconnect (name, socketId)](#apidoc.element.noflo.OutPorts.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>endGroup (name, socketId)](#apidoc.element.noflo.OutPorts.prototype.endGroup)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>model (options)](#apidoc.element.noflo.OutPorts.prototype.model)
1.  [function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>send (name, data, socketId)](#apidoc.element.noflo.OutPorts.prototype.send)

#### [module noflo.Platform](#apidoc.module.noflo.Platform)
1.  [function <span class="apidocSignatureSpan">noflo.Platform.</span>deprecated (message)](#apidoc.element.noflo.Platform.deprecated)
1.  [function <span class="apidocSignatureSpan">noflo.Platform.</span>isBrowser ()](#apidoc.element.noflo.Platform.isBrowser)

#### [module noflo.Port](#apidoc.module.noflo.Port)
1.  boolean <span class="apidocSignatureSpan">noflo.Port.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.</span>Port (type)](#apidoc.element.noflo.Port.Port)
1.  [function <span class="apidocSignatureSpan">noflo.Port.</span>EventEmitter ()](#apidoc.element.noflo.Port.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.Port.</span>init ()](#apidoc.element.noflo.Port.init)
1.  [function <span class="apidocSignatureSpan">noflo.Port.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Port.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.Port.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.Port.</span>__super__

#### [module noflo.Port.prototype](#apidoc.module.noflo.Port.prototype)
1.  boolean <span class="apidocSignatureSpan">noflo.Port.prototype.</span>required
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>attach (socket)](#apidoc.element.noflo.Port.prototype.attach)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>attachSocket (socket, localId)](#apidoc.element.noflo.Port.prototype.attachSocket)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>beginGroup (group)](#apidoc.element.noflo.Port.prototype.beginGroup)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>canAttach ()](#apidoc.element.noflo.Port.prototype.canAttach)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>clear ()](#apidoc.element.noflo.Port.prototype.clear)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>connect ()](#apidoc.element.noflo.Port.prototype.connect)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>constructor (type)](#apidoc.element.noflo.Port.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>detach (socket)](#apidoc.element.noflo.Port.prototype.detach)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>disconnect ()](#apidoc.element.noflo.Port.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>endGroup ()](#apidoc.element.noflo.Port.prototype.endGroup)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>getDataType ()](#apidoc.element.noflo.Port.prototype.getDataType)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>getDescription ()](#apidoc.element.noflo.Port.prototype.getDescription)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>getId ()](#apidoc.element.noflo.Port.prototype.getId)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isAddressable ()](#apidoc.element.noflo.Port.prototype.isAddressable)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isAttached ()](#apidoc.element.noflo.Port.prototype.isAttached)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isConnected ()](#apidoc.element.noflo.Port.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isRequired ()](#apidoc.element.noflo.Port.prototype.isRequired)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>listAttached ()](#apidoc.element.noflo.Port.prototype.listAttached)
1.  [function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>send (data)](#apidoc.element.noflo.Port.prototype.send)
1.  string <span class="apidocSignatureSpan">noflo.Port.prototype.</span>description

#### [module noflo.Ports](#apidoc.module.noflo.Ports)
1.  [function <span class="apidocSignatureSpan">noflo.Ports.</span>InPorts ()](#apidoc.element.noflo.Ports.InPorts)
1.  [function <span class="apidocSignatureSpan">noflo.Ports.</span>OutPorts ()](#apidoc.element.noflo.Ports.OutPorts)
1.  [function <span class="apidocSignatureSpan">noflo.Ports.</span>normalizePortName (name)](#apidoc.element.noflo.Ports.normalizePortName)

#### [module noflo.Utils](#apidoc.module.noflo.Utils)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>clone (obj)](#apidoc.element.noflo.Utils.clone)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>debounce (func, wait, immediate)](#apidoc.element.noflo.Utils.debounce)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>getValues (obj)](#apidoc.element.noflo.Utils.getValues)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>guessLanguageFromFilename (filename)](#apidoc.element.noflo.Utils.guessLanguageFromFilename)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>intersection (array)](#apidoc.element.noflo.Utils.intersection)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>optimizeCb (func, context, argCount)](#apidoc.element.noflo.Utils.optimizeCb)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>reduceRight (obj, iteratee, memo, context)](#apidoc.element.noflo.Utils.reduceRight)
1.  [function <span class="apidocSignatureSpan">noflo.Utils.</span>unique (array)](#apidoc.element.noflo.Utils.unique)

#### [module noflo.graph](#apidoc.module.noflo.graph)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>Graph (name1, options)](#apidoc.element.noflo.graph.Graph)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>createGraph (name, options)](#apidoc.element.noflo.graph.createGraph)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>equivalent (a, b, options)](#apidoc.element.noflo.graph.equivalent)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>loadFBP (fbpData, callback, metadata, caseSensitive)](#apidoc.element.noflo.graph.loadFBP)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>loadFile (file, callback, metadata, caseSensitive)](#apidoc.element.noflo.graph.loadFile)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>loadHTTP (url, callback)](#apidoc.element.noflo.graph.loadHTTP)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>loadJSON (definition, callback, metadata)](#apidoc.element.noflo.graph.loadJSON)
1.  [function <span class="apidocSignatureSpan">noflo.graph.</span>mergeResolveTheirs (base, to)](#apidoc.element.noflo.graph.mergeResolveTheirs)

#### [module noflo.helpers](#apidoc.module.noflo.helpers)
1.  [function <span class="apidocSignatureSpan">noflo.helpers.</span>CustomError (message, options)](#apidoc.element.noflo.helpers.CustomError)
1.  [function <span class="apidocSignatureSpan">noflo.helpers.</span>CustomizeError (err, options)](#apidoc.element.noflo.helpers.CustomizeError)
1.  [function <span class="apidocSignatureSpan">noflo.helpers.</span>GroupedInput (component, config, proc)](#apidoc.element.noflo.helpers.GroupedInput)
1.  [function <span class="apidocSignatureSpan">noflo.helpers.</span>MapComponent (component, func, config)](#apidoc.element.noflo.helpers.MapComponent)
1.  [function <span class="apidocSignatureSpan">noflo.helpers.</span>MultiError (component, group, errorPort, forwardedGroups, scope)](#apidoc.element.noflo.helpers.MultiError)
1.  [function <span class="apidocSignatureSpan">noflo.helpers.</span>WirePattern (component, config, proc)](#apidoc.element.noflo.helpers.WirePattern)

#### [module noflo.internalSocket](#apidoc.module.noflo.internalSocket)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.</span>InternalSocket (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.</span>createSocket ()](#apidoc.element.noflo.internalSocket.createSocket)

#### [module noflo.internalSocket.InternalSocket](#apidoc.module.noflo.internalSocket.InternalSocket)
1.  boolean <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.</span>InternalSocket (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket.InternalSocket)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>EventEmitter ()](#apidoc.element.noflo.internalSocket.InternalSocket.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>init ()](#apidoc.element.noflo.internalSocket.InternalSocket.init)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>listenerCount (emitter, type)](#apidoc.element.noflo.internalSocket.InternalSocket.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>__super__

#### [module noflo.internalSocket.InternalSocket.prototype](#apidoc.module.noflo.internalSocket.InternalSocket.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>beginGroup (group)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.beginGroup)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>connect ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.connect)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>constructor (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>debugEmitEvent (event, data)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.debugEmitEvent)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>disconnect ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>endGroup ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.endGroup)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>getId ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.getId)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>handleSocketEvent (event, payload, autoConnect)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.handleSocketEvent)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>ipToLegacy (ip)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.ipToLegacy)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>isConnected ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.isConnected)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>legacyToIp (event, payload)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.legacyToIp)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>post (ip, autoDisconnect)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.post)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>regularEmitEvent (event, data)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.regularEmitEvent)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>send (data)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.send)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>setDataDelegate (delegate)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.setDataDelegate)
1.  [function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>setDebug (active)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.setDebug)

#### [module noflo.journal](#apidoc.module.noflo.journal)
1.  [function <span class="apidocSignatureSpan">noflo.journal.</span>Journal (graph, metadata, store)](#apidoc.element.noflo.journal.Journal)
1.  [function <span class="apidocSignatureSpan">noflo.journal.</span>JournalStore (graph1)](#apidoc.element.noflo.journal.JournalStore)
1.  [function <span class="apidocSignatureSpan">noflo.journal.</span>MemoryJournalStore (graph)](#apidoc.element.noflo.journal.MemoryJournalStore)

#### [module noflo.journal.JournalStore](#apidoc.module.noflo.journal.JournalStore)
1.  boolean <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.journal.</span>JournalStore (graph1)](#apidoc.element.noflo.journal.JournalStore.JournalStore)
1.  [function <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>EventEmitter ()](#apidoc.element.noflo.journal.JournalStore.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>init ()](#apidoc.element.noflo.journal.JournalStore.init)
1.  [function <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>listenerCount (emitter, type)](#apidoc.element.noflo.journal.JournalStore.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>__super__

#### [module noflo.journal.JournalStore.prototype](#apidoc.module.noflo.journal.JournalStore.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.journal.JournalStore.prototype.</span>constructor (graph1)](#apidoc.element.noflo.journal.JournalStore.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.journal.JournalStore.prototype.</span>fetchTransaction (revId, entries)](#apidoc.element.noflo.journal.JournalStore.prototype.fetchTransaction)
1.  [function <span class="apidocSignatureSpan">noflo.journal.JournalStore.prototype.</span>putTransaction (revId, entries)](#apidoc.element.noflo.journal.JournalStore.prototype.putTransaction)
1.  number <span class="apidocSignatureSpan">noflo.journal.JournalStore.prototype.</span>lastRevision

#### [module noflo.journal.MemoryJournalStore](#apidoc.module.noflo.journal.MemoryJournalStore)
1.  boolean <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>usingDomains
1.  [function <span class="apidocSignatureSpan">noflo.journal.</span>MemoryJournalStore (graph)](#apidoc.element.noflo.journal.MemoryJournalStore.MemoryJournalStore)
1.  [function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>EventEmitter ()](#apidoc.element.noflo.journal.MemoryJournalStore.EventEmitter)
1.  [function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>init ()](#apidoc.element.noflo.journal.MemoryJournalStore.init)
1.  [function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>listenerCount (emitter, type)](#apidoc.element.noflo.journal.MemoryJournalStore.listenerCount)
1.  number <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>defaultMaxListeners
1.  object <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>__super__

#### [module noflo.journal.MemoryJournalStore.prototype](#apidoc.module.noflo.journal.MemoryJournalStore.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.prototype.</span>constructor (graph)](#apidoc.element.noflo.journal.MemoryJournalStore.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.prototype.</span>fetchTransaction (revId)](#apidoc.element.noflo.journal.MemoryJournalStore.prototype.fetchTransaction)
1.  [function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.prototype.</span>putTransaction (revId, entries)](#apidoc.element.noflo.journal.MemoryJournalStore.prototype.putTransaction)

#### [module noflo.streams](#apidoc.module.noflo.streams)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>IP (data1)](#apidoc.element.noflo.streams.IP)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>StreamReceiver (port1, buffered, process)](#apidoc.element.noflo.streams.StreamReceiver)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>StreamSender (port1, ordered)](#apidoc.element.noflo.streams.StreamSender)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>Substream (key)](#apidoc.element.noflo.streams.Substream)

#### [module noflo.streams.IP](#apidoc.module.noflo.streams.IP)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>IP (data1)](#apidoc.element.noflo.streams.IP.IP)

#### [module noflo.streams.IP.prototype](#apidoc.module.noflo.streams.IP.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.streams.IP.prototype.</span>getValue ()](#apidoc.element.noflo.streams.IP.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">noflo.streams.IP.prototype.</span>sendTo (port)](#apidoc.element.noflo.streams.IP.prototype.sendTo)
1.  [function <span class="apidocSignatureSpan">noflo.streams.IP.prototype.</span>toObject ()](#apidoc.element.noflo.streams.IP.prototype.toObject)

#### [module noflo.streams.StreamReceiver](#apidoc.module.noflo.streams.StreamReceiver)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>StreamReceiver (port1, buffered, process)](#apidoc.element.noflo.streams.StreamReceiver.StreamReceiver)

#### [module noflo.streams.StreamReceiver.prototype](#apidoc.module.noflo.streams.StreamReceiver.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamReceiver.prototype.</span>read ()](#apidoc.element.noflo.streams.StreamReceiver.prototype.read)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamReceiver.prototype.</span>resetCurrent ()](#apidoc.element.noflo.streams.StreamReceiver.prototype.resetCurrent)

#### [module noflo.streams.StreamSender](#apidoc.module.noflo.streams.StreamSender)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>StreamSender (port1, ordered)](#apidoc.element.noflo.streams.StreamSender.StreamSender)

#### [module noflo.streams.StreamSender.prototype](#apidoc.module.noflo.streams.StreamSender.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>beginGroup (group)](#apidoc.element.noflo.streams.StreamSender.prototype.beginGroup)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>disconnect ()](#apidoc.element.noflo.streams.StreamSender.prototype.disconnect)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>done ()](#apidoc.element.noflo.streams.StreamSender.prototype.done)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>endGroup ()](#apidoc.element.noflo.streams.StreamSender.prototype.endGroup)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>flush ()](#apidoc.element.noflo.streams.StreamSender.prototype.flush)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>isAttached ()](#apidoc.element.noflo.streams.StreamSender.prototype.isAttached)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>resetCurrent ()](#apidoc.element.noflo.streams.StreamSender.prototype.resetCurrent)
1.  [function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>send (data)](#apidoc.element.noflo.streams.StreamSender.prototype.send)

#### [module noflo.streams.Substream](#apidoc.module.noflo.streams.Substream)
1.  [function <span class="apidocSignatureSpan">noflo.streams.</span>Substream (key)](#apidoc.element.noflo.streams.Substream.Substream)

#### [module noflo.streams.Substream.prototype](#apidoc.module.noflo.streams.Substream.prototype)
1.  [function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>getKey ()](#apidoc.element.noflo.streams.Substream.prototype.getKey)
1.  [function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>getValue ()](#apidoc.element.noflo.streams.Substream.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>push (value)](#apidoc.element.noflo.streams.Substream.prototype.push)
1.  [function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>sendTo (port)](#apidoc.element.noflo.streams.Substream.prototype.sendTo)
1.  [function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>toObject ()](#apidoc.element.noflo.streams.Substream.prototype.toObject)



# <a name="apidoc.module.noflo"></a>[module noflo](#apidoc.module.noflo)

#### <a name="apidoc.element.noflo.ArrayPort"></a>[function <span class="apidocSignatureSpan">noflo.</span>ArrayPort (type)](#apidoc.element.noflo.ArrayPort)
- description and source-code
```javascript
function ArrayPort(type) {
  this.type = type;
  platform.deprecated('noflo.ArrayPort is deprecated. Please port to noflo.InPort/noflo.OutPort and use addressable: true');
  ArrayPort.__super__.constructor.call(this, this.type);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.AsyncComponent"></a>[function <span class="apidocSignatureSpan">noflo.</span>AsyncComponent (inPortName, outPortName, errPortName)](#apidoc.element.noflo.AsyncComponent)
- description and source-code
```javascript
function AsyncComponent(inPortName, outPortName, errPortName) {
  this.inPortName = inPortName != null ? inPortName : "in";
  this.outPortName = outPortName != null ? outPortName : "out";
  this.errPortName = errPortName != null ? errPortName : "error";
  this.error = bind(this.error, this);
  platform.deprecated('noflo.AsyncComponent is deprecated. Please port to Process API');
  if (!this.inPorts[this.inPortName]) {
    throw new Error("no inPort named '" + this.inPortName + "'");
  }
  if (!this.outPorts[this.outPortName]) {
    throw new Error("no outPort named '" + this.outPortName + "'");
  }
  this.load = 0;
  this.q = [];
  this.errorGroups = [];
  this.outPorts.load = new port.Port();
  this.inPorts[this.inPortName].on("begingroup", (function(_this) {
    return function(group) {
      if (_this.load > 0) {
        return _this.q.push({
          name: "begingroup",
          data: group
        });
      }
      _this.errorGroups.push(group);
      return _this.outPorts[_this.outPortName].beginGroup(group);
    };
  })(this));
  this.inPorts[this.inPortName].on("endgroup", (function(_this) {
    return function() {
      if (_this.load > 0) {
        return _this.q.push({
          name: "endgroup"
        });
      }
      _this.errorGroups.pop();
      return _this.outPorts[_this.outPortName].endGroup();
    };
  })(this));
  this.inPorts[this.inPortName].on("disconnect", (function(_this) {
    return function() {
      if (_this.load > 0) {
        return _this.q.push({
          name: "disconnect"
        });
      }
      _this.outPorts[_this.outPortName].disconnect();
      _this.errorGroups = [];
      if (_this.outPorts.load.isAttached()) {
        return _this.outPorts.load.disconnect();
      }
    };
  })(this));
  this.inPorts[this.inPortName].on("data", (function(_this) {
    return function(data) {
      if (_this.q.length > 0) {
        return _this.q.push({
          name: "data",
          data: data
        });
      }
      return _this.processData(data);
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.BasePort"></a>[function <span class="apidocSignatureSpan">noflo.</span>BasePort (options)](#apidoc.element.noflo.BasePort)
- description and source-code
```javascript
function BasePort(options) {
  this.handleOptions(options);
  this.sockets = [];
  this.node = null;
  this.name = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Component"></a>[function <span class="apidocSignatureSpan">noflo.</span>Component (options)](#apidoc.element.noflo.Component)
- description and source-code
```javascript
function Component(options) {
  this.error = bind(this.error, this);
  var ref, ref1, ref2;
  if (!options) {
    options = {};
  }
  if (!options.inPorts) {
    options.inPorts = {};
  }
  if (options.inPorts instanceof ports.InPorts) {
    this.inPorts = options.inPorts;
  } else {
    this.inPorts = new ports.InPorts(options.inPorts);
  }
  if (!options.outPorts) {
    options.outPorts = {};
  }
  if (options.outPorts instanceof ports.OutPorts) {
    this.outPorts = options.outPorts;
  } else {
    this.outPorts = new ports.OutPorts(options.outPorts);
  }
  if (options.icon) {
    this.icon = options.icon;
  }
  if (options.description) {
    this.description = options.description;
  }
  this.started = false;
  this.load = 0;
  this.ordered = (ref = options.ordered) != null ? ref : false;
  this.autoOrdering = (ref1 = options.autoOrdering) != null ? ref1 : null;
  this.outputQ = [];
  this.bracketContext = {
    "in": {},
    out: {}
  };
  this.activateOnInput = (ref2 = options.activateOnInput) != null ? ref2 : true;
  this.forwardBrackets = {
    "in": ['out', 'error']
  };
  if ('forwardBrackets' in options) {
    this.forwardBrackets = options.forwardBrackets;
  }
  if (typeof options.process === 'function') {
    this.process(options.process);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.ComponentLoader"></a>[function <span class="apidocSignatureSpan">noflo.</span>ComponentLoader (baseDir, options)](#apidoc.element.noflo.ComponentLoader)
- description and source-code
```javascript
function ComponentLoader(baseDir, options) {
  this.baseDir = baseDir;
  this.options = options != null ? options : {};
  this.components = null;
  this.libraryIcons = {};
  this.processing = false;
  this.ready = false;
  if (typeof this.setMaxListeners === 'function') {
    this.setMaxListeners(0);
  }
}
```
- example usage
```shell
...
  } else {
    this.baseDir = graph.baseDir || '/';
  }
  this.startupDate = null;
  if (graph.componentLoader) {
    this.loader = graph.componentLoader;
  } else {
    this.loader = new componentLoader.ComponentLoader(this.baseDir, this.options);
  }
}

Network.prototype.uptime = function() {
  if (!this.startupDate) {
    return 0;
  }
...
```

#### <a name="apidoc.element.noflo.Graph"></a>[function <span class="apidocSignatureSpan">noflo.</span>Graph (name1, options)](#apidoc.element.noflo.Graph)
- description and source-code
```javascript
function Graph(name1, options) {
  this.name = name1 != null ? name1 : '';
  if (options == null) {
    options = {};
  }
  this.properties = {};
  this.nodes = [];
  this.edges = [];
  this.initializers = [];
  this.exports = [];
  this.inports = {};
  this.outports = {};
  this.groups = [];
  this.transaction = {
    id: null,
    depth: 0
  };
  this.caseSensitive = options.caseSensitive || false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.IP"></a>[function <span class="apidocSignatureSpan">noflo.</span>IP (type, data, options)](#apidoc.element.noflo.IP)
- description and source-code
```javascript
function IP(type, data, options) {
  var key, val;
  this.type = type != null ? type : 'data';
  this.data = data != null ? data : null;
  if (options == null) {
    options = {};
  }
  this._isIP = true;
  this.scope = null;
  this.owner = null;
  this.clonable = false;
  this.index = null;
  for (key in options) {
    val = options[key];
    this[key] = val;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort"></a>[function <span class="apidocSignatureSpan">noflo.</span>InPort (options, process)](#apidoc.element.noflo.InPort)
- description and source-code
```javascript
function InPort(options, process) {
  this.process = null;
  if (!process && typeof options === 'function') {
    process = options;
    options = {};
  }
  if (options == null) {
    options = {};
  }
  if (options.buffered == null) {
    options.buffered = false;
  }
  if (options.control == null) {
    options.control = false;
  }
  if (options.triggering == null) {
    options.triggering = true;
  }
  if (!process && options && options.process) {
    process = options.process;
    delete options.process;
  }
  if (process) {
    platform.deprecated('InPort process callback is deprecated. Please use Process API or the InPort handle option');
    if (typeof process !== 'function') {
      throw new Error('process must be a function');
    }
    this.process = process;
  }
  if (options.handle) {
    platform.deprecated('InPort handle callback is deprecated. Please use Process API');
    if (typeof options.handle !== 'function') {
      throw new Error('handle must be a function');
    }
    this.handle = options.handle;
    delete options.handle;
  }
  InPort.__super__.constructor.call(this, options);
  this.prepareBuffer();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPorts"></a>[function <span class="apidocSignatureSpan">noflo.</span>InPorts ()](#apidoc.element.noflo.InPorts)
- description and source-code
```javascript
function InPorts() {
  return InPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
this.network = null;
this.ready = true;
this.started = false;
this.starting = false;
this.baseDir = null;
this.loader = null;
this.load = 0;
this.inPorts = new noflo.InPorts({
  graph: {
    datatype: 'all',
    description: 'NoFlo graph definition to be used with the subgraph component',
    required: true
  }
});
this.outPorts = new noflo.OutPorts;
...
```

#### <a name="apidoc.element.noflo.Journal"></a>[function <span class="apidocSignatureSpan">noflo.</span>Journal (graph, metadata, store)](#apidoc.element.noflo.Journal)
- description and source-code
```javascript
function Journal(graph, metadata, store) {
  this.endTransaction = bind(this.endTransaction, this);
  this.startTransaction = bind(this.startTransaction, this);
  var edge, group, iip, j, k, l, len, len1, len2, len3, m, n, node, ref, ref1, ref2, ref3, ref4, ref5, v;
  this.graph = graph;
  this.entries = [];
  this.subscribed = true;
  this.store = store || new MemoryJournalStore(this.graph);
  if (this.store.transactions.length === 0) {
    this.currentRevision = -1;
    this.startTransaction('initial', metadata);
    ref = this.graph.nodes;
    for (j = 0, len = ref.length; j < len; j++) {
      node = ref[j];
      this.appendCommand('addNode', node);
    }
    ref1 = this.graph.edges;
    for (l = 0, len1 = ref1.length; l < len1; l++) {
      edge = ref1[l];
      this.appendCommand('addEdge', edge);
    }
    ref2 = this.graph.initializers;
    for (m = 0, len2 = ref2.length; m < len2; m++) {
      iip = ref2[m];
      this.appendCommand('addInitial', iip);
    }
    if (Object.keys(this.graph.properties).length > 0) {
      this.appendCommand('changeProperties', this.graph.properties, {});
    }
    ref3 = this.graph.inports;
    for (k in ref3) {
      v = ref3[k];
      this.appendCommand('addInport', {
        name: k,
        port: v
      });
    }
    ref4 = this.graph.outports;
    for (k in ref4) {
      v = ref4[k];
      this.appendCommand('addOutport', {
        name: k,
        port: v
      });
    }
    ref5 = this.graph.groups;
    for (n = 0, len3 = ref5.length; n < len3; n++) {
      group = ref5[n];
      this.appendCommand('addGroup', group);
    }
    this.endTransaction('initial', metadata);
  } else {
    this.currentRevision = this.store.lastRevision;
  }
  this.graph.on('addNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('addNode', node);
    };
  })(this));
  this.graph.on('removeNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('removeNode', node);
    };
  })(this));
  this.graph.on('renameNode', (function(_this) {
    return function(oldId, newId) {
      var args;
      args = {
        oldId: oldId,
        newId: newId
      };
      return _this.appendCommand('renameNode', args);
    };
  })(this));
  this.graph.on('changeNode', (function(_this) {
    return function(node, oldMeta) {
      return _this.appendCommand('changeNode', {
        id: node.id,
        "new": node.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('addEdge', edge);
    };
  })(this));
  this.graph.on('removeEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('removeEdge', edge);
    };
  })(this));
  this.graph.on('changeEdge', (function(_this) {
    return function(edge, oldMeta) {
      return _this.appendCommand('changeEdge', {
        from: edge.from,
        to: edge.to,
        "new": edge.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('addInitial', iip);
    };
  })(this));
  this.graph.on('removeInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('removeInitial', iip);
    };
  })(this));
  this.graph.on('changeProperties', (function(_this) {
    return function(newProps, oldProps) {
      return _this.appendCommand('changeProperties', {
        "new": newProps,
        old: oldProps
      });
    };
  })(this));
  this.graph.on('addGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('addGroup', group);
    };
  })(this));
  this.graph.on('renameGroup', (function(_this) {
    return function(oldName, newName) {
      return _this.appendCommand('renameGroup', {
        oldName: oldName,
        newName: newName
      });
    };
  })(this));
  this.graph.on('removeGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('removeGroup', group);
    };
  })( ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Network"></a>[function <span class="apidocSignatureSpan">noflo.</span>Network (graph, options)](#apidoc.element.noflo.Network)
- description and source-code
```javascript
function Network(graph, options) {
  this.options = options != null ? options : {};
  this.processes = {};
  this.connections = [];
  this.initials = [];
  this.nextInitials = [];
  this.defaults = [];
  this.graph = graph;
  this.started = false;
  this.debug = true;
  this.eventBuffer = [];
  if (!platform.isBrowser()) {
    this.baseDir = graph.baseDir || process.cwd();
  } else {
    this.baseDir = graph.baseDir || '/';
  }
  this.startupDate = null;
  if (graph.componentLoader) {
    this.loader = graph.componentLoader;
  } else {
    this.loader = new componentLoader.ComponentLoader(this.baseDir, this.options);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPort"></a>[function <span class="apidocSignatureSpan">noflo.</span>OutPort (options)](#apidoc.element.noflo.OutPort)
- description and source-code
```javascript
function OutPort(options) {
  this.cache = {};
  OutPort.__super__.constructor.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPorts"></a>[function <span class="apidocSignatureSpan">noflo.</span>OutPorts ()](#apidoc.element.noflo.OutPorts)
- description and source-code
```javascript
function OutPorts() {
  return OutPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
}
if (!options.outPorts) {
  options.outPorts = {};
}
if (options.outPorts instanceof ports.OutPorts) {
  this.outPorts = options.outPorts;
} else {
  this.outPorts = new ports.OutPorts(options.outPorts);
}
if (options.icon) {
  this.icon = options.icon;
}
if (options.description) {
  this.description = options.description;
}
...
```

#### <a name="apidoc.element.noflo.Port"></a>[function <span class="apidocSignatureSpan">noflo.</span>Port (type)](#apidoc.element.noflo.Port)
- description and source-code
```javascript
function Port(type) {
  this.type = type;
  platform.deprecated('noflo.Port is deprecated. Please port to noflo.InPort/noflo.OutPort');
  if (!this.type) {
    this.type = 'all';
  }
  if (this.type === 'integer') {
    this.type = 'int';
  }
  this.sockets = [];
  this.from = null;
  this.node = null;
  this.name = null;
}
```
- example usage
```shell
...
}
if (!this.outPorts[this.outPortName]) {
  throw new Error("no outPort named '" + this.outPortName + "'");
}
this.load = 0;
this.q = [];
this.errorGroups = [];
this.outPorts.load = new port.Port();
this.inPorts[this.inPortName].on("begingroup", (function(_this) {
  return function(group) {
    if (_this.load > 0) {
      return _this.q.push({
        name: "begingroup",
        data: group
      });
...
```

#### <a name="apidoc.element.noflo.asCallback"></a>[function <span class="apidocSignatureSpan">noflo.</span>asCallback (component, options)](#apidoc.element.noflo.asCallback)
- description and source-code
```javascript
asCallback = function (component, options) {
  options = normalizeOptions(options, component);
  return function(inputs, callback) {
    return prepareNetwork(component, options, function(err, network) {
      var inputMap, resultType;
      if (err) {
        return callback(err);
      }
      resultType = getType(inputs, network);
      inputMap = prepareInputMap(inputs, resultType, network);
      return runNetwork(network, inputMap, options, function(err, outputMap) {
        if (err) {
          return callback(err);
        }
        return sendOutputMap(outputMap, resultType, options, callback);
      });
    });
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.createNetwork"></a>[function <span class="apidocSignatureSpan">noflo.</span>createNetwork (graph, callback, options)](#apidoc.element.noflo.createNetwork)
- description and source-code
```javascript
createNetwork = function (graph, callback, options) {
  var network, networkReady;
  if (typeof options !== 'object') {
    options = {
      delay: options
    };
  }
  if (typeof callback !== 'function') {
    callback = function(err) {
      if (err) {
        throw err;
      }
    };
  }
  network = new exports.Network(graph, options);
  networkReady = function(network) {
    return network.start(function(err) {
      if (err) {
        return callback(err);
      }
      return callback(null, network);
    });
  };
  network.loader.listComponents(function(err) {
    if (err) {
      return callback(err);
    }
    if (graph.nodes.length === 0) {
      return networkReady(network);
    }
    if (options.delay) {
      callback(null, network);
      return;
    }
    return network.connect(function(err) {
      if (err) {
        return callback(err);
      }
      return networkReady(network);
    });
  });
  return network;
}
```
- example usage
```shell
...
  })(this));
}

Graph.prototype.setGraph = function(graph, callback) {
  this.ready = false;
  if (typeof graph === 'object') {
    if (typeof graph.addNode === 'function') {
      this.createNetwork(graph, callback);
      return;
    }
    noflo.graph.loadJSON(graph, (function(_this) {
      return function(err, instance) {
        if (err) {
          return callback(err);
        }
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket"></a>[function <span class="apidocSignatureSpan">noflo.</span>internalSocket.InternalSocket (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket)
- description and source-code
```javascript
function InternalSocket(metadata) {
  this.metadata = metadata != null ? metadata : {};
  this.brackets = [];
  this.connected = false;
  this.dataDelegate = null;
  this.debug = false;
  this.emitEvent = this.regularEmitEvent;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.isBrowser"></a>[function <span class="apidocSignatureSpan">noflo.</span>isBrowser ()](#apidoc.element.noflo.isBrowser)
- description and source-code
```javascript
isBrowser = function () {
  if (typeof process !== 'undefined' && process.execPath && process.execPath.match(/node|iojs/)) {
    return false;
  }
  return true;
}
```
- example usage
```shell
...
this.initials = [];
this.nextInitials = [];
this.defaults = [];
this.graph = graph;
this.started = false;
this.debug = true;
this.eventBuffer = [];
if (!platform.isBrowser()) {
  this.baseDir = graph.baseDir || process.cwd();
} else {
  this.baseDir = graph.baseDir || '/';
}
this.startupDate = null;
if (graph.componentLoader) {
  this.loader = graph.componentLoader;
...
```

#### <a name="apidoc.element.noflo.journal.JournalStore"></a>[function <span class="apidocSignatureSpan">noflo.</span>journal.JournalStore (graph1)](#apidoc.element.noflo.journal.JournalStore)
- description and source-code
```javascript
function JournalStore(graph1) {
  this.graph = graph1;
  this.lastRevision = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore"></a>[function <span class="apidocSignatureSpan">noflo.</span>journal.MemoryJournalStore (graph)](#apidoc.element.noflo.journal.MemoryJournalStore)
- description and source-code
```javascript
function MemoryJournalStore(graph) {
  MemoryJournalStore.__super__.constructor.call(this, graph);
  this.transactions = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.loadFile"></a>[function <span class="apidocSignatureSpan">noflo.</span>loadFile (file, options, callback)](#apidoc.element.noflo.loadFile)
- description and source-code
```javascript
loadFile = function (file, options, callback) {
  var baseDir;
  if (!callback) {
    callback = options;
    baseDir = null;
  }
  if (callback && typeof options !== 'object') {
    options = {
      baseDir: options
    };
  }
  return exports.graph.loadFile(file, function(err, net) {
    if (err) {
      return callback(err);
    }
    if (options.baseDir) {
      net.baseDir = options.baseDir;
    }
    return exports.createNetwork(net, callback, options);
  });
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (graph.substr(0, 1) !== "/" && graph.substr(1, 1) !== ":" && process && process.cwd) {
  graph = (process.cwd()) + "/" + graph;
}
return noflo.graph.loadFile(graph, (function(_this) {
  return function(err, instance) {
    if (err) {
      return callback(err);
    }
    instance.baseDir = _this.baseDir;
    return _this.createNetwork(instance, callback);
  };
...
```

#### <a name="apidoc.element.noflo.saveFile"></a>[function <span class="apidocSignatureSpan">noflo.</span>saveFile (graph, file, callback)](#apidoc.element.noflo.saveFile)
- description and source-code
```javascript
saveFile = function (graph, file, callback) {
  return exports.graph.save(file, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.IP"></a>[function <span class="apidocSignatureSpan">noflo.</span>streams.IP (data1)](#apidoc.element.noflo.streams.IP)
- description and source-code
```javascript
function IP(data1) {
  this.data = data1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.StreamReceiver"></a>[function <span class="apidocSignatureSpan">noflo.</span>streams.StreamReceiver (port1, buffered, process)](#apidoc.element.noflo.streams.StreamReceiver)
- description and source-code
```javascript
function StreamReceiver(port1, buffered, process) {
  this.port = port1;
  this.buffered = buffered != null ? buffered : false;
  this.process = process != null ? process : null;
  this.q = [];
  this.resetCurrent();
  this.port.process = (function(_this) {
    return function(event, payload, index) {
      var stream;
      switch (event) {
        case 'connect':
          if (typeof _this.process === 'function') {
            return _this.process('connect', index);
          }
          break;
        case 'begingroup':
          _this.level++;
          stream = new Substream(payload);
          if (_this.level === 1) {
            _this.root = stream;
            _this.parent = null;
          } else {
            _this.parent = _this.current;
          }
          return _this.current = stream;
        case 'endgroup':
          if (_this.level > 0) {
            _this.level--;
          }
          if (_this.level === 0) {
            if (_this.buffered) {
              _this.q.push(_this.root);
              _this.process('readable', index);
            } else {
              if (typeof _this.process === 'function') {
                _this.process('data', _this.root, index);
              }
            }
            return _this.resetCurrent();
          } else {
            _this.parent.push(_this.current);
            return _this.current = _this.parent;
          }
          break;
        case 'data':
          if (_this.level === 0) {
            return _this.q.push(new IP(payload));
          } else {
            return _this.current.push(new IP(payload));
          }
          break;
        case 'disconnect':
          if (typeof _this.process === 'function') {
            return _this.process('disconnect', index);
          }
      }
    };
  })(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.StreamSender"></a>[function <span class="apidocSignatureSpan">noflo.</span>streams.StreamSender (port1, ordered)](#apidoc.element.noflo.streams.StreamSender)
- description and source-code
```javascript
function StreamSender(port1, ordered) {
  this.port = port1;
  this.ordered = ordered != null ? ordered : false;
  this.q = [];
  this.resetCurrent();
  this.resolved = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.Substream"></a>[function <span class="apidocSignatureSpan">noflo.</span>streams.Substream (key)](#apidoc.element.noflo.streams.Substream)
- description and source-code
```javascript
function Substream(key) {
  this.key = key;
  this.value = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.ArrayPort"></a>[module noflo.ArrayPort](#apidoc.module.noflo.ArrayPort)

#### <a name="apidoc.element.noflo.ArrayPort.ArrayPort"></a>[function <span class="apidocSignatureSpan">noflo.</span>ArrayPort (type)](#apidoc.element.noflo.ArrayPort.ArrayPort)
- description and source-code
```javascript
function ArrayPort(type) {
  this.type = type;
  platform.deprecated('noflo.ArrayPort is deprecated. Please port to noflo.InPort/noflo.OutPort and use addressable: true');
  ArrayPort.__super__.constructor.call(this, this.type);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.ArrayPort.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.</span>EventEmitter ()](#apidoc.element.noflo.ArrayPort.EventEmitter)
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

#### <a name="apidoc.element.noflo.ArrayPort.init"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.</span>init ()](#apidoc.element.noflo.ArrayPort.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.ArrayPort.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.ArrayPort.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.ArrayPort.prototype"></a>[module noflo.ArrayPort.prototype](#apidoc.module.noflo.ArrayPort.prototype)

#### <a name="apidoc.element.noflo.ArrayPort.prototype.attach"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>attach (socket, socketId)](#apidoc.element.noflo.ArrayPort.prototype.attach)
- description and source-code
```javascript
attach = function (socket, socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    socketId = this.sockets.length;
  }
  this.sockets[socketId] = socket;
  return this.attachSocket(socket, socketId);
}
```
- example usage
```shell
...
  runNetwork = function(network, inputs, options, callback) {
var inPorts, inSockets, outPorts, outSockets, process, received;
process = network.getNode(options.name);
inPorts = Object.keys(network.graph.inports);
inSockets = {};
inPorts.forEach(function(inport) {
  inSockets[inport] = internalSocket.createSocket();
  return process.component.inPorts[inport].attach(inSockets[inport]);
});
received = [];
outPorts = Object.keys(network.graph.outports);
outSockets = {};
outPorts.forEach(function(outport) {
  outSockets[outport] = internalSocket.createSocket();
  process.component.outPorts[outport].attach(outSockets[outport]);
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.beginGroup"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>beginGroup (group, socketId)](#apidoc.element.noflo.ArrayPort.prototype.beginGroup)
- description and source-code
```javascript
beginGroup = function (group, socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    if (!this.sockets.length) {
      throw new Error((this.getId()) + ": No connections available");
    }
    this.sockets.forEach((function(_this) {
      return function(socket, index) {
        if (!socket) {
          return;
        }
        return _this.beginGroup(group, index);
      };
    })(this));
    return;
  }
  if (!this.sockets[socketId]) {
    throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
  }
  if (this.isConnected(socketId)) {
    return this.sockets[socketId].beginGroup(group);
  }
  this.sockets[socketId].once("connect", (function(_this) {
    return function() {
      return _this.sockets[socketId].beginGroup(group);
    };
  })(this));
  return this.sockets[socketId].connect();
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.beginGroup(group, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.connect"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>connect (socketId)](#apidoc.element.noflo.ArrayPort.prototype.connect)
- description and source-code
```javascript
connect = function (socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    if (!this.sockets.length) {
      throw new Error((this.getId()) + ": No connections available");
    }
    this.sockets.forEach(function(socket) {
      if (!socket) {
        return;
      }
      return socket.connect();
    });
    return;
  }
  if (!this.sockets[socketId]) {
    throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
  }
  return this.sockets[socketId].connect();
}
```
- example usage
```shell
...
        return function(err, network1) {
_this.network = network1;
if (err) {
  return callback(err);
}
_this.emit('network', _this.network);
_this.subscribeNetwork(_this.network);
return _this.network.connect(function(err) {
  var name, node, ref;
  if (err) {
    return callback(err);
  }
  ref = _this.network.processes;
  for (name in ref) {
    node = ref[name];
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>constructor (type)](#apidoc.element.noflo.ArrayPort.prototype.constructor)
- description and source-code
```javascript
function ArrayPort(type) {
  this.type = type;
  platform.deprecated('noflo.ArrayPort is deprecated. Please port to noflo.InPort/noflo.OutPort and use addressable: true');
  ArrayPort.__super__.constructor.call(this, this.type);
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>disconnect (socketId)](#apidoc.element.noflo.ArrayPort.prototype.disconnect)
- description and source-code
```javascript
disconnect = function (socketId) {
  var i, len, ref, socket;
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    if (!this.sockets.length) {
      throw new Error((this.getId()) + ": No connections available");
    }
    ref = this.sockets;
    for (i = 0, len = ref.length; i < len; i++) {
      socket = ref[i];
      if (!socket) {
        return;
      }
      socket.disconnect();
    }
    return;
  }
  if (!this.sockets[socketId]) {
    return;
  }
  return this.sockets[socketId].disconnect();
}
```
- example usage
```shell
...
  }
  ref = this.sockets;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    if (!socket) {
      return;
    }
    socket.disconnect();
  }
  return;
}
if (!this.sockets[socketId]) {
  return;
}
return this.sockets[socketId].disconnect();
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.endGroup"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>endGroup (socketId)](#apidoc.element.noflo.ArrayPort.prototype.endGroup)
- description and source-code
```javascript
endGroup = function (socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    if (!this.sockets.length) {
      throw new Error((this.getId()) + ": No connections available");
    }
    this.sockets.forEach((function(_this) {
      return function(socket, index) {
        if (!socket) {
          return;
        }
        return _this.endGroup(index);
      };
    })(this));
    return;
  }
  if (!this.sockets[socketId]) {
    throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
  }
  return this.sockets[socketId].endGroup();
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.endGroup(index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.isAddressable"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>isAddressable ()](#apidoc.element.noflo.ArrayPort.prototype.isAddressable)
- description and source-code
```javascript
isAddressable = function () {
  return true;
}
```
- example usage
```shell
...
  return this.options.description;
};

BasePort.prototype.attach = function(socket, index) {
  if (index == null) {
    index = null;
  }
  if (!this.isAddressable() || index === null) {
    index = this.sockets.length;
  }
  this.sockets[index] = socket;
  this.attachSocket(socket, index);
  if (this.isAddressable()) {
    this.emit('attach', socket, index);
    return;
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.isAttached"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>isAttached (socketId)](#apidoc.element.noflo.ArrayPort.prototype.isAttached)
- description and source-code
```javascript
isAttached = function (socketId) {
  var i, len, ref, socket;
  if (socketId === void 0) {
    ref = this.sockets;
    for (i = 0, len = ref.length; i < len; i++) {
      socket = ref[i];
      if (socket) {
        return true;
      }
    }
    return false;
  }
  if (this.sockets[socketId]) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
    if (_this.load > 0) {
      return _this.q.push({
        name: "disconnect"
      });
    }
    _this.outPorts[_this.outPortName].disconnect();
    _this.errorGroups = [];
    if (_this.outPorts.load.isAttached()) {
      return _this.outPorts.load.disconnect();
    }
  };
})(this));
this.inPorts[this.inPortName].on("data", (function(_this) {
  return function(data) {
    if (_this.q.length > 0) {
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>isConnected (socketId)](#apidoc.element.noflo.ArrayPort.prototype.isConnected)
- description and source-code
```javascript
isConnected = function (socketId) {
  var connected;
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    connected = false;
    this.sockets.forEach(function(socket) {
      if (!socket) {
        return;
      }
      if (socket.isConnected()) {
        return connected = true;
      }
    });
    return connected;
  }
  if (!this.sockets[socketId]) {
    return false;
  }
  return this.sockets[socketId].isConnected();
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
if (this.isConnected(socketId)) {
  return this.sockets[socketId].beginGroup(group);
}
this.sockets[socketId].once("connect", (function(_this) {
  return function() {
    return _this.sockets[socketId].beginGroup(group);
  };
})(this));
...
```

#### <a name="apidoc.element.noflo.ArrayPort.prototype.send"></a>[function <span class="apidocSignatureSpan">noflo.ArrayPort.prototype.</span>send (data, socketId)](#apidoc.element.noflo.ArrayPort.prototype.send)
- description and source-code
```javascript
send = function (data, socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    if (!this.sockets.length) {
      throw new Error((this.getId()) + ": No connections available");
    }
    this.sockets.forEach((function(_this) {
      return function(socket, index) {
        if (!socket) {
          return;
        }
        return _this.send(data, index);
      };
    })(this));
    return;
  }
  if (!this.sockets[socketId]) {
    throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
  }
  if (this.isConnected(socketId)) {
    return this.sockets[socketId].send(data);
  }
  this.sockets[socketId].once("connect", (function(_this) {
    return function() {
      return _this.sockets[socketId].send(data);
    };
  })(this));
  return this.sockets[socketId].connect();
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.send(data, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```



# <a name="apidoc.module.noflo.AsCallback"></a>[module noflo.AsCallback](#apidoc.module.noflo.AsCallback)

#### <a name="apidoc.element.noflo.AsCallback.asCallback"></a>[function <span class="apidocSignatureSpan">noflo.AsCallback.</span>asCallback (component, options)](#apidoc.element.noflo.AsCallback.asCallback)
- description and source-code
```javascript
asCallback = function (component, options) {
  options = normalizeOptions(options, component);
  return function(inputs, callback) {
    return prepareNetwork(component, options, function(err, network) {
      var inputMap, resultType;
      if (err) {
        return callback(err);
      }
      resultType = getType(inputs, network);
      inputMap = prepareInputMap(inputs, resultType, network);
      return runNetwork(network, inputMap, options, function(err, outputMap) {
        if (err) {
          return callback(err);
        }
        return sendOutputMap(outputMap, resultType, options, callback);
      });
    });
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.AsyncComponent"></a>[module noflo.AsyncComponent](#apidoc.module.noflo.AsyncComponent)

#### <a name="apidoc.element.noflo.AsyncComponent.AsyncComponent"></a>[function <span class="apidocSignatureSpan">noflo.</span>AsyncComponent (inPortName, outPortName, errPortName)](#apidoc.element.noflo.AsyncComponent.AsyncComponent)
- description and source-code
```javascript
function AsyncComponent(inPortName, outPortName, errPortName) {
  this.inPortName = inPortName != null ? inPortName : "in";
  this.outPortName = outPortName != null ? outPortName : "out";
  this.errPortName = errPortName != null ? errPortName : "error";
  this.error = bind(this.error, this);
  platform.deprecated('noflo.AsyncComponent is deprecated. Please port to Process API');
  if (!this.inPorts[this.inPortName]) {
    throw new Error("no inPort named '" + this.inPortName + "'");
  }
  if (!this.outPorts[this.outPortName]) {
    throw new Error("no outPort named '" + this.outPortName + "'");
  }
  this.load = 0;
  this.q = [];
  this.errorGroups = [];
  this.outPorts.load = new port.Port();
  this.inPorts[this.inPortName].on("begingroup", (function(_this) {
    return function(group) {
      if (_this.load > 0) {
        return _this.q.push({
          name: "begingroup",
          data: group
        });
      }
      _this.errorGroups.push(group);
      return _this.outPorts[_this.outPortName].beginGroup(group);
    };
  })(this));
  this.inPorts[this.inPortName].on("endgroup", (function(_this) {
    return function() {
      if (_this.load > 0) {
        return _this.q.push({
          name: "endgroup"
        });
      }
      _this.errorGroups.pop();
      return _this.outPorts[_this.outPortName].endGroup();
    };
  })(this));
  this.inPorts[this.inPortName].on("disconnect", (function(_this) {
    return function() {
      if (_this.load > 0) {
        return _this.q.push({
          name: "disconnect"
        });
      }
      _this.outPorts[_this.outPortName].disconnect();
      _this.errorGroups = [];
      if (_this.outPorts.load.isAttached()) {
        return _this.outPorts.load.disconnect();
      }
    };
  })(this));
  this.inPorts[this.inPortName].on("data", (function(_this) {
    return function(data) {
      if (_this.q.length > 0) {
        return _this.q.push({
          name: "data",
          data: data
        });
      }
      return _this.processData(data);
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.AsyncComponent.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>EventEmitter ()](#apidoc.element.noflo.AsyncComponent.EventEmitter)
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

#### <a name="apidoc.element.noflo.AsyncComponent.init"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>init ()](#apidoc.element.noflo.AsyncComponent.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.AsyncComponent.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.</span>listenerCount (emitter, type)](#apidoc.element.noflo.AsyncComponent.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.AsyncComponent.prototype"></a>[module noflo.AsyncComponent.prototype](#apidoc.module.noflo.AsyncComponent.prototype)

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>constructor (inPortName, outPortName, errPortName)](#apidoc.element.noflo.AsyncComponent.prototype.constructor)
- description and source-code
```javascript
function AsyncComponent(inPortName, outPortName, errPortName) {
  this.inPortName = inPortName != null ? inPortName : "in";
  this.outPortName = outPortName != null ? outPortName : "out";
  this.errPortName = errPortName != null ? errPortName : "error";
  this.error = bind(this.error, this);
  platform.deprecated('noflo.AsyncComponent is deprecated. Please port to Process API');
  if (!this.inPorts[this.inPortName]) {
    throw new Error("no inPort named '" + this.inPortName + "'");
  }
  if (!this.outPorts[this.outPortName]) {
    throw new Error("no outPort named '" + this.outPortName + "'");
  }
  this.load = 0;
  this.q = [];
  this.errorGroups = [];
  this.outPorts.load = new port.Port();
  this.inPorts[this.inPortName].on("begingroup", (function(_this) {
    return function(group) {
      if (_this.load > 0) {
        return _this.q.push({
          name: "begingroup",
          data: group
        });
      }
      _this.errorGroups.push(group);
      return _this.outPorts[_this.outPortName].beginGroup(group);
    };
  })(this));
  this.inPorts[this.inPortName].on("endgroup", (function(_this) {
    return function() {
      if (_this.load > 0) {
        return _this.q.push({
          name: "endgroup"
        });
      }
      _this.errorGroups.pop();
      return _this.outPorts[_this.outPortName].endGroup();
    };
  })(this));
  this.inPorts[this.inPortName].on("disconnect", (function(_this) {
    return function() {
      if (_this.load > 0) {
        return _this.q.push({
          name: "disconnect"
        });
      }
      _this.outPorts[_this.outPortName].disconnect();
      _this.errorGroups = [];
      if (_this.outPorts.load.isAttached()) {
        return _this.outPorts.load.disconnect();
      }
    };
  })(this));
  this.inPorts[this.inPortName].on("data", (function(_this) {
    return function(data) {
      if (_this.q.length > 0) {
        return _this.q.push({
          name: "data",
          data: data
        });
      }
      return _this.processData(data);
    };
  })(this));
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.decrementLoad"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>decrementLoad ()](#apidoc.element.noflo.AsyncComponent.prototype.decrementLoad)
- description and source-code
```javascript
decrementLoad = function () {
  if (this.load === 0) {
    throw new Error("load cannot be negative");
  }
  this.load--;
  if (this.outPorts.load.isAttached()) {
    this.outPorts.load.send(this.load);
  }
  if (this.outPorts.load.isAttached()) {
    this.outPorts.load.disconnect();
  }
  if (typeof process !== 'undefined' && process.execPath && process.execPath.indexOf('node') !== -1) {
    return process.nextTick((function(_this) {
      return function() {
        return _this.processQueue();
      };
    })(this));
  } else {
    return setTimeout((function(_this) {
      return function() {
        return _this.processQueue();
      };
    })(this), 0);
  }
}
```
- example usage
```shell
...
AsyncComponent.prototype.processData = function(data) {
  this.incrementLoad();
  return this.doAsync(data, (function(_this) {
    return function(err) {
      if (err) {
        _this.error(err, _this.errorGroups, _this.errPortName);
      }
      return _this.decrementLoad();
    };
  })(this));
};

AsyncComponent.prototype.incrementLoad = function() {
  this.load++;
  if (this.outPorts.load.isAttached()) {
...
```

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.doAsync"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>doAsync (data, callback)](#apidoc.element.noflo.AsyncComponent.prototype.doAsync)
- description and source-code
```javascript
doAsync = function (data, callback) {
  return callback(new Error("AsyncComponents must implement doAsync"));
}
```
- example usage
```shell
...
      return _this.processData(data);
    };
  })(this));
}

AsyncComponent.prototype.processData = function(data) {
  this.incrementLoad();
  return this.doAsync(data, (function(_this) {
    return function(err) {
      if (err) {
        _this.error(err, _this.errorGroups, _this.errPortName);
      }
      return _this.decrementLoad();
    };
  })(this));
...
```

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.error"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>error (e, groups, errorPort)](#apidoc.element.noflo.AsyncComponent.prototype.error)
- description and source-code
```javascript
error = function (e, groups, errorPort) {
  var group, i, j, len, len1;
  if (groups == null) {
    groups = [];
  }
  if (errorPort == null) {
    errorPort = 'error';
  }
  if (this.outPorts[errorPort] && (this.outPorts[errorPort].isAttached() || !this.outPorts[errorPort].isRequired())) {
    for (i = 0, len = groups.length; i < len; i++) {
      group = groups[i];
      this.outPorts[errorPort].beginGroup(group);
    }
    this.outPorts[errorPort].send(e);
    for (j = 0, len1 = groups.length; j < len1; j++) {
      group = groups[j];
      this.outPorts[errorPort].endGroup();
    }
    this.outPorts[errorPort].disconnect();
    return;
  }
  throw e;
}
```
- example usage
```shell
...
  this.inPorts.graph.on('ip', (function(_this) {
    return function(packet) {
      if (packet.type !== 'data') {
        return;
      }
      return _this.setGraph(packet.data, function(err) {
        if (err) {
          return _this.error(err);
        }
      });
    };
  })(this));
}

Graph.prototype.setGraph = function(graph, callback) {
...
```

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.incrementLoad"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>incrementLoad ()](#apidoc.element.noflo.AsyncComponent.prototype.incrementLoad)
- description and source-code
```javascript
incrementLoad = function () {
  this.load++;
  if (this.outPorts.load.isAttached()) {
    this.outPorts.load.send(this.load);
  }
  if (this.outPorts.load.isAttached()) {
    return this.outPorts.load.disconnect();
  }
}
```
- example usage
```shell
...
      }
      return _this.processData(data);
    };
  })(this));
}

AsyncComponent.prototype.processData = function(data) {
  this.incrementLoad();
  return this.doAsync(data, (function(_this) {
    return function(err) {
      if (err) {
        _this.error(err, _this.errorGroups, _this.errPortName);
      }
      return _this.decrementLoad();
    };
...
```

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.processData"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>processData (data)](#apidoc.element.noflo.AsyncComponent.prototype.processData)
- description and source-code
```javascript
processData = function (data) {
  this.incrementLoad();
  return this.doAsync(data, (function(_this) {
    return function(err) {
      if (err) {
        _this.error(err, _this.errorGroups, _this.errPortName);
      }
      return _this.decrementLoad();
    };
  })(this));
}
```
- example usage
```shell
...
    return function(data) {
      if (_this.q.length > 0) {
        return _this.q.push({
          name: "data",
          data: data
        });
      }
      return _this.processData(data);
    };
  })(this));
}

AsyncComponent.prototype.processData = function(data) {
  this.incrementLoad();
  return this.doAsync(data, (function(_this) {
...
```

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.processQueue"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>processQueue ()](#apidoc.element.noflo.AsyncComponent.prototype.processQueue)
- description and source-code
```javascript
processQueue = function () {
  var event, processedData;
  if (this.load > 0) {
    return;
  }
  processedData = false;
  while (this.q.length > 0) {
    event = this.q[0];
    switch (event.name) {
      case "begingroup":
        if (processedData) {
          return;
        }
        this.outPorts[this.outPortName].beginGroup(event.data);
        this.errorGroups.push(event.data);
        this.q.shift();
        break;
      case "endgroup":
        if (processedData) {
          return;
        }
        this.outPorts[this.outPortName].endGroup();
        this.errorGroups.pop();
        this.q.shift();
        break;
      case "disconnect":
        if (processedData) {
          return;
        }
        this.outPorts[this.outPortName].disconnect();
        if (this.outPorts.load.isAttached()) {
          this.outPorts.load.disconnect();
        }
        this.errorGroups = [];
        this.q.shift();
        break;
      case "data":
        this.processData(event.data);
        this.q.shift();
        processedData = true;
    }
  }
}
```
- example usage
```shell
...
}
if (this.outPorts.load.isAttached()) {
  this.outPorts.load.disconnect();
}
if (typeof process !== 'undefined' && process.execPath && process.execPath.indexOf('node') !== -1) {
  return process.nextTick((function(_this) {
    return function() {
      return _this.processQueue();
    };
  })(this));
} else {
  return setTimeout((function(_this) {
    return function() {
      return _this.processQueue();
    };
...
```

#### <a name="apidoc.element.noflo.AsyncComponent.prototype.tearDown"></a>[function <span class="apidocSignatureSpan">noflo.AsyncComponent.prototype.</span>tearDown (callback)](#apidoc.element.noflo.AsyncComponent.prototype.tearDown)
- description and source-code
```javascript
tearDown = function (callback) {
  this.q = [];
  this.errorGroups = [];
  return callback();
}
```
- example usage
```shell
...
      return callback();
    }
    _this.started = false;
    _this.emit('end');
    return callback();
  };
})(this);
return this.tearDown((function(_this) {
  return function(err) {
    var checkLoad;
    if (err) {
      return callback(err);
    }
    if (_this.load > 0) {
      checkLoad = function(load) {
...
```



# <a name="apidoc.module.noflo.BasePort"></a>[module noflo.BasePort](#apidoc.module.noflo.BasePort)

#### <a name="apidoc.element.noflo.BasePort.BasePort"></a>[function <span class="apidocSignatureSpan">noflo.</span>BasePort (options)](#apidoc.element.noflo.BasePort.BasePort)
- description and source-code
```javascript
function BasePort(options) {
  this.handleOptions(options);
  this.sockets = [];
  this.node = null;
  this.name = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.BasePort.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.BasePort.</span>EventEmitter ()](#apidoc.element.noflo.BasePort.EventEmitter)
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

#### <a name="apidoc.element.noflo.BasePort.init"></a>[function <span class="apidocSignatureSpan">noflo.BasePort.</span>init ()](#apidoc.element.noflo.BasePort.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.BasePort.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.BasePort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.BasePort.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.Component"></a>[module noflo.Component](#apidoc.module.noflo.Component)

#### <a name="apidoc.element.noflo.Component.Component"></a>[function <span class="apidocSignatureSpan">noflo.</span>Component (options)](#apidoc.element.noflo.Component.Component)
- description and source-code
```javascript
function Component(options) {
  this.error = bind(this.error, this);
  var ref, ref1, ref2;
  if (!options) {
    options = {};
  }
  if (!options.inPorts) {
    options.inPorts = {};
  }
  if (options.inPorts instanceof ports.InPorts) {
    this.inPorts = options.inPorts;
  } else {
    this.inPorts = new ports.InPorts(options.inPorts);
  }
  if (!options.outPorts) {
    options.outPorts = {};
  }
  if (options.outPorts instanceof ports.OutPorts) {
    this.outPorts = options.outPorts;
  } else {
    this.outPorts = new ports.OutPorts(options.outPorts);
  }
  if (options.icon) {
    this.icon = options.icon;
  }
  if (options.description) {
    this.description = options.description;
  }
  this.started = false;
  this.load = 0;
  this.ordered = (ref = options.ordered) != null ? ref : false;
  this.autoOrdering = (ref1 = options.autoOrdering) != null ? ref1 : null;
  this.outputQ = [];
  this.bracketContext = {
    "in": {},
    out: {}
  };
  this.activateOnInput = (ref2 = options.activateOnInput) != null ? ref2 : true;
  this.forwardBrackets = {
    "in": ['out', 'error']
  };
  if ('forwardBrackets' in options) {
    this.forwardBrackets = options.forwardBrackets;
  }
  if (typeof options.process === 'function') {
    this.process(options.process);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Component.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.Component.</span>EventEmitter ()](#apidoc.element.noflo.Component.EventEmitter)
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

#### <a name="apidoc.element.noflo.Component.init"></a>[function <span class="apidocSignatureSpan">noflo.Component.</span>init ()](#apidoc.element.noflo.Component.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Component.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.Component.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Component.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.Component.prototype"></a>[module noflo.Component.prototype](#apidoc.module.noflo.Component.prototype)

#### <a name="apidoc.element.noflo.Component.prototype.activate"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>activate (context)](#apidoc.element.noflo.Component.prototype.activate)
- description and source-code
```javascript
activate = function (context) {
  if (context.activated) {
    return;
  }
  context.activated = true;
  context.deactivated = false;
  this.load++;
  this.emit('activate', this.load);
  if (this.ordered || this.autoOrdering) {
    return this.outputQ.push(context.result);
  }
}
```
- example usage
```shell
...
var contexts;
contexts = [];
this.network.on('start', (function(_this) {
  return function() {
    var ctx;
    ctx = {};
    contexts.push(ctx);
    return _this.activate(ctx);
  };
})(this));
return this.network.on('end', (function(_this) {
  return function() {
    var ctx;
    ctx = contexts.pop();
    if (!ctx) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.addBracketForwards"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>addBracketForwards (result)](#apidoc.element.noflo.Component.prototype.addBracketForwards)
- description and source-code
```javascript
addBracketForwards = function (result) {
  var context, i, ipClone, j, k, l, len1, len2, len3, len4, port, ref, ref1, ref2, ref3, ref4, ref5;
  if ((ref = result.__bracketClosingBefore) != null ? ref.length : void 0) {
    ref1 = result.__bracketClosingBefore;
    for (i = 0, len1 = ref1.length; i < len1; i++) {
      context = ref1[i];
      debugBrackets(this.nodeId + " closeBracket-A from '" + context.source + "' to " + context.ports + ": '" + context.closeIp.
data + "'");
      if (!context.ports.length) {
        continue;
      }
      ref2 = context.ports;
      for (j = 0, len2 = ref2.length; j < len2; j++) {
        port = ref2[j];
        ipClone = context.closeIp.clone();
        this.addToResult(result, port, ipClone, true);
        this.getBracketContext('out', port, ipClone.scope).pop();
      }
    }
  }
  if (result.__bracketContext) {
    Object.keys(result.__bracketContext).reverse().forEach((function(_this) {
      return function(inport) {
        var ctx, datas, forwardedOpens, idx, idxIps, ip, ips, k, l, len3, len4, len5, m, outport, portIdentifier, results, unforwarded
;
        context = result.__bracketContext[inport];
        if (!context.length) {
          return;
        }
        results = [];
        for (outport in result) {
          ips = result[outport];
          if (outport.indexOf('__') === 0) {
            continue;
          }
          if (_this.outPorts[outport].isAddressable()) {
            for (idx in ips) {
              idxIps = ips[idx];
              datas = idxIps.filter(function(ip) {
                return ip.type === 'data';
              });
              if (!datas.length) {
                continue;
              }
              portIdentifier = outport + "[" + idx + "]";
              unforwarded = _this.getForwardableContexts(inport, portIdentifier, context);
              if (!unforwarded.length) {
                continue;
              }
              forwardedOpens = [];
              for (k = 0, len3 = unforwarded.length; k < len3; k++) {
                ctx = unforwarded[k];
                debugBrackets(_this.nodeId + " openBracket from '" + inport + "' to '" + portIdentifier + "': '" + ctx.ip.data + "'");
                ipClone = ctx.ip.clone();
                ipClone.index = parseInt(idx);
                forwardedOpens.push(ipClone);
                ctx.ports.push(portIdentifier);
                _this.getBracketContext('out', outport, ctx.ip.scope, idx).push(ctx);
              }
              forwardedOpens.reverse();
              for (l = 0, len4 = forwardedOpens.length; l < len4; l++) {
                ip = forwardedOpens[l];
                _this.addToResult(result, outport, ip, true);
              }
            }
            continue;
          }
          datas = ips.filter(function(ip) {
            return ip.type === 'data';
          });
          if (!datas.length) {
            continue;
          }
          unforwarded = _this.getForwardableContexts(inport, outport, context);
          if (!unforwarded.length) {
            continue;
          }
          forwardedOpens = [];
          for (m = 0, len5 = unforwarded.length; m < len5; m++) {
            ctx = unforwarded[m];
            debugBrackets(_this.nodeId + " openBracket from '" + inport + "' to '" + outport + "': '" + ctx.ip.data + "'");
            forwardedOpens.push(ctx.ip.clone());
            ctx.ports.push(outport);
            _this.getBracketContext('out', outport, ctx.ip.scope).push(ctx);
          }
          forwardedOpens.reverse();
          results.push((function() {
            var len6, n, results1;
            results1 = [];
            for (n = 0, len6 = forwardedOpens.length; n < len6; n++) {
              ip = forwardedOpens[n];
              results1.push(this.addToResult(result, outport, ip, true));
            }
            return results1;
          }).call(_this));
        }
        return results;
      };
    })(this));
  }
  if ((ref3 = result.__bracketClosingAfter) != null ? ref3.length : void 0) {
    ref4 = result.__bracketClosingAfter;
    for (k = 0, len3 = ref4.leng ...
```
- example usage
```shell
...
var i, idx, idxIps, ip, ips, j, len1, len2, port, portIdentifier, result, results;
results = [];
while (this.outputQ.length > 0) {
  result = this.outputQ[0];
  if (!result.__resolved) {
    break;
  }
  this.addBracketForwards(result);
  for (port in result) {
    ips = result[port];
    if (port.indexOf('__') === 0) {
      continue;
    }
    if (this.outPorts.ports[port].isAddressable()) {
      for (idx in ips) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.addToResult"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>addToResult (result, port, ip, before)](#apidoc.element.noflo.Component.prototype.addToResult)
- description and source-code
```javascript
addToResult = function (result, port, ip, before) {
  var idx, index, method, name, ref;
  if (before == null) {
    before = false;
  }
  ref = ports.normalizePortName(port), name = ref.name, index = ref.index;
  method = before ? 'unshift' : 'push';
  if (this.outPorts[name].isAddressable()) {
    idx = index ? parseInt(index) : ip.index;
    if (!result[name]) {
      result[name] = {};
    }
    if (!result[name][idx]) {
      result[name][idx] = [];
    }
    ip.index = idx;
    result[name][idx][method](ip);
    return;
  }
  if (!result[name]) {
    result[name] = [];
  }
  return result[name][method](ip);
}
```
- example usage
```shell
...
    if (!context.ports.length) {
      continue;
    }
    ref2 = context.ports;
    for (j = 0, len2 = ref2.length; j < len2; j++) {
      port = ref2[j];
      ipClone = context.closeIp.clone();
      this.addToResult(result, port, ipClone, true);
      this.getBracketContext('out', port, ipClone.scope).pop();
    }
  }
}
if (result.__bracketContext) {
  Object.keys(result.__bracketContext).reverse().forEach((function(_this) {
    return function(inport) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>constructor (options)](#apidoc.element.noflo.Component.prototype.constructor)
- description and source-code
```javascript
function Component(options) {
  this.error = bind(this.error, this);
  var ref, ref1, ref2;
  if (!options) {
    options = {};
  }
  if (!options.inPorts) {
    options.inPorts = {};
  }
  if (options.inPorts instanceof ports.InPorts) {
    this.inPorts = options.inPorts;
  } else {
    this.inPorts = new ports.InPorts(options.inPorts);
  }
  if (!options.outPorts) {
    options.outPorts = {};
  }
  if (options.outPorts instanceof ports.OutPorts) {
    this.outPorts = options.outPorts;
  } else {
    this.outPorts = new ports.OutPorts(options.outPorts);
  }
  if (options.icon) {
    this.icon = options.icon;
  }
  if (options.description) {
    this.description = options.description;
  }
  this.started = false;
  this.load = 0;
  this.ordered = (ref = options.ordered) != null ? ref : false;
  this.autoOrdering = (ref1 = options.autoOrdering) != null ? ref1 : null;
  this.outputQ = [];
  this.bracketContext = {
    "in": {},
    out: {}
  };
  this.activateOnInput = (ref2 = options.activateOnInput) != null ? ref2 : true;
  this.forwardBrackets = {
    "in": ['out', 'error']
  };
  if ('forwardBrackets' in options) {
    this.forwardBrackets = options.forwardBrackets;
  }
  if (typeof options.process === 'function') {
    this.process(options.process);
  }
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.deactivate"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>deactivate (context)](#apidoc.element.noflo.Component.prototype.deactivate)
- description and source-code
```javascript
deactivate = function (context) {
  if (context.deactivated) {
    return;
  }
  context.deactivated = true;
  context.activated = false;
  if (this.isOrdered()) {
    this.processOutputQueue();
  }
  this.load--;
  return this.emit('deactivate', this.load);
}
```
- example usage
```shell
...
  return this.network.on('end', (function(_this) {
    return function() {
      var ctx;
      ctx = contexts.pop();
      if (!ctx) {
        return;
      }
      return _this.deactivate(ctx);
    };
  })(this));
};

Graph.prototype.isExportedInport = function(port, nodeName, portName) {
  var exported, i, len, priv, pub, ref, ref1;
  ref = this.network.graph.inports;
...
```

#### <a name="apidoc.element.noflo.Component.prototype.error"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>error (e, groups, errorPort, scope)](#apidoc.element.noflo.Component.prototype.error)
- description and source-code
```javascript
error = function (e, groups, errorPort, scope) {
  var group, i, j, len1, len2;
  if (groups == null) {
    groups = [];
  }
  if (errorPort == null) {
    errorPort = 'error';
  }
  if (scope == null) {
    scope = null;
  }
  if (this.outPorts[errorPort] && (this.outPorts[errorPort].isAttached() || !this.outPorts[errorPort].isRequired())) {
    for (i = 0, len1 = groups.length; i < len1; i++) {
      group = groups[i];
      this.outPorts[errorPort].openBracket(group, {
        scope: scope
      });
    }
    this.outPorts[errorPort].data(e, {
      scope: scope
    });
    for (j = 0, len2 = groups.length; j < len2; j++) {
      group = groups[j];
      this.outPorts[errorPort].closeBracket(group, {
        scope: scope
      });
    }
    return;
  }
  throw e;
}
```
- example usage
```shell
...
  this.inPorts.graph.on('ip', (function(_this) {
    return function(packet) {
      if (packet.type !== 'data') {
        return;
      }
      return _this.setGraph(packet.data, function(err) {
        if (err) {
          return _this.error(err);
        }
      });
    };
  })(this));
}

Graph.prototype.setGraph = function(graph, callback) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.getBracketContext"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getBracketContext (type, port, scope, idx)](#apidoc.element.noflo.Component.prototype.getBracketContext)
- description and source-code
```javascript
getBracketContext = function (type, port, scope, idx) {
  var index, name, portsList, ref;
  ref = ports.normalizePortName(port), name = ref.name, index = ref.index;
  if (idx != null) {
    index = idx;
  }
  portsList = type === 'in' ? this.inPorts : this.outPorts;
  if (portsList[name].isAddressable()) {
    port = name + "[" + index + "]";
  }
  if (!this.bracketContext[type][port]) {
    this.bracketContext[type][port] = {};
  }
  if (!this.bracketContext[type][port][scope]) {
    this.bracketContext[type][port][scope] = [];
  }
  return this.bracketContext[type][port][scope];
}
```
- example usage
```shell
...
  return ip.type === 'data';
});
if (this.outputQ.length >= this.load && dataPackets.length === 0) {
  if (buf[0] !== ip) {
    return;
  }
  port.get(ip.scope, ip.index);
  context = this.getBracketContext('in', port.name, ip.scope, ip.index).pop();
  context.closeIp = ip;
  debugBrackets(this.nodeId + " closeBracket-C from '" + context.source + "' to " + context.ports + ": '" + ip.data + "'");
  result = {
    __resolved: true,
    __bracketClosingAfter: [context]
  };
  this.outputQ.push(result);
...
```

#### <a name="apidoc.element.noflo.Component.prototype.getDescription"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getDescription ()](#apidoc.element.noflo.Component.prototype.getDescription)
- description and source-code
```javascript
getDescription = function () {
  return this.description;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Component.prototype.getForwardableContexts"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getForwardableContexts (inport, outport, contexts)](#apidoc.element.noflo.Component.prototype.getForwardableContexts)
- description and source-code
```javascript
getForwardableContexts = function (inport, outport, contexts) {
  var forwardable, index, name, ref;
  ref = ports.normalizePortName(outport), name = ref.name, index = ref.index;
  forwardable = [];
  contexts.forEach((function(_this) {
    return function(ctx, idx) {
      var outContext;
      if (!_this.isForwardingOutport(inport, name)) {
        return;
      }
      if (ctx.ports.indexOf(outport) !== -1) {
        return;
      }
      outContext = _this.getBracketContext('out', name, ctx.ip.scope, index)[idx];
      if (outContext) {
        if (outContext.ip.data === ctx.ip.data && outContext.ports.indexOf(outport) !== -1) {
          return;
        }
      }
      return forwardable.push(ctx);
    };
  })(this));
  return forwardable;
}
```
- example usage
```shell
...
datas = idxIps.filter(function(ip) {
  return ip.type === 'data';
});
if (!datas.length) {
  continue;
}
portIdentifier = outport + "[" + idx + "]";
unforwarded = _this.getForwardableContexts(inport, portIdentifier, context);
if (!unforwarded.length) {
  continue;
}
forwardedOpens = [];
for (k = 0, len3 = unforwarded.length; k < len3; k++) {
  ctx = unforwarded[k];
  debugBrackets(_this.nodeId + " openBracket from '" + inport + "' to '" + portIdentifier + "': '" + ctx.ip.data + "'");
...
```

#### <a name="apidoc.element.noflo.Component.prototype.getIcon"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>getIcon ()](#apidoc.element.noflo.Component.prototype.getIcon)
- description and source-code
```javascript
getIcon = function () {
  return this.icon;
}
```
- example usage
```shell
...
      });
    };
  })(this));
};

ComponentLoader.prototype.setIcon = function(name, instance) {
  var componentName, library, ref;
  if (!instance.getIcon || instance.getIcon()) {
    return;
  }
  ref = name.split('/'), library = ref[0], componentName = ref[1];
  if (componentName && this.getLibraryIcon(library)) {
    instance.setIcon(this.getLibraryIcon(library));
    return;
  }
...
```

#### <a name="apidoc.element.noflo.Component.prototype.handleIP"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>handleIP (ip, port)](#apidoc.element.noflo.Component.prototype.handleIP)
- description and source-code
```javascript
handleIP = function (ip, port) {
  var buf, context, dataPackets, e, error1, input, output, result;
  if (!port.options.triggering) {
    return;
  }
  if (ip.type === 'openBracket' && this.autoOrdering === null && !this.ordered) {
    debug(this.nodeId + " port '" + port.name + "' entered auto-ordering mode");
    this.autoOrdering = true;
  }
  result = {};
  if (this.isForwardingInport(port)) {
    if (ip.type === 'openBracket') {
      return;
    }
    if (ip.type === 'closeBracket') {
      buf = port.getBuffer(ip.scope, ip.index);
      dataPackets = buf.filter(function(ip) {
        return ip.type === 'data';
      });
      if (this.outputQ.length >= this.load && dataPackets.length === 0) {
        if (buf[0] !== ip) {
          return;
        }
        port.get(ip.scope, ip.index);
        context = this.getBracketContext('in', port.name, ip.scope, ip.index).pop();
        context.closeIp = ip;
        debugBrackets(this.nodeId + " closeBracket-C from '" + context.source + "' to " + context.ports + ": '" + ip.data + "'");
        result = {
          __resolved: true,
          __bracketClosingAfter: [context]
        };
        this.outputQ.push(result);
        this.processOutputQueue();
      }
      if (!dataPackets.length) {
        return;
      }
    }
  }
  context = new ProcessContext(ip, this, port, result);
  input = new ProcessInput(this.inPorts, context);
  output = new ProcessOutput(this.outPorts, context);
  try {
    this.handle(input, output, context);
  } catch (error1) {
    e = error1;
    this.deactivate(context);
    output.sendDone(e);
  }
  if (context.activated) {
    return;
  }
  if (port.isAddressable()) {
    debug(this.nodeId + " packet on '" + port.name + "[" + ip.index + "]' didn't match preconditions: " + ip.type);
    return;
  }
  debug(this.nodeId + " packet on '" + port.name + "' didn't match preconditions: " + ip.type);
}
```
- example usage
```shell
...
ref = this.inPorts.ports;
fn = (function(_this) {
  return function(name, port) {
    if (!port.name) {
      port.name = name;
    }
    return port.on('ip', function(ip) {
      return _this.handleIP(ip, port);
    });
  };
})(this);
for (name in ref) {
  port = ref[name];
  fn(name, port);
}
...
```

#### <a name="apidoc.element.noflo.Component.prototype.isForwardingInport"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isForwardingInport (port)](#apidoc.element.noflo.Component.prototype.isForwardingInport)
- description and source-code
```javascript
isForwardingInport = function (port) {
  var portName;
  if (typeof port === 'string') {
    portName = port;
  } else {
    portName = port.name;
  }
  if (portName in this.forwardBrackets) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
  return;
}
if (ip.type === 'openBracket' && this.autoOrdering === null && !this.ordered) {
  debug(this.nodeId + " port '" + port.name + "' entered auto-ordering mode");
  this.autoOrdering = true;
}
result = {};
if (this.isForwardingInport(port)) {
  if (ip.type === 'openBracket') {
    return;
  }
  if (ip.type === 'closeBracket') {
    buf = port.getBuffer(ip.scope, ip.index);
    dataPackets = buf.filter(function(ip) {
      return ip.type === 'data';
...
```

#### <a name="apidoc.element.noflo.Component.prototype.isForwardingOutport"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isForwardingOutport (inport, outport)](#apidoc.element.noflo.Component.prototype.isForwardingOutport)
- description and source-code
```javascript
isForwardingOutport = function (inport, outport) {
  var inportName, outportName;
  if (typeof inport === 'string') {
    inportName = inport;
  } else {
    inportName = inport.name;
  }
  if (typeof outport === 'string') {
    outportName = outport;
  } else {
    outportName = outport.name;
  }
  if (!this.forwardBrackets[inportName]) {
    return false;
  }
  if (this.forwardBrackets[inportName].indexOf(outportName) !== -1) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
    Component.prototype.getForwardableContexts = function(inport, outport, contexts) {
var forwardable, index, name, ref;
ref = ports.normalizePortName(outport), name = ref.name, index = ref.index;
forwardable = [];
contexts.forEach((function(_this) {
  return function(ctx, idx) {
    var outContext;
    if (!_this.isForwardingOutport(inport, name)) {
      return;
    }
    if (ctx.ports.indexOf(outport) !== -1) {
      return;
    }
    outContext = _this.getBracketContext('out', name, ctx.ip.scope, index)[idx];
    if (outContext) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.isLegacy"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isLegacy ()](#apidoc.element.noflo.Component.prototype.isLegacy)
- description and source-code
```javascript
isLegacy = function () {
  if (this.handle) {
    return false;
  }
  if (this._wpData) {
    return false;
  }
  return true;
}
```
- example usage
```shell
...
      data: ip.data,
      metadata: socket.metadata
    });
  };
})(this));
socket.on('connect', (function(_this) {
  return function() {
    if (source && source.component.isLegacy()) {
      if (!source.component.__openConnections) {
        source.component.__openConnections = 0;
      }
      source.component.__openConnections++;
    }
    return _this.bufferedEmit('connect', {
      id: socket.getId(),
...
```

#### <a name="apidoc.element.noflo.Component.prototype.isOrdered"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isOrdered ()](#apidoc.element.noflo.Component.prototype.isOrdered)
- description and source-code
```javascript
isOrdered = function () {
  if (this.ordered) {
    return true;
  }
  if (this.autoOrdering) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...

Component.prototype.deactivate = function(context) {
  if (context.deactivated) {
    return;
  }
  context.deactivated = true;
  context.activated = false;
  if (this.isOrdered()) {
    this.processOutputQueue();
  }
  this.load--;
  return this.emit('deactivate', this.load);
};

return Component;
...
```

#### <a name="apidoc.element.noflo.Component.prototype.isReady"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isReady ()](#apidoc.element.noflo.Component.prototype.isReady)
- description and source-code
```javascript
isReady = function () {
  return true;
}
```
- example usage
```shell
...

Graph.prototype.isSubgraph = function() {
  return true;
};

Graph.prototype.setUp = function(callback) {
  this.starting = true;
  if (!this.isReady()) {
    this.once('ready', (function(_this) {
      return function() {
        return _this.setUp(callback);
      };
    })(this));
    return;
  }
...
```

#### <a name="apidoc.element.noflo.Component.prototype.isStarted"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isStarted ()](#apidoc.element.noflo.Component.prototype.isStarted)
- description and source-code
```javascript
isStarted = function () {
  return this.started;
}
```
- example usage
```shell
...
  }
  this.inPorts.add(targetPortName, port);
  this.inPorts[targetPortName].once('connect', (function(_this) {
    return function() {
      if (_this.starting) {
        return;
      }
      if (_this.isStarted()) {
        return;
      }
      return _this.start(function() {});
    };
  })(this));
}
for (portName in outPorts) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.isSubgraph"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>isSubgraph ()](#apidoc.element.noflo.Component.prototype.isSubgraph)
- description and source-code
```javascript
isSubgraph = function () {
  return false;
}
```
- example usage
```shell
...
    return;
  }
  ref = name.split('/'), library = ref[0], componentName = ref[1];
  if (componentName && this.getLibraryIcon(library)) {
    instance.setIcon(this.getLibraryIcon(library));
    return;
  }
  if (instance.isSubgraph()) {
    instance.setIcon('sitemap');
    return;
  }
  instance.setIcon('square');
};

ComponentLoader.prototype.getLibraryIcon = function(prefix) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.prepareForwarding"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>prepareForwarding ()](#apidoc.element.noflo.Component.prototype.prepareForwarding)
- description and source-code
```javascript
prepareForwarding = function () {
  var i, inPort, len1, outPort, outPorts, ref, results, tmp;
  ref = this.forwardBrackets;
  results = [];
  for (inPort in ref) {
    outPorts = ref[inPort];
    if (!(inPort in this.inPorts.ports)) {
      delete this.forwardBrackets[inPort];
      continue;
    }
    tmp = [];
    for (i = 0, len1 = outPorts.length; i < len1; i++) {
      outPort = outPorts[i];
      if (outPort in this.outPorts.ports) {
        tmp.push(outPort);
      }
    }
    if (tmp.length === 0) {
      results.push(delete this.forwardBrackets[inPort]);
    } else {
      results.push(this.forwardBrackets[inPort] = tmp);
    }
  }
  return results;
}
```
- example usage
```shell
...
var fn, name, port, ref;
if (typeof handle !== 'function') {
  throw new Error("Process handler must be a function");
}
if (!this.inPorts) {
  throw new Error("Component ports must be defined before process function");
}
this.prepareForwarding();
this.handle = handle;
ref = this.inPorts.ports;
fn = (function(_this) {
  return function(name, port) {
    if (!port.name) {
      port.name = name;
    }
...
```

#### <a name="apidoc.element.noflo.Component.prototype.process"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>process (handle)](#apidoc.element.noflo.Component.prototype.process)
- description and source-code
```javascript
process = function (handle) {
  var fn, name, port, ref;
  if (typeof handle !== 'function') {
    throw new Error("Process handler must be a function");
  }
  if (!this.inPorts) {
    throw new Error("Component ports must be defined before process function");
  }
  this.prepareForwarding();
  this.handle = handle;
  ref = this.inPorts.ports;
  fn = (function(_this) {
    return function(name, port) {
      if (!port.name) {
        port.name = name;
      }
      return port.on('ip', function(ip) {
        return _this.handleIP(ip, port);
      });
    };
  })(this);
  for (name in ref) {
    port = ref[name];
    fn(name, port);
  }
  return this;
}
```
- example usage
```shell
...
  this.forwardBrackets = {
    "in": ['out', 'error']
  };
  if ('forwardBrackets' in options) {
    this.forwardBrackets = options.forwardBrackets;
  }
  if (typeof options.process === 'function') {
    this.process(options.process);
  }
}

Component.prototype.getDescription = function() {
  return this.description;
};
...
```

#### <a name="apidoc.element.noflo.Component.prototype.processOutputQueue"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>processOutputQueue ()](#apidoc.element.noflo.Component.prototype.processOutputQueue)
- description and source-code
```javascript
processOutputQueue = function () {
  var i, idx, idxIps, ip, ips, j, len1, len2, port, portIdentifier, result, results;
  results = [];
  while (this.outputQ.length > 0) {
    result = this.outputQ[0];
    if (!result.__resolved) {
      break;
    }
    this.addBracketForwards(result);
    for (port in result) {
      ips = result[port];
      if (port.indexOf('__') === 0) {
        continue;
      }
      if (this.outPorts.ports[port].isAddressable()) {
        for (idx in ips) {
          idxIps = ips[idx];
          idx = parseInt(idx);
          if (!this.outPorts.ports[port].isAttached(idx)) {
            continue;
          }
          for (i = 0, len1 = idxIps.length; i < len1; i++) {
            ip = idxIps[i];
            portIdentifier = port + "[" + ip.index + "]";
            if (ip.type === 'openBracket') {
              debugSend(this.nodeId + " sending " + portIdentifier + " < '" + ip.data + "'");
            } else if (ip.type === 'closeBracket') {
              debugSend(this.nodeId + " sending " + portIdentifier + " > '" + ip.data + "'");
            } else {
              debugSend(this.nodeId + " sending " + portIdentifier + " DATA");
            }
            this.outPorts[port].sendIP(ip);
          }
        }
        continue;
      }
      if (!this.outPorts.ports[port].isAttached()) {
        continue;
      }
      for (j = 0, len2 = ips.length; j < len2; j++) {
        ip = ips[j];
        portIdentifier = port;
        if (ip.type === 'openBracket') {
          debugSend(this.nodeId + " sending " + portIdentifier + " < '" + ip.data + "'");
        } else if (ip.type === 'closeBracket') {
          debugSend(this.nodeId + " sending " + portIdentifier + " > '" + ip.data + "'");
        } else {
          debugSend(this.nodeId + " sending " + portIdentifier + " DATA");
        }
        this.outPorts[port].sendIP(ip);
      }
    }
    results.push(this.outputQ.shift());
  }
  return results;
}
```
- example usage
```shell
...
      context.closeIp = ip;
      debugBrackets(this.nodeId + " closeBracket-C from '" + context.source + "' to " + context.ports + ": '" + ip.data + "'");
      result = {
        __resolved: true,
        __bracketClosingAfter: [context]
      };
      this.outputQ.push(result);
      this.processOutputQueue();
    }
    if (!dataPackets.length) {
      return;
    }
  }
}
context = new ProcessContext(ip, this, port, result);
...
```

#### <a name="apidoc.element.noflo.Component.prototype.setIcon"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>setIcon (icon)](#apidoc.element.noflo.Component.prototype.setIcon)
- description and source-code
```javascript
setIcon = function (icon) {
  this.icon = icon;
  return this.emit('icon', this.icon);
}
```
- example usage
```shell
...
      }
      if (name === 'Graph') {
        instance.baseDir = _this.baseDir;
      }
      if (typeof name === 'string') {
        instance.componentName = name;
      }
      _this.setIcon(name, instance);
      return callback(null, instance);
    };
  })(this));
};

ComponentLoader.prototype.createComponent = function(name, component, metadata, callback) {
  var implementation, instance;
...
```

#### <a name="apidoc.element.noflo.Component.prototype.setUp"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>setUp (callback)](#apidoc.element.noflo.Component.prototype.setUp)
- description and source-code
```javascript
setUp = function (callback) {
  return callback();
}
```
- example usage
```shell
...
};

Graph.prototype.setUp = function(callback) {
  this.starting = true;
  if (!this.isReady()) {
    this.once('ready', (function(_this) {
      return function() {
        return _this.setUp(callback);
      };
    })(this));
    return;
  }
  if (!this.network) {
    return callback(null);
  }
...
```

#### <a name="apidoc.element.noflo.Component.prototype.shutdown"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>shutdown (callback)](#apidoc.element.noflo.Component.prototype.shutdown)
- description and source-code
```javascript
shutdown = function (callback) {
  var finalize;
  finalize = (function(_this) {
    return function() {
      var inPort, inPorts, portName;
      inPorts = _this.inPorts.ports || _this.inPorts;
      for (portName in inPorts) {
        inPort = inPorts[portName];
        if (typeof inPort.clear !== 'function') {
          continue;
        }
        inPort.clear();
      }
      _this.bracketContext = {
        "in": {},
        out: {}
      };
      if (!_this.isStarted()) {
        return callback();
      }
      _this.started = false;
      _this.emit('end');
      return callback();
    };
  })(this);
  return this.tearDown((function(_this) {
    return function(err) {
      var checkLoad;
      if (err) {
        return callback(err);
      }
      if (_this.load > 0) {
        checkLoad = function(load) {
          if (load > 0) {
            return;
          }
          this.removeListener('deactivate', checkLoad);
          return finalize();
        };
        _this.on('deactivate', checkLoad);
        return;
      }
      return finalize();
    };
  })(this));
}
```
- example usage
```shell
...
  })(this));
};

Network.prototype.removeNode = function(node, callback) {
  if (!this.processes[node.id]) {
    return callback(new Error("Node " + node.id + " not found"));
  }
  return this.processes[node.id].component.shutdown((function(_this) {
    return function(err) {
      if (err) {
        return callback(err);
      }
      delete _this.processes[node.id];
      return callback(null);
    };
...
```

#### <a name="apidoc.element.noflo.Component.prototype.start"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>start (callback)](#apidoc.element.noflo.Component.prototype.start)
- description and source-code
```javascript
start = function (callback) {
  if (this.isStarted()) {
    return callback();
  }
  return this.setUp((function(_this) {
    return function(err) {
      if (err) {
        return callback(err);
      }
      _this.started = true;
      _this.emit('start');
      return callback(null);
    };
  })(this));
}
```
- example usage
```shell
...
    return function() {
      if (_this.starting) {
        return;
      }
      if (_this.isStarted()) {
        return;
      }
      return _this.start(function() {});
    };
  })(this));
}
for (portName in outPorts) {
  port = outPorts[portName];
  targetPortName = this.isExportedOutport(port, name, portName);
  if (targetPortName === false) {
...
```

#### <a name="apidoc.element.noflo.Component.prototype.tearDown"></a>[function <span class="apidocSignatureSpan">noflo.Component.prototype.</span>tearDown (callback)](#apidoc.element.noflo.Component.prototype.tearDown)
- description and source-code
```javascript
tearDown = function (callback) {
  return callback();
}
```
- example usage
```shell
...
      return callback();
    }
    _this.started = false;
    _this.emit('end');
    return callback();
  };
})(this);
return this.tearDown((function(_this) {
  return function(err) {
    var checkLoad;
    if (err) {
      return callback(err);
    }
    if (_this.load > 0) {
      checkLoad = function(load) {
...
```



# <a name="apidoc.module.noflo.ComponentLoader"></a>[module noflo.ComponentLoader](#apidoc.module.noflo.ComponentLoader)

#### <a name="apidoc.element.noflo.ComponentLoader.ComponentLoader"></a>[function <span class="apidocSignatureSpan">noflo.</span>ComponentLoader (baseDir, options)](#apidoc.element.noflo.ComponentLoader.ComponentLoader)
- description and source-code
```javascript
function ComponentLoader(baseDir, options) {
  this.baseDir = baseDir;
  this.options = options != null ? options : {};
  this.components = null;
  this.libraryIcons = {};
  this.processing = false;
  this.ready = false;
  if (typeof this.setMaxListeners === 'function') {
    this.setMaxListeners(0);
  }
}
```
- example usage
```shell
...
  } else {
    this.baseDir = graph.baseDir || '/';
  }
  this.startupDate = null;
  if (graph.componentLoader) {
    this.loader = graph.componentLoader;
  } else {
    this.loader = new componentLoader.ComponentLoader(this.baseDir, this.options);
  }
}

Network.prototype.uptime = function() {
  if (!this.startupDate) {
    return 0;
  }
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>EventEmitter ()](#apidoc.element.noflo.ComponentLoader.EventEmitter)
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

#### <a name="apidoc.element.noflo.ComponentLoader.init"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>init ()](#apidoc.element.noflo.ComponentLoader.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.ComponentLoader.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.</span>listenerCount (emitter, type)](#apidoc.element.noflo.ComponentLoader.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.ComponentLoader.prototype"></a>[module noflo.ComponentLoader.prototype](#apidoc.module.noflo.ComponentLoader.prototype)

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.clear"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>clear ()](#apidoc.element.noflo.ComponentLoader.prototype.clear)
- description and source-code
```javascript
clear = function () {
  this.components = null;
  this.ready = false;
  return this.processing = false;
}
```
- example usage
```shell
...
var inPort, inPorts, portName;
inPorts = _this.inPorts.ports || _this.inPorts;
for (portName in inPorts) {
  inPort = inPorts[portName];
  if (typeof inPort.clear !== 'function') {
    continue;
  }
  inPort.clear();
}
_this.bracketContext = {
  "in": {},
  out: {}
};
if (!_this.isStarted()) {
  return callback();
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>constructor (baseDir, options)](#apidoc.element.noflo.ComponentLoader.prototype.constructor)
- description and source-code
```javascript
function ComponentLoader(baseDir, options) {
  this.baseDir = baseDir;
  this.options = options != null ? options : {};
  this.components = null;
  this.libraryIcons = {};
  this.processing = false;
  this.ready = false;
  if (typeof this.setMaxListeners === 'function') {
    this.setMaxListeners(0);
  }
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.createComponent"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>createComponent (name, component, metadata, callback)](#apidoc.element.noflo.ComponentLoader.prototype.createComponent)
- description and source-code
```javascript
createComponent = function (name, component, metadata, callback) {
  var implementation, instance;
  implementation = component;
  if (!implementation) {
    return callback(new Error("Component " + name + " not available"));
  }
  if (typeof implementation === 'string') {
    if (typeof registerLoader.dynamicLoad === 'function') {
      registerLoader.dynamicLoad(name, implementation, metadata, callback);
      return;
    }
    return callback(Error("Dynamic loading of " + implementation + " for component " + name + " not available on this platform."));
  }
  if (typeof implementation.getComponent === 'function') {
    instance = implementation.getComponent(metadata);
  } else if (typeof implementation === 'function') {
    instance = implementation(metadata);
  } else {
    callback(new Error("Invalid type " + (typeof implementation) + " for component " + name + "."));
    return;
  }
  return callback(null, instance);
}
```
- example usage
```shell
...
      return function() {
        return _this.loadGraph(name, component, callback, metadata);
      };
    })(this), 0);
  }
  return;
}
return this.createComponent(name, component, metadata, (function(_this) {
  return function(err, instance) {
    if (err) {
      return callback(err);
    }
    if (!instance) {
      callback(new Error("Component " + name + " could not be loaded."));
      return;
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.getLibraryIcon"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>getLibraryIcon (prefix)](#apidoc.element.noflo.ComponentLoader.prototype.getLibraryIcon)
- description and source-code
```javascript
getLibraryIcon = function (prefix) {
  if (this.libraryIcons[prefix]) {
    return this.libraryIcons[prefix];
  }
  return null;
}
```
- example usage
```shell
...

    ComponentLoader.prototype.setIcon = function(name, instance) {
var componentName, library, ref;
if (!instance.getIcon || instance.getIcon()) {
  return;
}
ref = name.split('/'), library = ref[0], componentName = ref[1];
if (componentName && this.getLibraryIcon(library)) {
  instance.setIcon(this.getLibraryIcon(library));
  return;
}
if (instance.isSubgraph()) {
  instance.setIcon('sitemap');
  return;
}
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.getModulePrefix"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>getModulePrefix (name)](#apidoc.element.noflo.ComponentLoader.prototype.getModulePrefix)
- description and source-code
```javascript
getModulePrefix = function (name) {
  if (!name) {
    return '';
  }
  if (name === 'noflo') {
    return '';
  }
  if (name[0] === '@') {
    name = name.replace(/\@[a-z\-]+\//, '');
  }
  return name.replace('noflo-', '');
}
```
- example usage
```shell
...

ComponentLoader.prototype.setLibraryIcon = function(prefix, icon) {
  return this.libraryIcons[prefix] = icon;
};

ComponentLoader.prototype.normalizeName = function(packageId, name) {
  var fullName, prefix;
  prefix = this.getModulePrefix(packageId);
  fullName = prefix + "/" + name;
  if (!packageId) {
    fullName = name;
  }
  return fullName;
};
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.getSource"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>getSource (name, callback)](#apidoc.element.noflo.ComponentLoader.prototype.getSource)
- description and source-code
```javascript
getSource = function (name, callback) {
  if (!registerLoader.getSource) {
    return callback(new Error('getSource not allowed'));
  }
  if (!this.ready) {
    this.listComponents((function(_this) {
      return function(err) {
        if (err) {
          return callback(err);
        }
        return _this.getSource(name, callback);
      };
    })(this));
    return;
  }
  return registerLoader.getSource(this, name, callback);
}
```
- example usage
```shell
...
  }
  if (!this.ready) {
    this.listComponents((function(_this) {
      return function(err) {
        if (err) {
          return callback(err);
        }
        return _this.getSource(name, callback);
      };
    })(this));
    return;
  }
  return registerLoader.getSource(this, name, callback);
};
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.isGraph"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>isGraph (cPath)](#apidoc.element.noflo.ComponentLoader.prototype.isGraph)
- description and source-code
```javascript
isGraph = function (cPath) {
  if (typeof cPath === 'object' && cPath instanceof fbpGraph.Graph) {
    return true;
  }
  if (typeof cPath === 'object' && cPath.processes && cPath.connections) {
    return true;
  }
  if (typeof cPath !== 'string') {
    return false;
  }
  return cPath.indexOf('.fbp') !== -1 || cPath.indexOf('.json') !== -1;
}
```
- example usage
```shell
...
    }
  }
  if (!component) {
    callback(new Error("Component " + name + " not available with base " + this.baseDir));
    return;
  }
}
if (this.isGraph(component)) {
  if (typeof process !== 'undefined' && process.execPath && process.execPath.indexOf('node') !== -1) {
    process.nextTick((function(_this) {
      return function() {
        return _this.loadGraph(name, component, callback, metadata);
      };
    })(this));
  } else {
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.listComponents"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>listComponents (callback)](#apidoc.element.noflo.ComponentLoader.prototype.listComponents)
- description and source-code
```javascript
listComponents = function (callback) {
  if (this.processing) {
    this.once('ready', (function(_this) {
      return function() {
        return callback(null, _this.components);
      };
    })(this));
    return;
  }
  if (this.components) {
    return callback(null, this.components);
  }
  this.ready = false;
  this.processing = true;
  this.components = {};
  registerLoader.register(this, (function(_this) {
    return function(err) {
      if (err) {
        if (callback) {
          return callback(err);
        }
        throw err;
      }
      _this.processing = false;
      _this.ready = true;
      _this.emit('ready', true);
      if (callback) {
        return callback(null, _this.components);
      }
    };
  })(this));
}
```
- example usage
```shell
...
    };
  })(this));
};

ComponentLoader.prototype.load = function(name, callback, metadata) {
  var component, componentName;
  if (!this.ready) {
    this.listComponents((function(_this) {
      return function(err) {
        if (err) {
          return callback(err);
        }
        return _this.load(name, callback, metadata);
      };
    })(this));
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.load"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>load (name, callback, metadata)](#apidoc.element.noflo.ComponentLoader.prototype.load)
- description and source-code
```javascript
load = function (name, callback, metadata) {
  var component, componentName;
  if (!this.ready) {
    this.listComponents((function(_this) {
      return function(err) {
        if (err) {
          return callback(err);
        }
        return _this.load(name, callback, metadata);
      };
    })(this));
    return;
  }
  component = this.components[name];
  if (!component) {
    for (componentName in this.components) {
      if (componentName.split('/')[1] === name) {
        component = this.components[componentName];
        break;
      }
    }
    if (!component) {
      callback(new Error("Component " + name + " not available with base " + this.baseDir));
      return;
    }
  }
  if (this.isGraph(component)) {
    if (typeof process !== 'undefined' && process.execPath && process.execPath.indexOf('node') !== -1) {
      process.nextTick((function(_this) {
        return function() {
          return _this.loadGraph(name, component, callback, metadata);
        };
      })(this));
    } else {
      setTimeout((function(_this) {
        return function() {
          return _this.loadGraph(name, component, callback, metadata);
        };
      })(this), 0);
    }
    return;
  }
  return this.createComponent(name, component, metadata, (function(_this) {
    return function(err, instance) {
      if (err) {
        return callback(err);
      }
      if (!instance) {
        callback(new Error("Component " + name + " could not be loaded."));
        return;
      }
      if (name === 'Graph') {
        instance.baseDir = _this.baseDir;
      }
      if (typeof name === 'string') {
        instance.componentName = name;
      }
      _this.setIcon(name, instance);
      return callback(null, instance);
    };
  })(this));
}
```
- example usage
```shell
...
  if (!options.raw) {
    options.raw = false;
  }
  return options;
};

prepareNetwork = function(component, options, callback) {
  return options.loader.load(component, function(err, instance) {
    var def, graph, inPorts, network, nodeName, outPorts, port;
    if (err) {
      return callback(err);
    }
    graph = new Graph(options.name);
    nodeName = options.name;
    graph.addNode(nodeName, component);
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.loadGraph"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>loadGraph (name, component, callback, metadata)](#apidoc.element.noflo.ComponentLoader.prototype.loadGraph)
- description and source-code
```javascript
loadGraph = function (name, component, callback, metadata) {
  this.createComponent(name, this.components['Graph'], metadata, (function(_this) {
    return function(err, graph) {
      var graphSocket;
      if (err) {
        return callback(err);
      }
      graphSocket = internalSocket.createSocket();
      graph.loader = _this;
      graph.baseDir = _this.baseDir;
      graph.inPorts.remove('graph');
      graph.setGraph(component, function(err) {
        if (err) {
          return callback(err);
        }
        _this.setIcon(name, graph);
        return callback(null, graph);
      });
    };
  })(this));
}
```
- example usage
```shell
...
    return;
  }
}
if (this.isGraph(component)) {
  if (typeof process !== 'undefined' && process.execPath && process.execPath.indexOf('node') !== -1) {
    process.nextTick((function(_this) {
      return function() {
        return _this.loadGraph(name, component, callback, metadata);
      };
    })(this));
  } else {
    setTimeout((function(_this) {
      return function() {
        return _this.loadGraph(name, component, callback, metadata);
      };
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.normalizeName"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>normalizeName (packageId, name)](#apidoc.element.noflo.ComponentLoader.prototype.normalizeName)
- description and source-code
```javascript
normalizeName = function (packageId, name) {
  var fullName, prefix;
  prefix = this.getModulePrefix(packageId);
  fullName = prefix + "/" + name;
  if (!packageId) {
    fullName = name;
  }
  return fullName;
}
```
- example usage
```shell
...
    fullName = name;
  }
  return fullName;
};

ComponentLoader.prototype.registerComponent = function(packageId, name, cPath, callback) {
  var fullName;
  fullName = this.normalizeName(packageId, name);
  this.components[fullName] = cPath;
  if (callback) {
    return callback();
  }
};

ComponentLoader.prototype.registerGraph = function(packageId, name, gPath, callback) {
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.registerComponent"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>registerComponent (packageId, name, cPath, callback)](#apidoc.element.noflo.ComponentLoader.prototype.registerComponent)
- description and source-code
```javascript
registerComponent = function (packageId, name, cPath, callback) {
  var fullName;
  fullName = this.normalizeName(packageId, name);
  this.components[fullName] = cPath;
  if (callback) {
    return callback();
  }
}
```
- example usage
```shell
...
  this.components[fullName] = cPath;
  if (callback) {
    return callback();
  }
};

ComponentLoader.prototype.registerGraph = function(packageId, name, gPath, callback) {
  return this.registerComponent(packageId, name, gPath, callback);
};

ComponentLoader.prototype.registerLoader = function(loader, callback) {
  return loader(this, callback);
};

ComponentLoader.prototype.setSource = function(packageId, name, source, language, callback) {
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.registerGraph"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>registerGraph (packageId, name, gPath, callback)](#apidoc.element.noflo.ComponentLoader.prototype.registerGraph)
- description and source-code
```javascript
registerGraph = function (packageId, name, gPath, callback) {
  return this.registerComponent(packageId, name, gPath, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.registerLoader"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>registerLoader (loader, callback)](#apidoc.element.noflo.ComponentLoader.prototype.registerLoader)
- description and source-code
```javascript
registerLoader = function (loader, callback) {
  return loader(this, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.setIcon"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>setIcon (name, instance)](#apidoc.element.noflo.ComponentLoader.prototype.setIcon)
- description and source-code
```javascript
setIcon = function (name, instance) {
  var componentName, library, ref;
  if (!instance.getIcon || instance.getIcon()) {
    return;
  }
  ref = name.split('/'), library = ref[0], componentName = ref[1];
  if (componentName && this.getLibraryIcon(library)) {
    instance.setIcon(this.getLibraryIcon(library));
    return;
  }
  if (instance.isSubgraph()) {
    instance.setIcon('sitemap');
    return;
  }
  instance.setIcon('square');
}
```
- example usage
```shell
...
      }
      if (name === 'Graph') {
        instance.baseDir = _this.baseDir;
      }
      if (typeof name === 'string') {
        instance.componentName = name;
      }
      _this.setIcon(name, instance);
      return callback(null, instance);
    };
  })(this));
};

ComponentLoader.prototype.createComponent = function(name, component, metadata, callback) {
  var implementation, instance;
...
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.setLibraryIcon"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>setLibraryIcon (prefix, icon)](#apidoc.element.noflo.ComponentLoader.prototype.setLibraryIcon)
- description and source-code
```javascript
setLibraryIcon = function (prefix, icon) {
  return this.libraryIcons[prefix] = icon;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.ComponentLoader.prototype.setSource"></a>[function <span class="apidocSignatureSpan">noflo.ComponentLoader.prototype.</span>setSource (packageId, name, source, language, callback)](#apidoc.element.noflo.ComponentLoader.prototype.setSource)
- description and source-code
```javascript
setSource = function (packageId, name, source, language, callback) {
  if (!registerLoader.setSource) {
    return callback(new Error('setSource not allowed'));
  }
  if (!this.ready) {
    this.listComponents((function(_this) {
      return function(err) {
        if (err) {
          return callback(err);
        }
        return _this.setSource(packageId, name, source, language, callback);
      };
    })(this));
    return;
  }
  return registerLoader.setSource(this, packageId, name, source, language, callback);
}
```
- example usage
```shell
...
  }
  if (!this.ready) {
    this.listComponents((function(_this) {
      return function(err) {
        if (err) {
          return callback(err);
        }
        return _this.setSource(packageId, name, source, language, callback);
      };
    })(this));
    return;
  }
  return registerLoader.setSource(this, packageId, name, source, language, callback);
};
...
```



# <a name="apidoc.module.noflo.Graph"></a>[module noflo.Graph](#apidoc.module.noflo.Graph)

#### <a name="apidoc.element.noflo.Graph.Graph"></a>[function <span class="apidocSignatureSpan">noflo.</span>Graph (name1, options)](#apidoc.element.noflo.Graph.Graph)
- description and source-code
```javascript
function Graph(name1, options) {
  this.name = name1 != null ? name1 : '';
  if (options == null) {
    options = {};
  }
  this.properties = {};
  this.nodes = [];
  this.edges = [];
  this.initializers = [];
  this.exports = [];
  this.inports = {};
  this.outports = {};
  this.groups = [];
  this.transaction = {
    id: null,
    depth: 0
  };
  this.caseSensitive = options.caseSensitive || false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.Graph.</span>EventEmitter ()](#apidoc.element.noflo.Graph.EventEmitter)
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

#### <a name="apidoc.element.noflo.Graph.init"></a>[function <span class="apidocSignatureSpan">noflo.Graph.</span>init ()](#apidoc.element.noflo.Graph.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.Graph.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Graph.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.Graph.prototype"></a>[module noflo.Graph.prototype](#apidoc.module.noflo.Graph.prototype)

#### <a name="apidoc.element.noflo.Graph.prototype.addEdge"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addEdge (outNode, outPort, inNode, inPort, metadata)](#apidoc.element.noflo.Graph.prototype.addEdge)
- description and source-code
```javascript
addEdge = function (outNode, outPort, inNode, inPort, metadata) {
  var edge, i, len, ref;
  if (metadata == null) {
    metadata = {};
  }
  outPort = this.getPortName(outPort);
  inPort = this.getPortName(inPort);
  ref = this.edges;
  for (i = 0, len = ref.length; i < len; i++) {
    edge = ref[i];
    if (edge.from.node === outNode && edge.from.port === outPort && edge.to.node === inNode && edge.to.port === inPort) {
      return;
    }
  }
  if (!this.getNode(outNode)) {
    return;
  }
  if (!this.getNode(inNode)) {
    return;
  }
  this.checkTransactionStart();
  edge = {
    from: {
      node: outNode,
      port: outPort
    },
    to: {
      node: inNode,
      port: inPort
    },
    metadata: metadata
  };
  this.edges.push(edge);
  this.emit('addEdge', edge);
  this.checkTransactionEnd();
  return edge;
}
```
- example usage
```shell
...
}
if (!from.component) {
  return callback(new Error("No component defined for outbound node " + edge.from.node));
}
if (!from.component.isReady()) {
  from.component.once("ready", (function(_this) {
    return function() {
      return _this.addEdge(edge, callback);
    };
  })(this));
  return;
}
to = this.getNode(edge.to.node);
if (!to) {
  return callback(new Error("No process defined for inbound node " + edge.to.node));
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.addEdgeIndex"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addEdgeIndex (outNode, outPort, outIndex, inNode, inPort, inIndex, metadata)](#apidoc.element.noflo.Graph.prototype.addEdgeIndex)
- description and source-code
```javascript
addEdgeIndex = function (outNode, outPort, outIndex, inNode, inPort, inIndex, metadata) {
  var edge;
  if (metadata == null) {
    metadata = {};
  }
  if (!this.getNode(outNode)) {
    return;
  }
  if (!this.getNode(inNode)) {
    return;
  }
  outPort = this.getPortName(outPort);
  inPort = this.getPortName(inPort);
  if (inIndex === null) {
    inIndex = void 0;
  }
  if (outIndex === null) {
    outIndex = void 0;
  }
  if (!metadata) {
    metadata = {};
  }
  this.checkTransactionStart();
  edge = {
    from: {
      node: outNode,
      port: outPort,
      index: outIndex
    },
    to: {
      node: inNode,
      port: inPort,
      index: inIndex
    },
    metadata: metadata
  };
  this.edges.push(edge);
  this.emit('addEdge', edge);
  this.checkTransactionEnd();
  return edge;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.addExport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addExport (publicPort, nodeKey, portKey, metadata)](#apidoc.element.noflo.Graph.prototype.addExport)
- description and source-code
```javascript
addExport = function (publicPort, nodeKey, portKey, metadata) {
  var exported;
  if (metadata == null) {
    metadata = {
      x: 0,
      y: 0
    };
  }
  platform.deprecated('fbp-graph.Graph exports is deprecated: please use specific inport or outport instead');
  if (!this.getNode(nodeKey)) {
    return;
  }
  this.checkTransactionStart();
  exported = {
    "public": this.getPortName(publicPort),
    process: nodeKey,
    port: this.getPortName(portKey),
    metadata: metadata
  };
  this.exports.push(exported);
  this.emit('addExport', exported);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.addGraphInitial"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addGraphInitial (data, node, metadata)](#apidoc.element.noflo.Graph.prototype.addGraphInitial)
- description and source-code
```javascript
addGraphInitial = function (data, node, metadata) {
  var inport;
  inport = this.inports[node];
  if (!inport) {
    return;
  }
  return this.addInitial(data, inport.process, inport.port, metadata);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.addGraphInitialIndex"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addGraphInitialIndex (data, node, index, metadata)](#apidoc.element.noflo.Graph.prototype.addGraphInitialIndex)
- description and source-code
```javascript
addGraphInitialIndex = function (data, node, index, metadata) {
  var inport;
  inport = this.inports[node];
  if (!inport) {
    return;
  }
  return this.addInitialIndex(data, inport.process, inport.port, index, metadata);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.addGroup"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addGroup (group, nodes, metadata)](#apidoc.element.noflo.Graph.prototype.addGroup)
- description and source-code
```javascript
addGroup = function (group, nodes, metadata) {
  var g;
  this.checkTransactionStart();
  g = {
    name: group,
    nodes: nodes,
    metadata: metadata
  };
  this.groups.push(g);
  this.emit('addGroup', g);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.addInitial"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addInitial (data, node, port, metadata)](#apidoc.element.noflo.Graph.prototype.addInitial)
- description and source-code
```javascript
addInitial = function (data, node, port, metadata) {
  var initializer;
  if (!this.getNode(node)) {
    return;
  }
  port = this.getPortName(port);
  this.checkTransactionStart();
  initializer = {
    from: {
      data: data
    },
    to: {
      node: node,
      port: port
    },
    metadata: metadata
  };
  this.initializers.push(initializer);
  this.emit('addInitial', initializer);
  this.checkTransactionEnd();
  return initializer;
}
```
- example usage
```shell
...
}
if (!(to.component.isReady() || to.component.inPorts[initializer.to.port])) {
  if (to.component.setMaxListeners) {
    to.component.setMaxListeners(0);
  }
  to.component.once("ready", (function(_this) {
    return function() {
      return _this.addInitial(initializer, callback);
    };
  })(this));
  return;
}
this.connectPort(socket, to, initializer.to.port, initializer.to.index, true);
this.connections.push(socket);
init = {
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.addInitialIndex"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addInitialIndex (data, node, port, index, metadata)](#apidoc.element.noflo.Graph.prototype.addInitialIndex)
- description and source-code
```javascript
addInitialIndex = function (data, node, port, index, metadata) {
  var initializer;
  if (!this.getNode(node)) {
    return;
  }
  if (index === null) {
    index = void 0;
  }
  port = this.getPortName(port);
  this.checkTransactionStart();
  initializer = {
    from: {
      data: data
    },
    to: {
      node: node,
      port: port,
      index: index
    },
    metadata: metadata
  };
  this.initializers.push(initializer);
  this.emit('addInitial', initializer);
  this.checkTransactionEnd();
  return initializer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.addInport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addInport (publicPort, nodeKey, portKey, metadata)](#apidoc.element.noflo.Graph.prototype.addInport)
- description and source-code
```javascript
addInport = function (publicPort, nodeKey, portKey, metadata) {
  if (!this.getNode(nodeKey)) {
    return;
  }
  publicPort = this.getPortName(publicPort);
  this.checkTransactionStart();
  this.inports[publicPort] = {
    process: nodeKey,
    port: this.getPortName(portKey),
    metadata: metadata
  };
  this.emit('addInport', publicPort, this.inports[publicPort]);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
...
  for (i = 0, len = ref1.length; i < len; i++) {
    exported = ref1[i];
    if (!(exported.process === nodeName && exported.port === portName)) {
      continue;
    }
    this.network.graph.checkTransactionStart();
    this.network.graph.removeExport(exported["public"]);
    this.network.graph.addInport(exported["public"], exported.process, exported.port, exported.metadata);
    this.network.graph.checkTransactionEnd();
    return exported["public"];
  }
  return false;
};

Graph.prototype.isExportedOutport = function(port, nodeName, portName) {
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.addNode"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addNode (id, component, metadata)](#apidoc.element.noflo.Graph.prototype.addNode)
- description and source-code
```javascript
addNode = function (id, component, metadata) {
  var node;
  this.checkTransactionStart();
  if (!metadata) {
    metadata = {};
  }
  node = {
    id: id,
    component: component,
    metadata: metadata
  };
  this.nodes.push(node);
  this.emit('addNode', node);
  this.checkTransactionEnd();
  return node;
}
```
- example usage
```shell
...
    return options.loader.load(component, function(err, instance) {
var def, graph, inPorts, network, nodeName, outPorts, port;
if (err) {
  return callback(err);
}
graph = new Graph(options.name);
nodeName = options.name;
graph.addNode(nodeName, component);
inPorts = instance.inPorts.ports || instance.inPorts;
outPorts = instance.outPorts.ports || instance.outPorts;
for (port in inPorts) {
  def = inPorts[port];
  graph.addInport(port, nodeName, port);
}
for (port in outPorts) {
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.addOutport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>addOutport (publicPort, nodeKey, portKey, metadata)](#apidoc.element.noflo.Graph.prototype.addOutport)
- description and source-code
```javascript
addOutport = function (publicPort, nodeKey, portKey, metadata) {
  if (!this.getNode(nodeKey)) {
    return;
  }
  publicPort = this.getPortName(publicPort);
  this.checkTransactionStart();
  this.outports[publicPort] = {
    process: nodeKey,
    port: this.getPortName(portKey),
    metadata: metadata
  };
  this.emit('addOutport', publicPort, this.outports[publicPort]);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
...
  for (i = 0, len = ref1.length; i < len; i++) {
    exported = ref1[i];
    if (!(exported.process === nodeName && exported.port === portName)) {
      continue;
    }
    this.network.graph.checkTransactionStart();
    this.network.graph.removeExport(exported["public"]);
    this.network.graph.addOutport(exported["public"], exported.process, exported.port, exported.metadata);
    this.network.graph.checkTransactionEnd();
    return exported["public"];
  }
  return false;
};

Graph.prototype.setToReady = function() {
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.checkTransactionEnd"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>checkTransactionEnd ()](#apidoc.element.noflo.Graph.prototype.checkTransactionEnd)
- description and source-code
```javascript
checkTransactionEnd = function () {
  if (this.transaction.id === 'implicit') {
    this.transaction.depth -= 1;
  }
  if (this.transaction.depth === 0) {
    return this.endTransaction('implicit');
  }
}
```
- example usage
```shell
...
    exported = ref1[i];
    if (!(exported.process === nodeName && exported.port === portName)) {
      continue;
    }
    this.network.graph.checkTransactionStart();
    this.network.graph.removeExport(exported["public"]);
    this.network.graph.addInport(exported["public"], exported.process, exported.port, exported.metadata);
    this.network.graph.checkTransactionEnd();
    return exported["public"];
  }
  return false;
};

Graph.prototype.isExportedOutport = function(port, nodeName, portName) {
  var exported, i, len, priv, pub, ref, ref1;
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.checkTransactionStart"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>checkTransactionStart ()](#apidoc.element.noflo.Graph.prototype.checkTransactionStart)
- description and source-code
```javascript
checkTransactionStart = function () {
  if (!this.transaction.id) {
    return this.startTransaction('implicit');
  } else if (this.transaction.id === 'implicit') {
    return this.transaction.depth += 1;
  }
}
```
- example usage
```shell
...
  }
  ref1 = this.network.graph.exports;
  for (i = 0, len = ref1.length; i < len; i++) {
    exported = ref1[i];
    if (!(exported.process === nodeName && exported.port === portName)) {
      continue;
    }
    this.network.graph.checkTransactionStart();
    this.network.graph.removeExport(exported["public"]);
    this.network.graph.addInport(exported["public"], exported.process, exported.port, exported.metadata);
    this.network.graph.checkTransactionEnd();
    return exported["public"];
  }
  return false;
};
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>constructor (name1, options)](#apidoc.element.noflo.Graph.prototype.constructor)
- description and source-code
```javascript
function Graph(name1, options) {
  this.name = name1 != null ? name1 : '';
  if (options == null) {
    options = {};
  }
  this.properties = {};
  this.nodes = [];
  this.edges = [];
  this.initializers = [];
  this.exports = [];
  this.inports = {};
  this.outports = {};
  this.groups = [];
  this.transaction = {
    id: null,
    depth: 0
  };
  this.caseSensitive = options.caseSensitive || false;
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.endTransaction"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>endTransaction (id, metadata)](#apidoc.element.noflo.Graph.prototype.endTransaction)
- description and source-code
```javascript
endTransaction = function (id, metadata) {
  if (!this.transaction.id) {
    throw Error("Attempted to end non-existing transaction");
  }
  this.transaction.id = null;
  this.transaction.depth = 0;
  return this.emit('endTransaction', id, metadata);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.getEdge"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>getEdge (node, port, node2, port2)](#apidoc.element.noflo.Graph.prototype.getEdge)
- description and source-code
```javascript
getEdge = function (node, port, node2, port2) {
  var edge, i, index, len, ref;
  port = this.getPortName(port);
  port2 = this.getPortName(port2);
  ref = this.edges;
  for (index = i = 0, len = ref.length; i < len; index = ++i) {
    edge = ref[index];
    if (!edge) {
      continue;
    }
    if (edge.from.node === node && edge.from.port === port) {
      if (edge.to.node === node2 && edge.to.port === port2) {
        return edge;
      }
    }
  }
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.getNode"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>getNode (id)](#apidoc.element.noflo.Graph.prototype.getNode)
- description and source-code
```javascript
getNode = function (id) {
  var i, len, node, ref;
  ref = this.nodes;
  for (i = 0, len = ref.length; i < len; i++) {
    node = ref[i];
    if (!node) {
      continue;
    }
    if (node.id === id) {
      return node;
    }
  }
  return null;
}
```
- example usage
```shell
...
      return callback(null, network);
    });
  });
};

runNetwork = function(network, inputs, options, callback) {
  var inPorts, inSockets, outPorts, outSockets, process, received;
  process = network.getNode(options.name);
  inPorts = Object.keys(network.graph.inports);
  inSockets = {};
  inPorts.forEach(function(inport) {
    inSockets[inport] = internalSocket.createSocket();
    return process.component.inPorts[inport].attach(inSockets[inport]);
  });
  received = [];
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.getPortName"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>getPortName (port)](#apidoc.element.noflo.Graph.prototype.getPortName)
- description and source-code
```javascript
getPortName = function (port) {
  if (this.caseSensitive) {
    return port;
  } else {
    return port.toLowerCase();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeEdge"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeEdge (node, port, node2, port2)](#apidoc.element.noflo.Graph.prototype.removeEdge)
- description and source-code
```javascript
removeEdge = function (node, port, node2, port2) {
  var edge, i, index, j, k, len, len1, len2, ref, ref1, toKeep, toRemove;
  this.checkTransactionStart();
  port = this.getPortName(port);
  port2 = this.getPortName(port2);
  toRemove = [];
  toKeep = [];
  if (node2 && port2) {
    ref = this.edges;
    for (index = i = 0, len = ref.length; i < len; index = ++i) {
      edge = ref[index];
      if (edge.from.node === node && edge.from.port === port && edge.to.node === node2 && edge.to.port === port2) {
        this.setEdgeMetadata(edge.from.node, edge.from.port, edge.to.node, edge.to.port, {});
        toRemove.push(edge);
      } else {
        toKeep.push(edge);
      }
    }
  } else {
    ref1 = this.edges;
    for (index = j = 0, len1 = ref1.length; j < len1; index = ++j) {
      edge = ref1[index];
      if ((edge.from.node === node && edge.from.port === port) || (edge.to.node === node && edge.to.port === port)) {
        this.setEdgeMetadata(edge.from.node, edge.from.port, edge.to.node, edge.to.port, {});
        toRemove.push(edge);
      } else {
        toKeep.push(edge);
      }
    }
  }
  this.edges = toKeep;
  for (k = 0, len2 = toRemove.length; k < len2; k++) {
    edge = toRemove[k];
    this.emit('removeEdge', edge);
  }
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeExport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeExport (publicPort)](#apidoc.element.noflo.Graph.prototype.removeExport)
- description and source-code
```javascript
removeExport = function (publicPort) {
  var exported, found, i, idx, len, ref;
  platform.deprecated('fbp-graph.Graph exports is deprecated: please use specific inport or outport instead');
  publicPort = this.getPortName(publicPort);
  found = null;
  ref = this.exports;
  for (idx = i = 0, len = ref.length; i < len; idx = ++i) {
    exported = ref[idx];
    if (exported["public"] === publicPort) {
      found = exported;
    }
  }
  if (!found) {
    return;
  }
  this.checkTransactionStart();
  this.exports.splice(this.exports.indexOf(found), 1);
  this.emit('removeExport', found);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
...
  ref1 = this.network.graph.exports;
  for (i = 0, len = ref1.length; i < len; i++) {
    exported = ref1[i];
    if (!(exported.process === nodeName && exported.port === portName)) {
      continue;
    }
    this.network.graph.checkTransactionStart();
    this.network.graph.removeExport(exported["public"]);
    this.network.graph.addInport(exported["public"], exported.process, exported.port, exported.metadata);
    this.network.graph.checkTransactionEnd();
    return exported["public"];
  }
  return false;
};
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeGraphInitial"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeGraphInitial (node)](#apidoc.element.noflo.Graph.prototype.removeGraphInitial)
- description and source-code
```javascript
removeGraphInitial = function (node) {
  var inport;
  inport = this.inports[node];
  if (!inport) {
    return;
  }
  return this.removeInitial(inport.process, inport.port);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeGroup"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeGroup (groupName)](#apidoc.element.noflo.Graph.prototype.removeGroup)
- description and source-code
```javascript
removeGroup = function (groupName) {
  var group, i, len, ref;
  this.checkTransactionStart();
  ref = this.groups;
  for (i = 0, len = ref.length; i < len; i++) {
    group = ref[i];
    if (!group) {
      continue;
    }
    if (group.name !== groupName) {
      continue;
    }
    this.setGroupMetadata(group.name, {});
    this.groups.splice(this.groups.indexOf(group), 1);
    this.emit('removeGroup', group);
  }
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeInitial"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeInitial (node, port)](#apidoc.element.noflo.Graph.prototype.removeInitial)
- description and source-code
```javascript
removeInitial = function (node, port) {
  var edge, i, index, j, len, len1, ref, toKeep, toRemove;
  port = this.getPortName(port);
  this.checkTransactionStart();
  toRemove = [];
  toKeep = [];
  ref = this.initializers;
  for (index = i = 0, len = ref.length; i < len; index = ++i) {
    edge = ref[index];
    if (edge.to.node === node && edge.to.port === port) {
      toRemove.push(edge);
    } else {
      toKeep.push(edge);
    }
  }
  this.initializers = toKeep;
  for (j = 0, len1 = toRemove.length; j < len1; j++) {
    edge = toRemove[j];
    this.emit('removeInitial', edge);
  }
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeInport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeInport (publicPort)](#apidoc.element.noflo.Graph.prototype.removeInport)
- description and source-code
```javascript
removeInport = function (publicPort) {
  var port;
  publicPort = this.getPortName(publicPort);
  if (!this.inports[publicPort]) {
    return;
  }
  this.checkTransactionStart();
  port = this.inports[publicPort];
  this.setInportMetadata(publicPort, {});
  delete this.inports[publicPort];
  this.emit('removeInport', publicPort, port);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeNode"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeNode (id)](#apidoc.element.noflo.Graph.prototype.removeNode)
- description and source-code
```javascript
removeNode = function (id) {
  var edge, exported, group, i, index, initializer, j, k, l, len, len1, len2, len3, len4, len5, len6, len7, len8, m, n, node, o,
p, priv, pub, q, ref, ref1, ref2, ref3, ref4, ref5, toRemove;
  node = this.getNode(id);
  if (!node) {
    return;
  }
  this.checkTransactionStart();
  toRemove = [];
  ref = this.edges;
  for (i = 0, len = ref.length; i < len; i++) {
    edge = ref[i];
    if ((edge.from.node === node.id) || (edge.to.node === node.id)) {
      toRemove.push(edge);
    }
  }
  for (j = 0, len1 = toRemove.length; j < len1; j++) {
    edge = toRemove[j];
    this.removeEdge(edge.from.node, edge.from.port, edge.to.node, edge.to.port);
  }
  toRemove = [];
  ref1 = this.initializers;
  for (k = 0, len2 = ref1.length; k < len2; k++) {
    initializer = ref1[k];
    if (initializer.to.node === node.id) {
      toRemove.push(initializer);
    }
  }
  for (l = 0, len3 = toRemove.length; l < len3; l++) {
    initializer = toRemove[l];
    this.removeInitial(initializer.to.node, initializer.to.port);
  }
  toRemove = [];
  ref2 = this.exports;
  for (m = 0, len4 = ref2.length; m < len4; m++) {
    exported = ref2[m];
    if (this.getPortName(id) === exported.process) {
      toRemove.push(exported);
    }
  }
  for (n = 0, len5 = toRemove.length; n < len5; n++) {
    exported = toRemove[n];
    this.removeExport(exported["public"]);
  }
  toRemove = [];
  ref3 = this.inports;
  for (pub in ref3) {
    priv = ref3[pub];
    if (priv.process === id) {
      toRemove.push(pub);
    }
  }
  for (o = 0, len6 = toRemove.length; o < len6; o++) {
    pub = toRemove[o];
    this.removeInport(pub);
  }
  toRemove = [];
  ref4 = this.outports;
  for (pub in ref4) {
    priv = ref4[pub];
    if (priv.process === id) {
      toRemove.push(pub);
    }
  }
  for (p = 0, len7 = toRemove.length; p < len7; p++) {
    pub = toRemove[p];
    this.removeOutport(pub);
  }
  ref5 = this.groups;
  for (q = 0, len8 = ref5.length; q < len8; q++) {
    group = ref5[q];
    if (!group) {
      continue;
    }
    index = group.nodes.indexOf(id);
    if (index === -1) {
      continue;
    }
    group.nodes.splice(index, 1);
  }
  this.setNodeMetadata(id, {});
  if (-1 !== this.nodes.indexOf(node)) {
    this.nodes.splice(this.nodes.indexOf(node), 1);
  }
  this.emit('removeNode', node);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.removeOutport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>removeOutport (publicPort)](#apidoc.element.noflo.Graph.prototype.removeOutport)
- description and source-code
```javascript
removeOutport = function (publicPort) {
  var port;
  publicPort = this.getPortName(publicPort);
  if (!this.outports[publicPort]) {
    return;
  }
  this.checkTransactionStart();
  port = this.outports[publicPort];
  this.setOutportMetadata(publicPort, {});
  delete this.outports[publicPort];
  this.emit('removeOutport', publicPort, port);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.renameGroup"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameGroup (oldName, newName)](#apidoc.element.noflo.Graph.prototype.renameGroup)
- description and source-code
```javascript
renameGroup = function (oldName, newName) {
  var group, i, len, ref;
  this.checkTransactionStart();
  ref = this.groups;
  for (i = 0, len = ref.length; i < len; i++) {
    group = ref[i];
    if (!group) {
      continue;
    }
    if (group.name !== oldName) {
      continue;
    }
    group.name = newName;
    this.emit('renameGroup', oldName, newName);
  }
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.renameInport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameInport (oldPort, newPort)](#apidoc.element.noflo.Graph.prototype.renameInport)
- description and source-code
```javascript
renameInport = function (oldPort, newPort) {
  oldPort = this.getPortName(oldPort);
  newPort = this.getPortName(newPort);
  if (!this.inports[oldPort]) {
    return;
  }
  this.checkTransactionStart();
  this.inports[newPort] = this.inports[oldPort];
  delete this.inports[oldPort];
  this.emit('renameInport', oldPort, newPort);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.renameNode"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameNode (oldId, newId)](#apidoc.element.noflo.Graph.prototype.renameNode)
- description and source-code
```javascript
renameNode = function (oldId, newId) {
  var edge, exported, group, i, iip, index, j, k, l, len, len1, len2, len3, node, priv, pub, ref, ref1, ref2, ref3, ref4, ref5;
  this.checkTransactionStart();
  node = this.getNode(oldId);
  if (!node) {
    return;
  }
  node.id = newId;
  ref = this.edges;
  for (i = 0, len = ref.length; i < len; i++) {
    edge = ref[i];
    if (!edge) {
      continue;
    }
    if (edge.from.node === oldId) {
      edge.from.node = newId;
    }
    if (edge.to.node === oldId) {
      edge.to.node = newId;
    }
  }
  ref1 = this.initializers;
  for (j = 0, len1 = ref1.length; j < len1; j++) {
    iip = ref1[j];
    if (!iip) {
      continue;
    }
    if (iip.to.node === oldId) {
      iip.to.node = newId;
    }
  }
  ref2 = this.inports;
  for (pub in ref2) {
    priv = ref2[pub];
    if (priv.process === oldId) {
      priv.process = newId;
    }
  }
  ref3 = this.outports;
  for (pub in ref3) {
    priv = ref3[pub];
    if (priv.process === oldId) {
      priv.process = newId;
    }
  }
  ref4 = this.exports;
  for (k = 0, len2 = ref4.length; k < len2; k++) {
    exported = ref4[k];
    if (exported.process === oldId) {
      exported.process = newId;
    }
  }
  ref5 = this.groups;
  for (l = 0, len3 = ref5.length; l < len3; l++) {
    group = ref5[l];
    if (!group) {
      continue;
    }
    index = group.nodes.indexOf(oldId);
    if (index === -1) {
      continue;
    }
    group.nodes[index] = newId;
  }
  this.emit('renameNode', oldId, newId);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
...
      return;
    }
    processing = true;
    op = graphOps.shift();
    cb = processOps;
    switch (op.op) {
      case 'renameNode':
        return _this.renameNode(op.details.from, op.details.to, cb);
      default:
        return _this[op.op](op.details, cb);
    }
  };
})(this);
this.graph.on('addNode', function(node) {
  registerOp('addNode', node);
...
```

#### <a name="apidoc.element.noflo.Graph.prototype.renameOutport"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>renameOutport (oldPort, newPort)](#apidoc.element.noflo.Graph.prototype.renameOutport)
- description and source-code
```javascript
renameOutport = function (oldPort, newPort) {
  oldPort = this.getPortName(oldPort);
  newPort = this.getPortName(newPort);
  if (!this.outports[oldPort]) {
    return;
  }
  this.checkTransactionStart();
  this.outports[newPort] = this.outports[oldPort];
  delete this.outports[oldPort];
  this.emit('renameOutport', oldPort, newPort);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.save"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>save (file, callback)](#apidoc.element.noflo.Graph.prototype.save)
- description and source-code
```javascript
save = function (file, callback) {
  var json;
  if (platform.isBrowser()) {
    return callback(new Error("Saving graphs not supported on browser"));
  }
  json = JSON.stringify(this.toJSON(), null, 4);
  return require('fs').writeFile(file + ".json", json, "utf-8", function(err, data) {
    if (err) {
      throw err;
    }
    return callback(file);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.setEdgeMetadata"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setEdgeMetadata (node, port, node2, port2, metadata)](#apidoc.element.noflo.Graph.prototype.setEdgeMetadata)
- description and source-code
```javascript
setEdgeMetadata = function (node, port, node2, port2, metadata) {
  var before, edge, item, val;
  edge = this.getEdge(node, port, node2, port2);
  if (!edge) {
    return;
  }
  this.checkTransactionStart();
  before = clone(edge.metadata);
  if (!edge.metadata) {
    edge.metadata = {};
  }
  for (item in metadata) {
    val = metadata[item];
    if (val != null) {
      edge.metadata[item] = val;
    } else {
      delete edge.metadata[item];
    }
  }
  this.emit('changeEdge', edge, before);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.setGroupMetadata"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setGroupMetadata (groupName, metadata)](#apidoc.element.noflo.Graph.prototype.setGroupMetadata)
- description and source-code
```javascript
setGroupMetadata = function (groupName, metadata) {
  var before, group, i, item, len, ref, val;
  this.checkTransactionStart();
  ref = this.groups;
  for (i = 0, len = ref.length; i < len; i++) {
    group = ref[i];
    if (!group) {
      continue;
    }
    if (group.name !== groupName) {
      continue;
    }
    before = clone(group.metadata);
    for (item in metadata) {
      val = metadata[item];
      if (val != null) {
        group.metadata[item] = val;
      } else {
        delete group.metadata[item];
      }
    }
    this.emit('changeGroup', group, before);
  }
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.setInportMetadata"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setInportMetadata (publicPort, metadata)](#apidoc.element.noflo.Graph.prototype.setInportMetadata)
- description and source-code
```javascript
setInportMetadata = function (publicPort, metadata) {
  var before, item, val;
  publicPort = this.getPortName(publicPort);
  if (!this.inports[publicPort]) {
    return;
  }
  this.checkTransactionStart();
  before = clone(this.inports[publicPort].metadata);
  if (!this.inports[publicPort].metadata) {
    this.inports[publicPort].metadata = {};
  }
  for (item in metadata) {
    val = metadata[item];
    if (val != null) {
      this.inports[publicPort].metadata[item] = val;
    } else {
      delete this.inports[publicPort].metadata[item];
    }
  }
  this.emit('changeInport', publicPort, this.inports[publicPort], before);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.setNodeMetadata"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setNodeMetadata (id, metadata)](#apidoc.element.noflo.Graph.prototype.setNodeMetadata)
- description and source-code
```javascript
setNodeMetadata = function (id, metadata) {
  var before, item, node, val;
  node = this.getNode(id);
  if (!node) {
    return;
  }
  this.checkTransactionStart();
  before = clone(node.metadata);
  if (!node.metadata) {
    node.metadata = {};
  }
  for (item in metadata) {
    val = metadata[item];
    if (val != null) {
      node.metadata[item] = val;
    } else {
      delete node.metadata[item];
    }
  }
  this.emit('changeNode', node, before);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.setOutportMetadata"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setOutportMetadata (publicPort, metadata)](#apidoc.element.noflo.Graph.prototype.setOutportMetadata)
- description and source-code
```javascript
setOutportMetadata = function (publicPort, metadata) {
  var before, item, val;
  publicPort = this.getPortName(publicPort);
  if (!this.outports[publicPort]) {
    return;
  }
  this.checkTransactionStart();
  before = clone(this.outports[publicPort].metadata);
  if (!this.outports[publicPort].metadata) {
    this.outports[publicPort].metadata = {};
  }
  for (item in metadata) {
    val = metadata[item];
    if (val != null) {
      this.outports[publicPort].metadata[item] = val;
    } else {
      delete this.outports[publicPort].metadata[item];
    }
  }
  this.emit('changeOutport', publicPort, this.outports[publicPort], before);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.setProperties"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>setProperties (properties)](#apidoc.element.noflo.Graph.prototype.setProperties)
- description and source-code
```javascript
setProperties = function (properties) {
  var before, item, val;
  this.checkTransactionStart();
  before = clone(this.properties);
  for (item in properties) {
    val = properties[item];
    this.properties[item] = val;
  }
  this.emit('changeProperties', this.properties, before);
  return this.checkTransactionEnd();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.startTransaction"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>startTransaction (id, metadata)](#apidoc.element.noflo.Graph.prototype.startTransaction)
- description and source-code
```javascript
startTransaction = function (id, metadata) {
  if (this.transaction.id) {
    throw Error("Nested transactions not supported");
  }
  this.transaction.id = id;
  this.transaction.depth = 1;
  return this.emit('startTransaction', id, metadata);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.toDOT"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>toDOT ()](#apidoc.element.noflo.Graph.prototype.toDOT)
- description and source-code
```javascript
toDOT = function () {
  var cleanID, cleanPort, data, dot, edge, i, id, initializer, j, k, len, len1, len2, node, ref, ref1, ref2;
  cleanID = function(id) {
    return id.replace(/\s*/g, "");
  };
  cleanPort = function(port) {
    return port.replace(/\./g, "");
  };
  dot = "digraph {\n";
  ref = this.nodes;
  for (i = 0, len = ref.length; i < len; i++) {
    node = ref[i];
    dot += "    " + (cleanID(node.id)) + " [label=" + node.id + " shape=box]\n";
  }
  ref1 = this.initializers;
  for (id = j = 0, len1 = ref1.length; j < len1; id = ++j) {
    initializer = ref1[id];
    if (typeof initializer.from.data === 'function') {
      data = 'Function';
    } else {
      data = initializer.from.data;
    }
    dot += "    data" + id + " [label=\"'" + data + "'\" shape=plaintext]\n";
    dot += "    data" + id + " -> " + (cleanID(initializer.to.node)) + "[headlabel=" + (cleanPort(initializer.to.port)) + " labelfontcolor
=blue labelfontsize=8.0]\n";
  }
  ref2 = this.edges;
  for (k = 0, len2 = ref2.length; k < len2; k++) {
    edge = ref2[k];
    dot += "    " + (cleanID(edge.from.node)) + " -> " + (cleanID(edge.to.node)) + "[taillabel=" + (cleanPort(edge.from.port)) + "
headlabel=" + (cleanPort(edge.to.port)) + " labelfontcolor=blue labelfontsize=8.0]\n";
  }
  dot += "}";
  return dot;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>toJSON ()](#apidoc.element.noflo.Graph.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  var connection, edge, exported, group, groupData, i, initializer, j, json, k, l, len, len1, len2, len3, len4, m, node, priv, property
, pub, ref, ref1, ref2, ref3, ref4, ref5, ref6, ref7, value;
  json = {
    caseSensitive: this.caseSensitive,
    properties: {},
    inports: {},
    outports: {},
    groups: [],
    processes: {},
    connections: []
  };
  if (this.name) {
    json.properties.name = this.name;
  }
  ref = this.properties;
  for (property in ref) {
    value = ref[property];
    json.properties[property] = value;
  }
  ref1 = this.inports;
  for (pub in ref1) {
    priv = ref1[pub];
    json.inports[pub] = priv;
  }
  ref2 = this.outports;
  for (pub in ref2) {
    priv = ref2[pub];
    json.outports[pub] = priv;
  }
  ref3 = this.exports;
  for (i = 0, len = ref3.length; i < len; i++) {
    exported = ref3[i];
    if (!json.exports) {
      json.exports = [];
    }
    json.exports.push(exported);
  }
  ref4 = this.groups;
  for (j = 0, len1 = ref4.length; j < len1; j++) {
    group = ref4[j];
    groupData = {
      name: group.name,
      nodes: group.nodes
    };
    if (Object.keys(group.metadata).length) {
      groupData.metadata = group.metadata;
    }
    json.groups.push(groupData);
  }
  ref5 = this.nodes;
  for (k = 0, len2 = ref5.length; k < len2; k++) {
    node = ref5[k];
    json.processes[node.id] = {
      component: node.component
    };
    if (node.metadata) {
      json.processes[node.id].metadata = node.metadata;
    }
  }
  ref6 = this.edges;
  for (l = 0, len3 = ref6.length; l < len3; l++) {
    edge = ref6[l];
    connection = {
      src: {
        process: edge.from.node,
        port: edge.from.port,
        index: edge.from.index
      },
      tgt: {
        process: edge.to.node,
        port: edge.to.port,
        index: edge.to.index
      }
    };
    if (Object.keys(edge.metadata).length) {
      connection.metadata = edge.metadata;
    }
    json.connections.push(connection);
  }
  ref7 = this.initializers;
  for (m = 0, len4 = ref7.length; m < len4; m++) {
    initializer = ref7[m];
    json.connections.push({
      data: initializer.from.data,
      tgt: {
        process: initializer.to.node,
        port: initializer.to.port,
        index: initializer.to.index
      }
    });
  }
  return json;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Graph.prototype.toYUML"></a>[function <span class="apidocSignatureSpan">noflo.Graph.prototype.</span>toYUML ()](#apidoc.element.noflo.Graph.prototype.toYUML)
- description and source-code
```javascript
toYUML = function () {
  var edge, i, initializer, j, len, len1, ref, ref1, yuml;
  yuml = [];
  ref = this.initializers;
  for (i = 0, len = ref.length; i < len; i++) {
    initializer = ref[i];
    yuml.push("(start)[" + initializer.to.port + "]->(" + initializer.to.node + ")");
  }
  ref1 = this.edges;
  for (j = 0, len1 = ref1.length; j < len1; j++) {
    edge = ref1[j];
    yuml.push("(" + edge.from.node + ")[" + edge.from.port + "]->(" + edge.to.node + ")");
  }
  return yuml.join(",");
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.IP"></a>[module noflo.IP](#apidoc.module.noflo.IP)

#### <a name="apidoc.element.noflo.IP.IP"></a>[function <span class="apidocSignatureSpan">noflo.</span>IP (type, data, options)](#apidoc.element.noflo.IP.IP)
- description and source-code
```javascript
function IP(type, data, options) {
  var key, val;
  this.type = type != null ? type : 'data';
  this.data = data != null ? data : null;
  if (options == null) {
    options = {};
  }
  this._isIP = true;
  this.scope = null;
  this.owner = null;
  this.clonable = false;
  this.index = null;
  for (key in options) {
    val = options[key];
    this[key] = val;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.IP.isIP"></a>[function <span class="apidocSignatureSpan">noflo.IP.</span>isIP (obj)](#apidoc.element.noflo.IP.isIP)
- description and source-code
```javascript
isIP = function (obj) {
  return obj && typeof obj === 'object' && obj._isIP === true;
}
```
- example usage
```shell
...
      for (i = 0, len = inputs.length; i < len; i++) {
inputMap = inputs[i];
results.push((function() {
  var results1;
  results1 = [];
  for (port in inputMap) {
    value = inputMap[port];
    if (IP.isIP(value)) {
      inSockets[port].post(value);
      continue;
    }
    results1.push(inSockets[port].post(new IP('data', value)));
  }
  return results1;
})());
...
```



# <a name="apidoc.module.noflo.IP.prototype"></a>[module noflo.IP.prototype](#apidoc.module.noflo.IP.prototype)

#### <a name="apidoc.element.noflo.IP.prototype.clone"></a>[function <span class="apidocSignatureSpan">noflo.IP.prototype.</span>clone ()](#apidoc.element.noflo.IP.prototype.clone)
- description and source-code
```javascript
clone = function () {
  var ip, key, val;
  ip = new IP(this.type);
  for (key in this) {
    val = this[key];
    if (['owner'].indexOf(key) !== -1) {
      continue;
    }
    if (val === null) {
      continue;
    }
    if (typeof val === 'object') {
      ip[key] = JSON.parse(JSON.stringify(val));
    } else {
      ip[key] = val;
    }
  }
  return ip;
}
```
- example usage
```shell
...
    debugBrackets(this.nodeId + " closeBracket-A from '" + context.source + "' to " + context.ports + ": '" + context.closeIp.data
 + "'");
    if (!context.ports.length) {
      continue;
    }
    ref2 = context.ports;
    for (j = 0, len2 = ref2.length; j < len2; j++) {
      port = ref2[j];
      ipClone = context.closeIp.clone();
      this.addToResult(result, port, ipClone, true);
      this.getBracketContext('out', port, ipClone.scope).pop();
    }
  }
}
if (result.__bracketContext) {
  Object.keys(result.__bracketContext).reverse().forEach((function(_this) {
...
```

#### <a name="apidoc.element.noflo.IP.prototype.drop"></a>[function <span class="apidocSignatureSpan">noflo.IP.prototype.</span>drop ()](#apidoc.element.noflo.IP.prototype.drop)
- description and source-code
```javascript
drop = function () {
  var key, results, val;
  results = [];
  for (key in this) {
    val = this[key];
    results.push(delete this[key]);
  }
  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.IP.prototype.move"></a>[function <span class="apidocSignatureSpan">noflo.IP.prototype.</span>move (owner)](#apidoc.element.noflo.IP.prototype.move)
- description and source-code
```javascript
move = function (owner) {
  this.owner = owner;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.InPort"></a>[module noflo.InPort](#apidoc.module.noflo.InPort)

#### <a name="apidoc.element.noflo.InPort.InPort"></a>[function <span class="apidocSignatureSpan">noflo.</span>InPort (options, process)](#apidoc.element.noflo.InPort.InPort)
- description and source-code
```javascript
function InPort(options, process) {
  this.process = null;
  if (!process && typeof options === 'function') {
    process = options;
    options = {};
  }
  if (options == null) {
    options = {};
  }
  if (options.buffered == null) {
    options.buffered = false;
  }
  if (options.control == null) {
    options.control = false;
  }
  if (options.triggering == null) {
    options.triggering = true;
  }
  if (!process && options && options.process) {
    process = options.process;
    delete options.process;
  }
  if (process) {
    platform.deprecated('InPort process callback is deprecated. Please use Process API or the InPort handle option');
    if (typeof process !== 'function') {
      throw new Error('process must be a function');
    }
    this.process = process;
  }
  if (options.handle) {
    platform.deprecated('InPort handle callback is deprecated. Please use Process API');
    if (typeof options.handle !== 'function') {
      throw new Error('handle must be a function');
    }
    this.handle = options.handle;
    delete options.handle;
  }
  InPort.__super__.constructor.call(this, options);
  this.prepareBuffer();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.InPort.</span>EventEmitter ()](#apidoc.element.noflo.InPort.EventEmitter)
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

#### <a name="apidoc.element.noflo.InPort.init"></a>[function <span class="apidocSignatureSpan">noflo.InPort.</span>init ()](#apidoc.element.noflo.InPort.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.InPort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.InPort.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.InPort.__super__"></a>[module noflo.InPort.__super__](#apidoc.module.noflo.InPort.__super__)

#### <a name="apidoc.element.noflo.InPort.__super__.attach"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>attach (socket, index)](#apidoc.element.noflo.InPort.__super__.attach)
- description and source-code
```javascript
attach = function (socket, index) {
  if (index == null) {
    index = null;
  }
  if (!this.isAddressable() || index === null) {
    index = this.sockets.length;
  }
  this.sockets[index] = socket;
  this.attachSocket(socket, index);
  if (this.isAddressable()) {
    this.emit('attach', socket, index);
    return;
  }
  return this.emit('attach', socket);
}
```
- example usage
```shell
...
  runNetwork = function(network, inputs, options, callback) {
var inPorts, inSockets, outPorts, outSockets, process, received;
process = network.getNode(options.name);
inPorts = Object.keys(network.graph.inports);
inSockets = {};
inPorts.forEach(function(inport) {
  inSockets[inport] = internalSocket.createSocket();
  return process.component.inPorts[inport].attach(inSockets[inport]);
});
received = [];
outPorts = Object.keys(network.graph.outports);
outSockets = {};
outPorts.forEach(function(outport) {
  outSockets[outport] = internalSocket.createSocket();
  process.component.outPorts[outport].attach(outSockets[outport]);
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.attachSocket"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>attachSocket ()](#apidoc.element.noflo.InPort.__super__.attachSocket)
- description and source-code
```javascript
attachSocket = function () {}
```
- example usage
```shell
...
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    socketId = this.sockets.length;
  }
  this.sockets[socketId] = socket;
  return this.attachSocket(socket, socketId);
};

ArrayPort.prototype.connect = function(socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.canAttach"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>canAttach ()](#apidoc.element.noflo.InPort.__super__.canAttach)
- description and source-code
```javascript
canAttach = function () {
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.__super__.constructor"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>constructor (options)](#apidoc.element.noflo.InPort.__super__.constructor)
- description and source-code
```javascript
function BasePort(options) {
  this.handleOptions(options);
  this.sockets = [];
  this.node = null;
  this.name = null;
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.detach"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>detach (socket)](#apidoc.element.noflo.InPort.__super__.detach)
- description and source-code
```javascript
detach = function (socket) {
  var index;
  index = this.sockets.indexOf(socket);
  if (index === -1) {
    return;
  }
  this.sockets[index] = void 0;
  if (this.isAddressable()) {
    this.emit('detach', socket, index);
    return;
  }
  return this.emit('detach', socket);
}
```
- example usage
```shell
...
    return received.push(res);
  });
});
network.once('end', function() {
  var port, socket;
  for (port in outSockets) {
    socket = outSockets[port];
    process.component.outPorts[port].detach(socket);
  }
  outSockets = {};
  inSockets = {};
  return callback(null, received);
});
return network.start(function(err) {
  var i, inputMap, len, port, results, value;
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.getDataType"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>getDataType ()](#apidoc.element.noflo.InPort.__super__.getDataType)
- description and source-code
```javascript
getDataType = function () {
  return this.options.datatype;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.__super__.getDescription"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>getDescription ()](#apidoc.element.noflo.InPort.__super__.getDescription)
- description and source-code
```javascript
getDescription = function () {
  return this.options.description;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.__super__.getId"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>getId ()](#apidoc.element.noflo.InPort.__super__.getId)
- description and source-code
```javascript
getId = function () {
  if (!(this.node && this.name)) {
    return 'Port';
  }
  return this.node + " " + (this.name.toUpperCase());
}
```
- example usage
```shell
...

    ArrayPort.prototype.connect = function(socketId) {
if (socketId == null) {
  socketId = null;
}
if (socketId === null) {
  if (!this.sockets.length) {
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach(function(socket) {
    if (!socket) {
      return;
    }
    return socket.connect();
  });
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.handleOptions"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>handleOptions (options)](#apidoc.element.noflo.InPort.__super__.handleOptions)
- description and source-code
```javascript
handleOptions = function (options) {
  if (!options) {
    options = {};
  }
  if (!options.datatype) {
    options.datatype = 'all';
  }
  if (options.required === void 0) {
    options.required = false;
  }
  if (options.datatype === 'integer') {
    options.datatype = 'int';
  }
  if (validTypes.indexOf(options.datatype) === -1) {
    throw new Error("Invalid port datatype '" + options.datatype + "' specified, valid are " + (validTypes.join(', ')));
  }
  if (options.type && options.type.indexOf('/') === -1) {
    throw new Error("Invalid port type '" + options.type + "' specified. Should be URL or MIME type");
  }
  return this.options = options;
}
```
- example usage
```shell
...

  validTypes = ['all', 'string', 'number', 'int', 'object', 'array', 'boolean', 'color', 'date', 'bang', 'function', 'buffer', '
stream'];

  BasePort = (function(superClass) {
extend(BasePort, superClass);

function BasePort(options) {
  this.handleOptions(options);
  this.sockets = [];
  this.node = null;
  this.name = null;
}

BasePort.prototype.handleOptions = function(options) {
  if (!options) {
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.isAddressable"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isAddressable ()](#apidoc.element.noflo.InPort.__super__.isAddressable)
- description and source-code
```javascript
isAddressable = function () {
  if (this.options.addressable) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
  return this.options.description;
};

BasePort.prototype.attach = function(socket, index) {
  if (index == null) {
    index = null;
  }
  if (!this.isAddressable() || index === null) {
    index = this.sockets.length;
  }
  this.sockets[index] = socket;
  this.attachSocket(socket, index);
  if (this.isAddressable()) {
    this.emit('attach', socket, index);
    return;
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.isAttached"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isAttached (socketId)](#apidoc.element.noflo.InPort.__super__.isAttached)
- description and source-code
```javascript
isAttached = function (socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (this.isAddressable() && socketId !== null) {
    if (this.sockets[socketId]) {
      return true;
    }
    return false;
  }
  if (this.sockets.length) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
    if (_this.load > 0) {
      return _this.q.push({
        name: "disconnect"
      });
    }
    _this.outPorts[_this.outPortName].disconnect();
    _this.errorGroups = [];
    if (_this.outPorts.load.isAttached()) {
      return _this.outPorts.load.disconnect();
    }
  };
})(this));
this.inPorts[this.inPortName].on("data", (function(_this) {
  return function(data) {
    if (_this.q.length > 0) {
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.isBuffered"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isBuffered ()](#apidoc.element.noflo.InPort.__super__.isBuffered)
- description and source-code
```javascript
isBuffered = function () {
  if (this.options.buffered) {
    return true;
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.__super__.isConnected"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isConnected (socketId)](#apidoc.element.noflo.InPort.__super__.isConnected)
- description and source-code
```javascript
isConnected = function (socketId) {
  var connected;
  if (socketId == null) {
    socketId = null;
  }
  if (this.isAddressable()) {
    if (socketId === null) {
      throw new Error((this.getId()) + ": Socket ID required");
    }
    if (!this.sockets[socketId]) {
      throw new Error((this.getId()) + ": Socket " + socketId + " not available");
    }
    return this.sockets[socketId].isConnected();
  }
  connected = false;
  this.sockets.forEach(function(socket) {
    if (!socket) {
      return;
    }
    if (socket.isConnected()) {
      return connected = true;
    }
  });
  return connected;
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
if (this.isConnected(socketId)) {
  return this.sockets[socketId].beginGroup(group);
}
this.sockets[socketId].once("connect", (function(_this) {
  return function() {
    return _this.sockets[socketId].beginGroup(group);
  };
})(this));
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.isRequired"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>isRequired ()](#apidoc.element.noflo.InPort.__super__.isRequired)
- description and source-code
```javascript
isRequired = function () {
  if (this.options.required) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
var group, i, j, len, len1;
if (groups == null) {
  groups = [];
}
if (errorPort == null) {
  errorPort = 'error';
}
if (this.outPorts[errorPort] && (this.outPorts[errorPort].isAttached() || !this.outPorts[errorPort].isRequired())) {
  for (i = 0, len = groups.length; i < len; i++) {
    group = groups[i];
    this.outPorts[errorPort].beginGroup(group);
  }
  this.outPorts[errorPort].send(e);
  for (j = 0, len1 = groups.length; j < len1; j++) {
    group = groups[j];
...
```

#### <a name="apidoc.element.noflo.InPort.__super__.listAttached"></a>[function <span class="apidocSignatureSpan">noflo.InPort.__super__.</span>listAttached ()](#apidoc.element.noflo.InPort.__super__.listAttached)
- description and source-code
```javascript
listAttached = function () {
  var attached, i, idx, len, ref, socket;
  attached = [];
  ref = this.sockets;
  for (idx = i = 0, len = ref.length; i < len; idx = ++i) {
    socket = ref[idx];
    if (!socket) {
      continue;
    }
    attached.push(idx);
  }
  return attached;
}
```
- example usage
```shell
...
  args = 1 <= arguments.length ? slice.call(arguments, 0) : [];
  if (!args.length) {
    args = ['in'];
  }
  res = [];
  for (i = 0, len1 = args.length; i < len1; i++) {
    port = args[i];
    res.push(this.ports[port].listAttached());
  }
  if (args.length === 1) {
    return res.pop();
  }
  return res;
};
...
```



# <a name="apidoc.module.noflo.InPort.prototype"></a>[module noflo.InPort.prototype](#apidoc.module.noflo.InPort.prototype)

#### <a name="apidoc.element.noflo.InPort.prototype.attachSocket"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>attachSocket (socket, localId)](#apidoc.element.noflo.InPort.prototype.attachSocket)
- description and source-code
```javascript
attachSocket = function (socket, localId) {
  if (localId == null) {
    localId = null;
  }
  if (this.hasDefault()) {
    if (this.handle) {
      socket.setDataDelegate((function(_this) {
        return function() {
          return new IP('data', _this.options["default"]);
        };
      })(this));
    } else {
      socket.setDataDelegate((function(_this) {
        return function() {
          return _this.options["default"];
        };
      })(this));
    }
  }
  socket.on('connect', (function(_this) {
    return function() {
      return _this.handleSocketEvent('connect', socket, localId);
    };
  })(this));
  socket.on('begingroup', (function(_this) {
    return function(group) {
      return _this.handleSocketEvent('begingroup', group, localId);
    };
  })(this));
  socket.on('data', (function(_this) {
    return function(data) {
      _this.validateData(data);
      return _this.handleSocketEvent('data', data, localId);
    };
  })(this));
  socket.on('endgroup', (function(_this) {
    return function(group) {
      return _this.handleSocketEvent('endgroup', group, localId);
    };
  })(this));
  socket.on('disconnect', (function(_this) {
    return function() {
      return _this.handleSocketEvent('disconnect', socket, localId);
    };
  })(this));
  return socket.on('ip', (function(_this) {
    return function(ip) {
      return _this.handleIP(ip, localId);
    };
  })(this));
}
```
- example usage
```shell
...
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    socketId = this.sockets.length;
  }
  this.sockets[socketId] = socket;
  return this.attachSocket(socket, socketId);
};

ArrayPort.prototype.connect = function(socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.clear"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>clear ()](#apidoc.element.noflo.InPort.prototype.clear)
- description and source-code
```javascript
clear = function () {
  return this.prepareBuffer();
}
```
- example usage
```shell
...
var inPort, inPorts, portName;
inPorts = _this.inPorts.ports || _this.inPorts;
for (portName in inPorts) {
  inPort = inPorts[portName];
  if (typeof inPort.clear !== 'function') {
    continue;
  }
  inPort.clear();
}
_this.bracketContext = {
  "in": {},
  out: {}
};
if (!_this.isStarted()) {
  return callback();
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>constructor (options, process)](#apidoc.element.noflo.InPort.prototype.constructor)
- description and source-code
```javascript
function InPort(options, process) {
  this.process = null;
  if (!process && typeof options === 'function') {
    process = options;
    options = {};
  }
  if (options == null) {
    options = {};
  }
  if (options.buffered == null) {
    options.buffered = false;
  }
  if (options.control == null) {
    options.control = false;
  }
  if (options.triggering == null) {
    options.triggering = true;
  }
  if (!process && options && options.process) {
    process = options.process;
    delete options.process;
  }
  if (process) {
    platform.deprecated('InPort process callback is deprecated. Please use Process API or the InPort handle option');
    if (typeof process !== 'function') {
      throw new Error('process must be a function');
    }
    this.process = process;
  }
  if (options.handle) {
    platform.deprecated('InPort handle callback is deprecated. Please use Process API');
    if (typeof options.handle !== 'function') {
      throw new Error('handle must be a function');
    }
    this.handle = options.handle;
    delete options.handle;
  }
  InPort.__super__.constructor.call(this, options);
  this.prepareBuffer();
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.contains"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>contains ()](#apidoc.element.noflo.InPort.prototype.contains)
- description and source-code
```javascript
contains = function () {
  platform.deprecated('InPort.contains is deprecated. Use InPort.has instead');
  if (!this.isBuffered()) {
    throw new Error('Contains query is only possible on buffered ports');
  }
  return this.buffer.filter(function(packet) {
    if (packet.event === 'data') {
      return true;
    }
  }).length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.get"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>get (scope, idx)](#apidoc.element.noflo.InPort.prototype.get)
- description and source-code
```javascript
get = function (scope, idx) {
  var res;
  res = this.getFromBuffer(scope, idx);
  if (res !== void 0) {
    return res;
  }
  return this.getFromBuffer(null, idx, true);
}
```
- example usage
```shell
...
dataPackets = buf.filter(function(ip) {
  return ip.type === 'data';
});
if (this.outputQ.length >= this.load && dataPackets.length === 0) {
  if (buf[0] !== ip) {
    return;
  }
  port.get(ip.scope, ip.index);
  context = this.getBracketContext('in', port.name, ip.scope, ip.index).pop();
  context.closeIp = ip;
  debugBrackets(this.nodeId + " closeBracket-C from '" + context.source + "' to " + context.ports + ": '" + ip.data + "'");
  result = {
    __resolved: true,
    __bracketClosingAfter: [context]
  };
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.getBuffer"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>getBuffer (scope, idx, initial)](#apidoc.element.noflo.InPort.prototype.getBuffer)
- description and source-code
```javascript
getBuffer = function (scope, idx, initial) {
  if (initial == null) {
    initial = false;
  }
  if (this.isAddressable()) {
    if (scope != null) {
      if (!(scope in this.scopedBuffer)) {
        return void 0;
      }
      if (!(idx in this.scopedBuffer[scope])) {
        return void 0;
      }
      return this.scopedBuffer[scope][idx];
    }
    if (initial) {
      if (!(idx in this.iipBuffer)) {
        return void 0;
      }
      return this.iipBuffer[idx];
    }
    if (!(idx in this.indexedBuffer)) {
      return void 0;
    }
    return this.indexedBuffer[idx];
  }
  if (scope != null) {
    if (!(scope in this.scopedBuffer)) {
      return void 0;
    }
    return this.scopedBuffer[scope];
  }
  if (initial) {
    return this.iipBuffer;
  }
  return this.buffer;
}
```
- example usage
```shell
...
}
result = {};
if (this.isForwardingInport(port)) {
  if (ip.type === 'openBracket') {
    return;
  }
  if (ip.type === 'closeBracket') {
    buf = port.getBuffer(ip.scope, ip.index);
    dataPackets = buf.filter(function(ip) {
      return ip.type === 'data';
    });
    if (this.outputQ.length >= this.load && dataPackets.length === 0) {
      if (buf[0] !== ip) {
        return;
      }
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.getFromBuffer"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>getFromBuffer (scope, idx, initial)](#apidoc.element.noflo.InPort.prototype.getFromBuffer)
- description and source-code
```javascript
getFromBuffer = function (scope, idx, initial) {
  var buf;
  if (initial == null) {
    initial = false;
  }
  buf = this.getBuffer(scope, idx, initial);
  if (!(buf != null ? buf.length : void 0)) {
    return void 0;
  }
  if (this.options.control) {
    return buf[buf.length - 1];
  } else {
    return buf.shift();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.handleIP"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>handleIP (ip, id)](#apidoc.element.noflo.InPort.prototype.handleIP)
- description and source-code
```javascript
handleIP = function (ip, id) {
  var buf;
  if (this.process) {
    return;
  }
  if (this.options.control && ip.type !== 'data') {
    return;
  }
  ip.owner = this.nodeInstance;
  if (this.isAddressable()) {
    ip.index = id;
  }
  buf = this.prepareBufferForIP(ip);
  buf.push(ip);
  if (this.options.control && buf.length > 1) {
    buf.shift();
  }
  if (this.handle) {
    this.handle(ip, this.nodeInstance);
  }
  return this.emit('ip', ip, id);
}
```
- example usage
```shell
...
ref = this.inPorts.ports;
fn = (function(_this) {
  return function(name, port) {
    if (!port.name) {
      port.name = name;
    }
    return port.on('ip', function(ip) {
      return _this.handleIP(ip, port);
    });
  };
})(this);
for (name in ref) {
  port = ref[name];
  fn(name, port);
}
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.handleSocketEvent"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>handleSocketEvent (event, payload, id)](#apidoc.element.noflo.InPort.prototype.handleSocketEvent)
- description and source-code
```javascript
handleSocketEvent = function (event, payload, id) {
  if (this.isBuffered()) {
    this.buffer.push({
      event: event,
      payload: payload,
      id: id
    });
    if (this.isAddressable()) {
      if (this.process) {
        this.process(event, id, this.nodeInstance);
      }
      this.emit(event, id);
    } else {
      if (this.process) {
        this.process(event, this.nodeInstance);
      }
      this.emit(event);
    }
    return;
  }
  if (this.process) {
    if (this.isAddressable()) {
      this.process(event, payload, id, this.nodeInstance);
    } else {
      this.process(event, payload, this.nodeInstance);
    }
  }
  if (this.isAddressable()) {
    return this.emit(event, payload, id);
  }
  return this.emit(event, payload);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.has"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>has (scope, idx, validate)](#apidoc.element.noflo.InPort.prototype.has)
- description and source-code
```javascript
has = function (scope, idx, validate) {
  if (!this.isAddressable()) {
    validate = idx;
    idx = null;
  }
  if (this.hasIPinBuffer(scope, idx, validate)) {
    return true;
  }
  if (this.hasIIP(idx, validate)) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
}
for (i = 0, len1 = args.length; i < len1; i++) {
  port = args[i];
  if (Array.isArray(port)) {
    if (!this.ports[port[0]].isAddressable()) {
      throw new Error("Non-addressable ports, access must be with string " + port[0]);
    }
    if (!this.ports[port[0]].has(this.scope, port[1], validate)) {
      return false;
    }
    continue;
  }
  if (this.ports[port].isAddressable()) {
    throw new Error("For addressable ports, access must be with array [" + port + ", idx]");
  }
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.hasDefault"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>hasDefault ()](#apidoc.element.noflo.InPort.prototype.hasDefault)
- description and source-code
```javascript
hasDefault = function () {
  return this.options["default"] !== void 0;
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
ref = process.component.inPorts.ports;
for (key in ref) {
  port = ref[key];
  if (typeof port.hasDefault === 'function' && port.hasDefault() && !port.isAttached()) {
    socket = internalSocket.createSocket();
    socket.setDebug(this.debug);
    this.subscribeSocket(socket);
    this.connectPort(socket, process, key, void 0, true);
    this.connections.push(socket);
    this.defaults.push(socket);
  }
...
```

#### <a name="apidoc.element.noflo.InPort.prototype.hasIIP"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>hasIIP (idx, validate)](#apidoc.element.noflo.InPort.prototype.hasIIP)
- description and source-code
```javascript
hasIIP = function (idx, validate) {
  return this.hasIPinBuffer(null, idx, validate, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.hasIPinBuffer"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>hasIPinBuffer (scope, idx, validate, initial)](#apidoc.element.noflo.InPort.prototype.hasIPinBuffer)
- description and source-code
```javascript
hasIPinBuffer = function (scope, idx, validate, initial) {
  var buf, i, len, packet;
  if (initial == null) {
    initial = false;
  }
  buf = this.getBuffer(scope, idx, initial);
  if (!(buf != null ? buf.length : void 0)) {
    return false;
  }
  for (i = 0, len = buf.length; i < len; i++) {
    packet = buf[i];
    if (validate(packet)) {
      return true;
    }
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.length"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>length (scope, idx)](#apidoc.element.noflo.InPort.prototype.length)
- description and source-code
```javascript
length = function (scope, idx) {
  var buf;
  buf = this.getBuffer(scope, idx);
  if (!buf) {
    return 0;
  }
  return buf.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.prepareBuffer"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>prepareBuffer ()](#apidoc.element.noflo.InPort.prototype.prepareBuffer)
- description and source-code
```javascript
prepareBuffer = function () {
  this.buffer = [];
  if (this.isAddressable()) {
    this.indexedBuffer = {};
  }
  this.scopedBuffer = {};
  return this.iipBuffer = this.isAddressable() ? {} : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.prepareBufferForIP"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>prepareBufferForIP (ip)](#apidoc.element.noflo.InPort.prototype.prepareBufferForIP)
- description and source-code
```javascript
prepareBufferForIP = function (ip) {
  if (this.isAddressable()) {
    if (ip.scope != null) {
      if (!(ip.scope in this.scopedBuffer)) {
        this.scopedBuffer[ip.scope] = [];
      }
      if (!(ip.index in this.scopedBuffer[ip.scope])) {
        this.scopedBuffer[ip.scope][ip.index] = [];
      }
      return this.scopedBuffer[ip.scope][ip.index];
    }
    if (ip.initial) {
      if (!(ip.index in this.iipBuffer)) {
        this.iipBuffer[ip.index] = [];
      }
      return this.iipBuffer[ip.index];
    }
    if (!(ip.index in this.indexedBuffer)) {
      this.indexedBuffer[ip.index] = [];
    }
    return this.indexedBuffer[ip.index];
  }
  if (ip.scope != null) {
    if (!(ip.scope in this.scopedBuffer)) {
      this.scopedBuffer[ip.scope] = [];
    }
    return this.scopedBuffer[ip.scope];
  }
  if (ip.initial) {
    return this.iipBuffer;
  }
  return this.buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.ready"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>ready (scope, idx)](#apidoc.element.noflo.InPort.prototype.ready)
- description and source-code
```javascript
ready = function (scope, idx) {
  return this.length(scope) > 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.receive"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>receive ()](#apidoc.element.noflo.InPort.prototype.receive)
- description and source-code
```javascript
receive = function () {
  platform.deprecated('InPort.receive is deprecated. Use InPort.get instead');
  if (!this.isBuffered()) {
    throw new Error('Receive is only possible on buffered ports');
  }
  return this.buffer.shift();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPort.prototype.validateData"></a>[function <span class="apidocSignatureSpan">noflo.InPort.prototype.</span>validateData (data)](#apidoc.element.noflo.InPort.prototype.validateData)
- description and source-code
```javascript
validateData = function (data) {
  if (!this.options.values) {
    return;
  }
  if (this.options.values.indexOf(data) === -1) {
    throw new Error("Invalid data='" + data + "' received, not in [" + this.options.values + "]");
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.InPorts"></a>[module noflo.InPorts](#apidoc.module.noflo.InPorts)

#### <a name="apidoc.element.noflo.InPorts.InPorts"></a>[function <span class="apidocSignatureSpan">noflo.</span>InPorts ()](#apidoc.element.noflo.InPorts.InPorts)
- description and source-code
```javascript
function InPorts() {
  return InPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
this.network = null;
this.ready = true;
this.started = false;
this.starting = false;
this.baseDir = null;
this.loader = null;
this.load = 0;
this.inPorts = new noflo.InPorts({
  graph: {
    datatype: 'all',
    description: 'NoFlo graph definition to be used with the subgraph component',
    required: true
  }
});
this.outPorts = new noflo.OutPorts;
...
```

#### <a name="apidoc.element.noflo.InPorts.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.</span>EventEmitter ()](#apidoc.element.noflo.InPorts.EventEmitter)
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

#### <a name="apidoc.element.noflo.InPorts.init"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.</span>init ()](#apidoc.element.noflo.InPorts.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.InPorts.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.</span>listenerCount (emitter, type)](#apidoc.element.noflo.InPorts.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.InPorts.__super__"></a>[module noflo.InPorts.__super__](#apidoc.module.noflo.InPorts.__super__)

#### <a name="apidoc.element.noflo.InPorts.__super__.add"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>add (name, options, process)](#apidoc.element.noflo.InPorts.__super__.add)
- description and source-code
```javascript
add = function (name, options, process) {
  if (name === 'add' || name === 'remove') {
    throw new Error('Add and remove are restricted port names');
  }
  if (!name.match(/^[a-z0-9_\.\/]+$/)) {
    throw new Error("Port names can only contain lowercase alphanumeric characters and underscores. '" + name + "' not allowed");
  }
  if (this.ports[name]) {
    this.remove(name);
  }
  if (typeof options === 'object' && options.canAttach) {
    this.ports[name] = options;
  } else {
    this.ports[name] = new this.model(options, process);
  }
  this[name] = this.ports[name];
  this.emit('add', name);
  return this;
}
```
- example usage
```shell
...
outPorts = process.component.outPorts.ports || process.component.outPorts;
for (portName in inPorts) {
  port = inPorts[portName];
  targetPortName = this.isExportedInport(port, name, portName);
  if (targetPortName === false) {
    continue;
  }
  this.inPorts.add(targetPortName, port);
  this.inPorts[targetPortName].once('connect', (function(_this) {
    return function() {
      if (_this.starting) {
        return;
      }
      if (_this.isStarted()) {
        return;
...
```

#### <a name="apidoc.element.noflo.InPorts.__super__.constructor"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>constructor (ports)](#apidoc.element.noflo.InPorts.__super__.constructor)
- description and source-code
```javascript
function Ports(ports) {
  var name, options;
  this.ports = {};
  if (!ports) {
    return;
  }
  for (name in ports) {
    options = ports[name];
    this.add(name, options);
  }
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.InPorts.__super__.model"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>model (options, process)](#apidoc.element.noflo.InPorts.__super__.model)
- description and source-code
```javascript
function InPort(options, process) {
  this.process = null;
  if (!process && typeof options === 'function') {
    process = options;
    options = {};
  }
  if (options == null) {
    options = {};
  }
  if (options.buffered == null) {
    options.buffered = false;
  }
  if (options.control == null) {
    options.control = false;
  }
  if (options.triggering == null) {
    options.triggering = true;
  }
  if (!process && options && options.process) {
    process = options.process;
    delete options.process;
  }
  if (process) {
    platform.deprecated('InPort process callback is deprecated. Please use Process API or the InPort handle option');
    if (typeof process !== 'function') {
      throw new Error('process must be a function');
    }
    this.process = process;
  }
  if (options.handle) {
    platform.deprecated('InPort handle callback is deprecated. Please use Process API');
    if (typeof options.handle !== 'function') {
      throw new Error('handle must be a function');
    }
    this.handle = options.handle;
    delete options.handle;
  }
  InPort.__super__.constructor.call(this, options);
  this.prepareBuffer();
}
```
- example usage
```shell
...
  }
  if (this.ports[name]) {
    this.remove(name);
  }
  if (typeof options === 'object' && options.canAttach) {
    this.ports[name] = options;
  } else {
    this.ports[name] = new this.model(options, process);
  }
  this[name] = this.ports[name];
  this.emit('add', name);
  return this;
};

Ports.prototype.remove = function(name) {
...
```

#### <a name="apidoc.element.noflo.InPorts.__super__.remove"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.__super__.</span>remove (name)](#apidoc.element.noflo.InPorts.__super__.remove)
- description and source-code
```javascript
remove = function (name) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not defined");
  }
  delete this.ports[name];
  delete this[name];
  this.emit('remove', name);
  return this;
}
```
- example usage
```shell
...
var graphSocket;
if (err) {
  return callback(err);
}
graphSocket = internalSocket.createSocket();
graph.loader = _this;
graph.baseDir = _this.baseDir;
graph.inPorts.remove('graph');
graph.setGraph(component, function(err) {
  if (err) {
    return callback(err);
  }
  _this.setIcon(name, graph);
  return callback(null, graph);
});
...
```



# <a name="apidoc.module.noflo.InPorts.prototype"></a>[module noflo.InPorts.prototype](#apidoc.module.noflo.InPorts.prototype)

#### <a name="apidoc.element.noflo.InPorts.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.prototype.</span>constructor ()](#apidoc.element.noflo.InPorts.prototype.constructor)
- description and source-code
```javascript
function InPorts() {
  return InPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.InPorts.prototype.on"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.prototype.</span>on (name, event, callback)](#apidoc.element.noflo.InPorts.prototype.on)
- description and source-code
```javascript
on = function (name, event, callback) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not available");
  }
  return this.ports[name].on(event, callback);
}
```
- example usage
```shell
...
  graph: {
    datatype: 'all',
    description: 'NoFlo graph definition to be used with the subgraph component',
    required: true
  }
});
this.outPorts = new noflo.OutPorts;
this.inPorts.graph.on('ip', (function(_this) {
  return function(packet) {
    if (packet.type !== 'data') {
      return;
    }
    return _this.setGraph(packet.data, function(err) {
      if (err) {
        return _this.error(err);
...
```

#### <a name="apidoc.element.noflo.InPorts.prototype.once"></a>[function <span class="apidocSignatureSpan">noflo.InPorts.prototype.</span>once (name, event, callback)](#apidoc.element.noflo.InPorts.prototype.once)
- description and source-code
```javascript
once = function (name, event, callback) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not available");
  }
  return this.ports[name].once(event, callback);
}
```
- example usage
```shell
...
      for (portName in inPorts) {
port = inPorts[portName];
targetPortName = this.isExportedInport(port, name, portName);
if (targetPortName === false) {
  continue;
}
this.inPorts.add(targetPortName, port);
this.inPorts[targetPortName].once('connect', (function(_this) {
  return function() {
    if (_this.starting) {
      return;
    }
    if (_this.isStarted()) {
      return;
    }
...
```



# <a name="apidoc.module.noflo.Journal"></a>[module noflo.Journal](#apidoc.module.noflo.Journal)

#### <a name="apidoc.element.noflo.Journal.Journal"></a>[function <span class="apidocSignatureSpan">noflo.</span>Journal (graph, metadata, store)](#apidoc.element.noflo.Journal.Journal)
- description and source-code
```javascript
function Journal(graph, metadata, store) {
  this.endTransaction = bind(this.endTransaction, this);
  this.startTransaction = bind(this.startTransaction, this);
  var edge, group, iip, j, k, l, len, len1, len2, len3, m, n, node, ref, ref1, ref2, ref3, ref4, ref5, v;
  this.graph = graph;
  this.entries = [];
  this.subscribed = true;
  this.store = store || new MemoryJournalStore(this.graph);
  if (this.store.transactions.length === 0) {
    this.currentRevision = -1;
    this.startTransaction('initial', metadata);
    ref = this.graph.nodes;
    for (j = 0, len = ref.length; j < len; j++) {
      node = ref[j];
      this.appendCommand('addNode', node);
    }
    ref1 = this.graph.edges;
    for (l = 0, len1 = ref1.length; l < len1; l++) {
      edge = ref1[l];
      this.appendCommand('addEdge', edge);
    }
    ref2 = this.graph.initializers;
    for (m = 0, len2 = ref2.length; m < len2; m++) {
      iip = ref2[m];
      this.appendCommand('addInitial', iip);
    }
    if (Object.keys(this.graph.properties).length > 0) {
      this.appendCommand('changeProperties', this.graph.properties, {});
    }
    ref3 = this.graph.inports;
    for (k in ref3) {
      v = ref3[k];
      this.appendCommand('addInport', {
        name: k,
        port: v
      });
    }
    ref4 = this.graph.outports;
    for (k in ref4) {
      v = ref4[k];
      this.appendCommand('addOutport', {
        name: k,
        port: v
      });
    }
    ref5 = this.graph.groups;
    for (n = 0, len3 = ref5.length; n < len3; n++) {
      group = ref5[n];
      this.appendCommand('addGroup', group);
    }
    this.endTransaction('initial', metadata);
  } else {
    this.currentRevision = this.store.lastRevision;
  }
  this.graph.on('addNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('addNode', node);
    };
  })(this));
  this.graph.on('removeNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('removeNode', node);
    };
  })(this));
  this.graph.on('renameNode', (function(_this) {
    return function(oldId, newId) {
      var args;
      args = {
        oldId: oldId,
        newId: newId
      };
      return _this.appendCommand('renameNode', args);
    };
  })(this));
  this.graph.on('changeNode', (function(_this) {
    return function(node, oldMeta) {
      return _this.appendCommand('changeNode', {
        id: node.id,
        "new": node.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('addEdge', edge);
    };
  })(this));
  this.graph.on('removeEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('removeEdge', edge);
    };
  })(this));
  this.graph.on('changeEdge', (function(_this) {
    return function(edge, oldMeta) {
      return _this.appendCommand('changeEdge', {
        from: edge.from,
        to: edge.to,
        "new": edge.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('addInitial', iip);
    };
  })(this));
  this.graph.on('removeInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('removeInitial', iip);
    };
  })(this));
  this.graph.on('changeProperties', (function(_this) {
    return function(newProps, oldProps) {
      return _this.appendCommand('changeProperties', {
        "new": newProps,
        old: oldProps
      });
    };
  })(this));
  this.graph.on('addGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('addGroup', group);
    };
  })(this));
  this.graph.on('renameGroup', (function(_this) {
    return function(oldName, newName) {
      return _this.appendCommand('renameGroup', {
        oldName: oldName,
        newName: newName
      });
    };
  })(this));
  this.graph.on('removeGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('removeGroup', group);
    };
  })( ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.Journal.</span>EventEmitter ()](#apidoc.element.noflo.Journal.EventEmitter)
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

#### <a name="apidoc.element.noflo.Journal.init"></a>[function <span class="apidocSignatureSpan">noflo.Journal.</span>init ()](#apidoc.element.noflo.Journal.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.Journal.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Journal.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.Journal.prototype"></a>[module noflo.Journal.prototype](#apidoc.module.noflo.Journal.prototype)

#### <a name="apidoc.element.noflo.Journal.prototype.appendCommand"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>appendCommand (cmd, args, rev)](#apidoc.element.noflo.Journal.prototype.appendCommand)
- description and source-code
```javascript
appendCommand = function (cmd, args, rev) {
  var entry;
  if (!this.subscribed) {
    return;
  }
  entry = {
    cmd: cmd,
    args: clone(args)
  };
  if (rev != null) {
    entry.rev = rev;
  }
  return this.entries.push(entry);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.canRedo"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>canRedo ()](#apidoc.element.noflo.Journal.prototype.canRedo)
- description and source-code
```javascript
canRedo = function () {
  return this.currentRevision < this.store.lastRevision;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.canUndo"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>canUndo ()](#apidoc.element.noflo.Journal.prototype.canUndo)
- description and source-code
```javascript
canUndo = function () {
  return this.currentRevision > 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>constructor (graph, metadata, store)](#apidoc.element.noflo.Journal.prototype.constructor)
- description and source-code
```javascript
function Journal(graph, metadata, store) {
  this.endTransaction = bind(this.endTransaction, this);
  this.startTransaction = bind(this.startTransaction, this);
  var edge, group, iip, j, k, l, len, len1, len2, len3, m, n, node, ref, ref1, ref2, ref3, ref4, ref5, v;
  this.graph = graph;
  this.entries = [];
  this.subscribed = true;
  this.store = store || new MemoryJournalStore(this.graph);
  if (this.store.transactions.length === 0) {
    this.currentRevision = -1;
    this.startTransaction('initial', metadata);
    ref = this.graph.nodes;
    for (j = 0, len = ref.length; j < len; j++) {
      node = ref[j];
      this.appendCommand('addNode', node);
    }
    ref1 = this.graph.edges;
    for (l = 0, len1 = ref1.length; l < len1; l++) {
      edge = ref1[l];
      this.appendCommand('addEdge', edge);
    }
    ref2 = this.graph.initializers;
    for (m = 0, len2 = ref2.length; m < len2; m++) {
      iip = ref2[m];
      this.appendCommand('addInitial', iip);
    }
    if (Object.keys(this.graph.properties).length > 0) {
      this.appendCommand('changeProperties', this.graph.properties, {});
    }
    ref3 = this.graph.inports;
    for (k in ref3) {
      v = ref3[k];
      this.appendCommand('addInport', {
        name: k,
        port: v
      });
    }
    ref4 = this.graph.outports;
    for (k in ref4) {
      v = ref4[k];
      this.appendCommand('addOutport', {
        name: k,
        port: v
      });
    }
    ref5 = this.graph.groups;
    for (n = 0, len3 = ref5.length; n < len3; n++) {
      group = ref5[n];
      this.appendCommand('addGroup', group);
    }
    this.endTransaction('initial', metadata);
  } else {
    this.currentRevision = this.store.lastRevision;
  }
  this.graph.on('addNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('addNode', node);
    };
  })(this));
  this.graph.on('removeNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('removeNode', node);
    };
  })(this));
  this.graph.on('renameNode', (function(_this) {
    return function(oldId, newId) {
      var args;
      args = {
        oldId: oldId,
        newId: newId
      };
      return _this.appendCommand('renameNode', args);
    };
  })(this));
  this.graph.on('changeNode', (function(_this) {
    return function(node, oldMeta) {
      return _this.appendCommand('changeNode', {
        id: node.id,
        "new": node.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('addEdge', edge);
    };
  })(this));
  this.graph.on('removeEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('removeEdge', edge);
    };
  })(this));
  this.graph.on('changeEdge', (function(_this) {
    return function(edge, oldMeta) {
      return _this.appendCommand('changeEdge', {
        from: edge.from,
        to: edge.to,
        "new": edge.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('addInitial', iip);
    };
  })(this));
  this.graph.on('removeInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('removeInitial', iip);
    };
  })(this));
  this.graph.on('changeProperties', (function(_this) {
    return function(newProps, oldProps) {
      return _this.appendCommand('changeProperties', {
        "new": newProps,
        old: oldProps
      });
    };
  })(this));
  this.graph.on('addGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('addGroup', group);
    };
  })(this));
  this.graph.on('renameGroup', (function(_this) {
    return function(oldName, newName) {
      return _this.appendCommand('renameGroup', {
        oldName: oldName,
        newName: newName
      });
    };
  })(this));
  this.graph.on('removeGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('removeGroup', group);
    };
  })( ...
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.Journal.prototype.endTransaction"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>endTransaction (id, meta)](#apidoc.element.noflo.Journal.prototype.endTransaction)
- description and source-code
```javascript
endTransaction = function (id, meta) {
  if (!this.subscribed) {
    return;
  }
  this.appendCommand('endTransaction', {
    id: id,
    metadata: meta
  }, this.currentRevision);
  this.store.putTransaction(this.currentRevision, this.entries);
  return this.entries = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.executeEntry"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>executeEntry (entry)](#apidoc.element.noflo.Journal.prototype.executeEntry)
- description and source-code
```javascript
executeEntry = function (entry) {
  var a;
  a = entry.args;
  switch (entry.cmd) {
    case 'addNode':
      return this.graph.addNode(a.id, a.component);
    case 'removeNode':
      return this.graph.removeNode(a.id);
    case 'renameNode':
      return this.graph.renameNode(a.oldId, a.newId);
    case 'changeNode':
      return this.graph.setNodeMetadata(a.id, calculateMeta(a.old, a["new"]));
    case 'addEdge':
      return this.graph.addEdge(a.from.node, a.from.port, a.to.node, a.to.port);
    case 'removeEdge':
      return this.graph.removeEdge(a.from.node, a.from.port, a.to.node, a.to.port);
    case 'changeEdge':
      return this.graph.setEdgeMetadata(a.from.node, a.from.port, a.to.node, a.to.port, calculateMeta(a.old, a["new"]));
    case 'addInitial':
      return this.graph.addInitial(a.from.data, a.to.node, a.to.port);
    case 'removeInitial':
      return this.graph.removeInitial(a.to.node, a.to.port);
    case 'startTransaction':
      return null;
    case 'endTransaction':
      return null;
    case 'changeProperties':
      return this.graph.setProperties(a["new"]);
    case 'addGroup':
      return this.graph.addGroup(a.name, a.nodes, a.metadata);
    case 'renameGroup':
      return this.graph.renameGroup(a.oldName, a.newName);
    case 'removeGroup':
      return this.graph.removeGroup(a.name);
    case 'changeGroup':
      return this.graph.setGroupMetadata(a.name, calculateMeta(a.old, a["new"]));
    case 'addInport':
      return this.graph.addInport(a.name, a.port.process, a.port.port, a.port.metadata);
    case 'removeInport':
      return this.graph.removeInport(a.name);
    case 'renameInport':
      return this.graph.renameInport(a.oldId, a.newId);
    case 'changeInport':
      return this.graph.setInportMetadata(a.name, calculateMeta(a.old, a["new"]));
    case 'addOutport':
      return this.graph.addOutport(a.name, a.port.process, a.port.port, a.port.metadata(a.name));
    case 'removeOutport':
      return this.graph.removeOutport;
    case 'renameOutport':
      return this.graph.renameOutport(a.oldId, a.newId);
    case 'changeOutport':
      return this.graph.setOutportMetadata(a.name, calculateMeta(a.old, a["new"]));
    default:
      throw new Error("Unknown journal entry: " + entry.cmd);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.executeEntryInversed"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>executeEntryInversed (entry)](#apidoc.element.noflo.Journal.prototype.executeEntryInversed)
- description and source-code
```javascript
executeEntryInversed = function (entry) {
  var a;
  a = entry.args;
  switch (entry.cmd) {
    case 'addNode':
      return this.graph.removeNode(a.id);
    case 'removeNode':
      return this.graph.addNode(a.id, a.component);
    case 'renameNode':
      return this.graph.renameNode(a.newId, a.oldId);
    case 'changeNode':
      return this.graph.setNodeMetadata(a.id, calculateMeta(a["new"], a.old));
    case 'addEdge':
      return this.graph.removeEdge(a.from.node, a.from.port, a.to.node, a.to.port);
    case 'removeEdge':
      return this.graph.addEdge(a.from.node, a.from.port, a.to.node, a.to.port);
    case 'changeEdge':
      return this.graph.setEdgeMetadata(a.from.node, a.from.port, a.to.node, a.to.port, calculateMeta(a["new"], a.old));
    case 'addInitial':
      return this.graph.removeInitial(a.to.node, a.to.port);
    case 'removeInitial':
      return this.graph.addInitial(a.from.data, a.to.node, a.to.port);
    case 'startTransaction':
      return null;
    case 'endTransaction':
      return null;
    case 'changeProperties':
      return this.graph.setProperties(a.old);
    case 'addGroup':
      return this.graph.removeGroup(a.name);
    case 'renameGroup':
      return this.graph.renameGroup(a.newName, a.oldName);
    case 'removeGroup':
      return this.graph.addGroup(a.name, a.nodes, a.metadata);
    case 'changeGroup':
      return this.graph.setGroupMetadata(a.name, calculateMeta(a["new"], a.old));
    case 'addInport':
      return this.graph.removeInport(a.name);
    case 'removeInport':
      return this.graph.addInport(a.name, a.port.process, a.port.port, a.port.metadata);
    case 'renameInport':
      return this.graph.renameInport(a.newId, a.oldId);
    case 'changeInport':
      return this.graph.setInportMetadata(a.name, calculateMeta(a["new"], a.old));
    case 'addOutport':
      return this.graph.removeOutport(a.name);
    case 'removeOutport':
      return this.graph.addOutport(a.name, a.port.process, a.port.port, a.port.metadata);
    case 'renameOutport':
      return this.graph.renameOutport(a.newId, a.oldId);
    case 'changeOutport':
      return this.graph.setOutportMetadata(a.name, calculateMeta(a["new"], a.old));
    default:
      throw new Error("Unknown journal entry: " + entry.cmd);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.moveToRevision"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>moveToRevision (revId)](#apidoc.element.noflo.Journal.prototype.moveToRevision)
- description and source-code
```javascript
moveToRevision = function (revId) {
  var entries, entry, i, j, l, len, m, n, r, ref, ref1, ref2, ref3, ref4, ref5;
  if (revId === this.currentRevision) {
    return;
  }
  this.subscribed = false;
  if (revId > this.currentRevision) {
    for (r = j = ref = this.currentRevision + 1, ref1 = revId; ref <= ref1 ? j <= ref1 : j >= ref1; r = ref <= ref1 ? ++j : --j) {
      ref2 = this.store.fetchTransaction(r);
      for (l = 0, len = ref2.length; l < len; l++) {
        entry = ref2[l];
        this.executeEntry(entry);
      }
    }
  } else {
    for (r = m = ref3 = this.currentRevision, ref4 = revId + 1; m >= ref4; r = m += -1) {
      entries = this.store.fetchTransaction(r);
      for (i = n = ref5 = entries.length - 1; n >= 0; i = n += -1) {
        this.executeEntryInversed(entries[i]);
      }
    }
  }
  this.currentRevision = revId;
  return this.subscribed = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.redo"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>redo ()](#apidoc.element.noflo.Journal.prototype.redo)
- description and source-code
```javascript
redo = function () {
  if (!this.canRedo()) {
    return;
  }
  return this.moveToRevision(this.currentRevision + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.save"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>save (file, success)](#apidoc.element.noflo.Journal.prototype.save)
- description and source-code
```javascript
save = function (file, success) {
  var json;
  json = JSON.stringify(this.toJSON(), null, 4);
  return require('fs').writeFile(file + ".json", json, "utf-8", function(err, data) {
    if (err) {
      throw err;
    }
    return success(file);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.startTransaction"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>startTransaction (id, meta)](#apidoc.element.noflo.Journal.prototype.startTransaction)
- description and source-code
```javascript
startTransaction = function (id, meta) {
  if (!this.subscribed) {
    return;
  }
  if (this.entries.length > 0) {
    throw Error("Inconsistent @entries");
  }
  this.currentRevision++;
  return this.appendCommand('startTransaction', {
    id: id,
    metadata: meta
  }, this.currentRevision);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>toJSON (startRev, endRev)](#apidoc.element.noflo.Journal.prototype.toJSON)
- description and source-code
```javascript
toJSON = function (startRev, endRev) {
  var entries, entry, j, l, len, r, ref, ref1, ref2;
  startRev |= 0;
  endRev |= this.store.lastRevision;
  entries = [];
  for (r = j = ref = startRev, ref1 = endRev; j < ref1; r = j += 1) {
    ref2 = this.store.fetchTransaction(r);
    for (l = 0, len = ref2.length; l < len; l++) {
      entry = ref2[l];
      entries.push(entryToPrettyString(entry));
    }
  }
  return entries;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.toPrettyString"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>toPrettyString (startRev, endRev)](#apidoc.element.noflo.Journal.prototype.toPrettyString)
- description and source-code
```javascript
toPrettyString = function (startRev, endRev) {
  var e, entry, j, l, len, lines, r, ref, ref1;
  startRev |= 0;
  endRev |= this.store.lastRevision;
  lines = [];
  for (r = j = ref = startRev, ref1 = endRev; ref <= ref1 ? j < ref1 : j > ref1; r = ref <= ref1 ? ++j : --j) {
    e = this.store.fetchTransaction(r);
    for (l = 0, len = e.length; l < len; l++) {
      entry = e[l];
      lines.push(entryToPrettyString(entry));
    }
  }
  return lines.join('\n');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Journal.prototype.undo"></a>[function <span class="apidocSignatureSpan">noflo.Journal.prototype.</span>undo ()](#apidoc.element.noflo.Journal.prototype.undo)
- description and source-code
```javascript
undo = function () {
  if (!this.canUndo()) {
    return;
  }
  return this.moveToRevision(this.currentRevision - 1);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.Network"></a>[module noflo.Network](#apidoc.module.noflo.Network)

#### <a name="apidoc.element.noflo.Network.Network"></a>[function <span class="apidocSignatureSpan">noflo.</span>Network (graph, options)](#apidoc.element.noflo.Network.Network)
- description and source-code
```javascript
function Network(graph, options) {
  this.options = options != null ? options : {};
  this.processes = {};
  this.connections = [];
  this.initials = [];
  this.nextInitials = [];
  this.defaults = [];
  this.graph = graph;
  this.started = false;
  this.debug = true;
  this.eventBuffer = [];
  if (!platform.isBrowser()) {
    this.baseDir = graph.baseDir || process.cwd();
  } else {
    this.baseDir = graph.baseDir || '/';
  }
  this.startupDate = null;
  if (graph.componentLoader) {
    this.loader = graph.componentLoader;
  } else {
    this.loader = new componentLoader.ComponentLoader(this.baseDir, this.options);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Network.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.Network.</span>EventEmitter ()](#apidoc.element.noflo.Network.EventEmitter)
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

#### <a name="apidoc.element.noflo.Network.init"></a>[function <span class="apidocSignatureSpan">noflo.Network.</span>init ()](#apidoc.element.noflo.Network.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Network.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.Network.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Network.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.Network.prototype"></a>[module noflo.Network.prototype](#apidoc.module.noflo.Network.prototype)

#### <a name="apidoc.element.noflo.Network.prototype.addDefaults"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addDefaults (node, callback)](#apidoc.element.noflo.Network.prototype.addDefaults)
- description and source-code
```javascript
addDefaults = function (node, callback) {
  var key, port, process, ref, socket;
  process = this.processes[node.id];
  if (!process.component.isReady()) {
    if (process.component.setMaxListeners) {
      process.component.setMaxListeners(0);
    }
    process.component.once("ready", (function(_this) {
      return function() {
        return _this.addDefaults(process, callback);
      };
    })(this));
    return;
  }
  ref = process.component.inPorts.ports;
  for (key in ref) {
    port = ref[key];
    if (typeof port.hasDefault === 'function' && port.hasDefault() && !port.isAttached()) {
      socket = internalSocket.createSocket();
      socket.setDebug(this.debug);
      this.subscribeSocket(socket);
      this.connectPort(socket, process, key, void 0, true);
      this.connections.push(socket);
      this.defaults.push(socket);
    }
  }
  return callback();
}
```
- example usage
```shell
...
process = this.processes[node.id];
if (!process.component.isReady()) {
  if (process.component.setMaxListeners) {
    process.component.setMaxListeners(0);
  }
  process.component.once("ready", (function(_this) {
    return function() {
      return _this.addDefaults(process, callback);
    };
  })(this));
  return;
}
ref = process.component.inPorts.ports;
for (key in ref) {
  port = ref[key];
...
```

#### <a name="apidoc.element.noflo.Network.prototype.addEdge"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addEdge (edge, callback)](#apidoc.element.noflo.Network.prototype.addEdge)
- description and source-code
```javascript
addEdge = function (edge, callback) {
  var from, socket, to;
  socket = internalSocket.createSocket(edge.metadata);
  socket.setDebug(this.debug);
  from = this.getNode(edge.from.node);
  if (!from) {
    return callback(new Error("No process defined for outbound node " + edge.from.node));
  }
  if (!from.component) {
    return callback(new Error("No component defined for outbound node " + edge.from.node));
  }
  if (!from.component.isReady()) {
    from.component.once("ready", (function(_this) {
      return function() {
        return _this.addEdge(edge, callback);
      };
    })(this));
    return;
  }
  to = this.getNode(edge.to.node);
  if (!to) {
    return callback(new Error("No process defined for inbound node " + edge.to.node));
  }
  if (!to.component) {
    return callback(new Error("No component defined for inbound node " + edge.to.node));
  }
  if (!to.component.isReady()) {
    to.component.once("ready", (function(_this) {
      return function() {
        return _this.addEdge(edge, callback);
      };
    })(this));
    return;
  }
  this.subscribeSocket(socket, from);
  this.connectPort(socket, to, edge.to.port, edge.to.index, true);
  this.connectPort(socket, from, edge.from.port, edge.from.index, false);
  this.connections.push(socket);
  return callback();
}
```
- example usage
```shell
...
}
if (!from.component) {
  return callback(new Error("No component defined for outbound node " + edge.from.node));
}
if (!from.component.isReady()) {
  from.component.once("ready", (function(_this) {
    return function() {
      return _this.addEdge(edge, callback);
    };
  })(this));
  return;
}
to = this.getNode(edge.to.node);
if (!to) {
  return callback(new Error("No process defined for inbound node " + edge.to.node));
...
```

#### <a name="apidoc.element.noflo.Network.prototype.addInitial"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addInitial (initializer, callback)](#apidoc.element.noflo.Network.prototype.addInitial)
- description and source-code
```javascript
addInitial = function (initializer, callback) {
  var init, socket, to;
  socket = internalSocket.createSocket(initializer.metadata);
  socket.setDebug(this.debug);
  this.subscribeSocket(socket);
  to = this.getNode(initializer.to.node);
  if (!to) {
    return callback(new Error("No process defined for inbound node " + initializer.to.node));
  }
  if (!(to.component.isReady() || to.component.inPorts[initializer.to.port])) {
    if (to.component.setMaxListeners) {
      to.component.setMaxListeners(0);
    }
    to.component.once("ready", (function(_this) {
      return function() {
        return _this.addInitial(initializer, callback);
      };
    })(this));
    return;
  }
  this.connectPort(socket, to, initializer.to.port, initializer.to.index, true);
  this.connections.push(socket);
  init = {
    socket: socket,
    data: initializer.from.data
  };
  this.initials.push(init);
  this.nextInitials.push(init);
  if (this.isStarted()) {
    this.sendInitials();
  }
  return callback();
}
```
- example usage
```shell
...
}
if (!(to.component.isReady() || to.component.inPorts[initializer.to.port])) {
  if (to.component.setMaxListeners) {
    to.component.setMaxListeners(0);
  }
  to.component.once("ready", (function(_this) {
    return function() {
      return _this.addInitial(initializer, callback);
    };
  })(this));
  return;
}
this.connectPort(socket, to, initializer.to.port, initializer.to.index, true);
this.connections.push(socket);
init = {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.addNode"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>addNode (node, callback)](#apidoc.element.noflo.Network.prototype.addNode)
- description and source-code
```javascript
addNode = function (node, callback) {
  var process;
  if (this.processes[node.id]) {
    callback(null, this.processes[node.id]);
    return;
  }
  process = {
    id: node.id
  };
  if (!node.component) {
    this.processes[process.id] = process;
    callback(null, process);
    return;
  }
  return this.load(node.component, node.metadata, (function(_this) {
    return function(err, instance) {
      var inPorts, name, outPorts, port;
      if (err) {
        return callback(err);
      }
      instance.nodeId = node.id;
      process.component = instance;
      process.componentName = node.component;
      inPorts = process.component.inPorts.ports || process.component.inPorts;
      outPorts = process.component.outPorts.ports || process.component.outPorts;
      for (name in inPorts) {
        port = inPorts[name];
        port.node = node.id;
        port.nodeInstance = instance;
        port.name = name;
      }
      for (name in outPorts) {
        port = outPorts[name];
        port.node = node.id;
        port.nodeInstance = instance;
        port.name = name;
      }
      if (instance.isSubgraph()) {
        _this.subscribeSubgraph(process);
      }
      _this.subscribeNode(process);
      _this.processes[process.id] = process;
      return callback(null, process);
    };
  })(this));
}
```
- example usage
```shell
...
    return options.loader.load(component, function(err, instance) {
var def, graph, inPorts, network, nodeName, outPorts, port;
if (err) {
  return callback(err);
}
graph = new Graph(options.name);
nodeName = options.name;
graph.addNode(nodeName, component);
inPorts = instance.inPorts.ports || instance.inPorts;
outPorts = instance.outPorts.ports || instance.outPorts;
for (port in inPorts) {
  def = inPorts[port];
  graph.addInport(port, nodeName, port);
}
for (port in outPorts) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.bufferedEmit"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>bufferedEmit (event, payload)](#apidoc.element.noflo.Network.prototype.bufferedEmit)
- description and source-code
```javascript
bufferedEmit = function (event, payload) {
  var ev, i, len, ref;
  if (event === 'error' || event === 'process-error' || event === 'end') {
    this.emit(event, payload);
    return;
  }
  if (!this.isStarted() && event !== 'end') {
    this.eventBuffer.push({
      type: event,
      payload: payload
    });
    return;
  }
  this.emit(event, payload);
  if (event === 'start') {
    ref = this.eventBuffer;
    for (i = 0, len = ref.length; i < len; i++) {
      ev = ref[i];
      this.emit(ev.type, ev.payload);
    }
    return this.eventBuffer = [];
  }
}
```
- example usage
```shell
...
      processOps = (function(_this) {
return function(err) {
  var cb, op;
  if (err) {
    if (_this.listeners('process-error').length === 0) {
      throw err;
    }
    _this.bufferedEmit('process-error', err);
  }
  if (!graphOps.length) {
    processing = false;
    return;
  }
  processing = true;
  op = graphOps.shift();
...
```

#### <a name="apidoc.element.noflo.Network.prototype.checkIfFinished"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>checkIfFinished ()](#apidoc.element.noflo.Network.prototype.checkIfFinished)
- description and source-code
```javascript
checkIfFinished = function () {
  if (this.isRunning()) {
    return;
  }
  delete this.abortDebounce;
  if (!this.debouncedEnd) {
    this.debouncedEnd = utils.debounce((function(_this) {
      return function() {
        if (_this.abortDebounce) {
          return;
        }
        if (_this.isRunning()) {
          return;
        }
        return _this.setStarted(false);
      };
    })(this), 50);
  }
  return this.debouncedEnd();
}
```
- example usage
```shell
...
    });
    if (source && source.component.isLegacy()) {
      source.component.__openConnections--;
      if (source.component.__openConnections < 0) {
        source.component.__openConnections = 0;
      }
      if (source.component.__openConnections === 0) {
        return _this.checkIfFinished();
      }
    }
  };
})(this));
return socket.on('error', (function(_this) {
  return function(event) {
    if (_this.listeners('process-error').length === 0) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.connect"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>connect (done)](#apidoc.element.noflo.Network.prototype.connect)
- description and source-code
```javascript
connect = function (done) {
  var callStack, edges, initializers, nodes, serialize, setDefaults, subscribeGraph;
  if (done == null) {
    done = function() {};
  }
  callStack = 0;
  serialize = (function(_this) {
    return function(next, add) {
      return function(type) {
        return _this["add" + type](add, function(err) {
          if (err) {
            return done(err);
          }
          callStack++;
          if (callStack % 100 === 0) {
            setTimeout(function() {
              return next(type);
            }, 0);
            return;
          }
          return next(type);
        });
      };
    };
  })(this);
  subscribeGraph = (function(_this) {
    return function() {
      _this.subscribeGraph();
      return done();
    };
  })(this);
  setDefaults = utils.reduceRight(this.graph.nodes, serialize, subscribeGraph);
  initializers = utils.reduceRight(this.graph.initializers, serialize, function() {
    return setDefaults("Defaults");
  });
  edges = utils.reduceRight(this.graph.edges, serialize, function() {
    return initializers("Initial");
  });
  nodes = utils.reduceRight(this.graph.nodes, serialize, function() {
    return edges("Edge");
  });
  return nodes("Node");
}
```
- example usage
```shell
...
        return function(err, network1) {
_this.network = network1;
if (err) {
  return callback(err);
}
_this.emit('network', _this.network);
_this.subscribeNetwork(_this.network);
return _this.network.connect(function(err) {
  var name, node, ref;
  if (err) {
    return callback(err);
  }
  ref = _this.network.processes;
  for (name in ref) {
    node = ref[name];
...
```

#### <a name="apidoc.element.noflo.Network.prototype.connectPort"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>connectPort (socket, process, port, index, inbound)](#apidoc.element.noflo.Network.prototype.connectPort)
- description and source-code
```javascript
connectPort = function (socket, process, port, index, inbound) {
  if (inbound) {
    socket.to = {
      process: process,
      port: port,
      index: index
    };
    if (!(process.component.inPorts && process.component.inPorts[port])) {
      throw new Error("No inport '" + port + "' defined in process " + process.id + " (" + (socket.getId()) + ")");
      return;
    }
    if (process.component.inPorts[port].isAddressable()) {
      return process.component.inPorts[port].attach(socket, index);
    }
    return process.component.inPorts[port].attach(socket);
  }
  socket.from = {
    process: process,
    port: port,
    index: index
  };
  if (!(process.component.outPorts && process.component.outPorts[port])) {
    throw new Error("No outport '" + port + "' defined in process " + process.id + " (" + (socket.getId()) + ")");
    return;
  }
  if (process.component.outPorts[port].isAddressable()) {
    return process.component.outPorts[port].attach(socket, index);
  }
  return process.component.outPorts[port].attach(socket);
}
```
- example usage
```shell
...
      return function() {
        return _this.addEdge(edge, callback);
      };
    })(this));
    return;
  }
  this.subscribeSocket(socket, from);
  this.connectPort(socket, to, edge.to.port, edge.to.index, true);
  this.connectPort(socket, from, edge.from.port, edge.from.index, false);
  this.connections.push(socket);
  return callback();
};

Network.prototype.removeEdge = function(edge, callback) {
  var connection, i, len, ref, results;
...
```

#### <a name="apidoc.element.noflo.Network.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>constructor (graph, options)](#apidoc.element.noflo.Network.prototype.constructor)
- description and source-code
```javascript
function Network(graph, options) {
  this.options = options != null ? options : {};
  this.processes = {};
  this.connections = [];
  this.initials = [];
  this.nextInitials = [];
  this.defaults = [];
  this.graph = graph;
  this.started = false;
  this.debug = true;
  this.eventBuffer = [];
  if (!platform.isBrowser()) {
    this.baseDir = graph.baseDir || process.cwd();
  } else {
    this.baseDir = graph.baseDir || '/';
  }
  this.startupDate = null;
  if (graph.componentLoader) {
    this.loader = graph.componentLoader;
  } else {
    this.loader = new componentLoader.ComponentLoader(this.baseDir, this.options);
  }
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.getActiveProcesses"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>getActiveProcesses ()](#apidoc.element.noflo.Network.prototype.getActiveProcesses)
- description and source-code
```javascript
getActiveProcesses = function () {
  var active, name, process, ref;
  active = [];
  if (!this.started) {
    return active;
  }
  ref = this.processes;
  for (name in ref) {
    process = ref[name];
    if (process.component.load > 0) {
      active.push(name);
    }
    if (process.component.__openConnections > 0) {
      active.push(name);
    }
  }
  return active;
}
```
- example usage
```shell
...
  return this.started;
};

Network.prototype.isRunning = function() {
  if (!this.started) {
    return false;
  }
  return this.getActiveProcesses().length > 0;
};

Network.prototype.startComponents = function(callback) {
  var count, id, length, onProcessStart, process, ref, results;
  if (!callback) {
    callback = function() {};
  }
...
```

#### <a name="apidoc.element.noflo.Network.prototype.getDebug"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>getDebug ()](#apidoc.element.noflo.Network.prototype.getDebug)
- description and source-code
```javascript
getDebug = function () {
  return this.debug;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Network.prototype.getNode"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>getNode (id)](#apidoc.element.noflo.Network.prototype.getNode)
- description and source-code
```javascript
getNode = function (id) {
  return this.processes[id];
}
```
- example usage
```shell
...
      return callback(null, network);
    });
  });
};

runNetwork = function(network, inputs, options, callback) {
  var inPorts, inSockets, outPorts, outSockets, process, received;
  process = network.getNode(options.name);
  inPorts = Object.keys(network.graph.inports);
  inSockets = {};
  inPorts.forEach(function(inport) {
    inSockets[inport] = internalSocket.createSocket();
    return process.component.inPorts[inport].attach(inSockets[inport]);
  });
  received = [];
...
```

#### <a name="apidoc.element.noflo.Network.prototype.isRunning"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>isRunning ()](#apidoc.element.noflo.Network.prototype.isRunning)
- description and source-code
```javascript
isRunning = function () {
  if (!this.started) {
    return false;
  }
  return this.getActiveProcesses().length > 0;
}
```
- example usage
```shell
...
  this.started = true;
  return this.bufferedEmit('start', {
    start: this.startupDate
  });
};

Network.prototype.checkIfFinished = function() {
  if (this.isRunning()) {
    return;
  }
  delete this.abortDebounce;
  if (!this.debouncedEnd) {
    this.debouncedEnd = utils.debounce((function(_this) {
      return function() {
        if (_this.abortDebounce) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.isStarted"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>isStarted ()](#apidoc.element.noflo.Network.prototype.isStarted)
- description and source-code
```javascript
isStarted = function () {
  return this.started;
}
```
- example usage
```shell
...
  }
  this.inPorts.add(targetPortName, port);
  this.inPorts[targetPortName].once('connect', (function(_this) {
    return function() {
      if (_this.starting) {
        return;
      }
      if (_this.isStarted()) {
        return;
      }
      return _this.start(function() {});
    };
  })(this));
}
for (portName in outPorts) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.load"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>load (component, metadata, callback)](#apidoc.element.noflo.Network.prototype.load)
- description and source-code
```javascript
load = function (component, metadata, callback) {
  return this.loader.load(component, callback, metadata);
}
```
- example usage
```shell
...
  if (!options.raw) {
    options.raw = false;
  }
  return options;
};

prepareNetwork = function(component, options, callback) {
  return options.loader.load(component, function(err, instance) {
    var def, graph, inPorts, network, nodeName, outPorts, port;
    if (err) {
      return callback(err);
    }
    graph = new Graph(options.name);
    nodeName = options.name;
    graph.addNode(nodeName, component);
...
```

#### <a name="apidoc.element.noflo.Network.prototype.removeEdge"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>removeEdge (edge, callback)](#apidoc.element.noflo.Network.prototype.removeEdge)
- description and source-code
```javascript
removeEdge = function (edge, callback) {
  var connection, i, len, ref, results;
  ref = this.connections;
  results = [];
  for (i = 0, len = ref.length; i < len; i++) {
    connection = ref[i];
    if (!connection) {
      continue;
    }
    if (!(edge.to.node === connection.to.process.id && edge.to.port === connection.to.port)) {
      continue;
    }
    connection.to.process.component.inPorts[connection.to.port].detach(connection);
    if (edge.from.node) {
      if (connection.from && edge.from.node === connection.from.process.id && edge.from.port === connection.from.port) {
        connection.from.process.component.outPorts[connection.from.port].detach(connection);
      }
    }
    this.connections.splice(this.connections.indexOf(connection), 1);
    results.push(callback());
  }
  return results;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Network.prototype.removeInitial"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>removeInitial (initializer, callback)](#apidoc.element.noflo.Network.prototype.removeInitial)
- description and source-code
```javascript
removeInitial = function (initializer, callback) {
  var connection, i, init, j, k, len, len1, len2, ref, ref1, ref2;
  ref = this.connections;
  for (i = 0, len = ref.length; i < len; i++) {
    connection = ref[i];
    if (!connection) {
      continue;
    }
    if (!(initializer.to.node === connection.to.process.id && initializer.to.port === connection.to.port)) {
      continue;
    }
    connection.to.process.component.inPorts[connection.to.port].detach(connection);
    this.connections.splice(this.connections.indexOf(connection), 1);
    ref1 = this.initials;
    for (j = 0, len1 = ref1.length; j < len1; j++) {
      init = ref1[j];
      if (!init) {
        continue;
      }
      if (init.socket !== connection) {
        continue;
      }
      this.initials.splice(this.initials.indexOf(init), 1);
    }
    ref2 = this.nextInitials;
    for (k = 0, len2 = ref2.length; k < len2; k++) {
      init = ref2[k];
      if (!init) {
        continue;
      }
      if (init.socket !== connection) {
        continue;
      }
      this.nextInitials.splice(this.nextInitials.indexOf(init), 1);
    }
  }
  return callback();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Network.prototype.removeNode"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>removeNode (node, callback)](#apidoc.element.noflo.Network.prototype.removeNode)
- description and source-code
```javascript
removeNode = function (node, callback) {
  if (!this.processes[node.id]) {
    return callback(new Error("Node " + node.id + " not found"));
  }
  return this.processes[node.id].component.shutdown((function(_this) {
    return function(err) {
      if (err) {
        return callback(err);
      }
      delete _this.processes[node.id];
      return callback(null);
    };
  })(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Network.prototype.renameNode"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>renameNode (oldId, newId, callback)](#apidoc.element.noflo.Network.prototype.renameNode)
- description and source-code
```javascript
renameNode = function (oldId, newId, callback) {
  var inPorts, name, outPorts, port, process;
  process = this.getNode(oldId);
  if (!process) {
    return callback(new Error("Process " + oldId + " not found"));
  }
  process.id = newId;
  inPorts = process.component.inPorts.ports || process.component.inPorts;
  outPorts = process.component.outPorts.ports || process.component.outPorts;
  for (name in inPorts) {
    port = inPorts[name];
    if (!port) {
      continue;
    }
    port.node = newId;
  }
  for (name in outPorts) {
    port = outPorts[name];
    if (!port) {
      continue;
    }
    port.node = newId;
  }
  this.processes[newId] = process;
  delete this.processes[oldId];
  return callback(null);
}
```
- example usage
```shell
...
      return;
    }
    processing = true;
    op = graphOps.shift();
    cb = processOps;
    switch (op.op) {
      case 'renameNode':
        return _this.renameNode(op.details.from, op.details.to, cb);
      default:
        return _this[op.op](op.details, cb);
    }
  };
})(this);
this.graph.on('addNode', function(node) {
  registerOp('addNode', node);
...
```

#### <a name="apidoc.element.noflo.Network.prototype.sendDefaults"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>sendDefaults (callback)](#apidoc.element.noflo.Network.prototype.sendDefaults)
- description and source-code
```javascript
sendDefaults = function (callback) {
  var i, len, ref, socket;
  if (!callback) {
    callback = function() {};
  }
  if (!this.defaults.length) {
    return callback();
  }
  ref = this.defaults;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    if (socket.to.process.component.inPorts[socket.to.port].sockets.length !== 1) {
      continue;
    }
    socket.connect();
    socket.send();
    socket.disconnect();
  }
  return callback();
}
```
- example usage
```shell
...
if (err) {
  return callback(err);
}
return _this.sendInitials(function(err) {
  if (err) {
    return callback(err);
  }
  return _this.sendDefaults(function(err) {
    if (err) {
      return callback(err);
    }
    _this.setStarted(true);
    return callback(null);
  });
});
...
```

#### <a name="apidoc.element.noflo.Network.prototype.sendInitial"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>sendInitial (initial)](#apidoc.element.noflo.Network.prototype.sendInitial)
- description and source-code
```javascript
sendInitial = function (initial) {
  return initial.socket.post(new IP('data', initial.data, {
    initial: true
  }));
}
```
- example usage
```shell
...
}
send = (function(_this) {
  return function() {
    var i, initial, len, ref;
    ref = _this.initials;
    for (i = 0, len = ref.length; i < len; i++) {
      initial = ref[i];
      _this.sendInitial(initial);
    }
    _this.initials = [];
    return callback();
  };
})(this);
if (typeof process !== 'undefined' && process.execPath && process.execPath.indexOf('node') !== -1) {
  return process.nextTick(send);
...
```

#### <a name="apidoc.element.noflo.Network.prototype.sendInitials"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>sendInitials (callback)](#apidoc.element.noflo.Network.prototype.sendInitials)
- description and source-code
```javascript
sendInitials = function (callback) {
  var send;
  if (!callback) {
    callback = function() {};
  }
  send = (function(_this) {
    return function() {
      var i, initial, len, ref;
      ref = _this.initials;
      for (i = 0, len = ref.length; i < len; i++) {
        initial = ref[i];
        _this.sendInitial(initial);
      }
      _this.initials = [];
      return callback();
    };
  })(this);
  if (typeof process !== 'undefined' && process.execPath && process.execPath.indexOf('node') !== -1) {
    return process.nextTick(send);
  } else {
    return setTimeout(send, 0);
  }
}
```
- example usage
```shell
...
  init = {
    socket: socket,
    data: initializer.from.data
  };
  this.initials.push(init);
  this.nextInitials.push(init);
  if (this.isStarted()) {
    this.sendInitials();
  }
  return callback();
};

Network.prototype.removeInitial = function(initializer, callback) {
  var connection, i, init, j, k, len, len1, len2, ref, ref1, ref2;
  ref = this.connections;
...
```

#### <a name="apidoc.element.noflo.Network.prototype.setDebug"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>setDebug (active)](#apidoc.element.noflo.Network.prototype.setDebug)
- description and source-code
```javascript
setDebug = function (active) {
  var i, instance, len, process, processId, ref, ref1, results, socket;
  if (active === this.debug) {
    return;
  }
  this.debug = active;
  ref = this.connections;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    socket.setDebug(active);
  }
  ref1 = this.processes;
  results = [];
  for (processId in ref1) {
    process = ref1[processId];
    instance = process.component;
    if (instance.isSubgraph()) {
      results.push(instance.network.setDebug(active));
    } else {
      results.push(void 0);
    }
  }
  return results;
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (!node.component.network) {
  return;
}
node.component.network.setDebug(this.debug);
emitSub = (function(_this) {
  return function(type, data) {
    if (type === 'process-error' && _this.listeners('process-error').length === 0) {
      if (data.id && data.metadata && data.error) {
        throw data.error;
      }
      throw data;
...
```

#### <a name="apidoc.element.noflo.Network.prototype.setStarted"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>setStarted (started)](#apidoc.element.noflo.Network.prototype.setStarted)
- description and source-code
```javascript
setStarted = function (started) {
  if (this.started === started) {
    return;
  }
  if (!started) {
    this.started = false;
    this.bufferedEmit('end', {
      start: this.startupDate,
      end: new Date,
      uptime: this.uptime()
    });
    return;
  }
  if (!this.startupDate) {
    this.startupDate = new Date;
  }
  this.started = true;
  return this.bufferedEmit('start', {
    start: this.startupDate
  });
}
```
- example usage
```shell
...
        if (err) {
          return callback(err);
        }
        return _this.sendDefaults(function(err) {
          if (err) {
            return callback(err);
          }
          _this.setStarted(true);
          return callback(null);
        });
      });
    };
  })(this));
};
...
```

#### <a name="apidoc.element.noflo.Network.prototype.start"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>start (callback)](#apidoc.element.noflo.Network.prototype.start)
- description and source-code
```javascript
start = function (callback) {
  if (!callback) {
    platform.deprecated('Calling network.start() without callback is deprecated');
    callback = function() {};
  }
  if (this.debouncedEnd) {
    this.abortDebounce = true;
  }
  if (this.started) {
    this.stop((function(_this) {
      return function(err) {
        if (err) {
          return callback(err);
        }
        return _this.start(callback);
      };
    })(this));
    return;
  }
  this.initials = this.nextInitials.slice(0);
  this.eventBuffer = [];
  return this.startComponents((function(_this) {
    return function(err) {
      if (err) {
        return callback(err);
      }
      return _this.sendInitials(function(err) {
        if (err) {
          return callback(err);
        }
        return _this.sendDefaults(function(err) {
          if (err) {
            return callback(err);
          }
          _this.setStarted(true);
          return callback(null);
        });
      });
    };
  })(this));
}
```
- example usage
```shell
...
    return function() {
      if (_this.starting) {
        return;
      }
      if (_this.isStarted()) {
        return;
      }
      return _this.start(function() {});
    };
  })(this));
}
for (portName in outPorts) {
  port = outPorts[portName];
  targetPortName = this.isExportedOutport(port, name, portName);
  if (targetPortName === false) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.startComponents"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>startComponents (callback)](#apidoc.element.noflo.Network.prototype.startComponents)
- description and source-code
```javascript
startComponents = function (callback) {
  var count, id, length, onProcessStart, process, ref, results;
  if (!callback) {
    callback = function() {};
  }
  count = 0;
  length = this.processes ? Object.keys(this.processes).length : 0;
  onProcessStart = function(err) {
    if (err) {
      return callback(err);
    }
    count++;
    if (count === length) {
      return callback();
    }
  };
  if (!(this.processes && Object.keys(this.processes).length)) {
    return callback();
  }
  ref = this.processes;
  results = [];
  for (id in ref) {
    process = ref[id];
    if (process.component.isStarted()) {
      onProcessStart();
      continue;
    }
    if (process.component.start.length === 0) {
      platform.deprecated('component.start method without callback is deprecated');
      process.component.start();
      onProcessStart();
      continue;
    }
    results.push(process.component.start(onProcessStart));
  }
  return results;
}
```
- example usage
```shell
...
      return _this.start(callback);
    };
  })(this));
  return;
}
this.initials = this.nextInitials.slice(0);
this.eventBuffer = [];
return this.startComponents((function(_this) {
  return function(err) {
    if (err) {
      return callback(err);
    }
    return _this.sendInitials(function(err) {
      if (err) {
        return callback(err);
...
```

#### <a name="apidoc.element.noflo.Network.prototype.stop"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>stop (callback)](#apidoc.element.noflo.Network.prototype.stop)
- description and source-code
```javascript
stop = function (callback) {
  var connection, count, i, id, len, length, onProcessEnd, process, ref, ref1, results;
  if (!callback) {
    platform.deprecated('Calling network.stop() without callback is deprecated');
    callback = function() {};
  }
  if (this.debouncedEnd) {
    this.abortDebounce = true;
  }
  if (!this.started) {
    return callback(null);
  }
  ref = this.connections;
  for (i = 0, len = ref.length; i < len; i++) {
    connection = ref[i];
    if (!connection.isConnected()) {
      continue;
    }
    connection.disconnect();
  }
  count = 0;
  length = this.processes ? Object.keys(this.processes).length : 0;
  onProcessEnd = (function(_this) {
    return function(err) {
      if (err) {
        return callback(err);
      }
      count++;
      if (count === length) {
        _this.setStarted(false);
        return callback();
      }
    };
  })(this);
  if (!(this.processes && Object.keys(this.processes).length)) {
    this.setStarted(false);
    return callback();
  }
  ref1 = this.processes;
  results = [];
  for (id in ref1) {
    process = ref1[id];
    if (!process.component.isStarted()) {
      onProcessEnd();
      continue;
    }
    if (process.component.shutdown.length === 0) {
      platform.deprecated('component.shutdown method without callback is deprecated');
      process.component.shutdown();
      onProcessEnd();
      continue;
    }
    results.push(process.component.shutdown(onProcessEnd));
  }
  return results;
}
```
- example usage
```shell
...
};

Graph.prototype.tearDown = function(callback) {
  this.starting = false;
  if (!this.network) {
    return callback(null);
  }
  return this.network.stop(function(err) {
    if (err) {
      return callback(err);
    }
    return callback();
  });
};
...
```

#### <a name="apidoc.element.noflo.Network.prototype.subscribeGraph"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeGraph ()](#apidoc.element.noflo.Network.prototype.subscribeGraph)
- description and source-code
```javascript
subscribeGraph = function () {
  var graphOps, processOps, processing, registerOp;
  graphOps = [];
  processing = false;
  registerOp = function(op, details) {
    return graphOps.push({
      op: op,
      details: details
    });
  };
  processOps = (function(_this) {
    return function(err) {
      var cb, op;
      if (err) {
        if (_this.listeners('process-error').length === 0) {
          throw err;
        }
        _this.bufferedEmit('process-error', err);
      }
      if (!graphOps.length) {
        processing = false;
        return;
      }
      processing = true;
      op = graphOps.shift();
      cb = processOps;
      switch (op.op) {
        case 'renameNode':
          return _this.renameNode(op.details.from, op.details.to, cb);
        default:
          return _this[op.op](op.details, cb);
      }
    };
  })(this);
  this.graph.on('addNode', function(node) {
    registerOp('addNode', node);
    if (!processing) {
      return processOps();
    }
  });
  this.graph.on('removeNode', function(node) {
    registerOp('removeNode', node);
    if (!processing) {
      return processOps();
    }
  });
  this.graph.on('renameNode', function(oldId, newId) {
    registerOp('renameNode', {
      from: oldId,
      to: newId
    });
    if (!processing) {
      return processOps();
    }
  });
  this.graph.on('addEdge', function(edge) {
    registerOp('addEdge', edge);
    if (!processing) {
      return processOps();
    }
  });
  this.graph.on('removeEdge', function(edge) {
    registerOp('removeEdge', edge);
    if (!processing) {
      return processOps();
    }
  });
  this.graph.on('addInitial', function(iip) {
    registerOp('addInitial', iip);
    if (!processing) {
      return processOps();
    }
  });
  return this.graph.on('removeInitial', function(iip) {
    registerOp('removeInitial', iip);
    if (!processing) {
      return processOps();
    }
  });
}
```
- example usage
```shell
...
        return next(type);
      });
    };
  };
})(this);
subscribeGraph = (function(_this) {
  return function() {
    _this.subscribeGraph();
    return done();
  };
})(this);
setDefaults = utils.reduceRight(this.graph.nodes, serialize, subscribeGraph);
initializers = utils.reduceRight(this.graph.initializers, serialize, function() {
  return setDefaults("Defaults");
});
...
```

#### <a name="apidoc.element.noflo.Network.prototype.subscribeNode"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeNode (node)](#apidoc.element.noflo.Network.prototype.subscribeNode)
- description and source-code
```javascript
subscribeNode = function (node) {
  node.component.on('deactivate', (function(_this) {
    return function(load) {
      if (load > 0) {
        return;
      }
      return _this.checkIfFinished();
    };
  })(this));
  if (!node.component.getIcon) {
    return;
  }
  return node.component.on('icon', (function(_this) {
    return function() {
      return _this.bufferedEmit('icon', {
        id: node.id,
        icon: node.component.getIcon()
      });
    };
  })(this));
}
```
- example usage
```shell
...
        port.node = node.id;
        port.nodeInstance = instance;
        port.name = name;
      }
      if (instance.isSubgraph()) {
        _this.subscribeSubgraph(process);
      }
      _this.subscribeNode(process);
      _this.processes[process.id] = process;
      return callback(null, process);
    };
  })(this));
};

Network.prototype.removeNode = function(node, callback) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.subscribeSocket"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeSocket (socket, source)](#apidoc.element.noflo.Network.prototype.subscribeSocket)
- description and source-code
```javascript
subscribeSocket = function (socket, source) {
  socket.on('ip', (function(_this) {
    return function(ip) {
      return _this.bufferedEmit('ip', {
        id: socket.getId(),
        type: ip.type,
        socket: socket,
        data: ip.data,
        metadata: socket.metadata
      });
    };
  })(this));
  socket.on('connect', (function(_this) {
    return function() {
      if (source && source.component.isLegacy()) {
        if (!source.component.__openConnections) {
          source.component.__openConnections = 0;
        }
        source.component.__openConnections++;
      }
      return _this.bufferedEmit('connect', {
        id: socket.getId(),
        socket: socket,
        metadata: socket.metadata
      });
    };
  })(this));
  socket.on('begingroup', (function(_this) {
    return function(group) {
      return _this.bufferedEmit('begingroup', {
        id: socket.getId(),
        socket: socket,
        group: group,
        metadata: socket.metadata
      });
    };
  })(this));
  socket.on('data', (function(_this) {
    return function(data) {
      return _this.bufferedEmit('data', {
        id: socket.getId(),
        socket: socket,
        data: data,
        metadata: socket.metadata
      });
    };
  })(this));
  socket.on('endgroup', (function(_this) {
    return function(group) {
      return _this.bufferedEmit('endgroup', {
        id: socket.getId(),
        socket: socket,
        group: group,
        metadata: socket.metadata
      });
    };
  })(this));
  socket.on('disconnect', (function(_this) {
    return function() {
      _this.bufferedEmit('disconnect', {
        id: socket.getId(),
        socket: socket,
        metadata: socket.metadata
      });
      if (source && source.component.isLegacy()) {
        source.component.__openConnections--;
        if (source.component.__openConnections < 0) {
          source.component.__openConnections = 0;
        }
        if (source.component.__openConnections === 0) {
          return _this.checkIfFinished();
        }
      }
    };
  })(this));
  return socket.on('error', (function(_this) {
    return function(event) {
      if (_this.listeners('process-error').length === 0) {
        if (event.id && event.metadata && event.error) {
          throw event.error;
        }
        throw event;
      }
      return _this.bufferedEmit('process-error', event);
    };
  })(this));
}
```
- example usage
```shell
...
    to.component.once("ready", (function(_this) {
      return function() {
        return _this.addEdge(edge, callback);
      };
    })(this));
    return;
  }
  this.subscribeSocket(socket, from);
  this.connectPort(socket, to, edge.to.port, edge.to.index, true);
  this.connectPort(socket, from, edge.from.port, edge.from.index, false);
  this.connections.push(socket);
  return callback();
};

Network.prototype.removeEdge = function(edge, callback) {
...
```

#### <a name="apidoc.element.noflo.Network.prototype.subscribeSubgraph"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>subscribeSubgraph (node)](#apidoc.element.noflo.Network.prototype.subscribeSubgraph)
- description and source-code
```javascript
subscribeSubgraph = function (node) {
  var emitSub;
  if (!node.component.isReady()) {
    node.component.once('ready', (function(_this) {
      return function() {
        return _this.subscribeSubgraph(node);
      };
    })(this));
    return;
  }
  if (!node.component.network) {
    return;
  }
  node.component.network.setDebug(this.debug);
  emitSub = (function(_this) {
    return function(type, data) {
      if (type === 'process-error' && _this.listeners('process-error').length === 0) {
        if (data.id && data.metadata && data.error) {
          throw data.error;
        }
        throw data;
      }
      if (!data) {
        data = {};
      }
      if (data.subgraph) {
        if (!data.subgraph.unshift) {
          data.subgraph = [data.subgraph];
        }
        data.subgraph = data.subgraph.unshift(node.id);
      } else {
        data.subgraph = [node.id];
      }
      return _this.bufferedEmit(type, data);
    };
  })(this);
  node.component.network.on('connect', function(data) {
    return emitSub('connect', data);
  });
  node.component.network.on('begingroup', function(data) {
    return emitSub('begingroup', data);
  });
  node.component.network.on('data', function(data) {
    return emitSub('data', data);
  });
  node.component.network.on('endgroup', function(data) {
    return emitSub('endgroup', data);
  });
  node.component.network.on('disconnect', function(data) {
    return emitSub('disconnect', data);
  });
  node.component.network.on('ip', function(data) {
    return emitSub('ip', data);
  });
  return node.component.network.on('process-error', function(data) {
    return emitSub('process-error', data);
  });
}
```
- example usage
```shell
...
      for (name in outPorts) {
        port = outPorts[name];
        port.node = node.id;
        port.nodeInstance = instance;
        port.name = name;
      }
      if (instance.isSubgraph()) {
        _this.subscribeSubgraph(process);
      }
      _this.subscribeNode(process);
      _this.processes[process.id] = process;
      return callback(null, process);
    };
  })(this));
};
...
```

#### <a name="apidoc.element.noflo.Network.prototype.uptime"></a>[function <span class="apidocSignatureSpan">noflo.Network.prototype.</span>uptime ()](#apidoc.element.noflo.Network.prototype.uptime)
- description and source-code
```javascript
uptime = function () {
  if (!this.startupDate) {
    return 0;
  }
  return new Date() - this.startupDate;
}
```
- example usage
```shell
...
  return;
}
if (!started) {
  this.started = false;
  this.bufferedEmit('end', {
    start: this.startupDate,
    end: new Date,
    uptime: this.uptime()
  });
  return;
}
if (!this.startupDate) {
  this.startupDate = new Date;
}
this.started = true;
...
```



# <a name="apidoc.module.noflo.OutPort"></a>[module noflo.OutPort](#apidoc.module.noflo.OutPort)

#### <a name="apidoc.element.noflo.OutPort.OutPort"></a>[function <span class="apidocSignatureSpan">noflo.</span>OutPort (options)](#apidoc.element.noflo.OutPort.OutPort)
- description and source-code
```javascript
function OutPort(options) {
  this.cache = {};
  OutPort.__super__.constructor.call(this, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPort.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.</span>EventEmitter ()](#apidoc.element.noflo.OutPort.EventEmitter)
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

#### <a name="apidoc.element.noflo.OutPort.init"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.</span>init ()](#apidoc.element.noflo.OutPort.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPort.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.</span>listenerCount (emitter, type)](#apidoc.element.noflo.OutPort.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.OutPort.prototype"></a>[module noflo.OutPort.prototype](#apidoc.module.noflo.OutPort.prototype)

#### <a name="apidoc.element.noflo.OutPort.prototype.attach"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>attach (socket, index)](#apidoc.element.noflo.OutPort.prototype.attach)
- description and source-code
```javascript
attach = function (socket, index) {
  if (index == null) {
    index = null;
  }
  OutPort.__super__.attach.call(this, socket, index);
  if (this.isCaching() && (this.cache[index] != null)) {
    return this.send(this.cache[index], index);
  }
}
```
- example usage
```shell
...
  runNetwork = function(network, inputs, options, callback) {
var inPorts, inSockets, outPorts, outSockets, process, received;
process = network.getNode(options.name);
inPorts = Object.keys(network.graph.inports);
inSockets = {};
inPorts.forEach(function(inport) {
  inSockets[inport] = internalSocket.createSocket();
  return process.component.inPorts[inport].attach(inSockets[inport]);
});
received = [];
outPorts = Object.keys(network.graph.outports);
outSockets = {};
outPorts.forEach(function(outport) {
  outSockets[outport] = internalSocket.createSocket();
  process.component.outPorts[outport].attach(outSockets[outport]);
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.beginGroup"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>beginGroup (group, socketId)](#apidoc.element.noflo.OutPort.prototype.beginGroup)
- description and source-code
```javascript
beginGroup = function (group, socketId) {
  var sockets;
  if (socketId == null) {
    socketId = null;
  }
  sockets = this.getSockets(socketId);
  this.checkRequired(sockets);
  return sockets.forEach(function(socket) {
    if (!socket) {
      return;
    }
    return socket.beginGroup(group);
  });
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.beginGroup(group, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.checkRequired"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>checkRequired (sockets)](#apidoc.element.noflo.OutPort.prototype.checkRequired)
- description and source-code
```javascript
checkRequired = function (sockets) {
  if (sockets.length === 0 && this.isRequired()) {
    throw new Error((this.getId()) + ": No connections available");
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPort.prototype.closeBracket"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>closeBracket (data, options, socketId)](#apidoc.element.noflo.OutPort.prototype.closeBracket)
- description and source-code
```javascript
closeBracket = function (data, options, socketId) {
  if (data == null) {
    data = null;
  }
  if (options == null) {
    options = {};
  }
  if (socketId == null) {
    socketId = null;
  }
  return this.sendIP('closeBracket', data, options, socketId);
}
```
- example usage
```shell
...
      });
    }
    this.outPorts[errorPort].data(e, {
      scope: scope
    });
    for (j = 0, len2 = groups.length; j < len2; j++) {
      group = groups[j];
      this.outPorts[errorPort].closeBracket(group, {
        scope: scope
      });
    }
    return;
  }
  throw e;
};
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.connect"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>connect (socketId)](#apidoc.element.noflo.OutPort.prototype.connect)
- description and source-code
```javascript
connect = function (socketId) {
  var i, len, results, socket, sockets;
  if (socketId == null) {
    socketId = null;
  }
  sockets = this.getSockets(socketId);
  this.checkRequired(sockets);
  results = [];
  for (i = 0, len = sockets.length; i < len; i++) {
    socket = sockets[i];
    if (!socket) {
      continue;
    }
    results.push(socket.connect());
  }
  return results;
}
```
- example usage
```shell
...
        return function(err, network1) {
_this.network = network1;
if (err) {
  return callback(err);
}
_this.emit('network', _this.network);
_this.subscribeNetwork(_this.network);
return _this.network.connect(function(err) {
  var name, node, ref;
  if (err) {
    return callback(err);
  }
  ref = _this.network.processes;
  for (name in ref) {
    node = ref[name];
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>constructor (options)](#apidoc.element.noflo.OutPort.prototype.constructor)
- description and source-code
```javascript
function OutPort(options) {
  this.cache = {};
  OutPort.__super__.constructor.call(this, options);
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.data"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>data (data, options, socketId)](#apidoc.element.noflo.OutPort.prototype.data)
- description and source-code
```javascript
data = function (data, options, socketId) {
  if (options == null) {
    options = {};
  }
  if (socketId == null) {
    socketId = null;
  }
  return this.sendIP('data', data, options, socketId);
}
```
- example usage
```shell
...
      if (this.outPorts[errorPort] && (this.outPorts[errorPort].isAttached() || !this.outPorts[errorPort].isRequired())) {
for (i = 0, len1 = groups.length; i < len1; i++) {
  group = groups[i];
  this.outPorts[errorPort].openBracket(group, {
    scope: scope
  });
}
this.outPorts[errorPort].data(e, {
  scope: scope
});
for (j = 0, len2 = groups.length; j < len2; j++) {
  group = groups[j];
  this.outPorts[errorPort].closeBracket(group, {
    scope: scope
  });
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>disconnect (socketId)](#apidoc.element.noflo.OutPort.prototype.disconnect)
- description and source-code
```javascript
disconnect = function (socketId) {
  var i, len, results, socket, sockets;
  if (socketId == null) {
    socketId = null;
  }
  sockets = this.getSockets(socketId);
  this.checkRequired(sockets);
  results = [];
  for (i = 0, len = sockets.length; i < len; i++) {
    socket = sockets[i];
    if (!socket) {
      continue;
    }
    results.push(socket.disconnect());
  }
  return results;
}
```
- example usage
```shell
...
  }
  ref = this.sockets;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    if (!socket) {
      return;
    }
    socket.disconnect();
  }
  return;
}
if (!this.sockets[socketId]) {
  return;
}
return this.sockets[socketId].disconnect();
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.endGroup"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>endGroup (socketId)](#apidoc.element.noflo.OutPort.prototype.endGroup)
- description and source-code
```javascript
endGroup = function (socketId) {
  var i, len, results, socket, sockets;
  if (socketId == null) {
    socketId = null;
  }
  sockets = this.getSockets(socketId);
  this.checkRequired(sockets);
  results = [];
  for (i = 0, len = sockets.length; i < len; i++) {
    socket = sockets[i];
    if (!socket) {
      continue;
    }
    results.push(socket.endGroup());
  }
  return results;
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.endGroup(index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.getSockets"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>getSockets (socketId)](#apidoc.element.noflo.OutPort.prototype.getSockets)
- description and source-code
```javascript
getSockets = function (socketId) {
  if (this.isAddressable()) {
    if (socketId === null) {
      throw new Error((this.getId()) + " Socket ID required");
    }
    if (!this.sockets[socketId]) {
      return [];
    }
    return [this.sockets[socketId]];
  }
  return this.sockets;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPort.prototype.isCaching"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>isCaching ()](#apidoc.element.noflo.OutPort.prototype.isCaching)
- description and source-code
```javascript
isCaching = function () {
  if (this.options.caching) {
    return true;
  }
  return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPort.prototype.openBracket"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>openBracket (data, options, socketId)](#apidoc.element.noflo.OutPort.prototype.openBracket)
- description and source-code
```javascript
openBracket = function (data, options, socketId) {
  if (data == null) {
    data = null;
  }
  if (options == null) {
    options = {};
  }
  if (socketId == null) {
    socketId = null;
  }
  return this.sendIP('openBracket', data, options, socketId);
}
```
- example usage
```shell
...
}
if (scope == null) {
  scope = null;
}
if (this.outPorts[errorPort] && (this.outPorts[errorPort].isAttached() || !this.outPorts[errorPort].isRequired())) {
  for (i = 0, len1 = groups.length; i < len1; i++) {
    group = groups[i];
    this.outPorts[errorPort].openBracket(group, {
      scope: scope
    });
  }
  this.outPorts[errorPort].data(e, {
    scope: scope
  });
  for (j = 0, len2 = groups.length; j < len2; j++) {
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.send"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>send (data, socketId)](#apidoc.element.noflo.OutPort.prototype.send)
- description and source-code
```javascript
send = function (data, socketId) {
  var sockets;
  if (socketId == null) {
    socketId = null;
  }
  sockets = this.getSockets(socketId);
  this.checkRequired(sockets);
  if (this.isCaching() && data !== this.cache[socketId]) {
    this.cache[socketId] = data;
  }
  return sockets.forEach(function(socket) {
    if (!socket) {
      return;
    }
    return socket.send(data);
  });
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.send(data, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.OutPort.prototype.sendIP"></a>[function <span class="apidocSignatureSpan">noflo.OutPort.prototype.</span>sendIP (type, data, options, socketId, autoConnect)](#apidoc.element.noflo.OutPort.prototype.sendIP)
- description and source-code
```javascript
sendIP = function (type, data, options, socketId, autoConnect) {
  var i, ip, len, pristine, ref, socket, sockets;
  if (autoConnect == null) {
    autoConnect = true;
  }
  if (IP.isIP(type)) {
    ip = type;
    socketId = ip.index;
  } else {
    ip = new IP(type, data, options);
  }
  sockets = this.getSockets(socketId);
  this.checkRequired(sockets);
  if (this.isCaching() && data !== ((ref = this.cache[socketId]) != null ? ref.data : void 0)) {
    this.cache[socketId] = ip;
  }
  pristine = true;
  for (i = 0, len = sockets.length; i < len; i++) {
    socket = sockets[i];
    if (!socket) {
      continue;
    }
    if (pristine) {
      socket.post(ip, autoConnect);
      pristine = false;
    } else {
      if (ip.clonable) {
        ip = ip.clone();
      }
      socket.post(ip, autoConnect);
    }
  }
  return this;
}
```
- example usage
```shell
...
      if (ip.type === 'openBracket') {
        debugSend(this.nodeId + " sending " + portIdentifier + " < '" + ip.data + "'");
      } else if (ip.type === 'closeBracket') {
        debugSend(this.nodeId + " sending " + portIdentifier + " > '" + ip.data + "'");
      } else {
        debugSend(this.nodeId + " sending " + portIdentifier + " DATA");
      }
      this.outPorts[port].sendIP(ip);
    }
  }
  continue;
}
if (!this.outPorts.ports[port].isAttached()) {
  continue;
}
...
```



# <a name="apidoc.module.noflo.OutPorts"></a>[module noflo.OutPorts](#apidoc.module.noflo.OutPorts)

#### <a name="apidoc.element.noflo.OutPorts.OutPorts"></a>[function <span class="apidocSignatureSpan">noflo.</span>OutPorts ()](#apidoc.element.noflo.OutPorts.OutPorts)
- description and source-code
```javascript
function OutPorts() {
  return OutPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
}
if (!options.outPorts) {
  options.outPorts = {};
}
if (options.outPorts instanceof ports.OutPorts) {
  this.outPorts = options.outPorts;
} else {
  this.outPorts = new ports.OutPorts(options.outPorts);
}
if (options.icon) {
  this.icon = options.icon;
}
if (options.description) {
  this.description = options.description;
}
...
```

#### <a name="apidoc.element.noflo.OutPorts.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.</span>EventEmitter ()](#apidoc.element.noflo.OutPorts.EventEmitter)
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

#### <a name="apidoc.element.noflo.OutPorts.init"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.</span>init ()](#apidoc.element.noflo.OutPorts.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.OutPorts.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.</span>listenerCount (emitter, type)](#apidoc.element.noflo.OutPorts.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.OutPorts.prototype"></a>[module noflo.OutPorts.prototype](#apidoc.module.noflo.OutPorts.prototype)

#### <a name="apidoc.element.noflo.OutPorts.prototype.beginGroup"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>beginGroup (name, group, socketId)](#apidoc.element.noflo.OutPorts.prototype.beginGroup)
- description and source-code
```javascript
beginGroup = function (name, group, socketId) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not available");
  }
  return this.ports[name].beginGroup(group, socketId);
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.beginGroup(group, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.OutPorts.prototype.connect"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>connect (name, socketId)](#apidoc.element.noflo.OutPorts.prototype.connect)
- description and source-code
```javascript
connect = function (name, socketId) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not available");
  }
  return this.ports[name].connect(socketId);
}
```
- example usage
```shell
...
        return function(err, network1) {
_this.network = network1;
if (err) {
  return callback(err);
}
_this.emit('network', _this.network);
_this.subscribeNetwork(_this.network);
return _this.network.connect(function(err) {
  var name, node, ref;
  if (err) {
    return callback(err);
  }
  ref = _this.network.processes;
  for (name in ref) {
    node = ref[name];
...
```

#### <a name="apidoc.element.noflo.OutPorts.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>constructor ()](#apidoc.element.noflo.OutPorts.prototype.constructor)
- description and source-code
```javascript
function OutPorts() {
  return OutPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.OutPorts.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>disconnect (name, socketId)](#apidoc.element.noflo.OutPorts.prototype.disconnect)
- description and source-code
```javascript
disconnect = function (name, socketId) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not available");
  }
  return this.ports[name].disconnect(socketId);
}
```
- example usage
```shell
...
  }
  ref = this.sockets;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    if (!socket) {
      return;
    }
    socket.disconnect();
  }
  return;
}
if (!this.sockets[socketId]) {
  return;
}
return this.sockets[socketId].disconnect();
...
```

#### <a name="apidoc.element.noflo.OutPorts.prototype.endGroup"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>endGroup (name, socketId)](#apidoc.element.noflo.OutPorts.prototype.endGroup)
- description and source-code
```javascript
endGroup = function (name, socketId) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not available");
  }
  return this.ports[name].endGroup(socketId);
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.endGroup(index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.OutPorts.prototype.model"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>model (options)](#apidoc.element.noflo.OutPorts.prototype.model)
- description and source-code
```javascript
function OutPort(options) {
  this.cache = {};
  OutPort.__super__.constructor.call(this, options);
}
```
- example usage
```shell
...
  }
  if (this.ports[name]) {
    this.remove(name);
  }
  if (typeof options === 'object' && options.canAttach) {
    this.ports[name] = options;
  } else {
    this.ports[name] = new this.model(options, process);
  }
  this[name] = this.ports[name];
  this.emit('add', name);
  return this;
};

Ports.prototype.remove = function(name) {
...
```

#### <a name="apidoc.element.noflo.OutPorts.prototype.send"></a>[function <span class="apidocSignatureSpan">noflo.OutPorts.prototype.</span>send (name, data, socketId)](#apidoc.element.noflo.OutPorts.prototype.send)
- description and source-code
```javascript
send = function (name, data, socketId) {
  if (!this.ports[name]) {
    throw new Error("Port " + name + " not available");
  }
  return this.ports[name].send(data, socketId);
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.send(data, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```



# <a name="apidoc.module.noflo.Platform"></a>[module noflo.Platform](#apidoc.module.noflo.Platform)

#### <a name="apidoc.element.noflo.Platform.deprecated"></a>[function <span class="apidocSignatureSpan">noflo.Platform.</span>deprecated (message)](#apidoc.element.noflo.Platform.deprecated)
- description and source-code
```javascript
deprecated = function (message) {
  if (exports.isBrowser()) {
    if (window.NOFLO_FATAL_DEPRECATED) {
      throw new Error(message);
    }
    console.warn(message);
    return;
  }
  if (process.env.NOFLO_FATAL_DEPRECATED) {
    throw new Error(message);
  }
  return console.warn(message);
}
```
- example usage
```shell
...
  platform = require('./Platform');

  ArrayPort = (function(superClass) {
extend(ArrayPort, superClass);

function ArrayPort(type) {
  this.type = type;
  platform.deprecated('noflo.ArrayPort is deprecated. Please port to noflo.InPort/noflo.OutPort and use addressable: true');
  ArrayPort.__super__.constructor.call(this, this.type);
}

ArrayPort.prototype.attach = function(socket, socketId) {
  if (socketId == null) {
    socketId = null;
  }
...
```

#### <a name="apidoc.element.noflo.Platform.isBrowser"></a>[function <span class="apidocSignatureSpan">noflo.Platform.</span>isBrowser ()](#apidoc.element.noflo.Platform.isBrowser)
- description and source-code
```javascript
isBrowser = function () {
  if (typeof process !== 'undefined' && process.execPath && process.execPath.match(/node|iojs/)) {
    return false;
  }
  return true;
}
```
- example usage
```shell
...
this.initials = [];
this.nextInitials = [];
this.defaults = [];
this.graph = graph;
this.started = false;
this.debug = true;
this.eventBuffer = [];
if (!platform.isBrowser()) {
  this.baseDir = graph.baseDir || process.cwd();
} else {
  this.baseDir = graph.baseDir || '/';
}
this.startupDate = null;
if (graph.componentLoader) {
  this.loader = graph.componentLoader;
...
```



# <a name="apidoc.module.noflo.Port"></a>[module noflo.Port](#apidoc.module.noflo.Port)

#### <a name="apidoc.element.noflo.Port.Port"></a>[function <span class="apidocSignatureSpan">noflo.</span>Port (type)](#apidoc.element.noflo.Port.Port)
- description and source-code
```javascript
function Port(type) {
  this.type = type;
  platform.deprecated('noflo.Port is deprecated. Please port to noflo.InPort/noflo.OutPort');
  if (!this.type) {
    this.type = 'all';
  }
  if (this.type === 'integer') {
    this.type = 'int';
  }
  this.sockets = [];
  this.from = null;
  this.node = null;
  this.name = null;
}
```
- example usage
```shell
...
}
if (!this.outPorts[this.outPortName]) {
  throw new Error("no outPort named '" + this.outPortName + "'");
}
this.load = 0;
this.q = [];
this.errorGroups = [];
this.outPorts.load = new port.Port();
this.inPorts[this.inPortName].on("begingroup", (function(_this) {
  return function(group) {
    if (_this.load > 0) {
      return _this.q.push({
        name: "begingroup",
        data: group
      });
...
```

#### <a name="apidoc.element.noflo.Port.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.Port.</span>EventEmitter ()](#apidoc.element.noflo.Port.EventEmitter)
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

#### <a name="apidoc.element.noflo.Port.init"></a>[function <span class="apidocSignatureSpan">noflo.Port.</span>init ()](#apidoc.element.noflo.Port.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Port.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.Port.</span>listenerCount (emitter, type)](#apidoc.element.noflo.Port.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.Port.prototype"></a>[module noflo.Port.prototype](#apidoc.module.noflo.Port.prototype)

#### <a name="apidoc.element.noflo.Port.prototype.attach"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>attach (socket)](#apidoc.element.noflo.Port.prototype.attach)
- description and source-code
```javascript
attach = function (socket) {
  this.sockets.push(socket);
  return this.attachSocket(socket);
}
```
- example usage
```shell
...
  runNetwork = function(network, inputs, options, callback) {
var inPorts, inSockets, outPorts, outSockets, process, received;
process = network.getNode(options.name);
inPorts = Object.keys(network.graph.inports);
inSockets = {};
inPorts.forEach(function(inport) {
  inSockets[inport] = internalSocket.createSocket();
  return process.component.inPorts[inport].attach(inSockets[inport]);
});
received = [];
outPorts = Object.keys(network.graph.outports);
outSockets = {};
outPorts.forEach(function(outport) {
  outSockets[outport] = internalSocket.createSocket();
  process.component.outPorts[outport].attach(outSockets[outport]);
...
```

#### <a name="apidoc.element.noflo.Port.prototype.attachSocket"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>attachSocket (socket, localId)](#apidoc.element.noflo.Port.prototype.attachSocket)
- description and source-code
```javascript
attachSocket = function (socket, localId) {
  if (localId == null) {
    localId = null;
  }
  this.emit("attach", socket, localId);
  this.from = socket.from;
  if (socket.setMaxListeners) {
    socket.setMaxListeners(0);
  }
  socket.on("connect", (function(_this) {
    return function() {
      return _this.emit("connect", socket, localId);
    };
  })(this));
  socket.on("begingroup", (function(_this) {
    return function(group) {
      return _this.emit("begingroup", group, localId);
    };
  })(this));
  socket.on("data", (function(_this) {
    return function(data) {
      return _this.emit("data", data, localId);
    };
  })(this));
  socket.on("endgroup", (function(_this) {
    return function(group) {
      return _this.emit("endgroup", group, localId);
    };
  })(this));
  return socket.on("disconnect", (function(_this) {
    return function() {
      return _this.emit("disconnect", socket, localId);
    };
  })(this));
}
```
- example usage
```shell
...
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
    socketId = this.sockets.length;
  }
  this.sockets[socketId] = socket;
  return this.attachSocket(socket, socketId);
};

ArrayPort.prototype.connect = function(socketId) {
  if (socketId == null) {
    socketId = null;
  }
  if (socketId === null) {
...
```

#### <a name="apidoc.element.noflo.Port.prototype.beginGroup"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>beginGroup (group)](#apidoc.element.noflo.Port.prototype.beginGroup)
- description and source-code
```javascript
beginGroup = function (group) {
  if (this.sockets.length === 0) {
    throw new Error((this.getId()) + ": No connections available");
  }
  return this.sockets.forEach(function(socket) {
    if (socket.isConnected()) {
      return socket.beginGroup(group);
    }
    socket.once('connect', function() {
      return socket.beginGroup(group);
    });
    return socket.connect();
  });
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.beginGroup(group, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.Port.prototype.canAttach"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>canAttach ()](#apidoc.element.noflo.Port.prototype.canAttach)
- description and source-code
```javascript
canAttach = function () {
  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Port.prototype.clear"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>clear ()](#apidoc.element.noflo.Port.prototype.clear)
- description and source-code
```javascript
clear = function () {}
```
- example usage
```shell
...
var inPort, inPorts, portName;
inPorts = _this.inPorts.ports || _this.inPorts;
for (portName in inPorts) {
  inPort = inPorts[portName];
  if (typeof inPort.clear !== 'function') {
    continue;
  }
  inPort.clear();
}
_this.bracketContext = {
  "in": {},
  out: {}
};
if (!_this.isStarted()) {
  return callback();
...
```

#### <a name="apidoc.element.noflo.Port.prototype.connect"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>connect ()](#apidoc.element.noflo.Port.prototype.connect)
- description and source-code
```javascript
connect = function () {
  var i, len, ref, results, socket;
  if (this.sockets.length === 0) {
    throw new Error((this.getId()) + ": No connections available");
  }
  ref = this.sockets;
  results = [];
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    results.push(socket.connect());
  }
  return results;
}
```
- example usage
```shell
...
        return function(err, network1) {
_this.network = network1;
if (err) {
  return callback(err);
}
_this.emit('network', _this.network);
_this.subscribeNetwork(_this.network);
return _this.network.connect(function(err) {
  var name, node, ref;
  if (err) {
    return callback(err);
  }
  ref = _this.network.processes;
  for (name in ref) {
    node = ref[name];
...
```

#### <a name="apidoc.element.noflo.Port.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>constructor (type)](#apidoc.element.noflo.Port.prototype.constructor)
- description and source-code
```javascript
function Port(type) {
  this.type = type;
  platform.deprecated('noflo.Port is deprecated. Please port to noflo.InPort/noflo.OutPort');
  if (!this.type) {
    this.type = 'all';
  }
  if (this.type === 'integer') {
    this.type = 'int';
  }
  this.sockets = [];
  this.from = null;
  this.node = null;
  this.name = null;
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.Port.prototype.detach"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>detach (socket)](#apidoc.element.noflo.Port.prototype.detach)
- description and source-code
```javascript
detach = function (socket) {
  var index;
  if (this.sockets.length === 0) {
    return;
  }
  if (!socket) {
    socket = this.sockets[0];
  }
  index = this.sockets.indexOf(socket);
  if (index === -1) {
    return;
  }
  if (this.isAddressable()) {
    this.sockets[index] = void 0;
    this.emit('detach', socket, index);
    return;
  }
  this.sockets.splice(index, 1);
  return this.emit("detach", socket);
}
```
- example usage
```shell
...
    return received.push(res);
  });
});
network.once('end', function() {
  var port, socket;
  for (port in outSockets) {
    socket = outSockets[port];
    process.component.outPorts[port].detach(socket);
  }
  outSockets = {};
  inSockets = {};
  return callback(null, received);
});
return network.start(function(err) {
  var i, inputMap, len, port, results, value;
...
```

#### <a name="apidoc.element.noflo.Port.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>disconnect ()](#apidoc.element.noflo.Port.prototype.disconnect)
- description and source-code
```javascript
disconnect = function () {
  var i, len, ref, results, socket;
  if (this.sockets.length === 0) {
    throw new Error((this.getId()) + ": No connections available");
  }
  ref = this.sockets;
  results = [];
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    results.push(socket.disconnect());
  }
  return results;
}
```
- example usage
```shell
...
  }
  ref = this.sockets;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    if (!socket) {
      return;
    }
    socket.disconnect();
  }
  return;
}
if (!this.sockets[socketId]) {
  return;
}
return this.sockets[socketId].disconnect();
...
```

#### <a name="apidoc.element.noflo.Port.prototype.endGroup"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>endGroup ()](#apidoc.element.noflo.Port.prototype.endGroup)
- description and source-code
```javascript
endGroup = function () {
  var i, len, ref, results, socket;
  if (this.sockets.length === 0) {
    throw new Error((this.getId()) + ": No connections available");
  }
  ref = this.sockets;
  results = [];
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    results.push(socket.endGroup());
  }
  return results;
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.endGroup(index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.Port.prototype.getDataType"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>getDataType ()](#apidoc.element.noflo.Port.prototype.getDataType)
- description and source-code
```javascript
getDataType = function () {
  return this.type;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Port.prototype.getDescription"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>getDescription ()](#apidoc.element.noflo.Port.prototype.getDescription)
- description and source-code
```javascript
getDescription = function () {
  return this.description;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Port.prototype.getId"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>getId ()](#apidoc.element.noflo.Port.prototype.getId)
- description and source-code
```javascript
getId = function () {
  if (!(this.node && this.name)) {
    return 'Port';
  }
  return this.node + " " + (this.name.toUpperCase());
}
```
- example usage
```shell
...

    ArrayPort.prototype.connect = function(socketId) {
if (socketId == null) {
  socketId = null;
}
if (socketId === null) {
  if (!this.sockets.length) {
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach(function(socket) {
    if (!socket) {
      return;
    }
    return socket.connect();
  });
...
```

#### <a name="apidoc.element.noflo.Port.prototype.isAddressable"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isAddressable ()](#apidoc.element.noflo.Port.prototype.isAddressable)
- description and source-code
```javascript
isAddressable = function () {
  return false;
}
```
- example usage
```shell
...
  return this.options.description;
};

BasePort.prototype.attach = function(socket, index) {
  if (index == null) {
    index = null;
  }
  if (!this.isAddressable() || index === null) {
    index = this.sockets.length;
  }
  this.sockets[index] = socket;
  this.attachSocket(socket, index);
  if (this.isAddressable()) {
    this.emit('attach', socket, index);
    return;
...
```

#### <a name="apidoc.element.noflo.Port.prototype.isAttached"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isAttached ()](#apidoc.element.noflo.Port.prototype.isAttached)
- description and source-code
```javascript
isAttached = function () {
  if (this.sockets.length > 0) {
    return true;
  }
  return false;
}
```
- example usage
```shell
...
    if (_this.load > 0) {
      return _this.q.push({
        name: "disconnect"
      });
    }
    _this.outPorts[_this.outPortName].disconnect();
    _this.errorGroups = [];
    if (_this.outPorts.load.isAttached()) {
      return _this.outPorts.load.disconnect();
    }
  };
})(this));
this.inPorts[this.inPortName].on("data", (function(_this) {
  return function(data) {
    if (_this.q.length > 0) {
...
```

#### <a name="apidoc.element.noflo.Port.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isConnected ()](#apidoc.element.noflo.Port.prototype.isConnected)
- description and source-code
```javascript
isConnected = function () {
  var connected;
  connected = false;
  this.sockets.forEach(function(socket) {
    if (socket.isConnected()) {
      return connected = true;
    }
  });
  return connected;
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
if (this.isConnected(socketId)) {
  return this.sockets[socketId].beginGroup(group);
}
this.sockets[socketId].once("connect", (function(_this) {
  return function() {
    return _this.sockets[socketId].beginGroup(group);
  };
})(this));
...
```

#### <a name="apidoc.element.noflo.Port.prototype.isRequired"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>isRequired ()](#apidoc.element.noflo.Port.prototype.isRequired)
- description and source-code
```javascript
isRequired = function () {
  return this.required;
}
```
- example usage
```shell
...
var group, i, j, len, len1;
if (groups == null) {
  groups = [];
}
if (errorPort == null) {
  errorPort = 'error';
}
if (this.outPorts[errorPort] && (this.outPorts[errorPort].isAttached() || !this.outPorts[errorPort].isRequired())) {
  for (i = 0, len = groups.length; i < len; i++) {
    group = groups[i];
    this.outPorts[errorPort].beginGroup(group);
  }
  this.outPorts[errorPort].send(e);
  for (j = 0, len1 = groups.length; j < len1; j++) {
    group = groups[j];
...
```

#### <a name="apidoc.element.noflo.Port.prototype.listAttached"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>listAttached ()](#apidoc.element.noflo.Port.prototype.listAttached)
- description and source-code
```javascript
listAttached = function () {
  var attached, i, idx, len, ref, socket;
  attached = [];
  ref = this.sockets;
  for (idx = i = 0, len = ref.length; i < len; idx = ++i) {
    socket = ref[idx];
    if (!socket) {
      continue;
    }
    attached.push(idx);
  }
  return attached;
}
```
- example usage
```shell
...
  args = 1 <= arguments.length ? slice.call(arguments, 0) : [];
  if (!args.length) {
    args = ['in'];
  }
  res = [];
  for (i = 0, len1 = args.length; i < len1; i++) {
    port = args[i];
    res.push(this.ports[port].listAttached());
  }
  if (args.length === 1) {
    return res.pop();
  }
  return res;
};
...
```

#### <a name="apidoc.element.noflo.Port.prototype.send"></a>[function <span class="apidocSignatureSpan">noflo.Port.prototype.</span>send (data)](#apidoc.element.noflo.Port.prototype.send)
- description and source-code
```javascript
send = function (data) {
  if (this.sockets.length === 0) {
    throw new Error((this.getId()) + ": No connections available");
  }
  return this.sockets.forEach(function(socket) {
    if (socket.isConnected()) {
      return socket.send(data);
    }
    socket.once('connect', function() {
      return socket.send(data);
    });
    return socket.connect();
  });
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.send(data, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```



# <a name="apidoc.module.noflo.Ports"></a>[module noflo.Ports](#apidoc.module.noflo.Ports)

#### <a name="apidoc.element.noflo.Ports.InPorts"></a>[function <span class="apidocSignatureSpan">noflo.Ports.</span>InPorts ()](#apidoc.element.noflo.Ports.InPorts)
- description and source-code
```javascript
function InPorts() {
  return InPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
this.network = null;
this.ready = true;
this.started = false;
this.starting = false;
this.baseDir = null;
this.loader = null;
this.load = 0;
this.inPorts = new noflo.InPorts({
  graph: {
    datatype: 'all',
    description: 'NoFlo graph definition to be used with the subgraph component',
    required: true
  }
});
this.outPorts = new noflo.OutPorts;
...
```

#### <a name="apidoc.element.noflo.Ports.OutPorts"></a>[function <span class="apidocSignatureSpan">noflo.Ports.</span>OutPorts ()](#apidoc.element.noflo.Ports.OutPorts)
- description and source-code
```javascript
function OutPorts() {
  return OutPorts.__super__.constructor.apply(this, arguments);
}
```
- example usage
```shell
...
}
if (!options.outPorts) {
  options.outPorts = {};
}
if (options.outPorts instanceof ports.OutPorts) {
  this.outPorts = options.outPorts;
} else {
  this.outPorts = new ports.OutPorts(options.outPorts);
}
if (options.icon) {
  this.icon = options.icon;
}
if (options.description) {
  this.description = options.description;
}
...
```

#### <a name="apidoc.element.noflo.Ports.normalizePortName"></a>[function <span class="apidocSignatureSpan">noflo.Ports.</span>normalizePortName (name)](#apidoc.element.noflo.Ports.normalizePortName)
- description and source-code
```javascript
normalizePortName = function (name) {
  var matched, port;
  port = {
    name: name
  };
  if (name.indexOf('[') === -1) {
    return port;
  }
  matched = name.match(/(.*)\[([0-9]+)\]/);
  if (!(matched != null ? matched.length : void 0)) {
    return name;
  }
  port.name = matched[1];
  port.index = matched[2];
  return port;
}
```
- example usage
```shell
...
    return;
  }
  debug(this.nodeId + " packet on '" + port.name + "' didn't match preconditions: " + ip.type);
};

Component.prototype.getBracketContext = function(type, port, scope, idx) {
  var index, name, portsList, ref;
  ref = ports.normalizePortName(port), name = ref.name, index = ref.index;
  if (idx != null) {
    index = idx;
  }
  portsList = type === 'in' ? this.inPorts : this.outPorts;
  if (portsList[name].isAddressable()) {
    port = name + "[" + index + "]";
  }
...
```



# <a name="apidoc.module.noflo.Utils"></a>[module noflo.Utils](#apidoc.module.noflo.Utils)

#### <a name="apidoc.element.noflo.Utils.clone"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>clone (obj)](#apidoc.element.noflo.Utils.clone)
- description and source-code
```javascript
clone = function (obj) {
  var flags, key, newInstance;
  if ((obj == null) || typeof obj !== 'object') {
    return obj;
  }
  if (obj instanceof Date) {
    return new Date(obj.getTime());
  }
  if (obj instanceof RegExp) {
    flags = '';
    if (obj.global != null) {
      flags += 'g';
    }
    if (obj.ignoreCase != null) {
      flags += 'i';
    }
    if (obj.multiline != null) {
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
}
```
- example usage
```shell
...
    debugBrackets(this.nodeId + " closeBracket-A from '" + context.source + "' to " + context.ports + ": '" + context.closeIp.data
 + "'");
    if (!context.ports.length) {
      continue;
    }
    ref2 = context.ports;
    for (j = 0, len2 = ref2.length; j < len2; j++) {
      port = ref2[j];
      ipClone = context.closeIp.clone();
      this.addToResult(result, port, ipClone, true);
      this.getBracketContext('out', port, ipClone.scope).pop();
    }
  }
}
if (result.__bracketContext) {
  Object.keys(result.__bracketContext).reverse().forEach((function(_this) {
...
```

#### <a name="apidoc.element.noflo.Utils.debounce"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>debounce (func, wait, immediate)](#apidoc.element.noflo.Utils.debounce)
- description and source-code
```javascript
debounce = function (func, wait, immediate) {
  var args, context, later, result, timeout, timestamp;
  timeout = void 0;
  args = void 0;
  context = void 0;
  timestamp = void 0;
  result = void 0;
  later = function() {
    var last;
    last = Date.now - timestamp;
    if (last < wait && last >= 0) {
      timeout = setTimeout(later, wait - last);
    } else {
      timeout = null;
      if (!immediate) {
        result = func.apply(context, args);
        if (!timeout) {
          context = args = null;
        }
      }
    }
  };
  return function() {
    var callNow;
    context = this;
    args = arguments;
    timestamp = Date.now;
    callNow = immediate && !timeout;
    if (!timeout) {
      timeout = setTimeout(later, wait);
    }
    if (callNow) {
      result = func.apply(context, args);
      context = args = null;
    }
    return result;
  };
}
```
- example usage
```shell
...

    Network.prototype.checkIfFinished = function() {
if (this.isRunning()) {
  return;
}
delete this.abortDebounce;
if (!this.debouncedEnd) {
  this.debouncedEnd = utils.debounce((function(_this) {
    return function() {
      if (_this.abortDebounce) {
        return;
      }
      if (_this.isRunning()) {
        return;
      }
...
```

#### <a name="apidoc.element.noflo.Utils.getValues"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>getValues (obj)](#apidoc.element.noflo.Utils.getValues)
- description and source-code
```javascript
getValues = function (obj) {
  var i, keys, length, values;
  keys = getKeys(obj);
  length = keys.length;
  values = Array(length);
  i = 0;
  while (i < length) {
    values[i] = obj[keys[i]];
    i++;
  }
  return values;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Utils.guessLanguageFromFilename"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>guessLanguageFromFilename (filename)](#apidoc.element.noflo.Utils.guessLanguageFromFilename)
- description and source-code
```javascript
guessLanguageFromFilename = function (filename) {
  if (/.*\.coffee$/.test(filename)) {
    return 'coffeescript';
  }
  return 'javascript';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Utils.intersection"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>intersection (array)](#apidoc.element.noflo.Utils.intersection)
- description and source-code
```javascript
intersection = function (array) {
  var argsLength, i, item, j, k, l, ref, ref1, result;
  result = [];
  argsLength = arguments.length;
  for (i = k = 0, ref = array.length; 0 <= ref ? k <= ref : k >= ref; i = 0 <= ref ? ++k : --k) {
    item = array[i];
    if (contains(result, item)) {
      continue;
    }
    for (j = l = 1, ref1 = argsLength; 1 <= ref1 ? l <= ref1 : l >= ref1; j = 1 <= ref1 ? ++l : --l) {
      if (!contains(arguments[j], item)) {
        break;
      }
    }
    if (j === argsLength) {
      result.push(item);
    }
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Utils.optimizeCb"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>optimizeCb (func, context, argCount)](#apidoc.element.noflo.Utils.optimizeCb)
- description and source-code
```javascript
optimizeCb = function (func, context, argCount) {
  if (context === void 0) {
    return func;
  }
  switch ((argCount === null ? 3 : argCount)) {
    case 1:
      return function(value) {
        return func.call(context, value);
      };
    case 2:
      return function(value, other) {
        return func.call(context, value, other);
      };
    case 3:
      return function(value, index, collection) {
        return func.call(context, value, index, collection);
      };
    case 4:
      return function(accumulator, value, index, collection) {
        return func.call(context, accumulator, value, index, collection);
      };
  }
  return function() {
    return func.apply(context, arguments);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.Utils.reduceRight"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>reduceRight (obj, iteratee, memo, context)](#apidoc.element.noflo.Utils.reduceRight)
- description and source-code
```javascript
reduceRight = function (obj, iteratee, memo, context) {
  var index, keys, length;
  iteratee = optimizeCb(iteratee, context, 4);
  keys = Object.keys(obj);
  length = (keys || obj).length;
  index = dir > 0 ? 0 : length - 1;
  if (arguments.length < 3) {
    memo = obj[keys ? keys[index] : index];
    index += dir;
  }
  return iterator(obj, iteratee, memo, keys, index, length);
}
```
- example usage
```shell
...
})(this);
subscribeGraph = (function(_this) {
  return function() {
    _this.subscribeGraph();
    return done();
  };
})(this);
setDefaults = utils.reduceRight(this.graph.nodes, serialize, subscribeGraph);
initializers = utils.reduceRight(this.graph.initializers, serialize, function() {
  return setDefaults("Defaults");
});
edges = utils.reduceRight(this.graph.edges, serialize, function() {
  return initializers("Initial");
});
nodes = utils.reduceRight(this.graph.nodes, serialize, function() {
...
```

#### <a name="apidoc.element.noflo.Utils.unique"></a>[function <span class="apidocSignatureSpan">noflo.Utils.</span>unique (array)](#apidoc.element.noflo.Utils.unique)
- description and source-code
```javascript
unique = function (array) {
  var k, key, output, ref, results, value;
  output = {};
  for (key = k = 0, ref = array.length; 0 <= ref ? k < ref : k > ref; key = 0 <= ref ? ++k : --k) {
    output[array[key]] = array[key];
  }
  results = [];
  for (key in output) {
    value = output[key];
    results.push(value);
  }
  return results;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.graph"></a>[module noflo.graph](#apidoc.module.noflo.graph)

#### <a name="apidoc.element.noflo.graph.Graph"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>Graph (name1, options)](#apidoc.element.noflo.graph.Graph)
- description and source-code
```javascript
function Graph(name1, options) {
  this.name = name1 != null ? name1 : '';
  if (options == null) {
    options = {};
  }
  this.properties = {};
  this.nodes = [];
  this.edges = [];
  this.initializers = [];
  this.exports = [];
  this.inports = {};
  this.outports = {};
  this.groups = [];
  this.transaction = {
    id: null,
    depth: 0
  };
  this.caseSensitive = options.caseSensitive || false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.graph.createGraph"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>createGraph (name, options)](#apidoc.element.noflo.graph.createGraph)
- description and source-code
```javascript
createGraph = function (name, options) {
  return new Graph(name, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.graph.equivalent"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>equivalent (a, b, options)](#apidoc.element.noflo.graph.equivalent)
- description and source-code
```javascript
equivalent = function (a, b, options) {
  var A, B;
  if (options == null) {
    options = {};
  }
  A = JSON.stringify(a);
  B = JSON.stringify(b);
  return A === B;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.graph.loadFBP"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>loadFBP (fbpData, callback, metadata, caseSensitive)](#apidoc.element.noflo.graph.loadFBP)
- description and source-code
```javascript
loadFBP = function (fbpData, callback, metadata, caseSensitive) {
  var definition, e, error;
  if (metadata == null) {
    metadata = {};
  }
  if (caseSensitive == null) {
    caseSensitive = false;
  }
  try {
    definition = require('fbp').parse(fbpData, {
      caseSensitive: caseSensitive
    });
  } catch (error) {
    e = error;
    return callback(e);
  }
  return exports.loadJSON(definition, callback, metadata);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.graph.loadFile"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>loadFile (file, callback, metadata, caseSensitive)](#apidoc.element.noflo.graph.loadFile)
- description and source-code
```javascript
loadFile = function (file, callback, metadata, caseSensitive) {
  if (metadata == null) {
    metadata = {};
  }
  if (caseSensitive == null) {
    caseSensitive = false;
  }
  if (platform.isBrowser()) {
    exports.loadHTTP(file, function(err, data) {
      var definition;
      if (err) {
        return callback(err);
      }
      if (file.split('.').pop() === 'fbp') {
        return exports.loadFBP(data, callback, metadata);
      }
      definition = JSON.parse(data);
      return exports.loadJSON(definition, callback, metadata);
    });
    return;
  }
  return require('fs').readFile(file, "utf-8", function(err, data) {
    var definition;
    if (err) {
      return callback(err);
    }
    if (file.split('.').pop() === 'fbp') {
      return exports.loadFBP(data, callback, {}, caseSensitive);
    }
    definition = JSON.parse(data);
    return exports.loadJSON(definition, callback, {});
  });
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (graph.substr(0, 1) !== "/" && graph.substr(1, 1) !== ":" && process && process.cwd) {
  graph = (process.cwd()) + "/" + graph;
}
return noflo.graph.loadFile(graph, (function(_this) {
  return function(err, instance) {
    if (err) {
      return callback(err);
    }
    instance.baseDir = _this.baseDir;
    return _this.createNetwork(instance, callback);
  };
...
```

#### <a name="apidoc.element.noflo.graph.loadHTTP"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>loadHTTP (url, callback)](#apidoc.element.noflo.graph.loadHTTP)
- description and source-code
```javascript
loadHTTP = function (url, callback) {
  var req;
  req = new XMLHttpRequest;
  req.onreadystatechange = function() {
    if (req.readyState !== 4) {
      return;
    }
    if (req.status !== 200) {
      return callback(new Error("Failed to load " + url + ": HTTP " + req.status));
    }
    return callback(null, req.responseText);
  };
  req.open('GET', url, true);
  return req.send();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.graph.loadJSON"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>loadJSON (definition, callback, metadata)](#apidoc.element.noflo.graph.loadJSON)
- description and source-code
```javascript
loadJSON = function (definition, callback, metadata) {
  var caseSensitive, conn, def, exported, graph, group, i, id, j, k, len, len1, len2, portId, priv, processId, properties, property
, pub, ref, ref1, ref2, ref3, ref4, ref5, ref6, split, value;
  if (metadata == null) {
    metadata = {};
  }
  if (typeof definition === 'string') {
    definition = JSON.parse(definition);
  }
  if (!definition.properties) {
    definition.properties = {};
  }
  if (!definition.processes) {
    definition.processes = {};
  }
  if (!definition.connections) {
    definition.connections = [];
  }
  caseSensitive = definition.caseSensitive || false;
  graph = new Graph(definition.properties.name, {
    caseSensitive: caseSensitive
  });
  graph.startTransaction('loadJSON', metadata);
  properties = {};
  ref = definition.properties;
  for (property in ref) {
    value = ref[property];
    if (property === 'name') {
      continue;
    }
    properties[property] = value;
  }
  graph.setProperties(properties);
  ref1 = definition.processes;
  for (id in ref1) {
    def = ref1[id];
    if (!def.metadata) {
      def.metadata = {};
    }
    graph.addNode(id, def.component, def.metadata);
  }
  ref2 = definition.connections;
  for (i = 0, len = ref2.length; i < len; i++) {
    conn = ref2[i];
    metadata = conn.metadata ? conn.metadata : {};
    if (conn.data !== void 0) {
      if (typeof conn.tgt.index === 'number') {
        graph.addInitialIndex(conn.data, conn.tgt.process, graph.getPortName(conn.tgt.port), conn.tgt.index, metadata);
      } else {
        graph.addInitial(conn.data, conn.tgt.process, graph.getPortName(conn.tgt.port), metadata);
      }
      continue;
    }
    if (typeof conn.src.index === 'number' || typeof conn.tgt.index === 'number') {
      graph.addEdgeIndex(conn.src.process, graph.getPortName(conn.src.port), conn.src.index, conn.tgt.process, graph.getPortName
(conn.tgt.port), conn.tgt.index, metadata);
      continue;
    }
    graph.addEdge(conn.src.process, graph.getPortName(conn.src.port), conn.tgt.process, graph.getPortName(conn.tgt.port), metadata
);
  }
  if (definition.exports && definition.exports.length) {
    ref3 = definition.exports;
    for (j = 0, len1 = ref3.length; j < len1; j++) {
      exported = ref3[j];
      if (exported["private"]) {
        split = exported["private"].split('.');
        if (split.length !== 2) {
          continue;
        }
        processId = split[0];
        portId = split[1];
        for (id in definition.processes) {
          if (graph.getPortName(id) === graph.getPortName(processId)) {
            processId = id;
          }
        }
      } else {
        processId = exported.process;
        portId = graph.getPortName(exported.port);
      }
      graph.addExport(exported["public"], processId, portId, exported.metadata);
    }
  }
  if (definition.inports) {
    ref4 = definition.inports;
    for (pub in ref4) {
      priv = ref4[pub];
      graph.addInport(pub, priv.process, graph.getPortName(priv.port), priv.metadata);
    }
  }
  if (definition.outports) {
    ref5 = definition.outports;
    for (pub in ref5) {
      priv = ref5[pub];
      graph.addOutport(pub, priv.process, graph.getPortName(priv.port), priv.metadata);
    }
  }
  if (definition.groups) {
    ref6 = definition.groups;
    for (k = 0, len2 = ref6.length; k < len2; k++) {
      group = ref6[k];
      graph.addGroup(group.name, group.nodes, group.metadata || {});
    }
  }
  graph.endTransaction('loadJSON');
  return callback(null, graph);
}
```
- example usage
```shell
...
    Graph.prototype.setGraph = function(graph, callback) {
this.ready = false;
if (typeof graph === 'object') {
  if (typeof graph.addNode === 'function') {
    this.createNetwork(graph, callback);
    return;
  }
  noflo.graph.loadJSON(graph, (function(_this) {
    return function(err, instance) {
      if (err) {
        return callback(err);
      }
      instance.baseDir = _this.baseDir;
      return _this.createNetwork(instance, callback);
    };
...
```

#### <a name="apidoc.element.noflo.graph.mergeResolveTheirs"></a>[function <span class="apidocSignatureSpan">noflo.graph.</span>mergeResolveTheirs (base, to)](#apidoc.element.noflo.graph.mergeResolveTheirs)
- description and source-code
```javascript
mergeResolveTheirs = function (base, to) {
  var edge, exp, group, i, iip, j, k, l, len, len1, len2, len3, len4, m, node, priv, pub, ref, ref1, ref2, ref3, ref4, ref5, ref6
, results;
  resetGraph(base);
  ref = to.nodes;
  for (i = 0, len = ref.length; i < len; i++) {
    node = ref[i];
    base.addNode(node.id, node.component, node.metadata);
  }
  ref1 = to.edges;
  for (j = 0, len1 = ref1.length; j < len1; j++) {
    edge = ref1[j];
    base.addEdge(edge.from.node, edge.from.port, edge.to.node, edge.to.port, edge.metadata);
  }
  ref2 = to.initializers;
  for (k = 0, len2 = ref2.length; k < len2; k++) {
    iip = ref2[k];
    base.addInitial(iip.from.data, iip.to.node, iip.to.port, iip.metadata);
  }
  ref3 = to.exports;
  for (l = 0, len3 = ref3.length; l < len3; l++) {
    exp = ref3[l];
    base.addExport(exp["public"], exp.node, exp.port, exp.metadata);
  }
  base.setProperties(to.properties);
  ref4 = to.inports;
  for (pub in ref4) {
    priv = ref4[pub];
    base.addInport(pub, priv.process, priv.port, priv.metadata);
  }
  ref5 = to.outports;
  for (pub in ref5) {
    priv = ref5[pub];
    base.addOutport(pub, priv.process, priv.port, priv.metadata);
  }
  ref6 = to.groups;
  results = [];
  for (m = 0, len4 = ref6.length; m < len4; m++) {
    group = ref6[m];
    results.push(base.addGroup(group.name, group.nodes, group.metadata));
  }
  return results;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.helpers"></a>[module noflo.helpers](#apidoc.module.noflo.helpers)

#### <a name="apidoc.element.noflo.helpers.CustomError"></a>[function <span class="apidocSignatureSpan">noflo.helpers.</span>CustomError (message, options)](#apidoc.element.noflo.helpers.CustomError)
- description and source-code
```javascript
CustomError = function (message, options) {
  var err;
  err = new Error(message);
  return exports.CustomizeError(err, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.helpers.CustomizeError"></a>[function <span class="apidocSignatureSpan">noflo.helpers.</span>CustomizeError (err, options)](#apidoc.element.noflo.helpers.CustomizeError)
- description and source-code
```javascript
CustomizeError = function (err, options) {
  var key, val;
  for (key in options) {
    if (!hasProp.call(options, key)) continue;
    val = options[key];
    err[key] = val;
  }
  return err;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.helpers.GroupedInput"></a>[function <span class="apidocSignatureSpan">noflo.helpers.</span>GroupedInput (component, config, proc)](#apidoc.element.noflo.helpers.GroupedInput)
- description and source-code
```javascript
GroupedInput = function (component, config, proc) {
  var inPorts, outPorts, ref, setup;
  inPorts = 'in' in config ? config["in"] : 'in';
  if (!isArray(inPorts)) {
    inPorts = [inPorts];
  }
  outPorts = 'out' in config ? config.out : 'out';
  if (!isArray(outPorts)) {
    outPorts = [outPorts];
  }
  if (!('error' in config)) {
    config.error = 'error';
  }
  if (!('async' in config)) {
    config.async = false;
  }
  if (!('ordered' in config)) {
    config.ordered = true;
  }
  if (!('group' in config)) {
    config.group = false;
  }
  if (!('field' in config)) {
    config.field = null;
  }
  if (!('forwardGroups' in config)) {
    config.forwardGroups = false;
  }
  if (config.forwardGroups) {
    if (typeof config.forwardGroups === 'string') {
      config.forwardGroups = [config.forwardGroups];
    }
    if (typeof config.forwardGroups === 'boolean') {
      config.forwardGroups = inPorts;
    }
  }
  if (!('receiveStreams' in config)) {
    config.receiveStreams = false;
  }
  if (config.receiveStreams) {
    throw new Error('WirePattern receiveStreams is deprecated');
  }
  if (!('sendStreams' in config)) {
    config.sendStreams = false;
  }
  if (config.sendStreams) {
    throw new Error('WirePattern sendStreams is deprecated');
  }
  if (config.async) {
    config.sendStreams = outPorts;
  }
  if (!('params' in config)) {
    config.params = [];
  }
  if (typeof config.params === 'string') {
    config.params = [config.params];
  }
  if (!('name' in config)) {
    config.name = '';
  }
  if (!('dropInput' in config)) {
    config.dropInput = false;
  }
  if (!('arrayPolicy' in config)) {
    config.arrayPolicy = {
      "in": 'any',
      params: 'all'
    };
  }
  config.inPorts = inPorts;
  config.outPorts = outPorts;
  checkDeprecation(config, proc);
  if (config.legacy || (typeof process !== "undefined" && process !== null ? (ref = process.env) != null ? ref.NOFLO_WIREPATTERN_LEGACY
 : void 0 : void 0)) {
    platform.deprecated('noflo.helpers.WirePattern legacy mode is deprecated');
    setup = legacyWirePattern;
  } else {
    setup = processApiWirePattern;
  }
  return setup(component, config, proc);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.helpers.MapComponent"></a>[function <span class="apidocSignatureSpan">noflo.helpers.</span>MapComponent (component, func, config)](#apidoc.element.noflo.helpers.MapComponent)
- description and source-code
```javascript
MapComponent = function (component, func, config) {
  platform.deprecated('noflo.helpers.MapComponent is deprecated. Please port to Process API');
  if (!config) {
    config = {};
  }
  if (!config.inPort) {
    config.inPort = 'in';
  }
  if (!config.outPort) {
    config.outPort = 'out';
  }
  if (!component.forwardBrackets) {
    component.forwardBrackets = {};
  }
  component.forwardBrackets[config.inPort] = [config.outPort];
  return component.process(function(input, output) {
    var data, groups, outProxy;
    if (!input.hasData(config.inPort)) {
      return;
    }
    data = input.getData(config.inPort);
    groups = getGroupContext(component, config.inPort, input);
    outProxy = getOutputProxy([config.outPort], output);
    func(data, groups, outProxy);
    return output.done();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.helpers.MultiError"></a>[function <span class="apidocSignatureSpan">noflo.helpers.</span>MultiError (component, group, errorPort, forwardedGroups, scope)](#apidoc.element.noflo.helpers.MultiError)
- description and source-code
```javascript
MultiError = function (component, group, errorPort, forwardedGroups, scope) {
  var baseTearDown;
  if (group == null) {
    group = '';
  }
  if (errorPort == null) {
    errorPort = 'error';
  }
  if (forwardedGroups == null) {
    forwardedGroups = [];
  }
  if (scope == null) {
    scope = null;
  }
  platform.deprecated('noflo.helpers.MultiError is deprecated. Send errors to error port instead');
  component.hasErrors = false;
  component.errors = [];
  if (component.name && !group) {
    group = component.name;
  }
  if (!group) {
    group = 'Component';
  }
  component.error = function(e, groups) {
    if (groups == null) {
      groups = [];
    }
    component.errors.push({
      err: e,
      groups: forwardedGroups.concat(groups)
    });
    return component.hasErrors = true;
  };
  component.fail = function(e, groups) {
    var error, grp, j, k, l, len, len1, len2, ref, ref1, ref2;
    if (e == null) {
      e = null;
    }
    if (groups == null) {
      groups = [];
    }
    if (e) {
      component.error(e, groups);
    }
    if (!component.hasErrors) {
      return;
    }
    if (!(errorPort in component.outPorts)) {
      return;
    }
    if (!component.outPorts[errorPort].isAttached()) {
      return;
    }
    if (group) {
      component.outPorts[errorPort].openBracket(group, {
        scope: scope
      });
    }
    ref = component.errors;
    for (j = 0, len = ref.length; j < len; j++) {
      error = ref[j];
      ref1 = error.groups;
      for (k = 0, len1 = ref1.length; k < len1; k++) {
        grp = ref1[k];
        component.outPorts[errorPort].openBracket(grp, {
          scope: scope
        });
      }
      component.outPorts[errorPort].data(error.err, {
        scope: scope
      });
      ref2 = error.groups;
      for (l = 0, len2 = ref2.length; l < len2; l++) {
        grp = ref2[l];
        component.outPorts[errorPort].closeBracket(grp, {
          scope: scope
        });
      }
    }
    if (group) {
      component.outPorts[errorPort].closeBracket(group, {
        scope: scope
      });
    }
    component.hasErrors = false;
    return component.errors = [];
  };
  baseTearDown = component.tearDown;
  component.tearDown = function(callback) {
    component.hasErrors = false;
    component.errors = [];
    return baseTearDown.call(component, callback);
  };
  return component;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.helpers.WirePattern"></a>[function <span class="apidocSignatureSpan">noflo.helpers.</span>WirePattern (component, config, proc)](#apidoc.element.noflo.helpers.WirePattern)
- description and source-code
```javascript
WirePattern = function (component, config, proc) {
  var inPorts, outPorts, ref, setup;
  inPorts = 'in' in config ? config["in"] : 'in';
  if (!isArray(inPorts)) {
    inPorts = [inPorts];
  }
  outPorts = 'out' in config ? config.out : 'out';
  if (!isArray(outPorts)) {
    outPorts = [outPorts];
  }
  if (!('error' in config)) {
    config.error = 'error';
  }
  if (!('async' in config)) {
    config.async = false;
  }
  if (!('ordered' in config)) {
    config.ordered = true;
  }
  if (!('group' in config)) {
    config.group = false;
  }
  if (!('field' in config)) {
    config.field = null;
  }
  if (!('forwardGroups' in config)) {
    config.forwardGroups = false;
  }
  if (config.forwardGroups) {
    if (typeof config.forwardGroups === 'string') {
      config.forwardGroups = [config.forwardGroups];
    }
    if (typeof config.forwardGroups === 'boolean') {
      config.forwardGroups = inPorts;
    }
  }
  if (!('receiveStreams' in config)) {
    config.receiveStreams = false;
  }
  if (config.receiveStreams) {
    throw new Error('WirePattern receiveStreams is deprecated');
  }
  if (!('sendStreams' in config)) {
    config.sendStreams = false;
  }
  if (config.sendStreams) {
    throw new Error('WirePattern sendStreams is deprecated');
  }
  if (config.async) {
    config.sendStreams = outPorts;
  }
  if (!('params' in config)) {
    config.params = [];
  }
  if (typeof config.params === 'string') {
    config.params = [config.params];
  }
  if (!('name' in config)) {
    config.name = '';
  }
  if (!('dropInput' in config)) {
    config.dropInput = false;
  }
  if (!('arrayPolicy' in config)) {
    config.arrayPolicy = {
      "in": 'any',
      params: 'all'
    };
  }
  config.inPorts = inPorts;
  config.outPorts = outPorts;
  checkDeprecation(config, proc);
  if (config.legacy || (typeof process !== "undefined" && process !== null ? (ref = process.env) != null ? ref.NOFLO_WIREPATTERN_LEGACY
 : void 0 : void 0)) {
    platform.deprecated('noflo.helpers.WirePattern legacy mode is deprecated');
    setup = legacyWirePattern;
  } else {
    setup = processApiWirePattern;
  }
  return setup(component, config, proc);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.internalSocket"></a>[module noflo.internalSocket](#apidoc.module.noflo.internalSocket)

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.</span>InternalSocket (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket)
- description and source-code
```javascript
function InternalSocket(metadata) {
  this.metadata = metadata != null ? metadata : {};
  this.brackets = [];
  this.connected = false;
  this.dataDelegate = null;
  this.debug = false;
  this.emitEvent = this.regularEmitEvent;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.createSocket"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.</span>createSocket ()](#apidoc.element.noflo.internalSocket.createSocket)
- description and source-code
```javascript
createSocket = function () {
  return new InternalSocket;
}
```
- example usage
```shell
...

  runNetwork = function(network, inputs, options, callback) {
var inPorts, inSockets, outPorts, outSockets, process, received;
process = network.getNode(options.name);
inPorts = Object.keys(network.graph.inports);
inSockets = {};
inPorts.forEach(function(inport) {
  inSockets[inport] = internalSocket.createSocket();
  return process.component.inPorts[inport].attach(inSockets[inport]);
});
received = [];
outPorts = Object.keys(network.graph.outports);
outSockets = {};
outPorts.forEach(function(outport) {
  outSockets[outport] = internalSocket.createSocket();
...
```



# <a name="apidoc.module.noflo.internalSocket.InternalSocket"></a>[module noflo.internalSocket.InternalSocket](#apidoc.module.noflo.internalSocket.InternalSocket)

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.InternalSocket"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.</span>InternalSocket (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket.InternalSocket)
- description and source-code
```javascript
function InternalSocket(metadata) {
  this.metadata = metadata != null ? metadata : {};
  this.brackets = [];
  this.connected = false;
  this.dataDelegate = null;
  this.debug = false;
  this.emitEvent = this.regularEmitEvent;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>EventEmitter ()](#apidoc.element.noflo.internalSocket.InternalSocket.EventEmitter)
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

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.init"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>init ()](#apidoc.element.noflo.internalSocket.InternalSocket.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.</span>listenerCount (emitter, type)](#apidoc.element.noflo.internalSocket.InternalSocket.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.internalSocket.InternalSocket.prototype"></a>[module noflo.internalSocket.InternalSocket.prototype](#apidoc.module.noflo.internalSocket.InternalSocket.prototype)

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.beginGroup"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>beginGroup (group)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.beginGroup)
- description and source-code
```javascript
beginGroup = function (group) {
  return this.handleSocketEvent('begingroup', group);
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.beginGroup(group, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.connect"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>connect ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.connect)
- description and source-code
```javascript
connect = function () {
  if (this.connected) {
    return;
  }
  this.connected = true;
  return this.emitEvent('connect', null);
}
```
- example usage
```shell
...
        return function(err, network1) {
_this.network = network1;
if (err) {
  return callback(err);
}
_this.emit('network', _this.network);
_this.subscribeNetwork(_this.network);
return _this.network.connect(function(err) {
  var name, node, ref;
  if (err) {
    return callback(err);
  }
  ref = _this.network.processes;
  for (name in ref) {
    node = ref[name];
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>constructor (metadata)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.constructor)
- description and source-code
```javascript
function InternalSocket(metadata) {
  this.metadata = metadata != null ? metadata : {};
  this.brackets = [];
  this.connected = false;
  this.dataDelegate = null;
  this.debug = false;
  this.emitEvent = this.regularEmitEvent;
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.debugEmitEvent"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>debugEmitEvent (event, data)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.debugEmitEvent)
- description and source-code
```javascript
debugEmitEvent = function (event, data) {
  var error, error1;
  try {
    return this.emit(event, data);
  } catch (error1) {
    error = error1;
    if (error.id && error.metadata && error.error) {
      if (this.listeners('error').length === 0) {
        throw error.error;
      }
      this.emit('error', error);
      return;
    }
    if (this.listeners('error').length === 0) {
      throw error;
    }
    return this.emit('error', {
      id: this.to.process.id,
      error: error,
      metadata: this.metadata
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>disconnect ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.disconnect)
- description and source-code
```javascript
disconnect = function () {
  if (!this.connected) {
    return;
  }
  this.connected = false;
  return this.emitEvent('disconnect', null);
}
```
- example usage
```shell
...
  }
  ref = this.sockets;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    if (!socket) {
      return;
    }
    socket.disconnect();
  }
  return;
}
if (!this.sockets[socketId]) {
  return;
}
return this.sockets[socketId].disconnect();
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.endGroup"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>endGroup ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.endGroup)
- description and source-code
```javascript
endGroup = function () {
  return this.handleSocketEvent('endgroup');
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.endGroup(index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.getId"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>getId ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.getId)
- description and source-code
```javascript
getId = function () {
  var fromStr, toStr;
  fromStr = function(from) {
    return from.process.id + "() " + (from.port.toUpperCase());
  };
  toStr = function(to) {
    return (to.port.toUpperCase()) + " " + to.process.id + "()";
  };
  if (!(this.from || this.to)) {
    return "UNDEFINED";
  }
  if (this.from && !this.to) {
    return (fromStr(this.from)) + " -> ANON";
  }
  if (!this.from) {
    return "DATA -> " + (toStr(this.to));
  }
  return (fromStr(this.from)) + " -> " + (toStr(this.to));
}
```
- example usage
```shell
...

    ArrayPort.prototype.connect = function(socketId) {
if (socketId == null) {
  socketId = null;
}
if (socketId === null) {
  if (!this.sockets.length) {
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach(function(socket) {
    if (!socket) {
      return;
    }
    return socket.connect();
  });
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.handleSocketEvent"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>handleSocketEvent (event, payload, autoConnect)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.handleSocketEvent)
- description and source-code
```javascript
handleSocketEvent = function (event, payload, autoConnect) {
  var ip, isIP, legacy;
  if (autoConnect == null) {
    autoConnect = true;
  }
  isIP = event === 'ip' && IP.isIP(payload);
  ip = isIP ? payload : this.legacyToIp(event, payload);
  if (!ip) {
    return;
  }
  if (!this.isConnected() && autoConnect && this.brackets.length === 0) {
    this.connect();
  }
  if (event === 'begingroup') {
    this.brackets.push(payload);
  }
  if (isIP && ip.type === 'openBracket') {
    this.brackets.push(ip.data);
  }
  if (event === 'endgroup') {
    if (this.brackets.length === 0) {
      return;
    }
    ip.data = this.brackets.pop();
    payload = ip.data;
  }
  if (isIP && payload.type === 'closeBracket') {
    if (this.brackets.length === 0) {
      return;
    }
    this.brackets.pop();
  }
  this.emitEvent('ip', ip);
  if (!(ip && ip.type)) {
    return;
  }
  if (isIP) {
    legacy = this.ipToLegacy(ip);
    event = legacy.event;
    payload = legacy.payload;
  }
  if (event === 'connect') {
    this.connected = true;
  }
  if (event === 'disconnect') {
    this.connected = false;
  }
  return this.emitEvent(event, payload);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.ipToLegacy"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>ipToLegacy (ip)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.ipToLegacy)
- description and source-code
```javascript
ipToLegacy = function (ip) {
  var legacy;
  switch (ip.type) {
    case 'openBracket':
      return legacy = {
        event: 'begingroup',
        payload: ip.data
      };
    case 'data':
      return legacy = {
        event: 'data',
        payload: ip.data
      };
    case 'closeBracket':
      return legacy = {
        event: 'endgroup',
        payload: ip.data
      };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.isConnected"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>isConnected ()](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.isConnected)
- description and source-code
```javascript
isConnected = function () {
  return this.connected;
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
if (this.isConnected(socketId)) {
  return this.sockets[socketId].beginGroup(group);
}
this.sockets[socketId].once("connect", (function(_this) {
  return function() {
    return _this.sockets[socketId].beginGroup(group);
  };
})(this));
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.legacyToIp"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>legacyToIp (event, payload)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.legacyToIp)
- description and source-code
```javascript
legacyToIp = function (event, payload) {
  if (IP.isIP(payload)) {
    return payload;
  }
  switch (event) {
    case 'begingroup':
      return new IP('openBracket', payload);
    case 'endgroup':
      return new IP('closeBracket');
    case 'data':
      return new IP('data', payload);
    default:
      return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.post"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>post (ip, autoDisconnect)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.post)
- description and source-code
```javascript
post = function (ip, autoDisconnect) {
  if (autoDisconnect == null) {
    autoDisconnect = true;
  }
  if (ip === void 0 && typeof this.dataDelegate === 'function') {
    ip = this.dataDelegate();
  }
  if (!this.isConnected() && this.brackets.length === 0) {
    this.connect();
  }
  this.handleSocketEvent('ip', ip, false);
  if (autoDisconnect && this.isConnected() && this.brackets.length === 0) {
    return this.disconnect();
  }
}
```
- example usage
```shell
...
  inputMap = inputs[i];
  results.push((function() {
    var results1;
    results1 = [];
    for (port in inputMap) {
      value = inputMap[port];
      if (IP.isIP(value)) {
        inSockets[port].post(value);
        continue;
      }
      results1.push(inSockets[port].post(new IP('data', value)));
    }
    return results1;
  })());
}
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.regularEmitEvent"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>regularEmitEvent (event, data)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.regularEmitEvent)
- description and source-code
```javascript
regularEmitEvent = function (event, data) {
  return this.emit(event, data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.send"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>send (data)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.send)
- description and source-code
```javascript
send = function (data) {
  if (data === void 0 && typeof this.dataDelegate === 'function') {
    data = this.dataDelegate();
  }
  return this.handleSocketEvent('data', data);
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.send(data, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.setDataDelegate"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>setDataDelegate (delegate)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.setDataDelegate)
- description and source-code
```javascript
setDataDelegate = function (delegate) {
  if (typeof delegate !== 'function') {
    throw Error('A data delegate must be a function.');
  }
  return this.dataDelegate = delegate;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.internalSocket.InternalSocket.prototype.setDebug"></a>[function <span class="apidocSignatureSpan">noflo.internalSocket.InternalSocket.prototype.</span>setDebug (active)](#apidoc.element.noflo.internalSocket.InternalSocket.prototype.setDebug)
- description and source-code
```javascript
setDebug = function (active) {
  this.debug = active;
  return this.emitEvent = this.debug ? this.debugEmitEvent : this.regularEmitEvent;
}
```
- example usage
```shell
...
    };
  })(this));
  return;
}
if (!node.component.network) {
  return;
}
node.component.network.setDebug(this.debug);
emitSub = (function(_this) {
  return function(type, data) {
    if (type === 'process-error' && _this.listeners('process-error').length === 0) {
      if (data.id && data.metadata && data.error) {
        throw data.error;
      }
      throw data;
...
```



# <a name="apidoc.module.noflo.journal"></a>[module noflo.journal](#apidoc.module.noflo.journal)

#### <a name="apidoc.element.noflo.journal.Journal"></a>[function <span class="apidocSignatureSpan">noflo.journal.</span>Journal (graph, metadata, store)](#apidoc.element.noflo.journal.Journal)
- description and source-code
```javascript
function Journal(graph, metadata, store) {
  this.endTransaction = bind(this.endTransaction, this);
  this.startTransaction = bind(this.startTransaction, this);
  var edge, group, iip, j, k, l, len, len1, len2, len3, m, n, node, ref, ref1, ref2, ref3, ref4, ref5, v;
  this.graph = graph;
  this.entries = [];
  this.subscribed = true;
  this.store = store || new MemoryJournalStore(this.graph);
  if (this.store.transactions.length === 0) {
    this.currentRevision = -1;
    this.startTransaction('initial', metadata);
    ref = this.graph.nodes;
    for (j = 0, len = ref.length; j < len; j++) {
      node = ref[j];
      this.appendCommand('addNode', node);
    }
    ref1 = this.graph.edges;
    for (l = 0, len1 = ref1.length; l < len1; l++) {
      edge = ref1[l];
      this.appendCommand('addEdge', edge);
    }
    ref2 = this.graph.initializers;
    for (m = 0, len2 = ref2.length; m < len2; m++) {
      iip = ref2[m];
      this.appendCommand('addInitial', iip);
    }
    if (Object.keys(this.graph.properties).length > 0) {
      this.appendCommand('changeProperties', this.graph.properties, {});
    }
    ref3 = this.graph.inports;
    for (k in ref3) {
      v = ref3[k];
      this.appendCommand('addInport', {
        name: k,
        port: v
      });
    }
    ref4 = this.graph.outports;
    for (k in ref4) {
      v = ref4[k];
      this.appendCommand('addOutport', {
        name: k,
        port: v
      });
    }
    ref5 = this.graph.groups;
    for (n = 0, len3 = ref5.length; n < len3; n++) {
      group = ref5[n];
      this.appendCommand('addGroup', group);
    }
    this.endTransaction('initial', metadata);
  } else {
    this.currentRevision = this.store.lastRevision;
  }
  this.graph.on('addNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('addNode', node);
    };
  })(this));
  this.graph.on('removeNode', (function(_this) {
    return function(node) {
      return _this.appendCommand('removeNode', node);
    };
  })(this));
  this.graph.on('renameNode', (function(_this) {
    return function(oldId, newId) {
      var args;
      args = {
        oldId: oldId,
        newId: newId
      };
      return _this.appendCommand('renameNode', args);
    };
  })(this));
  this.graph.on('changeNode', (function(_this) {
    return function(node, oldMeta) {
      return _this.appendCommand('changeNode', {
        id: node.id,
        "new": node.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('addEdge', edge);
    };
  })(this));
  this.graph.on('removeEdge', (function(_this) {
    return function(edge) {
      return _this.appendCommand('removeEdge', edge);
    };
  })(this));
  this.graph.on('changeEdge', (function(_this) {
    return function(edge, oldMeta) {
      return _this.appendCommand('changeEdge', {
        from: edge.from,
        to: edge.to,
        "new": edge.metadata,
        old: oldMeta
      });
    };
  })(this));
  this.graph.on('addInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('addInitial', iip);
    };
  })(this));
  this.graph.on('removeInitial', (function(_this) {
    return function(iip) {
      return _this.appendCommand('removeInitial', iip);
    };
  })(this));
  this.graph.on('changeProperties', (function(_this) {
    return function(newProps, oldProps) {
      return _this.appendCommand('changeProperties', {
        "new": newProps,
        old: oldProps
      });
    };
  })(this));
  this.graph.on('addGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('addGroup', group);
    };
  })(this));
  this.graph.on('renameGroup', (function(_this) {
    return function(oldName, newName) {
      return _this.appendCommand('renameGroup', {
        oldName: oldName,
        newName: newName
      });
    };
  })(this));
  this.graph.on('removeGroup', (function(_this) {
    return function(group) {
      return _this.appendCommand('removeGroup', group);
    };
  })( ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.JournalStore"></a>[function <span class="apidocSignatureSpan">noflo.journal.</span>JournalStore (graph1)](#apidoc.element.noflo.journal.JournalStore)
- description and source-code
```javascript
function JournalStore(graph1) {
  this.graph = graph1;
  this.lastRevision = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore"></a>[function <span class="apidocSignatureSpan">noflo.journal.</span>MemoryJournalStore (graph)](#apidoc.element.noflo.journal.MemoryJournalStore)
- description and source-code
```javascript
function MemoryJournalStore(graph) {
  MemoryJournalStore.__super__.constructor.call(this, graph);
  this.transactions = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.journal.JournalStore"></a>[module noflo.journal.JournalStore](#apidoc.module.noflo.journal.JournalStore)

#### <a name="apidoc.element.noflo.journal.JournalStore.JournalStore"></a>[function <span class="apidocSignatureSpan">noflo.journal.</span>JournalStore (graph1)](#apidoc.element.noflo.journal.JournalStore.JournalStore)
- description and source-code
```javascript
function JournalStore(graph1) {
  this.graph = graph1;
  this.lastRevision = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.JournalStore.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>EventEmitter ()](#apidoc.element.noflo.journal.JournalStore.EventEmitter)
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

#### <a name="apidoc.element.noflo.journal.JournalStore.init"></a>[function <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>init ()](#apidoc.element.noflo.journal.JournalStore.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.JournalStore.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.journal.JournalStore.</span>listenerCount (emitter, type)](#apidoc.element.noflo.journal.JournalStore.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.journal.JournalStore.prototype"></a>[module noflo.journal.JournalStore.prototype](#apidoc.module.noflo.journal.JournalStore.prototype)

#### <a name="apidoc.element.noflo.journal.JournalStore.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.journal.JournalStore.prototype.</span>constructor (graph1)](#apidoc.element.noflo.journal.JournalStore.prototype.constructor)
- description and source-code
```javascript
function JournalStore(graph1) {
  this.graph = graph1;
  this.lastRevision = 0;
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.journal.JournalStore.prototype.fetchTransaction"></a>[function <span class="apidocSignatureSpan">noflo.journal.JournalStore.prototype.</span>fetchTransaction (revId, entries)](#apidoc.element.noflo.journal.JournalStore.prototype.fetchTransaction)
- description and source-code
```javascript
fetchTransaction = function (revId, entries) {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.JournalStore.prototype.putTransaction"></a>[function <span class="apidocSignatureSpan">noflo.journal.JournalStore.prototype.</span>putTransaction (revId, entries)](#apidoc.element.noflo.journal.JournalStore.prototype.putTransaction)
- description and source-code
```javascript
putTransaction = function (revId, entries) {
  if (revId > this.lastRevision) {
    this.lastRevision = revId;
  }
  return this.emit('transaction', revId);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.journal.MemoryJournalStore"></a>[module noflo.journal.MemoryJournalStore](#apidoc.module.noflo.journal.MemoryJournalStore)

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore.MemoryJournalStore"></a>[function <span class="apidocSignatureSpan">noflo.journal.</span>MemoryJournalStore (graph)](#apidoc.element.noflo.journal.MemoryJournalStore.MemoryJournalStore)
- description and source-code
```javascript
function MemoryJournalStore(graph) {
  MemoryJournalStore.__super__.constructor.call(this, graph);
  this.transactions = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore.EventEmitter"></a>[function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>EventEmitter ()](#apidoc.element.noflo.journal.MemoryJournalStore.EventEmitter)
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

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore.init"></a>[function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>init ()](#apidoc.element.noflo.journal.MemoryJournalStore.init)
- description and source-code
```javascript
init = function () {
  this.domain = null;
  if (EventEmitter.usingDomains) {
    // if there is an active domain, then attach to it.
    domain = domain || require('domain');
    if (domain.active && !(this instanceof domain.Domain)) {
      this.domain = domain.active;
    }
  }

  if (!this._events || this._events === Object.getPrototypeOf(this)._events) {
    this._events = new EventHandlers();
    this._eventsCount = 0;
  }

  this._maxListeners = this._maxListeners || undefined;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore.listenerCount"></a>[function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.</span>listenerCount (emitter, type)](#apidoc.element.noflo.journal.MemoryJournalStore.listenerCount)
- description and source-code
```javascript
listenerCount = function (emitter, type) {
  if (typeof emitter.listenerCount === 'function') {
    return emitter.listenerCount(type);
  } else {
    return listenerCount.call(emitter, type);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.journal.MemoryJournalStore.prototype"></a>[module noflo.journal.MemoryJournalStore.prototype](#apidoc.module.noflo.journal.MemoryJournalStore.prototype)

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore.prototype.constructor"></a>[function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.prototype.</span>constructor (graph)](#apidoc.element.noflo.journal.MemoryJournalStore.prototype.constructor)
- description and source-code
```javascript
function MemoryJournalStore(graph) {
  MemoryJournalStore.__super__.constructor.call(this, graph);
  this.transactions = [];
}
```
- example usage
```shell
...
      flags += 'm';
    }
    if (obj.sticky != null) {
      flags += 'y';
    }
    return new RegExp(obj.source, flags);
  }
  newInstance = new obj.constructor();
  for (key in obj) {
    newInstance[key] = clone(obj[key]);
  }
  return newInstance;
};

guessLanguageFromFilename = function(filename) {
...
```

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore.prototype.fetchTransaction"></a>[function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.prototype.</span>fetchTransaction (revId)](#apidoc.element.noflo.journal.MemoryJournalStore.prototype.fetchTransaction)
- description and source-code
```javascript
fetchTransaction = function (revId) {
  return this.transactions[revId];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.journal.MemoryJournalStore.prototype.putTransaction"></a>[function <span class="apidocSignatureSpan">noflo.journal.MemoryJournalStore.prototype.</span>putTransaction (revId, entries)](#apidoc.element.noflo.journal.MemoryJournalStore.prototype.putTransaction)
- description and source-code
```javascript
putTransaction = function (revId, entries) {
  MemoryJournalStore.__super__.putTransaction.call(this, revId, entries);
  return this.transactions[revId] = entries;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams"></a>[module noflo.streams](#apidoc.module.noflo.streams)

#### <a name="apidoc.element.noflo.streams.IP"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>IP (data1)](#apidoc.element.noflo.streams.IP)
- description and source-code
```javascript
function IP(data1) {
  this.data = data1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.StreamReceiver"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>StreamReceiver (port1, buffered, process)](#apidoc.element.noflo.streams.StreamReceiver)
- description and source-code
```javascript
function StreamReceiver(port1, buffered, process) {
  this.port = port1;
  this.buffered = buffered != null ? buffered : false;
  this.process = process != null ? process : null;
  this.q = [];
  this.resetCurrent();
  this.port.process = (function(_this) {
    return function(event, payload, index) {
      var stream;
      switch (event) {
        case 'connect':
          if (typeof _this.process === 'function') {
            return _this.process('connect', index);
          }
          break;
        case 'begingroup':
          _this.level++;
          stream = new Substream(payload);
          if (_this.level === 1) {
            _this.root = stream;
            _this.parent = null;
          } else {
            _this.parent = _this.current;
          }
          return _this.current = stream;
        case 'endgroup':
          if (_this.level > 0) {
            _this.level--;
          }
          if (_this.level === 0) {
            if (_this.buffered) {
              _this.q.push(_this.root);
              _this.process('readable', index);
            } else {
              if (typeof _this.process === 'function') {
                _this.process('data', _this.root, index);
              }
            }
            return _this.resetCurrent();
          } else {
            _this.parent.push(_this.current);
            return _this.current = _this.parent;
          }
          break;
        case 'data':
          if (_this.level === 0) {
            return _this.q.push(new IP(payload));
          } else {
            return _this.current.push(new IP(payload));
          }
          break;
        case 'disconnect':
          if (typeof _this.process === 'function') {
            return _this.process('disconnect', index);
          }
      }
    };
  })(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.StreamSender"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>StreamSender (port1, ordered)](#apidoc.element.noflo.streams.StreamSender)
- description and source-code
```javascript
function StreamSender(port1, ordered) {
  this.port = port1;
  this.ordered = ordered != null ? ordered : false;
  this.q = [];
  this.resetCurrent();
  this.resolved = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.Substream"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>Substream (key)](#apidoc.element.noflo.streams.Substream)
- description and source-code
```javascript
function Substream(key) {
  this.key = key;
  this.value = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams.IP"></a>[module noflo.streams.IP](#apidoc.module.noflo.streams.IP)

#### <a name="apidoc.element.noflo.streams.IP.IP"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>IP (data1)](#apidoc.element.noflo.streams.IP.IP)
- description and source-code
```javascript
function IP(data1) {
  this.data = data1;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams.IP.prototype"></a>[module noflo.streams.IP.prototype](#apidoc.module.noflo.streams.IP.prototype)

#### <a name="apidoc.element.noflo.streams.IP.prototype.getValue"></a>[function <span class="apidocSignatureSpan">noflo.streams.IP.prototype.</span>getValue ()](#apidoc.element.noflo.streams.IP.prototype.getValue)
- description and source-code
```javascript
getValue = function () {
  return this.data;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.IP.prototype.sendTo"></a>[function <span class="apidocSignatureSpan">noflo.streams.IP.prototype.</span>sendTo (port)](#apidoc.element.noflo.streams.IP.prototype.sendTo)
- description and source-code
```javascript
sendTo = function (port) {
  return port.send(this.data);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.IP.prototype.toObject"></a>[function <span class="apidocSignatureSpan">noflo.streams.IP.prototype.</span>toObject ()](#apidoc.element.noflo.streams.IP.prototype.toObject)
- description and source-code
```javascript
toObject = function () {
  return this.data;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams.StreamReceiver"></a>[module noflo.streams.StreamReceiver](#apidoc.module.noflo.streams.StreamReceiver)

#### <a name="apidoc.element.noflo.streams.StreamReceiver.StreamReceiver"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>StreamReceiver (port1, buffered, process)](#apidoc.element.noflo.streams.StreamReceiver.StreamReceiver)
- description and source-code
```javascript
function StreamReceiver(port1, buffered, process) {
  this.port = port1;
  this.buffered = buffered != null ? buffered : false;
  this.process = process != null ? process : null;
  this.q = [];
  this.resetCurrent();
  this.port.process = (function(_this) {
    return function(event, payload, index) {
      var stream;
      switch (event) {
        case 'connect':
          if (typeof _this.process === 'function') {
            return _this.process('connect', index);
          }
          break;
        case 'begingroup':
          _this.level++;
          stream = new Substream(payload);
          if (_this.level === 1) {
            _this.root = stream;
            _this.parent = null;
          } else {
            _this.parent = _this.current;
          }
          return _this.current = stream;
        case 'endgroup':
          if (_this.level > 0) {
            _this.level--;
          }
          if (_this.level === 0) {
            if (_this.buffered) {
              _this.q.push(_this.root);
              _this.process('readable', index);
            } else {
              if (typeof _this.process === 'function') {
                _this.process('data', _this.root, index);
              }
            }
            return _this.resetCurrent();
          } else {
            _this.parent.push(_this.current);
            return _this.current = _this.parent;
          }
          break;
        case 'data':
          if (_this.level === 0) {
            return _this.q.push(new IP(payload));
          } else {
            return _this.current.push(new IP(payload));
          }
          break;
        case 'disconnect':
          if (typeof _this.process === 'function') {
            return _this.process('disconnect', index);
          }
      }
    };
  })(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams.StreamReceiver.prototype"></a>[module noflo.streams.StreamReceiver.prototype](#apidoc.module.noflo.streams.StreamReceiver.prototype)

#### <a name="apidoc.element.noflo.streams.StreamReceiver.prototype.read"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamReceiver.prototype.</span>read ()](#apidoc.element.noflo.streams.StreamReceiver.prototype.read)
- description and source-code
```javascript
read = function () {
  if (this.q.length === 0) {
    return void 0;
  }
  return this.q.shift();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.StreamReceiver.prototype.resetCurrent"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamReceiver.prototype.</span>resetCurrent ()](#apidoc.element.noflo.streams.StreamReceiver.prototype.resetCurrent)
- description and source-code
```javascript
resetCurrent = function () {
  this.level = 0;
  this.root = null;
  this.current = null;
  return this.parent = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams.StreamSender"></a>[module noflo.streams.StreamSender](#apidoc.module.noflo.streams.StreamSender)

#### <a name="apidoc.element.noflo.streams.StreamSender.StreamSender"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>StreamSender (port1, ordered)](#apidoc.element.noflo.streams.StreamSender.StreamSender)
- description and source-code
```javascript
function StreamSender(port1, ordered) {
  this.port = port1;
  this.ordered = ordered != null ? ordered : false;
  this.q = [];
  this.resetCurrent();
  this.resolved = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams.StreamSender.prototype"></a>[module noflo.streams.StreamSender.prototype](#apidoc.module.noflo.streams.StreamSender.prototype)

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.beginGroup"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>beginGroup (group)](#apidoc.element.noflo.streams.StreamSender.prototype.beginGroup)
- description and source-code
```javascript
beginGroup = function (group) {
  var stream;
  this.level++;
  stream = new Substream(group);
  this.stack.push(stream);
  this.current = stream;
  return this;
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.beginGroup(group, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.disconnect"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>disconnect ()](#apidoc.element.noflo.streams.StreamSender.prototype.disconnect)
- description and source-code
```javascript
disconnect = function () {
  this.q.push(null);
  return this;
}
```
- example usage
```shell
...
  }
  ref = this.sockets;
  for (i = 0, len = ref.length; i < len; i++) {
    socket = ref[i];
    if (!socket) {
      return;
    }
    socket.disconnect();
  }
  return;
}
if (!this.sockets[socketId]) {
  return;
}
return this.sockets[socketId].disconnect();
...
```

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.done"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>done ()](#apidoc.element.noflo.streams.StreamSender.prototype.done)
- description and source-code
```javascript
done = function () {
  if (this.ordered) {
    this.resolved = true;
  } else {
    this.flush();
  }
  return this;
}
```
- example usage
```shell
...
    results.push(this.sendIP(port, packet));
  }
  return results;
};

ProcessOutput.prototype.sendDone = function(outputMap) {
  this.send(outputMap);
  return this.done();
};

ProcessOutput.prototype.pass = function(data, options) {
  var key, val;
  if (options == null) {
    options = {};
  }
...
```

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.endGroup"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>endGroup ()](#apidoc.element.noflo.streams.StreamSender.prototype.endGroup)
- description and source-code
```javascript
endGroup = function () {
  var parent, value;
  if (this.level > 0) {
    this.level--;
  }
  value = this.stack.pop();
  if (this.level === 0) {
    this.q.push(value);
    this.resetCurrent();
  } else {
    parent = this.stack[this.stack.length - 1];
    parent.push(value);
    this.current = parent;
  }
  return this;
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.endGroup(index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.flush"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>flush ()](#apidoc.element.noflo.streams.StreamSender.prototype.flush)
- description and source-code
```javascript
flush = function () {
  var i, ip, len, ref, res;
  res = false;
  if (this.q.length > 0) {
    ref = this.q;
    for (i = 0, len = ref.length; i < len; i++) {
      ip = ref[i];
      if (ip === null) {
        if (this.port.isConnected()) {
          this.port.disconnect();
        }
      } else {
        ip.sendTo(this.port);
      }
    }
    res = true;
  }
  this.q = [];
  return res;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.isAttached"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>isAttached ()](#apidoc.element.noflo.streams.StreamSender.prototype.isAttached)
- description and source-code
```javascript
isAttached = function () {
  return this.port.isAttached();
}
```
- example usage
```shell
...
    if (_this.load > 0) {
      return _this.q.push({
        name: "disconnect"
      });
    }
    _this.outPorts[_this.outPortName].disconnect();
    _this.errorGroups = [];
    if (_this.outPorts.load.isAttached()) {
      return _this.outPorts.load.disconnect();
    }
  };
})(this));
this.inPorts[this.inPortName].on("data", (function(_this) {
  return function(data) {
    if (_this.q.length > 0) {
...
```

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.resetCurrent"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>resetCurrent ()](#apidoc.element.noflo.streams.StreamSender.prototype.resetCurrent)
- description and source-code
```javascript
resetCurrent = function () {
  this.level = 0;
  this.current = null;
  return this.stack = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.StreamSender.prototype.send"></a>[function <span class="apidocSignatureSpan">noflo.streams.StreamSender.prototype.</span>send (data)](#apidoc.element.noflo.streams.StreamSender.prototype.send)
- description and source-code
```javascript
send = function (data) {
  if (this.level === 0) {
    this.q.push(new IP(data));
  } else {
    this.current.push(new IP(data));
  }
  return this;
}
```
- example usage
```shell
...
    throw new Error((this.getId()) + ": No connections available");
  }
  this.sockets.forEach((function(_this) {
    return function(socket, index) {
      if (!socket) {
        return;
      }
      return _this.send(data, index);
    };
  })(this));
  return;
}
if (!this.sockets[socketId]) {
  throw new Error((this.getId()) + ": No connection '" + socketId + "' available");
}
...
```



# <a name="apidoc.module.noflo.streams.Substream"></a>[module noflo.streams.Substream](#apidoc.module.noflo.streams.Substream)

#### <a name="apidoc.element.noflo.streams.Substream.Substream"></a>[function <span class="apidocSignatureSpan">noflo.streams.</span>Substream (key)](#apidoc.element.noflo.streams.Substream.Substream)
- description and source-code
```javascript
function Substream(key) {
  this.key = key;
  this.value = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.noflo.streams.Substream.prototype"></a>[module noflo.streams.Substream.prototype](#apidoc.module.noflo.streams.Substream.prototype)

#### <a name="apidoc.element.noflo.streams.Substream.prototype.getKey"></a>[function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>getKey ()](#apidoc.element.noflo.streams.Substream.prototype.getKey)
- description and source-code
```javascript
getKey = function () {
  return this.key;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.Substream.prototype.getValue"></a>[function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>getValue ()](#apidoc.element.noflo.streams.Substream.prototype.getValue)
- description and source-code
```javascript
getValue = function () {
  var hasKeys, i, ip, len, obj, ref, res, val;
  switch (this.value.length) {
    case 0:
      return null;
    case 1:
      if (typeof this.value[0].getValue === 'function') {
        if (this.value[0] instanceof Substream) {
          obj = {};
          obj[this.value[0].key] = this.value[0].getValue();
          return obj;
        } else {
          return this.value[0].getValue();
        }
      } else {
        return this.value[0];
      }
      break;
    default:
      res = [];
      hasKeys = false;
      ref = this.value;
      for (i = 0, len = ref.length; i < len; i++) {
        ip = ref[i];
        val = typeof ip.getValue === 'function' ? ip.getValue() : ip;
        if (ip instanceof Substream) {
          obj = {};
          obj[ip.key] = ip.getValue();
          res.push(obj);
        } else {
          res.push(val);
        }
      }
      return res;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.Substream.prototype.push"></a>[function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>push (value)](#apidoc.element.noflo.streams.Substream.prototype.push)
- description and source-code
```javascript
push = function (value) {
  return this.value.push(value);
}
```
- example usage
```shell
...
    Graph.prototype.subscribeNetwork = function(network) {
var contexts;
contexts = [];
this.network.on('start', (function(_this) {
  return function() {
    var ctx;
    ctx = {};
    contexts.push(ctx);
    return _this.activate(ctx);
  };
})(this));
return this.network.on('end', (function(_this) {
  return function() {
    var ctx;
    ctx = contexts.pop();
...
```

#### <a name="apidoc.element.noflo.streams.Substream.prototype.sendTo"></a>[function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>sendTo (port)](#apidoc.element.noflo.streams.Substream.prototype.sendTo)
- description and source-code
```javascript
sendTo = function (port) {
  var i, ip, len, ref;
  port.beginGroup(this.key);
  ref = this.value;
  for (i = 0, len = ref.length; i < len; i++) {
    ip = ref[i];
    if (ip instanceof Substream || ip instanceof IP) {
      ip.sendTo(port);
    } else {
      port.send(ip);
    }
  }
  return port.endGroup(this.key);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.noflo.streams.Substream.prototype.toObject"></a>[function <span class="apidocSignatureSpan">noflo.streams.Substream.prototype.</span>toObject ()](#apidoc.element.noflo.streams.Substream.prototype.toObject)
- description and source-code
```javascript
toObject = function () {
  var obj;
  obj = {};
  obj[this.key] = this.getValue();
  return obj;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
