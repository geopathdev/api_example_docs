## Use Case: Access details about a specific piece of inventory

#### There are several methods to access details about a specific piece of inventory. These first two examples read directly into the Geopath Inventory Database and return results that are always up to date. These calls will return information about inventory that is inactive or decomissioned if specificly given ids for it. 
##### 1. Using the `/inventory/{frame_id}` endpoint to return information about a single frame record and it's children
###### Call
_This is a GET call where you specify a frame id in the url_
`https://api.geopath.org/v2.1/inventory/spot/30649897`
###### Response:
_The response only includes information about the Frame and any child spots. This example is a Digital Bulletin that includes 8 spots._
```json
{
    "id": 30649897,
    "plant_frame_id": "004113-A",
    "illumination_start_time": "00:00:00",
    "illumination_end_time": "23:59:59",
    "max_height": 125,
    "max_width": 432,
    "max_pixel_height": null,
    "max_pixel_width": null,
    "construction_date": "2013-04-16T14:11:00.000Z",
    "description": null,
    "full_motion": false,
    "partial_motion": false,
    "rotating": true,
    "interactive": false,
    "audio": false,
    "digital": true,
    "media_name": "Digital Bulletins",
    "notes": null,
    "current_ind": true,
    "created_dtm": "2013-04-16T14:11:00.000Z",
    "updated_dtm": "2020-03-24T20:37:19.174Z",
    "updated_desc": "assignment VAI scores recalculated due to attribute change",
    "classification_type": {
        "id": 1,
        "name": "Roadside",
        "description": "Stationary outdoor inventory where audience move by those locations on a trip to a destination. Roadside audiences are persons within moving vehicles on roadways or persons traveling on pedestrian walkways.",
        "updated_desc": null
    },
    "construction": {
        "id": 30649897,
        "name": "(  28.540660, -81.378851)",
        "description": null,
        "created_dtm": "2013-04-16T14:11:00.000Z",
        "updated_dtm": "2020-03-24T20:37:19.174Z",
        "updated_desc": null,
        "construction_type": {
            "id": 1,
            "name": "Freestanding",
            "description": "freestanding structure taller than 10 feet tall",
            "updated_desc": null
        },
        "representations": [
            {
                "id": 46,
                "updated_desc": null,
                "representation_type": {
                    "id": 1,
                    "name": "Own",
                    "description": "the owner or leaseholder of an asset who may also manage that asset",
                    "updated_desc": null
                },
                "account": {
                    "id": 353,
                    "name": "Orlando",
                    "operator_code": "017",
                    "parent_account_id": 1,
                    "parent_account_name": "Clear Channel",
                    "updated_desc": null
                }
            }
        ],
        "location": {
            "id": 30735523,
            "orientation": 302,
            "primary_read": "R",
            "primary_artery": "S ORANGE AVE",
            "level": null,
            "levels_visible": null,
            "latitude": 28.540679,
            "longitude": -81.378889,
            "block_id": "120950189005061",
            "elevation": null,
            "geometry": {
                "type": "Point",
                "coordinates": [
                    -81.378889,
                    28.540679
                ]
            },
            "place_type": {
                "id": 532,
                "name": "Central Business District",
                "description": "The main business and commercial area of a town or city.",
                "updated_desc": null
            },
            "created_dtm": "2013-04-16T14:11:00.000Z",
            "updated_dtm": "2020-03-24T20:28:39.499Z",
            "dma_id": "534",
            "zip_code": "32801",
            "county_name": null,
            "state": null,
            "time_zone": "-5"
        },
        "operating_hours": []
    },
    "illumination_type": {
        "id": 3,
        "name": "Backlit",
        "description": "Surface illuminated from the back by non-ambient source",
        "updated_desc": null
    },
    "location": {
        "id": 30735523,
        "orientation": 302,
        "primary_read": "R",
        "primary_artery": "S ORANGE AVE",
        "level": null,
        "levels_visible": null,
        "latitude": 28.540679,
        "longitude": -81.378889,
        "block_id": "120950189005061",
        "elevation": null,
        "geometry": {
            "type": "Point",
            "coordinates": [
                -81.378889,
                28.540679
            ]
        },
        "place_type": {
            "id": 532,
            "name": "Central Business District",
            "description": "The main business and commercial area of a town or city.",
            "updated_desc": null
        },
        "created_dtm": "2013-04-16T14:11:00.000Z",
        "updated_dtm": "2020-03-24T20:28:39.499Z",
        "dma_id": "534",
        "zip_code": "32801",
        "county_name": "Orange County",
        "state": "FL",
        "time_zone": "-5"
    },
    "media_type": {
        "id": 2,
        "name": "Bulletin",
        "description": "extra large-sized standard products (approx. 10-20' H x 36-60' W)",
        "updated_desc": null
    },
    "placement_type": {
        "id": 538,
        "name": "Set Back",
        "description": "Frame located in a way that it can be seen by pedestrians on the same side of the street",
        "updated_desc": null
    },
    "status_type": {
        "id": 52,
        "name": "Published - Under Review",
        "description": "Measures created, but under review; inventory and measures available to licensed users"
    },
    "representations": [
        {
            "id": 46,
            "updated_desc": null,
            "representation_type": {
                "id": 1,
                "name": "Own",
                "description": "the owner or leaseholder of an asset who may also manage that asset",
                "updated_desc": null
            },
            "account": {
                "id": 353,
                "name": "Orlando",
                "operator_code": "017",
                "parent_account_id": 1,
                "parent_account_name": "Clear Channel",
                "updated_desc": null
            }
        }
    ],
    "layouts": [
        {
            "id": 30649897,
            "uri": null,
            "full_motion": false,
            "partial_motion": false,
            "rotating": false,
            "interactive": false,
            "audio": false,
            "share_of_voice": 1.0,
            "updated_desc": null,
            "representations": [
                {
                    "id": 46,
                    "updated_desc": null,
                    "representation_type": {
                        "id": 1,
                        "name": "Own",
                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                        "updated_desc": null
                    },
                    "account": {
                        "id": 353,
                        "name": "Orlando",
                        "operator_code": "017",
                        "parent_account_id": 1,
                        "parent_account_name": "Clear Channel",
                        "updated_desc": null
                    }
                }
            ],
            "faces": [
                {
                    "id": 30649897,
                    "uri": null,
                    "average_spot_length": 15,
                    "publisher_unique_face_id": null,
                    "height": 125,
                    "width": 432,
                    "pixel_height": null,
                    "pixel_width": null,
                    "top_left_pixel_x": null,
                    "top_left_pixel_y": null,
                    "spots_in_rotation": 8,
                    "updated_desc": null,
                    "representations": [
                        {
                            "id": 46,
                            "updated_desc": null,
                            "representation_type": {
                                "id": 1,
                                "name": "Own",
                                "description": "the owner or leaseholder of an asset who may also manage that asset",
                                "updated_desc": null
                            },
                            "account": {
                                "id": 353,
                                "name": "Orlando",
                                "operator_code": "017",
                                "parent_account_id": 1,
                                "parent_account_name": "Clear Channel",
                                "updated_desc": null
                            }
                        }
                    ],
                    "spots": [
                        {
                            "id": 30699542,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-E",
                            "created_dtm": "2014-04-08T00:00:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:19.174Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": null,
                            "total_msg_impressions": null
                        },
                        {
                            "id": 30699541,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-D",
                            "created_dtm": "2014-04-08T00:00:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:19.174Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": {
                                "measures_type": "Measures",
                                "period_days": 7,
                                "base_segment": "2032",
                                "target_segment": "2032",
                                "target_geo": "Defaulted to GLOBAL",
                                "market": "Defaulted to GLOBAL",
                                "index_comp_target": 100.0,
                                "pct_comp_pop_target_inmkt": 1.0,
                                "pct_comp_imp_target": 1.0,
                                "pct_comp_imp_target_inmkt": 1.0,
                                "freq_avg": 4.471983143,
                                "imp_target_inmkt": 81964.71998083,
                                "imp_target": 81964.71998083,
                                "imp_inmkt": 81964.71998083,
                                "imp": 81964.71998083,
                                "pct_imp_inmkt": 1.0,
                                "pct_imp_target_inmkt": 1.0,
                                "pop_inmkt": 329236175,
                                "pop_target_inmkt": 329236175,
                                "reach_pct": 0.005566974785,
                                "reach_net": 18328,
                                "trp": 0.02489541739,
                                "eff_freq_min": 3,
                                "eff_freq_avg": 5.498528624,
                                "eff_reach_net": 14907,
                                "eff_reach_pct": 0.004527650776
                            },
                            "total_msg_impressions": null
                        },
                        {
                            "id": 30699539,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-B",
                            "created_dtm": "2014-04-08T00:00:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:19.174Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": null,
                            "total_msg_impressions": null
                        },
                        {
                            "id": 30699544,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-G",
                            "created_dtm": "2014-04-08T00:00:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:19.174Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": null,
                            "total_msg_impressions": null
                        },
                        {
                            "id": 30699543,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-F",
                            "created_dtm": "2013-04-16T14:11:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:15.267Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": null,
                            "total_msg_impressions": null
                        },
                        {
                            "id": 30699540,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-C",
                            "created_dtm": "2014-04-08T00:00:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:19.174Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": null,
                            "total_msg_impressions": null
                        },
                        {
                            "id": 30649897,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-A",
                            "created_dtm": "2014-04-08T00:00:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:19.174Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": null,
                            "total_msg_impressions": null
                        },
                        {
                            "id": 30699545,
                            "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                            "publisher_unique_id": null,
                            "length": 15,
                            "full_motion": false,
                            "partial_motion": false,
                            "rotating": false,
                            "interactive": false,
                            "audio": false,
                            "share_of_voice": 0.125,
                            "plant_spot_id": "004113-H",
                            "created_dtm": "2014-04-08T00:00:00.000Z",
                            "updated_dtm": "2020-03-24T20:37:19.174Z",
                            "updated_desc": null,
                            "representations": [
                                {
                                    "id": 46,
                                    "updated_desc": null,
                                    "representation_type": {
                                        "id": 1,
                                        "name": "Own",
                                        "description": "the owner or leaseholder of an asset who may also manage that asset",
                                        "updated_desc": null
                                    },
                                    "account": {
                                        "id": 353,
                                        "name": "Orlando",
                                        "operator_code": "017",
                                        "parent_account_id": 1,
                                        "parent_account_name": "Clear Channel",
                                        "updated_desc": null
                                    }
                                }
                            ],
                            "measures": null,
                            "total_msg_impressions": null
                        }
                    ]
                }
            ]
        }
    ],
    "photos": []
}
```
##### 2. Using the `/inventory/spot/{spot_id}` endpoint to return only information about the spot
###### Call:
_This is a GET call where you specify a spot id in the url_
`https://api.geopath.org/v2.1/inventory/spot/30649897`
###### Response:
_The response only includes information about the SPOT. It includes a link to the the FRAME record as the frame_uri key_
```json
{
    "id": 30649897,
    "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
    "publisher_unique_id": null,
    "length": 15,
    "full_motion": false,
    "partial_motion": false,
    "rotating": false,
    "interactive": false,
    "audio": false,
    "share_of_voice": 0.125,
    "plant_spot_id": "004113-A",
    "created_dtm": "2014-04-08T00:00:00.000Z",
    "updated_dtm": "2020-03-24T20:37:19.174Z",
    "updated_desc": null,
    "representations": [
        {
            "id": 46,
            "updated_desc": null,
            "representation_type": {
                "id": 1,
                "name": "Own",
                "description": "the owner or leaseholder of an asset who may also manage that asset",
                "updated_desc": null
            },
            "account": {
                "id": 353,
                "name": "Orlando",
                "operator_code": "017",
                "parent_account_id": 1,
                "parent_account_name": "Clear Channel",
                "updated_desc": null
            }
        }
    ],
    "measures": {
        "measures_type": "Measures",
        "period_days": 7,
        "base_segment": "2032",
        "target_segment": "2032",
        "target_geo": "Defaulted to GLOBAL",
        "market": "Defaulted to GLOBAL",
        "index_comp_target": 100.0,
        "pct_comp_pop_target_inmkt": 1.0,
        "pct_comp_imp_target": 1.0,
        "pct_comp_imp_target_inmkt": 1.0,
        "freq_avg": 4.471983143,
        "imp_target_inmkt": 81964.71998083,
        "imp_target": 81964.71998083,
        "imp_inmkt": 81964.71998083,
        "imp": 81964.71998083,
        "pct_imp_inmkt": 1.0,
        "pct_imp_target_inmkt": 1.0,
        "pop_inmkt": 329236175,
        "pop_target_inmkt": 329236175,
        "reach_pct": 0.005566974785,
        "reach_net": 18328,
        "trp": 0.02489541739,
        "eff_freq_min": 3,
        "eff_freq_avg": 5.498528624,
        "eff_reach_net": 14907,
        "eff_reach_pct": 0.004527650776
    },
    "total_msg_impressions": null
}
```
#### These next example utilize the POST search endpoints are reference a static table that is updated on a weekly basis when impressions are updated. These searches do not return inventory that is inactive or decomissioned even if explicitly asked for those frames
##### 3. Using the ```inventory/search``` endpoint to post a list of one inventory id
###### Call:
_This call specifies a frame_id_
```json
{
    "id_type": "frame_id",
    "id_list": [
        "30649897"
    ]
}
```
###### Response:
_The response includes all 8 of the child spots, and is the same as the GET frame call_
```json
{
    "inventory_summary": {
        "inventory_count": 8,
        "invalid_ids": null,
        "filtered_invalid_ids": null,
        "inventory_items": [
            {
                "frame_id": 30649897,
                "plant_frame_id": "004113-A",
                "uri": null,
                "max_height": 125,
                "max_width": 432,
                "digital": true,
                "media_name": "Digital Bulletins",
                "frame_rotating": true,
                "illumination_start_time": "00:00:00",
                "illumination_end_time": "23:59:59",
                "created_dtm": "2013-04-16T14:11:00.000Z",
                "updated_dtm": "2020-03-24T20:37:19.174Z",
                "representations": [
                    {
                        "id": 46,
                        "updated_desc": null,
                        "representation_type": {
                            "id": 1,
                            "name": "Own",
                            "description": "the owner or leaseholder of an asset who may also manage that asset",
                            "updated_desc": null
                        },
                        "account": {
                            "id": 353,
                            "name": "Orlando",
                            "operator_code": "017",
                            "parent_account_id": 1,
                            "parent_account_name": "Clear Channel",
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
                    "id": 1,
                    "name": "Freestanding",
                    "description": "freestanding structure taller than 10 feet tall",
                    "updated_desc": null
                },
                "illumination_type": {
                    "id": 3,
                    "name": "Backlit",
                    "description": "Surface illuminated from the back by non-ambient source",
                    "updated_desc": null
                },
                "media_type": {
                    "id": 2,
                    "name": "Bulletin",
                    "description": "extra large-sized standard products (approx. 10-20' H x 36-60' W)",
                    "updated_desc": null
                },
                "media_status": {
                    "id": 52,
                    "name": "Published - Under Review",
                    "description": "Measures created, but under review; inventory and measures available to licensed users"
                },
                "location": {
                    "id": 30735523,
                    "orientation": 302,
                    "primary_read": "R",
                    "primary_artery": "S ORANGE AVE",
                    "level": null,
                    "levels_visible": null,
                    "latitude": 28.540679,
                    "longitude": -81.378889,
                    "block_id": "120950189005061",
                    "elevation": null,
                    "geometry": {
                        "type": "Point",
                        "coordinates": [
                            -81.378889,
                            28.540679
                        ]
                    },
                    "place_type": {
                        "id": 532,
                        "name": "Central Business District",
                        "description": "The main business and commercial area of a town or city.",
                        "updated_desc": null
                    },
                    "created_dtm": "2013-04-16T14:11:00.000Z",
                    "updated_dtm": "2020-03-24T20:28:39.499Z",
                    "dma_id": "534",
                    "zip_code": "32801",
                    "county_name": "Orange County",
                    "state": "FL",
                    "time_zone": "-5"
                },
                "placement_type": {
                    "id": 538,
                    "name": "Set Back",
                    "description": "Frame located in a way that it can be seen by pedestrians on the same side of the street",
                    "updated_desc": null
                },
                "spot_references": [
                    {
                        "spot_id": 30699542,
                        "plant_spot_id": "004113-E",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699540,
                        "plant_spot_id": "004113-C",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699544,
                        "plant_spot_id": "004113-G",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699545,
                        "plant_spot_id": "004113-H",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699543,
                        "plant_spot_id": "004113-F",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2013-04-16T14:11:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:15.267Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699539,
                        "plant_spot_id": "004113-B",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30649897,
                        "plant_spot_id": "004113-A",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699541,
                        "plant_spot_id": "004113-D",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    }
                ]
            }
        ],
        "pagination": {
            "page": 1,
            "page_size": 100,
            "number_of_pages": 1,
            "number_of_frames": 1,
            "number_of_spots": 1
        }
    }
}
```

