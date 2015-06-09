# idunn

## Vision

Idunn consists of a collection of components which cooperate to allow people to
publish, locate, and authenticate for/against network services, without the need
for trusted central authorities like the existing DNS and CA infrastructures.

## Components

### idunn-dht

The `idunn-dht` service provides endpoint location and service discovery via a
cryptographically-verified distributed hash table.  It acts as the Idunn
equivalent of the DNS infrastructure, and provides a DNS protocol interface, but
operates in a truly distributed fashion.  Instead of using a central authority
to attest a single shared name hierarchy, Idunn uses asymmetric cryptography to
allow participating peers to attest their own parallel independent namespaces.

Each `idunn-dht` resource record exists within a hierarchy “owned” by a
particular public key is signed by the corresponding private key.
