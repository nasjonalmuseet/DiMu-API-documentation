<h2>Retrieving pictures from the DiMu media servers</h2>
Pictures of each object can be retrieved by using the media identifier from either the Solr response

``` Javascript
artifact.defaultMediaIdentifier: "032wXVwUzT6J"
```

or from the detail view (media->pictures->identifier)

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

Use the mediaservers at `dms01.dimu.org`, e.g.

http://dms01.dimu.org/image/032wXVwUz7v2?dimension=250x250

The identifier key should be followed by a `dimension`parameter. Possible values for dimension are:
- max (full resolution, up to 4000px for the newest pictures
- 1200x1200
- 800x800
- 600x600
- 400x400
- 250x250

*<b>Note 1</b>: The prefixed subdomain of the media server, `dms01`, can be varied like dms02, dms03 ... up to dms09.*

*<b>Note 2</b>: A faster cached image index can be accessed by using a `fdms` prefix, e.g. `fdms01.dimu.org`. This should only be used after prior agreement with KulturIT.*

*<b>Note 3</b>: The images are in JPEG format, but served without .jpg suffix by default.
A custom filename can be specified by adding a `filename` parameter to the url, e.g.
`http://dms01.dimu.org/image/032wXVwUz7v2?dimension=250x250&filename=myFile.jpg`.
The `dms01.dimu.org` servers are not CORS enabled. 
The `fdms01.dimu.org` servers should be CORS enabled, but haven't been tested extensively.*


