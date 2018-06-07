---
title: Identification | Organization
keywords: usecase, Organization
tags: [rest, fhir, identification,development]
sidebar: accessrecord_rest_sidebar
permalink: restfulapis_identification_organization.html
summary: A formally or informally recognized grouping of people or organizations formed for the purpose of achieving some form of collective action. Includes companies, institutions, corporations, departments, community groups, healthcare practice groups, etc.
---


## 1. Read ##

<div markdown="span" class="alert alert-success" role="alert">
GET https://directory.spineservices.nhs.uk/STU3/Organization/[id]</div>

{% include custom/read.response.html resource="Organization" content="" %}

<script src="https://gist.github.com/IOPS-DEV/aa574228008b504d3df3d0902a6ae694.js"></script>

## 2. Search ##

<div markdown="span" class="alert alert-success" role="alert">
GET https://directory.spineservices.nhs.uk/STU3/Organization?[SearchParameters]</div>

Returns a `Bundle` of all `Organization` resources that match the specified search criteria.

By default the response will be returned in JSON, however XML is also supported.

### 2.1. Search Parameters ###

{% include custom/search.parameters.html resource="Organization" link="https://www.hl7.org/fhir/organization.html#search)" %}

| Name | Parameter Type | Description | Path |
|------|------|-------------|------|
| <a href="restfulapis_identification_organization.html#_id">`_id`</a> |`token`|The logical id of the resource (Code)|	Organization.id|
| <a href="restfulapis_identification_organization.html#_lastUpdated">`_lastUpdated`</a> |`date`| To select resources based on the last time they were changed|Organization.meta.lastUpdated|


Additional Parameters:

| Name | Parameter Type | Description | Allowable Content |
|------|------|-------------|------|
| <a href="restfulapis_identification_organization.html#_count">`_count`</a>|`number` | Number of results per page| Whole number |
| <a href="restfulapis_identification_organization.html#_summary">`_summary`</a>|`string`| Search only: just return a count of the matching resources, without returning the actual matches |'count'|

{% include custom/search.nopat.id.html para="2.1.1." resource="Organization" content="_id"  example="RTG" example2="RTG" text1="Code" example1="RTG (Derby Teaching Hospitals NHS Foundation Trust)" %}

{% include custom/search.lastupdated.html para="2.1.2." resource="Organization" content="_lastUpdated" example="gt2017-04-01" text1="Organization" text2="2017-04-01" %}

The supported prefixes for this search parameter are:

| Prefix | Description |
|------|------|
|gt|greater than|

{% include custom/search.nopat.identifier.html para="2.1.3." resource="Organization" content="identifier"  example="https://fhir.nhs.uk/Id/code|RTG" example2="RTG" text1="Code" text2="RTG (Derby Teaching Hospitals NHS Foundation Trust)" %}

{% include custom/search.nopat.string.html para="2.1.4." resource="Organization" content="name"  example="Derby Teaching Hospitals NHS Foundation Trust" text1="name" text2="Derby Teaching Hospitals NHS Foundation Trust" %}

Search expressions must:

-	Contain a minimum of 3 characters and a maximum of 100 characters
-	Only include characters (A-Z a-z 0-9 &()'+ -_ -./ : : @) 'Space'

**Begins with:**

By default, a field matches a string query if the value of the field equals or starts with the supplied parameter value, after both have been normalized by case and accent.

To search for a name that begins with "Leeds", the following search should be executed: 

```
GET https://directory.spineservices.nhs.uk/STU3/Organization?name=Leeds
```
This will return the records that have an Organization name that begins with "Leeds" e.g. RQS98 - Leeds Chest Clinic and RX847 - Leeds Central Ambulance Station etc.

**Contained match:**

The `:contains` modifier returns results that include the supplied parameter value anywhere within the field being searched.

To search for a name that contains "Leeds", the following search should be executed:

```
GET https://directory.spineservices.nhs.uk/STU3/Organization?name:contains=Leeds
```
This will return the records that have an Organization name that contains the word "Leeds" within its name e.g 5HL18 - South Leeds Clinical Assessment Service and B86013 - The North Leeds Medical Practice etc.




