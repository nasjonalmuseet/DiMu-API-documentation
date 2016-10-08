<h2>Collection object detailed view</h2>
http://api.dimu.org/artifact/uuid/3DF10C96-B33B-45C1-92BF-D9211CE574C8

The url above will return a JSON representation of the object. Below are comments on central parts of the metadata returned.
<h3>Titles</h3>
Titles are sometimes specificed with a language attribute. If none is present it is assumed that the title is in Norwegian.
``` Javascript
titles: [
  {
    status: "anvendt",
    language: "NOR",
    title: "Nature morte"
  },
  {
    status: "anvendt",
    language: "ENG",
    title: "Still life"
  },
  {
    status: "anvendt",
    language: "FRA",
    title: "Nature morte: pot à lait et fruits sur une table"
  },
  {
    status: "anvendt",
    language: "DEU",
    title: "Stilleben mit Milchkrug und Früchten auf einem Tisch"
  }
]
```

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
[Retrieving pictures from the DiMu media servers](retrieving-media.md).
<h3>Technique</h3>
``` Javascript
technique: {
techniques: [
{
sort: 1,
technique: "Olje"
}
]
}
```
<h3>Production</h3>
Some producers (persons) have a more detailed level of information, such as time and place of birth and death, sometimes with geocoordinates, as well as [VIAF](https://viaf.org/) identifier and link, which can for instanced be utilised to retrieve biographical information from VIAF, Wikipedia, Wikidata etc.
``` Javascript
producers: [
    {
      info: {
      references: [
        {
          url: "http://viaf.org/viaf/39374836",
          type: "VIAF",
          description: "permalink ",
          reference: "ID: 39374836"
        }
        ],
      places: [
        {
        coordinate: "43.529742, 5.4474270000000615",
        fields: [
        {
        sort: 1,
        number: 1,
        value: "Frankrike",
        name: "Land"
        },
        {
        sort: 5,
        number: 4,
        value: "Aix-en-Provence, Provence",
        name: "Områdepres"
        }
        ],
        role: {
        name: "Fødested, "
        },
        uuid: "6A851865-036D-45C3-80A0-46698E966C79"
        },
        {
        coordinate: "43.529742, 5.4474270000000615",
        fields: [
        {
        sort: 1,
        number: 1,
        value: "Frankrike",
        name: "Land"
        },
        {
        sort: 5,
        number: 4,
        value: "Aix-en-Provence, Provence",
        name: "Områdepres"
        }
        ],
        role: {
        name: "Dødssted, "
        },
        uuid: "6A851865-036D-45C3-80A0-46698E966C79"
        }
      ],
      nationality: "Frankrike",
      gender: "Mann",
      professions: [ ],
      alternativeNames: [ ]
      },
      role: {
      code: "10K",
      name: "Kunstner"
      },
      uuid: "B8AE304B-81C4-49F6-8EEA-DF6192AA4EBA",
      name: "Cézanne, Paul",
      type: "Person",
      id: 18981,
      publishLevel: "extended"
    }
]
