## Use Case: Locking down certain plan parameters.

#### When creating a plan sometimes a user will want to lock a certain parameter like number of a media type or TRPs. 

##### This can be accomplished in the ```https://api.geopath.org/v2.1/inventory/plans``` endpoint and using the ```lock``` object to set what you want locked. The lock object can be provided within different objects depending on the lock requirements. A Goal object is always required when using the endpoint, but can be set at 0 for a measure.

###### Call:
_This call locks the total number of Bulletin inventory in a specific market with a TRP goal of 100 over 1 week. Note that locking the number of inventory might make the request fail to reach a set goal._

```json
{
    "target_geography_list": [
        "DMA623"
    ],
    "target_segment": 2032,
    "media_type_group_list": [
        {
            "measures_range_list": [
                {
                    "type": "index_comp_target",
                    "min": 50,
                    "max": 1000
                },
                {
                    "type": "imp_target",
                    "min": 0
                }
            ],
            "media_type_list": [
                "Bulletin"
            ],
            "lock": {
                "measure": "spots",
                "value": 25
            }
        }
    ],
    "allocation_method": "equal",
    "goal": {
        "period_days": 7,
        "measure": "trp",
        "value": 100
    }
}
```

###### Response: 
_The response shows that the number of inventory was locked at 25 spots and failed to meet the goal of 100 TRPs._
```json
{
    "allocation_list": [
        {
            "measures": {
                "measures_type": "plan_measures",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "DMA623",
                "market": "DMA623",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 2.446190288,
                "imp_target_inmkt": 7043622.180732,
                "imp_target": 8212218.20723589,
                "imp_inmkt": 7043622.180732,
                "imp": 8212218.20723589,
                "pct_imp_inmkt": 0.8577003196,
                "pct_imp_target_inmkt": 0.8577003196,
                "pop_inmkt": 8191034,
                "pop_target_inmkt": 8191034,
                "reach_pct": 35.153379787,
                "reach_net": 2879425,
                "trp": 85.991856226,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.345805722,
                "eff_reach_net": 1317598,
                "eff_reach_pct": 16.085855097,
                "spots": 25
            },
            "media_type_group": {
                "classification_type_list": null,
                "construction_type_list": null,
                "media_type_list": [
                    "Bulletin"
                ],
                "frame_media_name_list": null,
                "operator_name_list": null,
                "include_spot_list": null,
                "exclude_spot_list": null,
                "digital": null,
                "rotating": null,
                "measures_range_list": [
                    {
                        "type": "index_comp_target",
                        "min": 50.0,
                        "max": 1000.0
                    },
                    {
                        "type": "imp_target",
                        "min": 0.0,
                        "max": null
                    }
                ],
                "lock": {
                    "measure": "spots",
                    "value": 25.0
                }
            }
        }
    ],
    "summaries": {
        "by_media_type_group": [
            {
                "measures": {
                    "measures_type": "plan_measures",
                    "period_days": 7,
                    "base_segment": "2032",
                    "target_segment": "2032",
                    "target_geo": "DMA623",
                    "market": "DMA623",
                    "index_comp_target": 100.0,
                    "pct_comp_pop_target_inmkt": 1.0,
                    "pct_comp_imp_target": 1.0,
                    "pct_comp_imp_target_inmkt": 1.0,
                    "freq_avg": 2.446190288,
                    "imp_target_inmkt": 7043622.180732,
                    "imp_target": 8212218.20723589,
                    "imp_inmkt": 7043622.180732,
                    "imp": 8212218.20723589,
                    "pct_imp_inmkt": 0.8577003196,
                    "pct_imp_target_inmkt": 0.8577003196,
                    "pop_inmkt": 8191034,
                    "pop_target_inmkt": 8191034,
                    "reach_pct": 35.153379787,
                    "reach_net": 2879425,
                    "trp": 85.991856226,
                    "eff_freq_min": 3,
                    "eff_freq_avg": 5.345805722,
                    "eff_reach_net": 1317598,
                    "eff_reach_pct": 16.085855097,
                    "spots": 25
                },
                "media_type_group": {
                    "classification_type_list": null,
                    "construction_type_list": null,
                    "media_type_list": [
                        "Bulletin"
                    ],
                    "frame_media_name_list": null,
                    "operator_name_list": null,
                    "include_spot_list": null,
                    "exclude_spot_list": null,
                    "digital": null,
                    "rotating": null,
                    "measures_range_list": [
                        {
                            "type": "index_comp_target",
                            "min": 50.0,
                            "max": 1000.0
                        },
                        {
                            "type": "imp_target",
                            "min": 0.0,
                            "max": null
                        }
                    ],
                    "lock": {
                        "measure": "spots",
                        "value": 25.0
                    }
                }
            }
        ],
        "by_operator": [
            {
                "measures": {
                    "measures_type": "plan_measures",
                    "period_days": 7,
                    "base_segment": "2032",
                    "target_segment": "2032",
                    "target_geo": "DMA623",
                    "market": "DMA623",
                    "index_comp_target": 100.0,
                    "pct_comp_pop_target_inmkt": 1.0,
                    "pct_comp_imp_target": 1.0,
                    "pct_comp_imp_target_inmkt": 1.0,
                    "freq_avg": 2.446190288,
                    "imp_target_inmkt": 7043622.180732,
                    "imp_target": 8212218.20723589,
                    "imp_inmkt": 7043622.180732,
                    "imp": 8212218.20723589,
                    "pct_imp_inmkt": 0.8577003196,
                    "pct_imp_target_inmkt": 0.8577003196,
                    "pop_inmkt": 8191034,
                    "pop_target_inmkt": 8191034,
                    "reach_pct": 35.153379787,
                    "reach_net": 2879425,
                    "trp": 85.991856226,
                    "eff_freq_min": 3,
                    "eff_freq_avg": 5.345805722,
                    "eff_reach_net": 1317598,
                    "eff_reach_pct": 16.085855097,
                    "spots": 25
                },
                "media_type_group": {
                    "classification_type_list": null,
                    "construction_type_list": null,
                    "media_type_list": [
                        "Bulletin"
                    ],
                    "frame_media_name_list": null,
                    "operator_name_list": null,
                    "include_spot_list": null,
                    "exclude_spot_list": null,
                    "digital": null,
                    "rotating": null,
                    "measures_range_list": [
                        {
                            "type": "index_comp_target",
                            "min": 50.0,
                            "max": 1000.0
                        },
                        {
                            "type": "imp_target",
                            "min": 0.0,
                            "max": null
                        }
                    ],
                    "lock": {
                        "measure": "spots",
                        "value": 25.0
                    }
                }
            }
        ],
        "total": {
            "measures": {
                "measures_type": "plan_measures",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "DMA623",
                "market": "DMA623",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 2.446190288,
                "imp_target_inmkt": 7043622.180732,
                "imp_target": 8212218.20723589,
                "imp_inmkt": 7043622.180732,
                "imp": 8212218.20723589,
                "pct_imp_inmkt": 0.8577003196,
                "pct_imp_target_inmkt": 0.8577003196,
                "pop_inmkt": 8191034,
                "pop_target_inmkt": 8191034,
                "reach_pct": 35.153379787,
                "reach_net": 2879425,
                "trp": 85.991856226,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.345805722,
                "eff_reach_net": 1317598,
                "eff_reach_pct": 16.085855097,
                "spots": 25
            },
            "media_type_group": {
                "classification_type_list": null,
                "construction_type_list": null,
                "media_type_list": [
                    "Bulletin"
                ],
                "frame_media_name_list": null,
                "operator_name_list": null,
                "include_spot_list": null,
                "exclude_spot_list": null,
                "digital": null,
                "rotating": null,
                "measures_range_list": [
                    {
                        "type": "index_comp_target",
                        "min": 50.0,
                        "max": 1000.0
                    },
                    {
                        "type": "imp_target",
                        "min": 0.0,
                        "max": null
                    }
                ],
                "lock": {
                    "measure": "spots",
                    "value": 25.0
                }
            }
        }
    }
}
```
###### Call:
_This call is locking the amount of inventory for a specific operators bulletins, while maintaining no lock on specific operators posters. Note that there are two lock objects set within the objects in the media_type_group_list._
```json
{
    "target_geography_list": [
        "DMA515"
    ],
    "target_segment": 2032,
    "media_type_group_list": [
        {
            "operator_name_list": [
                "Lamar"
            ],
            "frame_media_name_list": [],
            "measures_range_list": [
                {
                    "type": "index_comp_target",
                    "min": 50,
                    "max": 1000
                },
                {
                    "type": "imp_target",
                    "min": 0
                }
            ],
            "media_type_list": [
                "Bulletin"
            ],
            "lock": {
                "measure": "spots",
                "value": 1
            }
        },
        {
            "operator_name_list": [
                "Lamar"
            ],
            "frame_media_name_list": [],
            "measures_range_list": [
                {
                    "type": "index_comp_target",
                    "min": 50,
                    "max": 1000
                },
                {
                    "type": "imp_target",
                    "min": 0
                }
            ],
            "media_type_list": [
                "Poster"
            ],
            "lock": {
                "measure": "spots",
                "value": 1
            }
        },
        {
            "operator_name_list": [
                "OUTFRONT"
            ],
            "measures_range_list": [
                {
                    "type": "index_comp_target",
                    "min": 50,
                    "max": 1000
                },
                {
                    "type": "imp_target",
                    "min": 0
                }
            ],
            "media_type_list": [
                "Bulletin"
            ],
            "lock": {
                "measure": "spots",
                "value": 1
            }
        },
        {
            "operator_name_list": [
                "OUTFRONT"
            ],
            "measures_range_list": [
                {
                    "type": "index_comp_target",
                    "min": 50,
                    "max": 1000
                },
                {
                    "type": "imp_target",
                    "min": 0
                }
            ],
            "media_type_list": [
                "Poster"
            ],
            "lock": {
                "measure": "spots",
                "value": 15
            }
        }
    ],
    "allocation_method": "equal",
    "goal": {
        "period_days": 14,
        "measure": "trp",
        "value": 150
    }
}
```
###### Response: 
_The response shows the plan results in different as a total and by different aggregations. Note that locking the bulletins at 15 per operator failed to meet the TRP goal._
```json
{
    "allocation_list": [
        {
            "measures": {
                "measures_type": "plan_measures",
                "period_days": 14,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "DMA501",
                "market": "DMA501",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 4.207746887,
                "imp_target_inmkt": 1.23022167475307E7,
                "imp_target": 1.31125700218437E7,
                "imp_inmkt": 1.23022167475307E7,
                "imp": 1.31125700218437E7,
                "pct_imp_inmkt": 0.938200271,
                "pct_imp_target_inmkt": 0.938200271,
                "pop_inmkt": 21743768,
                "pop_target_inmkt": 21743768,
                "reach_pct": 13.446181262,
                "reach_net": 2923706,
                "trp": 56.57812734,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.561019674,
                "eff_reach_net": 2212223,
                "eff_reach_pct": 10.174056316,
                "spots": 15
            },
            "media_type_group": {
                "classification_type_list": null,
                "construction_type_list": null,
                "media_type_list": [
                    "Bulletin"
                ],
                "frame_media_name_list": [],
                "operator_name_list": [
                    "Lamar"
                ],
                "include_spot_list": null,
                "exclude_spot_list": null,
                "digital": null,
                "rotating": null,
                "measures_range_list": [
                    {
                        "type": "index_comp_target",
                        "min": 50.0,
                        "max": 1000.0
                    },
                    {
                        "type": "imp_target",
                        "min": 0.0,
                        "max": null
                    }
                ],
                "lock": {
                    "measure": "spots",
                    "value": 15.0
                }
            }
        },
        {
            "measures": {
                "measures_type": "plan_measures",
                "period_days": 14,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "DMA501",
                "market": "DMA501",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 5.67614061,
                "imp_target_inmkt": 1.64563402749068E7,
                "imp_target": 1.74169879830018E7,
                "imp_inmkt": 1.64563402749068E7,
                "imp": 1.74169879830018E7,
                "pct_imp_inmkt": 0.9448442114,
                "pct_imp_target_inmkt": 0.9448442114,
                "pop_inmkt": 21743768,
                "pop_target_inmkt": 21743768,
                "reach_pct": 13.333535082,
                "reach_net": 2899213,
                "trp": 75.683019957,
                "eff_freq_min": 3,
                "eff_freq_avg": 6.334258187,
                "eff_reach_net": 2597990,
                "eff_reach_pct": 11.948205729,
                "spots": 83
            },
            "media_type_group": {
                "classification_type_list": null,
                "construction_type_list": null,
                "media_type_list": [
                    "Poster"
                ],
                "frame_media_name_list": [],
                "operator_name_list": [
                    "Lamar"
                ],
                "include_spot_list": null,
                "exclude_spot_list": null,
                "digital": null,
                "rotating": null,
                "measures_range_list": [
                    {
                        "type": "index_comp_target",
                        "min": 50.0,
                        "max": 1000.0
                    },
                    {
                        "type": "imp_target",
                        "min": 0.0,
                        "max": null
                    }
                ],
                "lock": null
            }
        },
        {
            "measures": {
                "measures_type": "plan_measures",
                "period_days": 14,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "DMA501",
                "market": "DMA501",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 5.156854934,
                "imp_target_inmkt": 1.63376556638252E7,
                "imp_target": 1.67651655615922E7,
                "imp_inmkt": 1.63376556638252E7,
                "imp": 1.67651655615922E7,
                "pct_imp_inmkt": 0.9745001088,
                "pct_imp_target_inmkt": 0.9745001088,
                "pop_inmkt": 21743768,
                "pop_target_inmkt": 21743768,
                "reach_pct": 14.570351145,
                "reach_net": 3168143,
                "trp": 75.137187188,
                "eff_freq_min": 3,
                "eff_freq_avg": 6.023909691,
                "eff_reach_net": 2712135,
                "eff_reach_pct": 12.473159632,
                "spots": 15
            },
            "media_type_group": {
                "classification_type_list": null,
                "construction_type_list": null,
                "media_type_list": [
                    "Bulletin"
                ],
                "frame_media_name_list": [],
                "operator_name_list": [
                    "OUTFRONT"
                ],
                "include_spot_list": null,
                "exclude_spot_list": null,
                "digital": null,
                "rotating": null,
                "measures_range_list": [
                    {
                        "type": "index_comp_target",
                        "min": 50.0,
                        "max": 1000.0
                    },
                    {
                        "type": "imp_target",
                        "min": 0.0,
                        "max": null
                    }
                ],
                "lock": {
                    "measure": "spots",
                    "value": 15.0
                }
            }
        },
        {
            "measures": {
                "measures_type": "plan_measures",
                "period_days": 14,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "DMA501",
                "market": "DMA501",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 4.654720242,
                "imp_target_inmkt": 1.64568738673595E7,
                "imp_target": 1.71416949283274E7,
                "imp_inmkt": 1.64568738673595E7,
                "imp": 1.71416949283274E7,
                "pct_imp_inmkt": 0.9600493963,
                "pct_imp_target_inmkt": 0.9600493963,
                "pop_inmkt": 21743768,
                "pop_target_inmkt": 21743768,
                "reach_pct": 16.259940452,
                "reach_net": 3535524,
                "trp": 75.685473959,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.795824231,
                "eff_reach_net": 2839436,
                "eff_reach_pct": 13.058621336,
                "spots": 73
            },
            "media_type_group": {
                "classification_type_list": null,
                "construction_type_list": null,
                "media_type_list": [
                    "Poster"
                ],
                "frame_media_name_list": [],
                "operator_name_list": [
                    "OUTFRONT"
                ],
                "include_spot_list": null,
                "exclude_spot_list": null,
                "digital": null,
                "rotating": null,
                "measures_range_list": [
                    {
                        "type": "index_comp_target",
                        "min": 50.0,
                        "max": 1000.0
                    },
                    {
                        "type": "imp_target",
                        "min": 0.0,
                        "max": null
                    }
                ],
                "lock": null
            }
        }
    ],
    "summaries": {
        "by_media_type_group": [
            {
                "measures": {
                    "measures_type": "plan_measures",
                    "period_days": 14,
                    "base_segment": "2032",
                    "target_segment": "2032",
                    "target_geo": "DMA501",
                    "market": "DMA501",
                    "index_comp_target": 100.0,
                    "pct_comp_pop_target_inmkt": 1.0,
                    "pct_comp_imp_target": 1.0,
                    "pct_comp_imp_target_inmkt": 1.0,
                    "freq_avg": 5.519270977179628,
                    "imp_target_inmkt": 3.29132141422663E7,
                    "imp_target": 3.4558682911329195E7,
                    "imp_inmkt": 3.29132141422663E7,
                    "imp": 3.4558682911329195E7,
                    "pct_imp_inmkt": 0.9523862418806629,
                    "pct_imp_target_inmkt": 0.9523862418806629,
                    "pop_inmkt": 21743768,
                    "pop_target_inmkt": 21743768,
                    "reach_pct": 27.425450669520266,
                    "reach_net": 5963326,
                    "trp": 151.3684939163548,
                    "eff_freq_min": 3,
                    "eff_freq_avg": 6.455894551256478,
                    "eff_reach_net": 5098165,
                    "eff_reach_pct": 23.446556122403628,
                    "spots": 156
                },
                "media_type_group": {
                    "classification_type_list": null,
                    "construction_type_list": null,
                    "media_type_list": [
                        "Poster"
                    ],
                    "frame_media_name_list": [],
                    "operator_name_list": [
                        "Lamar",
                        "OUTFRONT"
                    ],
                    "include_spot_list": null,
                    "exclude_spot_list": null,
                    "digital": null,
                    "rotating": null,
                    "measures_range_list": [
                        {
                            "type": "index_comp_target",
                            "min": 50.0,
                            "max": 1000.0
                        },
                        {
                            "type": "imp_target",
                            "min": 0.0,
                            "max": null
                        }
                    ],
                    "lock": null
                }
            },
            {
                "measures": {
                    "measures_type": "plan_measures",
                    "period_days": 14,
                    "base_segment": "2032",
                    "target_segment": "2032",
                    "target_geo": "DMA501",
                    "market": "DMA501",
                    "index_comp_target": 100.0,
                    "pct_comp_pop_target_inmkt": 1.0,
                    "pct_comp_imp_target": 1.0,
                    "pct_comp_imp_target_inmkt": 1.0,
                    "freq_avg": 5.054818704234596,
                    "imp_target_inmkt": 2.86398724113559E7,
                    "imp_target": 2.98777355834359E7,
                    "imp_inmkt": 2.86398724113559E7,
                    "imp": 2.98777355834359E7,
                    "pct_imp_inmkt": 0.9585690432053269,
                    "pct_imp_target_inmkt": 0.9585690432053269,
                    "pop_inmkt": 21743768,
                    "pop_target_inmkt": 21743768,
                    "reach_pct": 26.057376581533408,
                    "reach_net": 5665856,
                    "trp": 131.7153145276196,
                    "eff_freq_min": 3,
                    "eff_freq_avg": 6.161200579004361,
                    "eff_reach_net": 4648424,
                    "eff_reach_pct": 21.378189662655743,
                    "spots": 30
                },
                "media_type_group": {
                    "classification_type_list": null,
                    "construction_type_list": null,
                    "media_type_list": [
                        "Bulletin"
                    ],
                    "frame_media_name_list": [],
                    "operator_name_list": [
                        "Lamar",
                        "OUTFRONT"
                    ],
                    "include_spot_list": null,
                    "exclude_spot_list": null,
                    "digital": null,
                    "rotating": null,
                    "measures_range_list": [
                        {
                            "type": "index_comp_target",
                            "min": 50.0,
                            "max": 1000.0
                        },
                        {
                            "type": "imp_target",
                            "min": 0.0,
                            "max": null
                        }
                    ],
                    "lock": {
                        "measure": "spots",
                        "value": 15.0
                    }
                }
            }
        ],
        "by_operator": [
            {
                "measures": {
                    "measures_type": "plan_measures",
                    "period_days": 14,
                    "base_segment": "2032",
                    "target_segment": "2032",
                    "target_geo": "DMA501",
                    "market": "DMA501",
                    "index_comp_target": 100.0,
                    "pct_comp_pop_target_inmkt": 1.0,
                    "pct_comp_imp_target": 1.0,
                    "pct_comp_imp_target_inmkt": 1.0,
                    "freq_avg": 5.293226943108967,
                    "imp_target_inmkt": 2.8758557022437498E7,
                    "imp_target": 3.05295580048455E7,
                    "imp_inmkt": 2.8758557022437498E7,
                    "imp": 3.05295580048455E7,
                    "pct_imp_inmkt": 0.9419906117826233,
                    "pct_imp_target_inmkt": 0.9419906117826233,
                    "pop_inmkt": 21743768,
                    "pop_target_inmkt": 21743768,
                    "reach_pct": 24.986865048241924,
                    "reach_net": 5433086,
                    "trp": 132.26114729718188,
                    "eff_freq_min": 3,
                    "eff_freq_avg": 6.326273208772847,
                    "eff_reach_net": 4545892,
                    "eff_reach_pct": 20.90664486538,
                    "spots": 98
                },
                "media_type_group": {
                    "classification_type_list": null,
                    "construction_type_list": null,
                    "media_type_list": [
                        "Bulletin",
                        "Poster"
                    ],
                    "frame_media_name_list": [],
                    "operator_name_list": [
                        "Lamar"
                    ],
                    "include_spot_list": null,
                    "exclude_spot_list": null,
                    "digital": null,
                    "rotating": null,
                    "measures_range_list": [
                        {
                            "type": "index_comp_target",
                            "min": 50.0,
                            "max": 1000.0
                        },
                        {
                            "type": "imp_target",
                            "min": 0.0,
                            "max": null
                        }
                    ],
                    "lock": {
                        "measure": "spots",
                        "value": 15.0
                    }
                }
            },
            {
                "measures": {
                    "measures_type": "plan_measures",
                    "period_days": 14,
                    "base_segment": "2032",
                    "target_segment": "2032",
                    "target_geo": "DMA501",
                    "market": "DMA501",
                    "index_comp_target": 100.0,
                    "pct_comp_pop_target_inmkt": 1.0,
                    "pct_comp_imp_target": 1.0,
                    "pct_comp_imp_target_inmkt": 1.0,
                    "freq_avg": 5.2992448272892,
                    "imp_target_inmkt": 3.2794529531184703E7,
                    "imp_target": 3.39068604899196E7,
                    "imp_inmkt": 3.2794529531184703E7,
                    "imp": 3.39068604899196E7,
                    "pct_imp_inmkt": 0.9671945163113644,
                    "pct_imp_target_inmkt": 0.9671945163113644,
                    "pop_inmkt": 21743768,
                    "pop_target_inmkt": 21743768,
                    "reach_pct": 28.461161177175697,
                    "reach_net": 6188529,
                    "trp": 150.8226611467925,
                    "eff_freq_min": 3,
                    "eff_freq_avg": 6.309790585791979,
                    "eff_reach_net": 5197404,
                    "eff_reach_pct": 23.9029582830223,
                    "spots": 88
                },
                "media_type_group": {
                    "classification_type_list": null,
                    "construction_type_list": null,
                    "media_type_list": [
                        "Bulletin",
                        "Poster"
                    ],
                    "frame_media_name_list": [],
                    "operator_name_list": [
                        "OUTFRONT"
                    ],
                    "include_spot_list": null,
                    "exclude_spot_list": null,
                    "digital": null,
                    "rotating": null,
                    "measures_range_list": [
                        {
                            "type": "index_comp_target",
                            "min": 50.0,
                            "max": 1000.0
                        },
                        {
                            "type": "imp_target",
                            "min": 0.0,
                            "max": null
                        }
                    ],
                    "lock": {
                        "measure": "spots",
                        "value": 15.0
                    }
                }
            }
        ],
        "total": {
            "measures": {
                "measures_type": "plan_measures",
                "period_days": 14,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "DMA501",
                "market": "DMA501",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 6.109308331632881,
                "imp_target_inmkt": 6.15530865536222E7,
                "imp_target": 6.44364184947651E7,
                "imp_inmkt": 6.15530865536222E7,
                "imp": 6.44364184947651E7,
                "pct_imp_inmkt": 0.9552530694831037,
                "pct_imp_target_inmkt": 0.9552530694831037,
                "pop_inmkt": 21743768,
                "pop_target_inmkt": 21743768,
                "reach_pct": 46.33647429091411,
                "reach_net": 10075295,
                "trp": 283.08380844397436,
                "eff_freq_min": 3,
                "eff_freq_avg": 7.110461666127006,
                "eff_reach_net": 8656693,
                "eff_reach_pct": 39.8122965478509,
                "spots": 186
            },
            "media_type_group": {
                "classification_type_list": null,
                "construction_type_list": null,
                "media_type_list": [
                    "Bulletin",
                    "Poster"
                ],
                "frame_media_name_list": [],
                "operator_name_list": [
                    "Lamar",
                    "OUTFRONT"
                ],
                "include_spot_list": null,
                "exclude_spot_list": null,
                "digital": null,
                "rotating": null,
                "measures_range_list": [
                    {
                        "type": "index_comp_target",
                        "min": 50.0,
                        "max": 1000.0
                    },
                    {
                        "type": "imp_target",
                        "min": 0.0,
                        "max": null
                    }
                ],
                "lock": {
                    "measure": "spots",
                    "value": 15.0
                }
            }
        }
    }
}
```
