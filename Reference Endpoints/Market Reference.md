## Use Case: Finding Markets

#### The Market Reference product allows you to search for defined geographic areas that can be used to filter inventory or limit measures to a single or group of areas. 

##### There are two GET endpoints in the Market Reference product one where you can search for markets, and one where you can get information, including spatial geometry (excluding DMA) about a specific market.

##### In general geopath currently supports 4 different market types: DMA, CBSA, County(abbreviated CNTY) and Zip Codes (ZIP). Using the ```https://api.geopath.org/v2.1/markets/search``` endpoint you can provide a string to search as well as set a type filter.

###### Call:
_This url is formatted with the parameters to search for zip codes that have the string 'NY'_

```https://api.geopath.org/v2.1/markets/search?type=Zip Codes&q=NY```

###### Response:
_The response includes an ID that can be used in other API search products as well as the long format name of the market. A pagination object is also include if the response is longer than 100(max and default page size) items._ 

```json
{
    "markets": [
        {
            "id": "ZIP14716",
            "name": "14716 - Brocton, NY",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP10567",
            "name": "10567 - Cortlandt Manor, NY",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP11225",
            "name": "11225 - Brooklyn, NY",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP12827",
            "name": "12827 - Fort Ann, NY",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP12546",
            "name": "12546 - Millerton, NY",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP14150",
            "name": "14150 - Tonawanda, NY",
            "type": "Zip Codes"
        },
        etc...
    ],
    "pagination": {
        "page": 1,
        "page_size": 100,
        "number_of_pages": 19,
        "next_page": "{{api.basepath}}/v2.1/markets/search?q=NY&type=Zip+Codes&page=2&pageSize=100"
    }
}
```

###### Call:
_This call just asks for markets that include the term 'Santa' without specifying a type_

```https://api.geopath.org/v2.1/markets/search?q=Santa```

###### Response:
_The response includes 84 markets across DMAs, CBSAs, Counties and Zip Codes that contain the word Santa_
```json
{
    "markets": [
        {
            "id": "CNTY06083",
            "name": "Santa Barbara County, CA",
            "type": "County"
        },
        {
            "id": "DMA790",
            "name": "Albuquerque-Santa Fe, NM",
            "type": "DMA"
        },
        {
            "id": "ZIP84655",
            "name": "84655 - Santaquin, UT",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP95065",
            "name": "95065 - Santa Cruz, CA",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP87505",
            "name": "87505 - Santa Fe, NM",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP77517",
            "name": "77517 - Santa Fe, TX",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP77510",
            "name": "77510 - Santa Fe, TX",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP88008",
            "name": "88008 - Santa Teresa, NM",
            "type": "Zip Codes"
        },
        {
            "id": "ZIP93111",
            "name": "93111 - Santa Barbara, CA",
            "type": "Zip Codes"
        },
        {
            "id": "CBSA04218",
            "name": "Santa Isabel, PR",
            "type": "CBSA"
        },
        {
            "id": "CBSA42100",
            "name": "Santa Cruz-Watsonville, CA Metropolitan Statistical Area",
            "type": "CBSA"
        },
        etc...
    ],
    "pagination": {
        "page": 1,
        "page_size": 100,
        "number_of_pages": 1,
        "next_page": null
    }
}
```

##### You can use any combination of searches to find the geographic markets you need for use in the other inventory search endpoints. The other GET endpoint in the Market Reference product is to get details about a specific market code.

###### Call:

```https://api.geopath.org/v2.1/markets/ZIP92091```

###### Response:
_The response includes the name of the market as well as the geometry of the market. This geometry of this response has been truncated. The geometry object could be used inside a seperate GeoJSON object for polygon creation in GIS systems._ 

```json
{
    "_id": null,
    "market": {
        "id": "ZIP92091",
        "name": "92091 - Rancho Santa Fe, CA",
        "type": "Zip Codes",
        "location": null,
        "createdAt": "2017-09-21 18:23:45.676872",
        "updatedAt": "2017-09-21 18:23:45.676872",
        "sourceMarketID": "92091",
        "geometry": {
            "type": "MultiPolygon",
            "coordinates": [
                [
                    [
                        [
                            -117.18712400017245,
                            33.05275399989722
                        ],
                        [
                            -117.18710600024167,
                            33.05281800015064
                        ],
                        [
                            -117.18710100001113,
                            33.05283800017361
                        ],
                        [
                            -117.18706700024181,
                            33.052909999896656
                        ],
                        [
                            -117.18695999980413,
                            33.05307899959621
                        ],
                        etc...
                    ]
                ]
            ]
        },
        "userID": null,
        "companyID": null
    }
```

#####
