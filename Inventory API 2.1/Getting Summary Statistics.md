## Use Case: Search for Summary Inventory Statistics

Using the `/inventory/summary/search` endpoint, you can search for summary statistics across a set of inventory. 

#### Sample: Search for summary of all impressions

###### Call:
_This call is asking for global 0+ impressions across all operators and media types._
```json
{
     "base_segment": 2032,
     "target_segment": 2032,
     "sort": {
         "measure": "pct_comp_imp_target",
         "type": "desc"
     },
     "measures_range_list": [
         {
             "type": "imp",
             "min": 0
         }
     ]
 }
```
###### Response:
_The response total is 65 Billion impressions across 639K frames / 734K spots_
```json
{
    "summary_level_list": [
        "Universe"
    ],
    "summaries": [
        {
            "measures_type": "aggregate_measures",
            "period_days": 7,
            "base_segment": "2032",
            "target_segment": "2032",
            "target_geo": "Defaulted to GLOBAL",
            "market": "Defaulted to GLOBAL",
            "index_comp_target": 100.0,
            "pct_comp_pop_target_inmkt": 1.0,
            "pct_comp_imp_target": 1.0,
            "pct_comp_imp_target_inmkt": 1.0,
            "freq_avg": 198.64833991,
            "imp_target_inmkt": 6.54022196020442E10,
            "imp_target": 6.54022196020442E10,
            "imp_inmkt": 6.54022196020442E10,
            "imp": 6.54022196020442E10,
            "pct_imp_inmkt": 1.0,
            "pct_imp_target_inmkt": 1.0,
            "pop_inmkt": 329236175,
            "pop_target_inmkt": 329236175,
            "reach_pct": 100.0,
            "reach_net": 329236175,
            "trp": 19864.833990993,
            "eff_freq_min": 3,
            "eff_freq_avg": 198.64833991,
            "eff_reach_net": 329236175,
            "eff_reach_pct": 100.0,
            "summarizes": {
                "type": "Universe",
                "summarizes_id_list": null,
                "id": null,
                "name": null,
                "geometry": null
            },
            "frames": 639946,
            "spots": 734804
        }
    ],
    "pagination": {
        "page": 1,
        "page_size": 1000,
        "number_of_pages": 1,
        "number_of_summaries": 1
    }
}
```


_Adding an additional search parameter into the call can change this._
#### Sample: Search for summary of all impressions of a specific company.
###### Call
_This call is asking for global 0+ impressions for a single operator across all their media types._
```json
{
    "base_segment": 2032,
    "target_segment": 2032,
    "operator_name_list": [
        "OUTFRONT"
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
    ]
}
```
###### Response:
_The response total is 1.3 Billion impressions across 64K frames / 75K spots_
```json
{
    "summary_level_list": [
        "Universe"
    ],
    "summaries": [
        {
            "measures_type": "aggregate_measures",
            "period_days": 7,
            "base_segment": "2032",
            "target_segment": "2032",
            "target_geo": "Defaulted to GLOBAL",
            "market": "Defaulted to GLOBAL",
            "index_comp_target": 100.0,
            "pct_comp_pop_target_inmkt": 1.0,
            "pct_comp_imp_target": 1.0,
            "pct_comp_imp_target_inmkt": 1.0,
            "freq_avg": 39.507893961,
            "imp_target_inmkt": 1.30074249248078E10,
            "imp_target": 1.30074249248078E10,
            "imp_inmkt": 1.30074249248078E10,
            "imp": 1.30074249248078E10,
            "pct_imp_inmkt": 1.0,
            "pct_imp_target_inmkt": 1.0,
            "pop_inmkt": 329236175,
            "pop_target_inmkt": 329236175,
            "reach_pct": 99.999977203,
            "reach_net": 329236100,
            "trp": 3950.788495465,
            "eff_freq_min": 3,
            "eff_freq_avg": 39.524948379,
            "eff_reach_net": 329094040,
            "eff_reach_pct": 99.956828723,
            "summarizes": {
                "type": "Universe",
                "summarizes_id_list": null,
                "id": null,
                "name": null,
                "geometry": null
            },
            "frames": 64619,
            "spots": 75004
        }
    ],
    "pagination": {
        "page": 1,
        "page_size": 1000,
        "number_of_pages": 1,
        "number_of_summaries": 1
    }
}
```

#### Sample: Very specific summary search.
###### Call
_This call is asking for local market Hispanic Persons 25-44 impressions for two specific operators poster inventory that generate over 100,000 impressions in a specific market._
```json
{
    "base_segment": 2032,
    "target_segment": 7619,
    "target_geography_list": [
        "DMA803"
    ],
    "inventory_market_list": [
        "DMA803"
    ],
    "operator_name_list": [
        "OUTFRONT",
        "Clear Channel"
    ],
    "media_type_list": [
        "Poster"
    ],
    "measures_range_list": [
        {
            "type": "imp",
            "min": 100000
        }
    ]
}
```
###### Response:
_The response includes all the same previous information about total impressions that would be there if asking for global information, but also includes the narrower market information where the  total is 779 million impressions across 3.9K frames / 3.9K spots_
```json
{
    "summary_level_list": [
        "Universe"
    ],
    "summaries": [
        {
            "measures_type": "aggregate_measures",
            "period_days": 7,
            "base_segment": "2032",
            "target_segment": "7619",
            "target_geo": "DMA803",
            "market": "DMA803",
            "index_comp_target": 121.079337699,
            "pct_comp_pop_target_inmkt": 0.106013,
            "pct_comp_imp_target": 0.1266190738,
            "pct_comp_imp_target_inmkt": 0.1283598383,
            "freq_avg": 49.232208946,
            "imp_target_inmkt": 9.71006195374118E7,
            "imp_target": 9.86522281540164E7,
            "imp_inmkt": 7.56471968508678E8,
            "imp": 7.79126123679314E8,
            "pct_imp_inmkt": 0.9709236355,
            "pct_imp_target_inmkt": 0.9842719354,
            "pop_inmkt": 18604423,
            "pop_target_inmkt": 1972303,
            "reach_pct": 99.999779752,
            "reach_net": 1972299,
            "trp": 4923.210051266,
            "eff_freq_min": 3,
            "eff_freq_avg": 49.237457196,
            "eff_reach_net": 1972088,
            "eff_reach_pct": 99.989120716,
            "summarizes": {
                "type": "Universe",
                "summarizes_id_list": null,
                "id": null,
                "name": null,
                "geometry": null
            },
            "frames": 3934,
            "spots": 3952
        }
    ],
    "pagination": {
        "page": 1,
        "page_size": 1000,
        "number_of_pages": 1,
        "number_of_summaries": 1
    }
}
```

