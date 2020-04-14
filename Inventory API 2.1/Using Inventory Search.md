## Using the ```inventory/search``` endpoint

#### This endpoint is a powerful tool to identify OOH inventory that match a wide variety of criteria.

##### Use Case: Get the top 100 frames for a specific operator and audience
###### Call:
_This call is asking for the top 100 spots (by percent composition of the target as part of the overall impressions) for 18+ for a specific operator_
```json
{
    "base_segment": 2032,
    "target_segment": 7166,
    "operator_name_list": [
        "Intersection"
    ],
    "sort": {
        "measure": "pct_comp_imp_target",
        "type": "desc"
    },
    "measures_range_list": [
        {
            "type": "imp",
            "min": 0
        }
    ],
    "page_size": 100
}
```
###### Response:
_The Response includes all inventory attributes for each **spot** at the end of the page there is a pagination object that details how many pages of responses there are to the query_
```json
{
    "inventory_summary": {
        "inventory_count": 100,
        "invalid_ids": null,
        "filtered_invalid_ids": null,
        "inventory_items": [
            {
                "frame_id": 30575310,
                "plant_frame_id": "010551L",
                "uri": null,
                "max_height": 50,
                "max_width": 26,
                "digital": false,
                "media_name": "Phone Kiosks",
                "frame_rotating": false,
                "illumination_start_time": "06:00:00",
                "illumination_end_time": "17:59:59",
                "created_dtm": "2011-11-02T11:27:00.000Z",
                "updated_dtm": "2019-11-21T02:43:55.031Z",
                "representations": [
                    {
                        "id": 307,
                        "updated_desc": null,
                        "representation_type": {
                            "id": 1,
                            "name": "Own",
                            "description": "the owner or leaseholder of an asset who may also manage that asset",
                            "updated_desc": null
                        },
                        "account": {
                            "id": 658,
                            "name": "New York",
                            "operator_code": "TIT",
                            "parent_account_id": 67,
                            "parent_account_name": "Intersection",
                            "updated_desc": null
                        }
                    }
                ],
                "classification_type": {
                    "id": 1,
                    "name": "Roadside",
                    "description": "Stationary outdoor inventory where audience move by those locations on a trip to a destination. Roadside audiences are persons within moving vehicles on roadways or persons traveling on pedestrian walkways.",
                    "updated_desc": null
                },
                "construction_type": {
                    "id": 4,
                    "name": "Furniture",
                    "description": "freestanding structure less than 10 feet tall",
                    "updated_desc": null
                },
                "illumination_type": {
                    "id": 1,
                    "name": "Sunlit Ambient",
                    "description": "Surface illuminated by ambient natural sunlight",
                    "updated_desc": null
                },
                "media_type": {
                    "id": 5,
                    "name": "Panel",
                    "description": "small-sized products (approx. 35\"H x 63\" W - 5-6' H x 11-13' W)",
                    "updated_desc": null
                },
                "media_status": {
                    "id": 51,
                    "name": "Published - Measured",
                    "description": "Measures created; inventory and measures available to licensed users"
                },
                "location": {
                    "id": 30588255,
                    "orientation": 180,
                    "primary_read": "R",
                    "primary_artery": "9th Ave.",
                    "level": null,
                    "levels_visible": null,
                    "latitude": 40.761571,
                    "longitude": -73.990253,
                    "block_id": "360610127002001",
                    "elevation": null,
                    "geometry": {
                        "type": "Point",
                        "coordinates": [
                            -73.990253,
                            40.761571
                        ]
                    },
                    "place_type": {
                        "id": 532,
                        "name": "Central Business District",
                        "description": "The main business and commercial area of a town or city.",
                        "updated_desc": null
                    },
                    "created_dtm": "2011-11-02T11:27:00.000Z",
                    "updated_dtm": "2020-02-03T12:20:50.390Z",
                    "dma_id": "501",
                    "zip_code": "10036",
                    "county_name": "New York County",
                    "state": "NY",
                    "time_zone": "-5"
                },
                "placement_type": {
                    "id": 537,
                    "name": "Curbside",
                    "description": "Frame located in a way that it cannot be seen by pedestrians on the same side of the street",
                    "updated_desc": null
                },
                "spot_references": [
                    {
                        "spot_id": 30575310,
                        "plant_spot_id": "010551L",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30575310",
                        "length": null,
                        "spot_rotating": null,
                        "created_dtm": "2011-11-02T11:27:00.000Z",
                        "updated_dtm": null,
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "7166",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 115.974424997,
                            "pct_comp_pop_target_inmkt": 0.775023,
                            "pct_comp_imp_target": 0.8988284678,
                            "pct_comp_imp_target_inmkt": 0.8988284678,
                            "freq_avg": 2.597673459,
                            "imp_target_inmkt": 26752.41727113,
                            "imp_target": 26752.41727113,
                            "imp_inmkt": 29763.651495564,
                            "imp": 29763.651495564,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 255165582,
                            "reach_pct": 0.004036048519,
                            "reach_net": 10299,
                            "trp": 0.01048433612,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.649890249,
                            "eff_reach_net": 4735,
                            "eff_reach_pct": 0.001855670757
                        }
                    }
                ]
            },
etc...
```

###### Response (pagination object at end):
_The pagination object tells which page has been requested and the overall number of pages. The frames and spots are the overall number returned in the initial search and page size lists the maximum number of spots displayed._ 
```json
        "pagination": {
            "page": 1,
            "page_size": 100,
            "number_of_pages": 534,
            "number_of_frames": 29960,
            "number_of_spots": 53359
        }
    }
}
```

##### Use Case: Get inventory that has been updated in the past month.
###### Call:
_This call is specifying an updated_date_range of just dates, but can also include specific times (time in UTC). It is searching across all inventory_ 
```json
{
    "updated_date_range": {
        "start_date": "2020-03-27",
        "end_date": "2020-02-26"
    }
}
```
_or_
```json
{
    "updated_date_range": {
        "start_date": "2020-03-27T12:00:00.000Z",
        "end_date": "2020-02-27T12:00:00.000Z"
    }
}
```
###### Response:
_The search response is a paginated response like the first example_




