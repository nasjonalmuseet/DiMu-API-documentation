# Using the DigitaltMuseum API
An overview of methods to query the DigitaltMuseum API. This description in created with a specific aim to facilitate querying Nasjonalmuseet's collection in DiMu, but can in principle be used to query any other collection or across all collections in DiMu.

The DigitaltMuseum API is provided by [KulturIT](http://www.kulturit.no). 
Their API documentation (in Norwegian) can be found at http://api.dimu.org/doc/public_api.html.
DigitaltMuseum contains more than 3,800,000 heritage objects from [Norway](http://www.digitaltmuseum.no) (1,8 mill. objects from 174 museums) and [Sweden](http://www.digitaltmuseum.se) (2 mill. objects from 51 museums) (14.09.2016).
Nasjonalmuseet currently has 36,000 objects available in DigitaltMuseum.

<h2>Museums and collections</h2>

An XML overview of museums or collections per country can be found like this:

`/api/owners?country=no&api.key=demo`
`/api/owners?country=se&api.key=demo`

The term `owner` here corresponds to museum or collection. Each owner has an element `identifier` which is used to limit an API search.

i API’et tilsvarer museum/samling og skal brukes for å avgrense søk. Heretter brukes owner istedet for museum/samling. Hver owner i XML har et element <identifier>, som skal brukes for å avgrense søk i indeks. Owner’s strukturen er flat, men owner’s som ligger under andre owners i hierarkiet inneholder et <parent>, som peker til overordnet owner.

Alle søk skal begrenses på en eller flere owner’s.
