# Grenache
DHT based high-performance microservices framework, by Bitfinex

#### Features
* Decentralised / Distributed architecture
* Easy Bootstrap
* Indefinite scalability and shapes
* High-Performance

### Implementations

#### Grape (the core)
* https://github.com/bitfinexcom/grenache-grape

#### Clients
* ZeroMQ transport: super-fast, perfect for internal networks
* WebSocket transport: great for Internet

Note: At the moment there is no interoperability between WebSocket and ZeroMQ implementations. A Proxy implementation will come later.

##### Node.JS Clients
* https://github.com/bitfinexcom/grenache-nodejs-zmq : ZeroMQ based Grape microservices
* https://github.com/bitfinexcom/grenache-nodejs-ws : WebSocket based Grape microservices

##### Ruby Clients
* https://github.com/bitfinexcom/grenache-ruby-ws : ZeroMQ based Grape microservices


### Background
* [Distributed Hash Table] (http://www.bittorrent.org/beps/bep_0005.html) introduction

#### Composition

##### 1. Grape: Grenache Discovery Node
* Grenache Network building
* DHT interaction APIs for Clients: service discovery, DHT data storage

**Features**

WebSocket API endpoints:
* Announce a Service
* Lookup a Service
* Push data to DHT

##### 2. Client: Grenache Client implementation on specific Transports
* Client/Worker: offer/publish and request/subscribe Services
* Patterns: request/reply, publish/subscribe
* Transports: ZeroMQ, WebSocket

**Features**
* Offer / Publish a Service: create and announce a Service on the DHT
* Request / Subscribe to Service: find a Service throught the DHT and connect to it

###Practice

![Grenache Structure](https://raw.githubusercontent.com/bitfinexcom/grenache/master/doc/structure.png)

* client: can both offer/publish or request/subscribe Services

### Contribute
Any contribution in form of question, issue, idea and pull requests is well accepted

### Contacts
* [Paolo Ardoino] (https://github.com/prdn)
