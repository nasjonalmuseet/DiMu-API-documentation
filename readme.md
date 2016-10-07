# Using the DigitaltMuseum API
An overview of methods to query the DigitaltMuseum (DiMu) API. This description in created with a specific aim to facilitate querying Nasjonalmuseet's collection in DiMu, but can in principle be used to query any other collection or across all collections in DiMu.

DigitaltMuseum contains more than 3,860,000 heritage objects from [Norway](http://www.digitaltmuseum.no) (1,85 mill. objects from 174 museums) and [Sweden](http://www.digitaltmuseum.se) (2 mill. objects from 51 museums) (27.09.2016).
Nasjonalmuseet currently has 36,000 objects available in DigitaltMuseum. [Nasjonalmuseet's metadata are licensed Creative Commons Zero CC0](license.md). Re-use is encouraged.

DigitaltMuseum and API to the metadata is provided by [KulturIT](http://www.kulturit.no). A general API documentation (Norwegian) is at http://api.dimu.org/doc/public_api.html. The documentation below is based on KulturIT's documentation and on Nasjonalmuseet's experience using the API to create web applications using our own data in DiMu. [Disclaimer](disclaimer.md)

The API endpoint is `http://api.dimu.org/`

<h2>DiMu museums and collections</h2>

An xml overview of museums or collections per country can be found like this:

```
/api/owners?country=no&api.key=demo
/api/owners?country=se&api.key=demo
```

The term `owner` here corresponds to a museum or collection. Each owner has an element `identifier` which is used to limit an API search. The `owner` structure is flat, but owners that are children of other owners in the hiearchy have a `parent` element. Calls to the API should always be limited to one or more owners unless you specifically need to query the entire index.

Nasjonalmuseet's owner code is `NMK`, however object metadata is kept under each individual collection: `NMK-A` (Architecture), `NMK-B` (Art) and `NMK-D` (Design). Nasjonalmuseet's exhibitions are organised under the `NMK` owner code.

<h2>Querying the DiMu Solr index</h2>

For queries to the DiMu Solr index most common parameters can be used, including paging, sorting and to a certain extent faceting.

<h3>Fields</h3>
There are several searchable fields in the solr index. Some are stored and not tokenized, and some fields are tokenized but not stored, but still searchable. Typical examples of stored fields are the `.ingress.` fields. The content of these fields are displayed in the search result. There are other stored fields that are not part of `.ingress.` that can be be used.

``` javascript
{
  artifact.ingress.title: "Stemma. Quattrocento [Maleri]",
  artifact.ingress.producer: "Slaattelid, Mari",
  artifact.uuid: "5A4FCFDD-CB15-4DB1-971F-4FF5D15E68F6",
  artifact.pictureCount: 1,
  artifact.defaultPictureIndex: 15618,
  artifact.childCount: 2,
  artifact.defaultMediaIdentifier: "012wWWHgNJLA",
  artifact.hasPictures: true,
  artifact.uniqueId: "021045839502",
  artifact.ingress.production.toYear: 1999,
  artifact.ingress.producerRole: "Kunstner",
  artifact.publishedDate: "2015-04-18T06:18:23.538Z",
  artifact.ingress.license: [
    "AC 1"
    ],
  identifier.id: "MS-04266-1999",
  artifact.hasChildren: true,
  identifier.owner: "NMK-B",
  artifact.type: "Fineart",
  artifact.ingress.production.fromYear: 1999,
  artifact.ingress.subjects: [
    "Bildende kunst"
    ],
  artifact.updatedDate: "2015-09-22T07:49:19.08Z"
}
```
<h4>Indexed fields</h4>
| Field name | Description |
| ---------- | ------------|
|*identifier.id*|Museum or collection's own identifier / inventory no., e.g. NMK.2005.0257|
|*identifier.owner*|Museum or collection code, e.g. NMK-B|
|*artifact.uniqueId*|DiMu-specific unique id for object, e.g. 021045835852|
|*artifact.name*|Name, alternative name, etc| 
|*artifact.type*|Type of object, e.g. 'Exhibition'|
|*artifact.classification*|Classification. Nasjonalmuseet uses [Outline](http://kulturnav.org/a8797483-ff02-4a4c-adf1-b406cbcd6fc2) where relevant.|
|*artifact.pictureCount*|No. of images for this object|
|*artifact.hasPictures*|*true* or *false*|
|*artifact.defaultMediaIdentifier*|Id for default picture on DiMu media server (DMS)|
|*artifact.publishedDate*|Date published to DiMu|
|*artifact.updatedDate*|Last updated|
|*artifact.ingress.title* or *artifact.title*|Object title|
|*artifact.ingress.producer* or *artifact.producer*|Producer|
|*artifact.ingress.producerRole*|Role code for producer: Artist, designer, architect etc|
|*artifact.ingress.additionalProducers*|Any additional producers|
|*artifact.ingress.production.fromYear* or *artifact.event.fromYear*|Production year start|
|*artifact.ingress.production.toYear* or *artifact.event.toYear*|Production year end|
|*artifact.ingress.production.place* or *artifact.event.place*|Production place|
|*artifact.eventDescription*|Event description||*artifact.ingress.classification*|Classification|
|*artifact.ingress.subjects*|Subjects|
|*artifact.depictedPerson*|Depicted person|
|*artifact.depictedPlace*|Depicted place|
|*artifact.material*|Material|
|*artifact.technique*|Technique|
|*artifact.ingress.license* or *artifact.license*|Object license (not picture license)|
|*allContent*|Free text search field (default)|

<h2>Detail view</h2>
A detailed view of individual objects can be requested, represented in JSON by default. Use the object’s artifact.uuid from the Solr result to retrieve a detailed view, e.g.
```
http://api.dimu.org/artifact/uuid/3DF10C96-B33B-45C1-92BF-D9211CE574C8
```
[Se here for an overview of the individual object representation](detail-view.md).

<h2>Retrieving media</h2>
All photo files from Nasjonalmuseet's collection are licensend [CC-BY-NC](https://creativecommons.org/licenses/by-nc/4.0/legalcode). The copyright of individual objects, in particular artworks, can carry a copyright that prevents free re-use. Any copyright for an individual object will be represented in the metadata.
[See here for a description of how to retrieve pictures from the DiMu media servers](retrieving-media.md).
