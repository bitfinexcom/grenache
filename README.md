# Grenache

Grenache is a DHT based high-performance microservices framework by Bitfinex.
Its decentralised and optimized for performance. Because its simple, it is easy
to understand and to set up.

Grenache uses Distributed Hashtables, known from Bittorrent, to build a network between peers.
Its based on [Kademlia](https://en.wikipedia.org/wiki/Kademlia).

Peers can send each other commands (RPC), and they can also store values in the DHT.
Pub/Sub is also possible.


#### Features
* Decentralised / Distributed architecture
* Easy Bootstrap
* Indefinite scalability and shapes
* High-Performance

### Implementations

#### Grape (the core)
* https://github.com/bitfinexcom/grenache-grape

#### Peer Implementations

Transports:
* WebSocket transport: super-fast, great for Internet
* HTTP transport: great for Internet
* ZeroMQ transport: super-fast, perfect for internal networks

Patterns:
* PUB/GET: put/get data to/from the DHT
* RPC: simple and efficient RPC pattern
* PUB/SUB: (Work In Progress)

Note: At the moment there is no interoperability between WebSocket and ZeroMQ implementations. A Proxy implementation will come later.

##### Node.JS Clients
* https://github.com/bitfinexcom/grenache-nodejs-ws : WebSocket based Grape microservices
* https://github.com/bitfinexcom/grenache-nodejs-http : HTTP based Grape microservices
* https://github.com/bitfinexcom/grenache-nodejs-zmq : ZeroMQ based Grape microservices
* https://github.com/bitfinexcom/grenache-nodejs-ws-tls : WebSocket based Grape microservices with TLS support

##### Ruby Clients
* https://github.com/bitfinexcom/grenache-ruby-ws : WebSocket based Grape microservices
* https://github.com/bitfinexcom/grenache-ruby-http : HTTP based Grape microservices


### Background
* [Distributed Hash Table](http://www.bittorrent.org/beps/bep_0005.html) introduction
* [Kademlia on Wikipedia](https://en.wikipedia.org/wiki/Kademlia)

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
* Transports: WebSocket, HTTP, ZeroMQ

**Features**
* Offer / Publish a Service: create and announce a Service on the DHT
* Request / Subscribe to Service: find a Service throught the DHT and connect to it

### Practice

![Grenache Structure](https://raw.githubusercontent.com/bitfinexcom/grenache/master/doc/structure.png)

* client: can both offer/publish or request/subscribe Services

### Contribute
Any contribution in form of question, issue, idea and pull requests is well accepted

### Contacts
* [Paolo Ardoino](https://github.com/prdn)
