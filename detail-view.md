<h2>Collection object detailed view</h2>
http://api.dimu.org/artifact/uuid/3DF10C96-B33B-45C1-92BF-D9211CE574C8
The url above will return a JSON representation of the object. Below are comments on central parts of the metadata returned.

<h3>Motif</h3>
Motif information varies in detail, and can contain depicted objects, people, places, geocoordinates, motif types/genres etc.
``` Javascript
{
motif: {
  depictedObjects: [ ],
  motifTypes: [
    "Stilleben"
  ],
  titles: [ ],
  classifications: [ ]
}
```
<h3>Media</h3>
This particular object has three pictures. Resolution is specified. If width and height is set to 0, the image is of older date and of low resolution (below 800px). The picture files can hold a separate copyright license than the actual collection object. All Nasjonalmuseet's picture files are licensend CC-BY-NC. If a collection object is under copyright, license information will be specificed in the metadata.
``` Javascript
media: {
  pictures: [
    {
      index: 113324,
      code: "0",
      width: 4000,
      licenses: [ ],
      photographer: "Jarre, Anne Hansteen",
      identifier: "032wXVwUzT6J",
      height: 3297
      }
    ],
  mediaFiles: [ ],
  movies: [ ]
}
```
<h3>Technique</h3>
``` Javascript
technique: {
techniques: [
{
sort: 1,
technique: "Olje"
}
]
},
partOfCollection: {
owner: {
identifier: "NMK",
id: 1,
name: "Nasjonalmuseet for kunst, arkitektur og design"
},
ownerId: "NMK",
id: 7,
uuid: "70893D84-C63C-4F5F-A4B1-491DCFC7B386",
name: "NMK billedkunst [eldre og moderne]"
},
copies: [ ],
coordinates: [ ],
subjects: [
{
nameType: "subject",
name: "Bildende kunst",
uuid: "BE0D8624-1B19-45ED-A0EF-71E05220406A"
}
],
uniqueId: "011042436982",
dimu_code: "011042436982",
eventWrap: {
placesOfProduction: [ ],
producers: [
{
info: {
nationality: "Norge",
professions: [ ],
alternativeNames: [
{
id: 17720,
name: "Gude, Hans Fredrik",
description: "Fullt navn"
}
],
places: [
{
coordinate: "59.9138688, 10.752245399999992",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "03",
number: 7,
value: "Oslo (fylke)",
name: "Fylke"
},
{
sort: 3,
code: "0301",
number: 2,
value: "Oslo",
name: "Kommune"
}
],
role: {
name: "Fødested, "
},
uuid: "8ABED23D-E315-40FB-9CB5-B6B6BD3A643A"
},
{
coordinate: "52.519171, 13.406091199999991",
fields: [
{
sort: 1,
number: 1,
value: "Tyskland",
name: "Land"
},
{
sort: 4,
number: 3,
value: "Berlin",
name: "Område"
}
],
role: {
name: "Dødssted, "
},
uuid: "1EE7603E-3C5C-42A4-A639-87371F0C5211"
}
],
gender: "Mann"
},
role: {
code: "10K",
name: "Kunstner"
},
uuid: "692ED30C-74B8-4146-935E-94C26DD63ED6",
name: "Gude, Hans",
type: "Person",
id: 17720,
publishLevel: "extended"
},
{
info: {
nationality: "Norge",
professions: [ ],
alternativeNames: [ ],
places: [
{
coordinate: "58.0276808, 7.4533303000000615",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "10",
number: 7,
value: "Vest-Agder",
name: "Fylke"
},
{
sort: 3,
code: "1002",
number: 2,
value: "Mandal",
name: "Kommune"
}
],
role: {
name: "Fødested, "
},
uuid: "167DA402-E7CE-493C-8D45-128F2399B39D"
},
{
coordinate: "59.9138688, 10.752245399999992",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "03",
number: 7,
value: "Oslo (fylke)",
name: "Fylke"
},
{
sort: 3,
code: "0301",
number: 2,
value: "Oslo",
name: "Kommune"
}
],
role: {
name: "Dødssted, "
},
uuid: "8ABED23D-E315-40FB-9CB5-B6B6BD3A643A"
}
],
gender: "Mann"
},
role: {
code: "10K",
name: "Kunstner"
},
uuid: "2510E079-AB33-49F8-B2F2-3BF2F3F733E8",
name: "Tidemand, Adolph",
type: "Person",
id: 17592,
publishLevel: "extended"
}
],
descriptiveDating: "1848",
production: {
sort: 6,
timespan: {
toDate: "18480101-133000-000",
fromDate: "18480101-133000-000"
},
eventType: "Produksjon",
relatedPersons: [
{
info: {
nationality: "Norge",
professions: [ ],
alternativeNames: [
{
id: 17720,
name: "Gude, Hans Fredrik",
description: "Fullt navn"
}
],
places: [
{
coordinate: "59.9138688, 10.752245399999992",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "03",
number: 7,
value: "Oslo (fylke)",
name: "Fylke"
},
{
sort: 3,
code: "0301",
number: 2,
value: "Oslo",
name: "Kommune"
}
],
role: {
name: "Fødested, "
},
uuid: "8ABED23D-E315-40FB-9CB5-B6B6BD3A643A"
},
{
coordinate: "52.519171, 13.406091199999991",
fields: [
{
sort: 1,
number: 1,
value: "Tyskland",
name: "Land"
},
{
sort: 4,
number: 3,
value: "Berlin",
name: "Område"
}
],
role: {
name: "Dødssted, "
},
uuid: "1EE7603E-3C5C-42A4-A639-87371F0C5211"
}
],
gender: "Mann"
},
role: {
code: "10K",
name: "Kunstner"
},
uuid: "692ED30C-74B8-4146-935E-94C26DD63ED6",
name: "Gude, Hans",
type: "Person",
id: 17720,
publishLevel: "extended"
},
{
info: {
nationality: "Norge",
professions: [ ],
alternativeNames: [ ],
places: [
{
coordinate: "58.0276808, 7.4533303000000615",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "10",
number: 7,
value: "Vest-Agder",
name: "Fylke"
},
{
sort: 3,
code: "1002",
number: 2,
value: "Mandal",
name: "Kommune"
}
],
role: {
name: "Fødested, "
},
uuid: "167DA402-E7CE-493C-8D45-128F2399B39D"
},
{
coordinate: "59.9138688, 10.752245399999992",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "03",
number: 7,
value: "Oslo (fylke)",
name: "Fylke"
},
{
sort: 3,
code: "0301",
number: 2,
value: "Oslo",
name: "Kommune"
}
],
role: {
name: "Dødssted, "
},
uuid: "8ABED23D-E315-40FB-9CB5-B6B6BD3A643A"
}
],
gender: "Mann"
},
role: {
code: "10K",
name: "Kunstner"
},
uuid: "2510E079-AB33-49F8-B2F2-3BF2F3F733E8",
name: "Tidemand, Adolph",
type: "Person",
id: 17592,
publishLevel: "extended"
}
],
relatedPlaces: [ ],
eventTypeClarification: "Produsert"
},
events: [
{
sort: 6,
timespan: {
toDate: "18480101-133000-000",
fromDate: "18480101-133000-000"
},
eventType: "Produksjon",
relatedPersons: [
{
info: {
nationality: "Norge",
professions: [ ],
alternativeNames: [
{
id: 17720,
name: "Gude, Hans Fredrik",
description: "Fullt navn"
}
],
places: [
{
coordinate: "59.9138688, 10.752245399999992",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "03",
number: 7,
value: "Oslo (fylke)",
name: "Fylke"
},
{
sort: 3,
code: "0301",
number: 2,
value: "Oslo",
name: "Kommune"
}
],
role: {
name: "Fødested, "
},
uuid: "8ABED23D-E315-40FB-9CB5-B6B6BD3A643A"
},
{
coordinate: "52.519171, 13.406091199999991",
fields: [
{
sort: 1,
number: 1,
value: "Tyskland",
name: "Land"
},
{
sort: 4,
number: 3,
value: "Berlin",
name: "Område"
}
],
role: {
name: "Dødssted, "
},
uuid: "1EE7603E-3C5C-42A4-A639-87371F0C5211"
}
],
gender: "Mann"
},
role: {
code: "10K",
name: "Kunstner"
},
uuid: "692ED30C-74B8-4146-935E-94C26DD63ED6",
name: "Gude, Hans",
type: "Person",
id: 17720,
publishLevel: "extended"
},
{
info: {
nationality: "Norge",
professions: [ ],
alternativeNames: [ ],
places: [
{
coordinate: "58.0276808, 7.4533303000000615",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "10",
number: 7,
value: "Vest-Agder",
name: "Fylke"
},
{
sort: 3,
code: "1002",
number: 2,
value: "Mandal",
name: "Kommune"
}
],
role: {
name: "Fødested, "
},
uuid: "167DA402-E7CE-493C-8D45-128F2399B39D"
},
{
coordinate: "59.9138688, 10.752245399999992",
fields: [
{
sort: 1,
number: 1,
value: "Norge",
name: "Land"
},
{
sort: 2,
code: "03",
number: 7,
value: "Oslo (fylke)",
name: "Fylke"
},
{
sort: 3,
code: "0301",
number: 2,
value: "Oslo",
name: "Kommune"
}
],
role: {
name: "Dødssted, "
},
uuid: "8ABED23D-E315-40FB-9CB5-B6B6BD3A643A"
}
],
gender: "Mann"
},
role: {
code: "10K",
name: "Kunstner"
},
uuid: "2510E079-AB33-49F8-B2F2-3BF2F3F733E8",
name: "Tidemand, Adolph",
type: "Person",
id: 17592,
publishLevel: "extended"
}
],
relatedPlaces: [ ],
eventTypeClarification: "Produsert"
}
],
acquisition: "Kjøpt 1895"
},
material: {
comment: "Olje på lerret",
materials: [
{
sort: 1,
material: "Lerret"
}
]
},
artifact_id: 2436982,
tags: [
{
source: "DIMU",
name: "Nasjonalromantikk"
}
],
rateCount: 0,
measures: [
{
sort: 1,
category: "Hovedmål",
type: "Høyde",
unit: "cm",
measure: 93.5
},
{
sort: 2,
category: "Hovedmål",
type: "Bredde",
unit: "cm",
measure: 130.1
},
{
sort: 3,
category: "Hovedmål",
type: "Dybde",
unit: "cm",
measure: 2.9
},
{
sort: 4,
category: "Rammemål",
type: "Dybde",
unit: "cm",
measure: 11.5
},
{
sort: 5,
category: "Rammemål",
type: "Bredde",
unit: "cm",
measure: 161.7
},
{
sort: 6,
category: "Rammemål",
type: "Høyde",
unit: "cm",
measure: 125.7
}
],
measureDescription: "93,5 x 130,1 x 2,9 cm",
alternativeIdentifiers: [ ],
partOfExhibitionUuids: [
"4A837DA3-904B-4447-9AF6-155A4D14A679",
"C2901D38-57A6-4DD0-B342-25FCE70F2522"
],
trademarks: [ ],
createdDate: "20131214-065714-962907",
dimuCode: "011042436982",
inscriptions: [ ],
classifications: [
{
code: "532",
system: "OU",
description: "Bildende kunst"
}
],
partOfFolderUuids: [
"7ac78c48-6d3d-11e2-ab71-ebc66a9caa67",
"dafbd94f-60b6-11e3-a165-b659863c44bf"
],
level: {
code: "9",
name: "Enkeltverk"
},
sourceId: "82612",
updatedDate: "20160930-040918-689159",
publishedDate: "20101208-230000-000",
relatedObjects: [
{
relationId: 28,
artifactType: "Fineart",
identifier: {
owner: "NMK-B",
id: "NMK.2005.0373"
},
relation: "Relatert motiv"
}
],
publishStatus: "published",
publishLevel: "limited",
childArtifacts: [
{
count: 0,
sort: 1,
uuid: "C4409CBB-D618-411D-9734-1A1CFC0B0DE4",
sourceId: "874515",
published: false,
dimuCode: "021066019698",
artifactType: "Artdesign",
identifier: "NG.M.00467.R",
description: "Ramme"
}
],
artifactType: "Fineart",
identifier: {
owner: "NMK-B",
id: "NG.M.00467"
},
unique_id: "011042436982"
}
```

