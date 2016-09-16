# Using the DigitaltMuseum API
An overview of methods to query the DigitaltMuseum (DiMu) API. This description in created with a specific aim to facilitate querying Nasjonalmuseet's collection in DiMu, but can in principle be used to query any other collection or across all collections in DiMu.

The DiMu API is provided by [KulturIT](http://www.kulturit.no). 
Their API documentation (in Norwegian) can be found at http://api.dimu.org/doc/public_api.html.
DigitaltMuseum contains more than 3,800,000 heritage objects from [Norway](http://www.digitaltmuseum.no) (1,8 mill. objects from 174 museums) and [Sweden](http://www.digitaltmuseum.se) (2 mill. objects from 51 museums) (14.09.2016).
Nasjonalmuseet currently has 36,000 objects available in DigitaltMuseum.

<h2>DiMu museums and collections</h2>

An XML overview of museums or collections per country can be found like this:

``` 
/api/owners?country=no&api.key=demo
/api/owners?country=se&api.key=demo
```

The term `owner` here corresponds to a museum or collection. Each owner has an element `identifier` which is used to limit an API search.
The `owner` structure is flat, but owners that are children of other owners in the hiearchy have a `parent` element. Calls to the API should always be limited to one or more owners unless you specifically need to query the entire index.

<h2>Querying DiMu Solr index</h2>

Queries to the DiMu Solr index supports most common parameters, including paging, sorting and to a certain extent faceting.

Fields:

Det finnes endel felter i solr indeksen, som er søkbare. Noen av feltene er lagret og ikke kjørt igjennom noen tokenizer og noen felter som er kjørt igjennom tokenizers, etc og er ikke lagret, men søkbare. Typiske eksempler på felter, som er lagret er .ingress. feltene. De blir brukt til å vise informasjon i søkeresultatet. Det finnes flere lagrede felter, som ikke har vært endel av ingress, og ikke heter .ingress., men som kan brukes.
