# <img src="https://raw.githubusercontent.com/claustres/mether/master/mether.png" width="56" height="44" /> Mether

Mether is a resilient secure distributed application platform using analogies from physics, hence the name created from :
* Matter, any substance made up of elementary building blocks such as quarks.
* Ether, a postulated medium for the propagation of non-mechanical interactions.

A Mether is also a communal or *Friendship* drinking vessel from the Celtic tradition, visitors were formally welcomed in 'peace and friendship' with a mether, just like we want to welcome you to this community. While the original utility of analogies was generative – producing a model that explained how it works - the analogy is also useful to communicate to new comers or non-developers about the project. 

## Objectives

Usually, applications are designed to be deployed knowing the state of the underlying infrastructure. This means that each time the state of the infrastructure changes the application configuration needs to be updated, leading to what is commonly refered as the *configuration hell*. Indeed, from the point of view of the application developer the infrastructure details such as IP addresses, network connectivity, discovery, messaging, etc. should be hidden and the deployment experience should be portable.

Mether provides a new paradigm where the application *shapes* the infrastructure as required just like a man shapes the physical world to create his tools. It means that Mether is a stateless infrastructure that auto-detect, auto-configure, auto-respond, auto-heal, auto-scale according to application requirements. Hiding how infrastructure achieved this behind a simple API, we believe resilient applications should be built and distributed more easily. 

Resilience is the conjunction of different factors that can be seen as guidelines :
* Open Source components
* Node diversity (e.g. geographic, jurisdictional, operating systems, etc.)
* Data integrity
* Stealth infrastructure (no identifiable topology)

## Basic concepts

In Physics, a *quark* is an elementary particle and a fundamental constituent of matter. In Mether, a quark is an elementary chunk of data and a fundamental constituent of information. Like in Physics, there are different types of quarks known as flavors. Flavors are non-hierarchical metadata assigned to a piece of information, like tags or labels, and allows a quark to be described and found again by searching. Quark content addressing is based on cryptographic-hashes allowing integrity checking and providing wide, secure, trustless exchanges of data. 

In Physics, a *hadron* is a composite particle made of quarks held together. In Mether, quarks can similarly be grouped in hadrons and manipulated as a batch.

In Mether, *atoms* are the smallest constituent unit of application functions that can reliably be moved from one computing environment to another, a.k.a. containers. 

In Physics, a *molecule* consists of a stable system composed of two or more atoms exhibing specific properties. In Mether, molecules adds a higher level of abstraction to atoms, which are containerized components. A molecule composes several existing fine-grained components into a single higher order composite element, which can be typically seen as a microservice, in order to achieve the appropriate "granularity" while promoting reuse and manageability of the underlying components.

In Physics, atoms interact, form molecules, and manifest further properties through interactions and force carriers or messenger particles of underlying fields. In Mether, application components interact through a *serverless messaging system* supported by a field of computers. In Physics, different exchange forces do exist e.g. the color force for quarks, the strong force for hadrons, the electromagnetic force for atoms and molecules. In Mether different built-in message exchanges do exist between each type of constituent at each scale.

## Working with Mether

The implementation of Mether is based on a message-oriented middleware used by the application to send commands to the infrastructure thanks to a simple protocol similar to [JSON-RPC](http://www.jsonrpc.org/specification). Then, the infrastructure ensures the transport protocol negotiation between the multiple formats supported by atoms (such as HTTP or JDBC). Mether is designed to avoid unecessary layers so that the parameters of the messages are directly formatted according to what is required by the underlyign technologies (e.g. container engine or database).

Application requirements with regard to the infrastructure are expressed using a Metherfile. At startup this file is converted into a set of command messages in order to :
* create the quarks required by each atom (a.k.a. container images)
* create the atoms required by the molecules (a.k.a. container instances)
* create the molecules required by the application (a.k.a. microservices)

## Candidate underlying technologies

* Distributed data storage to support Matter like
 * https://ipfs.io/
 * https://github.com/datproject/dat
 * https://github.com/mafintosh/hyperdrive
 * https://github.com/bigchaindb/bigchaindb
 * https://github.com/haadcode/orbit-db
 * http://orientdb.com/
* Distributed messaging to support Ether like
 * http://kafka.apache.org/
 * http://nsq.io/
 * https://github.com/edwardchoh/zmqbus-node
* Container manager to support Atoms like
 * https://www.docker.com/ 
 * http://kubernetes.io/



