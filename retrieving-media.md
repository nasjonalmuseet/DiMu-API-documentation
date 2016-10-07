<h2>Retrieving pictures from the DiMu media servers</h2>
Pictures of each object can be retrieved by using the media identifier from either the Solr result
``` Javascript
artifact.defaultMediaIdentifier: "012wWWHgNJLA"
```

or from the detail view (media=>pittures=>identfier)
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
