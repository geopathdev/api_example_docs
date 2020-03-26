## Use Case: Obtaining measures for a set of units with different dates
#### These examples use the `/measures/summary` endpoint to combine audience segments, markets, inventory and time to get measures

###### Call:
_These 3 calls are taking the same batch of 5 Bulletins and getting the Hispanic 18+ measures for a 1,2, & 4 week period in the New York CBSA with 3 minimum frequency. These are seperated out because you cannot have the same inventory returned for overlapping dates in a single call.
```json
{
    "base_segment": "2032",
    "target_segment_list": [
        "8018"
    ],
    "target_geography_list": [
        "CBSA35620"
    ],
    "min_freq": 3,
    "batch_list": [
        {
            "batch_id": "1",
            "id_list": [
                "310717",
                "30450358",
                "30496270",
                "30790081",
                "30492061"
            ],
            "period": {
                "start_date": "2020-04-01",
                "end_date": "2020-04-07"
            }
        }
    ]
}
```
```json
{
    "base_segment": "2032",
    "target_segment_list": [
        "8018"
    ],
    "target_geography_list": [
        "CBSA35620"
    ],
    "min_freq": 3,
    "batch_list": [
        {
            "batch_id": "1",
            "id_list": [
                "310717",
                "30450358",
                "30496270",
                "30790081",
                "30492061"
            ],
            "period": {
                "start_date": "2020-04-01",
                "end_date": "2020-04-14"
            }
        }
    ]
}
```
```json
{
    "base_segment": "2032",
    "target_segment_list": [
        "8018"
    ],
    "target_geography_list": [
        "CBSA35620"
    ],
    "min_freq": 3,
    "batch_list": [
        {
            "batch_id": "1",
            "id_list": [
                "310717",
                "30450358",
                "30496270",
                "30790081",
                "30492061"
            ],
            "period": {
                "start_date": "2020-04-01",
                "end_date": "2020-04-28"
            }
        }
    ]
}
```
###### Response:
_This is the response for the 1 week campaign, the other responses will be identical in structure with different measures depending on the time. It breaks down the measures by overall, by batch (will list multiple if there are multiple batches) and each spot in each batch individually._
```json
{
    "spots_with_no_measures": [],
    "measures_summaries": {
        "overall": {
            "measures_type": "overall",
            "period_days": 7,
            "base_segment": "2032",
            "target_segment": "2032",
            "target_geo": "CBSA35620",
            "market": "CBSA35620",
            "index_comp_target": 100.0,
            "pct_comp_pop_target_inmkt": 1.0,
            "pct_comp_imp_target": 1.0,
            "pct_comp_imp_target_inmkt": 1.0,
            "freq_avg": 3.3405391475818913,
            "imp_target_inmkt": 3331676.026833938,
            "imp_target": 3443587.3304748777,
            "imp_inmkt": 3331676.026833938,
            "imp": 3443587.3304748777,
            "pct_imp_inmkt": 0.967501534620437,
            "pct_imp_target_inmkt": 0.967501534620437,
            "pop_inmkt": 20431828,
            "pop_target_inmkt": 20431828,
            "reach_pct": 4.881339052565437,
            "reach_net": 997346,
            "trp": 16.306304197715143,
            "eff_freq_min": 3,
            "eff_freq_avg": 5.380610173563891,
            "eff_reach_net": 619200,
            "eff_reach_pct": 3.030567848574417,
            "frames": 5,
            "spots": 5,
            "summarizes": {
                "period": {
                    "start_date": "2020-04-01T00:00:00.000Z",
                    "end_date": "2020-04-07T23:59:59.999Z"
                }
            }
        },
        "by_batch": [
            {
                "measures_type": "by_batch",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 3.3405391475818913,
                "imp_target_inmkt": 3331676.026833938,
                "imp_target": 3443587.3304748777,
                "imp_inmkt": 3331676.026833938,
                "imp": 3443587.3304748777,
                "pct_imp_inmkt": 0.967501534620437,
                "pct_imp_target_inmkt": 0.967501534620437,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 4.881339052565437,
                "reach_net": 997346,
                "trp": 16.306304197715143,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.380610173563891,
                "eff_reach_net": 619200,
                "eff_reach_pct": 3.030567848574417,
                "frames": 5,
                "spots": 5,
                "summarizes": {
                    "batch_id": "1",
                    "id_list": [
                        "310717",
                        "30450358",
                        "30492061",
                        "30496270",
                        "30790081"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            }
        ],
        "by_spot_overall": [
            {
                "measures_type": "by_spot_overall",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 3.435869283014852,
                "imp_target_inmkt": 1183595.48759494,
                "imp_target": 1210603.9398637,
                "imp_inmkt": 1183595.48759494,
                "imp": 1210603.9398637,
                "pct_imp_inmkt": 0.9776901004701829,
                "pct_imp_target_inmkt": 0.9776901004701829,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 1.6860072740581988,
                "reach_net": 344482,
                "trp": 5.792900603876168,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.2776339598945485,
                "eff_reach_net": 224266,
                "eff_reach_pct": 1.0976321298326486,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "id_list": [
                        "310717"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_overall",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 4.580045512824158,
                "imp_target_inmkt": 118938.44414043,
                "imp_target": 123962.834425674,
                "imp_inmkt": 118938.44414043,
                "imp": 123962.834425674,
                "pct_imp_inmkt": 0.9594685753312898,
                "pct_imp_target_inmkt": 0.9594685753312898,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 0.12709990778621005,
                "reach_net": 25968,
                "trp": 0.5821233623365957,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.461167769132948,
                "eff_reach_net": 21778,
                "eff_reach_pct": 0.10659320257964122,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "id_list": [
                        "30450358"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_overall",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 3.34302023753179,
                "imp_target_inmkt": 1295516.92885098,
                "imp_target": 1361954.3282199,
                "imp_inmkt": 1295516.92885098,
                "imp": 1361954.3282199,
                "pct_imp_inmkt": 0.9512190695441639,
                "pct_imp_target_inmkt": 0.9512190695441639,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 1.8966922199999958,
                "reach_net": 387528,
                "trp": 6.3406804758290845,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.179272869434287,
                "eff_reach_net": 250134,
                "eff_reach_pct": 1.2242414399999846,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "id_list": [
                        "30492061"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_overall",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 3.114549131185019,
                "imp_target_inmkt": 501294.670916313,
                "imp_target": 511406.734610083,
                "imp_inmkt": 501294.670916313,
                "imp": 511406.734610083,
                "pct_imp_inmkt": 0.9802269641570523,
                "pct_imp_target_inmkt": 0.9802269641570523,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 0.7877541100000052,
                "reach_net": 160952,
                "trp": 2.453498878887944,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.215805577315259,
                "eff_reach_net": 96110,
                "eff_reach_pct": 0.47039692000000466,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "id_list": [
                        "30496270"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_overall",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 2.41912391056718,
                "imp_target_inmkt": 232330.495331275,
                "imp_target": 235659.493355521,
                "imp_inmkt": 232330.495331275,
                "imp": 235659.493355521,
                "pct_imp_inmkt": 0.9858736943848733,
                "pct_imp_target_inmkt": 0.9858736943848733,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 0.4700465618227678,
                "reach_net": 96039,
                "trp": 1.1371008767853517,
                "eff_freq_min": 3,
                "eff_freq_avg": 6.948348570184801,
                "eff_reach_net": 33436,
                "eff_reach_pct": 0.16365052289757376,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "id_list": [
                        "30790081"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            }
        ],
        "by_spot_batch": [
            {
                "measures_type": "by_spot_batch",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 3.435869283014852,
                "imp_target_inmkt": 1183595.48759494,
                "imp_target": 1210603.9398637,
                "imp_inmkt": 1183595.48759494,
                "imp": 1210603.9398637,
                "pct_imp_inmkt": 0.9776901004701829,
                "pct_imp_target_inmkt": 0.9776901004701829,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 1.6860072740581988,
                "reach_net": 344482,
                "trp": 5.792900603876168,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.2776339598945485,
                "eff_reach_net": 224266,
                "eff_reach_pct": 1.0976321298326486,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "batch_id": "1",
                    "id_list": [
                        "310717"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_batch",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 4.580045512824158,
                "imp_target_inmkt": 118938.44414043,
                "imp_target": 123962.834425674,
                "imp_inmkt": 118938.44414043,
                "imp": 123962.834425674,
                "pct_imp_inmkt": 0.9594685753312898,
                "pct_imp_target_inmkt": 0.9594685753312898,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 0.12709990778621005,
                "reach_net": 25968,
                "trp": 0.5821233623365957,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.461167769132948,
                "eff_reach_net": 21778,
                "eff_reach_pct": 0.10659320257964122,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "batch_id": "1",
                    "id_list": [
                        "30450358"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_batch",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 3.34302023753179,
                "imp_target_inmkt": 1295516.92885098,
                "imp_target": 1361954.3282199,
                "imp_inmkt": 1295516.92885098,
                "imp": 1361954.3282199,
                "pct_imp_inmkt": 0.9512190695441639,
                "pct_imp_target_inmkt": 0.9512190695441639,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 1.8966922199999958,
                "reach_net": 387528,
                "trp": 6.3406804758290845,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.179272869434287,
                "eff_reach_net": 250134,
                "eff_reach_pct": 1.2242414399999846,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "batch_id": "1",
                    "id_list": [
                        "30492061"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_batch",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 3.114549131185019,
                "imp_target_inmkt": 501294.670916313,
                "imp_target": 511406.734610083,
                "imp_inmkt": 501294.670916313,
                "imp": 511406.734610083,
                "pct_imp_inmkt": 0.9802269641570523,
                "pct_imp_target_inmkt": 0.9802269641570523,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 0.7877541100000052,
                "reach_net": 160952,
                "trp": 2.453498878887944,
                "eff_freq_min": 3,
                "eff_freq_avg": 5.215805577315259,
                "eff_reach_net": 96110,
                "eff_reach_pct": 0.47039692000000466,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "batch_id": "1",
                    "id_list": [
                        "30496270"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            },
            {
                "measures_type": "by_spot_batch",
                "period_days": 7,
                "base_segment": "2032",
                "target_segment": "2032",
                "target_geo": "CBSA35620",
                "market": "CBSA35620",
                "index_comp_target": 100.0,
                "pct_comp_pop_target_inmkt": 1.0,
                "pct_comp_imp_target": 1.0,
                "pct_comp_imp_target_inmkt": 1.0,
                "freq_avg": 2.41912391056718,
                "imp_target_inmkt": 232330.495331275,
                "imp_target": 235659.493355521,
                "imp_inmkt": 232330.495331275,
                "imp": 235659.493355521,
                "pct_imp_inmkt": 0.9858736943848733,
                "pct_imp_target_inmkt": 0.9858736943848733,
                "pop_inmkt": 20431828,
                "pop_target_inmkt": 20431828,
                "reach_pct": 0.4700465618227678,
                "reach_net": 96039,
                "trp": 1.1371008767853517,
                "eff_freq_min": 3,
                "eff_freq_avg": 6.948348570184801,
                "eff_reach_net": 33436,
                "eff_reach_pct": 0.16365052289757376,
                "frames": 1,
                "spots": 1,
                "summarizes": {
                    "batch_id": "1",
                    "id_list": [
                        "30790081"
                    ],
                    "period": {
                        "start_date": "2020-04-01T00:00:00.000Z",
                        "end_date": "2020-04-07T23:59:59.999Z"
                    }
                }
            }
        ]
    },
    "pagination": {
        "page": 1,
        "page_size": 1000,
        "number_of_pages": 1,
        "number_of_summaries": 12
    }
}
```