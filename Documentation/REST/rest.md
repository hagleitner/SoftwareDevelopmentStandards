---
layout: default
title: REST
nav_order: 20
permalink: /documentation/rest
---

# REST

We use Git as version control system.

## Naming 

Use lower case resource names like https://adventure-works.com/orders/1
### Endpoint naming

* Use lower-case only
* use dash to delimit words e.g. https://adventure-works.com/service-info

### Use plural where applicable

Use plural nouns for URIs that reference collections. It's a good practice to organize URIs for collections and items into a hierarchy. For example, /customers is the path to the customers collection, and /customers/5 is the path to the customer with ID equal to 5. This approach helps to keep the web API intuitive.

E.g. 

* The GET endpoint https://adventure-works.com/orders will deliver a collection of orders.
* The GET endpoing https://adventure-works.com/service-version will deliver a single data object, therefore singular is ok here.

## Elements with multiple Ids

If an element is identifiable by multiple Ids, we decide for a primary id. This is then used in endpoints like:

/standard/v1/devices/{primaryId}/datalinks

Additional Ids must be resolved first by the client. For this we provide a search-like endpoint:

/standard/v1/devices?identifierType=componentId?identifier="xyz"