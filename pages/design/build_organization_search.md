---
title: Build | Your project Search
keywords: development
tags: [build,development]
sidebar: overview_sidebar
permalink: build_organization_search.html
summary: "How to use the "Your project here" to perform searches on "service here", containing examples that use different technologies to perform a search. This includes HAPI Java, C# .NET and cURL."
---

{% include custom/ihe.reference.html apicontent="[Organization](restfulapis_identification_organization.html) "  odscontent="[NHS Digital ODS Offical Site](https://digital.nhs.uk/organisation-data-service)"  patterncontent="[Shared Repository](https://developer.nhs.uk/library/architecture/integration-patterns/portal/)" %}

## 1. Overview ##

{% include custom/usecase.html content="Add an example use case here" %}


Add an overview. Not too detailed but enough to provide a genral overview of the project/app.

Diagrams can be useful to explain flow.

"Your project here" provides an API using a [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) interface following a {% include custom/patterns.inline.html content="[resource API pattern](http://www.servicedesignpatterns.com/WebServiceAPIStyles/ResourceAPI)" %} to provide access to the "service/database/data store".

This is particularly suited to:
* A health portal securely exposing organisational information to browser based plugins.
* Medical devices which need to access organisational information.
* Mobile devices used by physicians which need to establish organisational information.
* Web based EPR/EHR applications which wish to provide dynamic updates of organisation details.
* Any low resource application which exposes organisational search functionality.
* A facade providing a simple API to a complex interface.

## 2. Client Organisation Search ##

### 2.1 Foundation ###


## 3. Search Parameters ##

Examples of using different technologies to perform a search.

| Parameter | Parameter Type | Description | HAPI Java | C# .NET | cURL |
|------|------|-------------|------|------|------|
| <a href="build_organization_search.html#31-search-using-ods-code">`_id`/`identifier`</a>|`token`|Search for ODS records based on their logical or business identifier|<a href="build_organization_search.html#311-hapi-java"><i class="fa fa-code"></i></a> | <a href="build_organization_search.html#312-c-net"><i class="fa fa-code"></i></a> | <a href="build_organization_search.html#313-curl"><i class="fa fa-code"></i></a> |
| <a href="build_organization_search.html#32-search-using-last-updated-date">`_lastUpdated`</a> |`date`| Search for ODS records based on their last updated date| <a href="build_organization_search.html#321-hapi-java"><i class="fa fa-code"></i></a>| <a href="build_organization_search.html#322-c-net"><i class="fa fa-code"></i></a>|<a href="build_organization_search.html#323-curl"><i class="fa fa-code"></i></a>|


### 3.1 Search using Code ###


#### 3.1.1 HAPI Java ####


#### 3.1.2 C# .NET ####


#### 3.1.3 cURL ####


### 3.2 Search using last updated date ###


#### 3.2.1 HAPI Java ####


#### 3.2.2 C# .NET ####


#### 3.2.3 cURL ####

      


