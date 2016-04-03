# Grenache
DHT based high-performance microservices framework, by Bitfinex

### Technology
* DHT definition: http://www.bittorrent.org/beps/bep_0005.html

#### Definitions

##### 1. Grape: Grenache Discovery Node
* Grenache Network building
* DHT interaction APIs for Clients: service discovery, DHT data storage

API:
* announce Service
* lookup Service
* write to DHT

##### 2. Client: Grenache Client implementation on specific Transports
* Client/Worker: offer/publish and request/subscribe Services
* Patterns: request/reply, publish/subscribe
* Transports: ZeroMQ, WebSocket

API:
* offer/publish Service: create and announce a Service on the DHT
* request/subscribe Service: find a Service throught the DHT and connect to it


#### Features
* Decentralised / Distributed
* High-Performance
* Indefinite growth and shapes

#### Structure Example

![Grenache Structure](https://raw.githubusercontent.com/bitfinexcom/grenache/master/doc/structure.png)

* client: can both offer/publish or request/subscribe Services

### Implementations

##### Grape
* https://github.com/bitfinexcom/grenache-grape

##### Node.JS Clients
* https://github.com/bitfinexcom/grenache-nodejs-zmq : ZeroMQ based Grape microservices
* https://github.com/bitfinexcom/grenache-nodejs-ws : WebSocket based Grape microservices

##### Ruby Clients
* https://github.com/bitfinexcom/grenache-ruby-zmq : ZeroMQ based Grape microservices
