## Use Case: Finding Audience Segments

#### The Segment Reference Product allows you to search the thousands of audiences Geopath offers that can be used in the other inventory search endpoints.

#### There are currently 3 endpoints within the Segement Reference Endpoint. A GET endpoint to search the entire catalog, A POST endpoint to provide a list of segment IDs and get information about them, and a GET endpoint to get information about a single segment ID.

#### The catalog search endpoint has many possible parameters to filter down possible results. This [document](http://api-docs.geopath.org/content/audience-demographics-behaviors-and-consumer-profile-segmentation) provides an overview of the hierarchy of audience sements

###### Call:
_This call provides all endpoints that include the term '25-54'. The text search parameter "q=" works best when using a single string with no spaces._

``` https://api.geopath.org/v2.1/segments/catalog?q=25-54```

###### Response:
_The response includes a total of 96 segments over 3 sources. It breaks down the result by Source, Category, Sub Categories, and Segments. The response has been truncated for space_

```json
{
    "sources": [
        {
            "id": 1,
            "name": "Claritas",
            "version": "2018",
            "description": "Claritas segments",
            "categories": [
                {
                    "id": 5,
                    "name": "Hispanicity",
                    "description": "Hispanicity",
                    "subcategories": [
                        {
                            "id": 39,
                            "name": "Coming Soon",
                            "description": "Coming Soon",
                            "segments": [
                                {
                                    "id": 5126,
                                    "id_ads": null,
                                    "id_v1": null,
                                    "available_search": false,
                                    "available_calc": false,
                                    "name": "Hispanicity/Life Stage Segment: Bi-Cultural Hispanic Workforce. Hispanic population between the ages of 25-54 and categorized as HA3",
                                    "description": "Hispanicity/Life Stage Segment: Bi-Cultural Hispanic Workforce. Hispanic population between the ages of 25-54 and categorized as HA3",
                                    "source_id": 1,
                                    "source_name": "Claritas",
                                    "version": "2018",
                                    "category_id": 5,
                                    "category_name": "Hispanicity",
                                    "subcategory_id": 39,
                                    "subcategory_name": "Coming Soon"
                                },
                                etc...
}
                            ]
                        }
                    ]
                }
            ]
        },
        {
            "id": 2,
            "name": "Claritas_geopath",
            "version": "2018",
            "description": "Claritas segments customized by Geopath",
            "categories": [
                {
                    "id": 3,
                    "name": "PopFacts",
                    "description": "PopFacts",
                    "subcategories": [
                        {
                            "id": 22,
                            "name": "Population",
                            "description": "Population",
                            "segments": [
                                {
                                    "id": 2023,
                                    "id_ads": null,
                                    "id_v1": null,
                                    "available_search": true,
                                    "available_calc": false,
                                    "name": "Hispanic Persons 25-54 yrs (depreciated)",
                                    "description": "Hispanic Persons 25-54 yrs (depreciated for segment 8374)",
                                    "source_id": 2,
                                    "source_name": "Claritas_geopath",
                                    "version": "2018",
                                    "category_id": 3,
                                    "category_name": "PopFacts",
                                    "subcategory_id": 22,
                                    "subcategory_name": "Population"
                                },
                                etc...

                            ]
                        }
                    ]
                }
            ]
        },
        {
            "id": 3,
            "name": "Claritas_Geopath",
            "version": "2019",
            "description": "Claritas segments customized by Geopath",
            "categories": [
                {
                    "id": 6,
                    "name": "PopFacts",
                    "description": "PopFacts",
                    "subcategories": [
                        {
                            "id": 98,
                            "name": "Combined Demographics",
                            "description": "Standard Segments by Age, HH Income, Ethnicity, Race, Gender",
                            "segments": [
                                {
                                    "id": 8530,
                                    "id_ads": "cdae2f39-1c2b-4426-b006-f90216b2ded5",
                                    "id_v1": null,
                                    "available_search": true,
                                    "available_calc": false,
                                    "name": "Females 25-54 yrs HHI $150k+",
                                    "description": "Females 25-54 yrs HHI $150k+",
                                    "source_id": 3,
                                    "source_name": "Claritas_Geopath",
                                    "version": "2019",
                                    "category_id": 6,
                                    "category_name": "PopFacts",
                                    "subcategory_id": 98,
                                    "subcategory_name": "Combined Demographics"
                                },
                                etc...
]
                        }
                    ]
                }
            ]
        }
    ],
    "pagination": {
        "page": 1,
        "page_size": 100,
        "number_of_pages": 1,
        "next_page": null
    }
}
```
