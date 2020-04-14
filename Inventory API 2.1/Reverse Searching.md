## Use Case: Finding Inventory based on geography or audience delivery

Often there are cases where the specific inventory isn't required, but it's important to find inventory that matches to the best market or target audience. 

### Best Market: 
##### The inventory search endpoint is utilized to find the top spots per market. Currently, only DMA, CBSA and County level impressions are available. Inventory can be filtered to smaller markets like ZIP Code. 
###### Call:
_This call asks for the spots sorted by the percent of in market impressions. It uses the target_geography_list to specify the county it's looking in, and then further narrows the inventory that is within a specific zip code. The measures_range_list parameter is used to limit the response to inventory that actually produces impressions in the market asked for (if this is not provided the response will include all inventory with the majority producing NULL in market impressions.)_
```json
{
    "target_geography_list": [
        "CNTY34023"
    ],
    "inventory_market_list": [
        "ZIP08904"
    ],
    "sort": {
        "measure": "pct_imp_target_inmkt",
        "type": "DESC"
    },
    "measures_range_list": [
        {
            "type": "imp_inmkt",
            "min": 1
        }
    ],
    "page": 1,
    "page_size": 1000
}
```
###### Response:
_The response is the standard inventory search response, but sorted to the specifications in the call. This response truncates frame details for space._
```json
{
    "inventory_summary": {
        "inventory_count": 5,
        "invalid_ids": null,
        "filtered_invalid_ids": null,
        "inventory_items": [
            {
                "frame_id": 631041,
                etc...
                "spot_references": [
                    {
                        "spot_id": 631041,
                        "uri": "{{api.basepath}}/v2.1/inventory/spot/631041",
                        "length": null,
                        "spot_rotating": false,
                        "created_dtm": "2005-09-03T00:00:00.000Z",
                        "updated_dtm": "2011-10-11T13:07:00.000Z",
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "CNTY34023",
                            "market": "CNTY34023",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 3.604300908,
                            "imp_target_inmkt": 52261.396395154,
                            "imp_target": 91957.562656792,
                            "imp_inmkt": 52261.396395154,
                            "imp": 91957.562656792,
                            "pct_imp_inmkt": 0.5683208089,
                            "pct_imp_target_inmkt": 0.5683208089,
                            "pop_inmkt": 847763,
                            "pop_target_inmkt": 847763,
                            "reach_pct": 1.710352041,
                            "reach_net": 14500,
                            "trp": 6.164623414,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 4.983678342,
                            "eff_reach_net": 10487,
                            "eff_reach_pct": 1.236962539
                        }
                    }
                ]
            },
            {
                "frame_id": 631043,
                etc...
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "CNTY34023",
                            "market": "CNTY34023",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 2.518249282,
                            "imp_target_inmkt": 20004.071179104,
                            "imp_target": 36186.786566725,
                            "imp_inmkt": 20004.071179104,
                            "imp": 36186.786566725,
                            "pct_imp_inmkt": 0.5528004301,
                            "pct_imp_target_inmkt": 0.5528004301,
                            "pop_inmkt": 847763,
                            "pop_target_inmkt": 847763,
                            "reach_pct": 0.9370121326,
                            "reach_net": 7944,
                            "trp": 2.35963013,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.421216439,
                            "eff_reach_net": 3690,
                            "eff_reach_pct": 0.4352584252
                        }
            },
            {
                "frame_id": 631044,
               etc...
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "2032",
                            "target_segment": "2032",
                            "target_geo": "CNTY34023",
                            "market": "CNTY34023",
                            "index_comp_target": 100.0,
                            "pct_comp_pop_target_inmkt": 1.0,
                            "pct_comp_imp_target": 1.0,
                            "pct_comp_imp_target_inmkt": 1.0,
                            "freq_avg": 3.841447479,
                            "imp_target_inmkt": 32605.566498443,
                            "imp_target": 59189.998261472,
                            "imp_inmkt": 32605.566498443,
                            "imp": 59189.998261472,
                            "pct_imp_inmkt": 0.5508627717,
                            "pct_imp_target_inmkt": 0.5508627717,
                            "pop_inmkt": 847763,
                            "pop_target_inmkt": 847763,
                            "reach_pct": 1.001203576,
                            "reach_net": 8488,
                            "trp": 3.846070954,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.029528405,
                            "eff_reach_net": 6483,
                            "eff_reach_pct": 0.7646981275
                        }
            }
        etc...
        "pagination": {
            "page": 1,
            "page_size": 1000,
            "number_of_pages": 1,
            "number_of_frames": 5,
            "number_of_spots": 5
        }
    }
}
```
### Best Audience:
##### The inventory search endpoint is utilized to find the top spots for a specific audience segment. This search can be can limited to a specific list of inventory, or inventory owned by specific company etc.... Inventory can also be filtered by a minimum number of target impressions to limit the response. 
###### Call:
_This call asks for the spots sorted by the index of the target impressions. It uses the inventory_market_list to specify the DMA when inventory is located. The measures_range_list parameter is used to limit the response to inventory that produces over 1000 impressions of the audience asked for (if this is not provided the response will include all inventory with some producing very low impressions for the audience.)_
```json
{
    "base_segment": 9072,
    "target_segment": 5559,
    "inventory_market_list": [
        "DMA501"
    ],
    "sort": {
        "measure": "index_comp_target",
        "type": "DESC"
    },
    "measures_range_list": [
        {
            "type": "imp_target",
            "min": 1000
        }
    ],
    "page": 1,
    "page_size": 1000
}
```
###### Response:
_The response is the standard inventory search response, but sorted to the specifications in the call. This response truncates frame details for space._
```json
{
    "inventory_summary": {
        "inventory_count": 1000,
        "invalid_ids": null,
        "filtered_invalid_ids": null,
        "inventory_items": [
            {
                "frame_id": 30952194,
                etc...,
                "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "9072",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 440.755178074,
                            "pct_comp_pop_target_inmkt": 20.661281,
                            "pct_comp_imp_target": 91.065665864,
                            "pct_comp_imp_target_inmkt": 91.065665864,
                            "freq_avg": 3.294405237,
                            "imp_target_inmkt": 45716.188531433,
                            "imp_target": 45716.188531433,
                            "imp_inmkt": 502.013443791,
                            "imp": 502.013443791,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 15934935,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.004214882265,
                            "reach_net": 13877,
                            "trp": 0.01388553021,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.163654901,
                            "eff_reach_net": 8853,
                            "eff_reach_pct": 0.002689089506
                        }
            },
            {
                "frame_id": 30951776,
                etc...
                        "measures": {
                            "measures_type": "Measures",
                            "period_days": 7,
                            "base_segment": "9072",
                            "target_segment": "2032",
                            "target_geo": "Defaulted to GLOBAL",
                            "market": "Defaulted to GLOBAL",
                            "index_comp_target": 440.755178074,
                            "pct_comp_pop_target_inmkt": 20.661281,
                            "pct_comp_imp_target": 91.065665864,
                            "pct_comp_imp_target_inmkt": 91.065665864,
                            "freq_avg": 3.294405237,
                            "imp_target_inmkt": 45716.188531433,
                            "imp_target": 45716.188531433,
                            "imp_inmkt": 502.013443791,
                            "imp": 502.013443791,
                            "pct_imp_inmkt": 1.0,
                            "pct_imp_target_inmkt": 1.0,
                            "pop_inmkt": 15934935,
                            "pop_target_inmkt": 329236175,
                            "reach_pct": 0.004214882265,
                            "reach_net": 13877,
                            "trp": 0.01388553021,
                            "eff_freq_min": 3,
                            "eff_freq_avg": 5.163654901,
                            "eff_reach_net": 8853,
                            "eff_reach_pct": 0.002689089506
                        }
            },
            etc...
        ],
        "pagination": {
            "page": 1,
            "page_size": 1000,
            "number_of_pages": 68,
            "number_of_frames": 42644,
            "number_of_spots": 67943
        }
    }
}
```