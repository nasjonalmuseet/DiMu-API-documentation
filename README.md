# Using the DigitaltMuseum API
An overview of methods to query the DigitaltMuseum (DiMu) API. This description in created with a specific aim to facilitate querying Nasjonalmuseet's collection in DiMu, but can in principle be used to query any other collection or across all collections in DiMu.

DigitaltMuseum contains more than 3,860,000 heritage objects from [Norway](http://www.digitaltmuseum.no) (1,85 mill. objects from 174 museums) and [Sweden](http://www.digitaltmuseum.se) (2 mill. objects from 51 museums) (27.09.2016).
Nasjonalmuseet currently has 36,000 objects available in DigitaltMuseum. 

DigitaltMuseum and API to the metadata is provided by [KulturIT](http://www.kulturit.no). A general API documentation (Norwegian) is at http://api.dimu.org/doc/public_api.html. The documentation below is based on KulturIT's documentation and on Nasjonalmuseet's experience using the API to create web applications using our own data in DiMu.

The API endpoint is `http://api.dimu.org/`

<h2>DiMu museums and collections</h2>

An XML overview of museums or collections per country can be found like this:

```
/api/owners?country=no&api.key=demo
/api/owners?country=se&api.key=demo
```

The term `owner` here corresponds to a museum or collection. Each owner has an element `identifier` which is used to limit an API search. The `owner` structure is flat, but owners that are children of other owners in the hiearchy have a `parent` element. Calls to the API should always be limited to one or more owners unless you specifically need to query the entire index.

Nasjonalmuseet's owner code is `NMK`, however object metadata is kept under each individual collection: `NMK-A` (Architecture), `NMK-B` (Art) and `NMK-D` (Design). Nasjonalmuseet's exhibitions are organised under the `NMK` owner code.

<h2>Querying the DiMu Solr index</h2>

For queries to the DiMu Solr index most common parameters can be used, including paging, sorting and to a certain extent faceting.

<h4>Fields:</h4>
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
| Field name | Description |
| ---------- | ------------|
|identifier.id|Identifiserer objektet|
|identifier.owner|Museum or collection code|

`artifact.uniqueId`                      : Unik Id for objekt. Fremtidens løsning for oppslag.
`artifact.type`                          : Type objekt
`artifact.pictureCount`                 : Antall bilder
`artifact.hasPictures`                   : true/false om objektet har bilde
`artifact.defaultMediaIdentifier`        : Id for standardbilde i Dimu Multimedia Server (DMS).
`artifact.defaultPictureIndex`           : imageId for standardbilde (utgår)
`artifact.publishedDate`                 : Dato for publisering
`artifact.updatedDate`                   : Dato for siste oppdatering
`artifact.ingress.title`                 : Tittel for objekt
`artifact.ingress.producer`              : Produsent for objekt
`artifact.ingress.producerRole`          : Rollekode for produsent
`artifact.ingress.additionalProducers`   : Evt. flere produsenter
`artifact.ingress.production.fromYear`   : Produksjonsår start intervall
`artifact.ingress.production.toYear`     : Produksjonsår slutt intervall
`artifact.ingress.production.place`      : Produksjonssted
`artifact.ingress.classification`        : Klassifisering
`artifact.ingress.subjects`              : Emneord
`artifact.ingress.license`               : Lisens