###### Call:
_This call specifies a spot_id_
```json
{
    "id_type": "spot_id",
    "id_list": [
        "30649897"
    ]
}
```
###### Response:
_The response only includes detail for that single spot, but includes all the information about the parent frame_
```json
{
    "inventory_summary": {
        "inventory_count": 1,
        "invalid_ids": null,
        "filtered_invalid_ids": null,
        "inventory_items": [
            {
                "frame_id": 30649897,
                "plant_frame_id": "004113-A",
                "uri": null,
                "max_height": 125,
                "max_width": 432,
                "digital": true,
                "media_name": "Digital Bulletins",
                "frame_rotating": true,
                "illumination_start_time": "00:00:00",
                "illumination_end_time": "23:59:59",
                "created_dtm": "2013-04-16T14:11:00.000Z",
                "updated_dtm": "2020-03-24T20:37:19.174Z",
                "representations": [
                    {
                        "id": 46,
                        "updated_desc": null,
                        "representation_type": {
                            "id": 1,
                            "name": "Own",
                            "description": "the owner or leaseholder of an asset who may also manage that asset",
                            "updated_desc": null
                        },
                        "account": {
                            "id": 353,
                            "name": "Orlando",
                            "operator_code": "017",
                            "parent_account_id": 1,
                            "parent_account_name": "Clear Channel",
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
                    "id": 1,
                    "name": "Freestanding",
                    "description": "freestanding structure taller than 10 feet tall",
                    "updated_desc": null
                },
                "illumination_type": {
                    "id": 3,
                    "name": "Backlit",
                    "description": "Surface illuminated from the back by non-ambient source",
                    "updated_desc": null
                },
                "media_type": {
                    "id": 2,
                    "name": "Bulletin",
                    "description": "extra large-sized standard products (approx. 10-20' H x 36-60' W)",
                    "updated_desc": null
                },
                "media_status": {
                    "id": 52,
                    "name": "Published - Under Review",
                    "description": "Measures created, but under review; inventory and measures available to licensed users"
                },
                "location": {
                    "id": 30735523,
                    "orientation": 302,
                    "primary_read": "R",
                    "primary_artery": "S ORANGE AVE",
                    "level": null,
                    "levels_visible": null,
                    "latitude": 28.540679,
                    "longitude": -81.378889,
                    "block_id": "120950189005061",
                    "elevation": null,
                    "geometry": {
                        "type": "Point",
                        "coordinates": [
                            -81.378889,
                            28.540679
                        ]
                    },
                    "place_type": {
                        "id": 532,
                        "name": "Central Business District",
                        "description": "The main business and commercial area of a town or city.",
                        "updated_desc": null
                    },
                    "created_dtm": "2013-04-16T14:11:00.000Z",
                    "updated_dtm": "2020-03-24T20:28:39.499Z",
                    "dma_id": "534",
                    "zip_code": "32801",
                    "county_name": "Orange County",
                    "state": "FL",
                    "time_zone": "-5"
                },
                "placement_type": {
                    "id": 538,
                    "name": "Set Back",
                    "description": "Frame located in a way that it can be seen by pedestrians on the same side of the street",
                    "updated_desc": null
                },
                "spot_references": [
                    {
                        "spot_id": 30649897,
                        "plant_spot_id": "004113-A",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    }
                ]
            }
        ],
        "pagination": {
            "page": 1,
            "page_size": 100,
            "number_of_pages": 1,
            "number_of_frames": 1,
            "number_of_spots": 1
        }
    }
}
```
###### Call:
_This call specifies a plant_frame_id and an operator. This is not required, but since operators may use identical identifiers it helps to be as specific as possible. Including an inventory_market_list may also be warranted since some operators re-use identifiers across regions._
```json
{
    "operator_name_list": [
        "Clear Channel"
    ],
    "id_type": "plant_frame_id",
    "id_list": [
        "004113-A"
    ]
}
```
###### Response:
_This response is identical to the GET frame and Search by frame_id response and included data on the 8 child spots. 
```json
{
    "inventory_summary": {
        "inventory_count": 8,
        "invalid_ids": null,
        "filtered_invalid_ids": null,
        "inventory_items": [
            {
                "frame_id": 30649897,
                "plant_frame_id": "004113-A",
                "uri": null,
                "max_height": 125,
                "max_width": 432,
                "digital": true,
                "media_name": "Digital Bulletins",
                "frame_rotating": true,
                "illumination_start_time": "00:00:00",
                "illumination_end_time": "23:59:59",
                "created_dtm": "2013-04-16T14:11:00.000Z",
                "updated_dtm": "2020-03-24T20:37:19.174Z",
                "representations": [
                    {
                        "id": 46,
                        "updated_desc": null,
                        "representation_type": {
                            "id": 1,
                            "name": "Own",
                            "description": "the owner or leaseholder of an asset who may also manage that asset",
                            "updated_desc": null
                        },
                        "account": {
                            "id": 353,
                            "name": "Orlando",
                            "operator_code": "017",
                            "parent_account_id": 1,
                            "parent_account_name": "Clear Channel",
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
                    "id": 1,
                    "name": "Freestanding",
                    "description": "freestanding structure taller than 10 feet tall",
                    "updated_desc": null
                },
                "illumination_type": {
                    "id": 3,
                    "name": "Backlit",
                    "description": "Surface illuminated from the back by non-ambient source",
                    "updated_desc": null
                },
                "media_type": {
                    "id": 2,
                    "name": "Bulletin",
                    "description": "extra large-sized standard products (approx. 10-20' H x 36-60' W)",
                    "updated_desc": null
                },
                "media_status": {
                    "id": 52,
                    "name": "Published - Under Review",
                    "description": "Measures created, but under review; inventory and measures available to licensed users"
                },
                "location": {
                    "id": 30735523,
                    "orientation": 302,
                    "primary_read": "R",
                    "primary_artery": "S ORANGE AVE",
                    "level": null,
                    "levels_visible": null,
                    "latitude": 28.540679,
                    "longitude": -81.378889,
                    "block_id": "120950189005061",
                    "elevation": null,
                    "geometry": {
                        "type": "Point",
                        "coordinates": [
                            -81.378889,
                            28.540679
                        ]
                    },
                    "place_type": {
                        "id": 532,
                        "name": "Central Business District",
                        "description": "The main business and commercial area of a town or city.",
                        "updated_desc": null
                    },
                    "created_dtm": "2013-04-16T14:11:00.000Z",
                    "updated_dtm": "2020-03-24T20:28:39.499Z",
                    "dma_id": "534",
                    "zip_code": "32801",
                    "county_name": "Orange County",
                    "state": "FL",
                    "time_zone": "-5"
                },
                "placement_type": {
                    "id": 538,
                    "name": "Set Back",
                    "description": "Frame located in a way that it can be seen by pedestrians on the same side of the street",
                    "updated_desc": null
                },
                "spot_references": [
                    {
                        "spot_id": 30649897,
                        "plant_spot_id": "004113-A",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699543,
                        "plant_spot_id": "004113-F",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2013-04-16T14:11:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:15.267Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699544,
                        "plant_spot_id": "004113-G",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699539,
                        "plant_spot_id": "004113-B",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699541,
                        "plant_spot_id": "004113-D",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699540,
                        "plant_spot_id": "004113-C",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699542,
                        "plant_spot_id": "004113-E",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    },
                    {
                        "spot_id": 30699545,
                        "plant_spot_id": "004113-H",
                        "frame_uri": "{{api.basepath}}/v2.1/inventory/30649897",
                        "length": 15,
                        "spot_rotating": false,
                        "created_dtm": "2014-04-08T00:00:00.000Z",
                        "updated_dtm": "2020-03-24T20:37:19.174Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 4.471983143,
                            "imp_target_inmkt": 81964.71998083,
                            "imp_target": 81964.71998083,
                            "imp_inmkt": 81964.71998083,
                            "imp": 81964.71998083,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 329236175,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.005566974785,
                            "reach_net": 18328,
                            "trp": 0.02489541739,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.498528624,
                            "eff_reach_net": 14907,
                            "eff_reach_pct": 0.004527650776
                        }
                    }
                ]
            }
        ],
        "pagination": {
            "page": 1,
            "page_size": 100,
            "number_of_pages": 1,
            "number_of_frames": 1,
            "number_of_spots": 1
        }
    }
}
```