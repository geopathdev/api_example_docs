### Use Case: Get all the spot ids for a specific operator.

##### Step 1: use the `inventory/spot/id/search` endpoint to get all the spot_ids for a specific operator.
###### Call:
_To get an accurate count of inventory include a minimum of 0 impressions in the measures_range_list_
```json
{
    "operator_name_list": [
        "Intersection"
    ],
    "measures_range_list": [
        {
            "type": "imp",
            "min": 0
        }
    ],
    "page_size": 50001
}
```

###### Response:
_As you can see the response includes a count of total inventory, and a pagination object. For this call there are 2 pages since the page size is capped at 50,000 spot results. A second call is needed to get the remainder of the spot_ids_
```json
{
    "inventory_summary": {
        "inventory_count": 26602,
        "pagination": {
            "page": 1,
            "page_size": 50001,
            "number_of_pages": 2,
            "number_of_frames": 29960,
            "number_of_spots": 53359
        },
        "frame_list": [
            {
                "frame_id": 50187935,
                "spot_id_list": [
                    50190589
                ]
            },
            {
                "frame_id": 30819503,
                "spot_id_list": [
                    30819637,
                    30819639,
                    30819640,
                    30819638,
                    30819503,
                    30819636
                ]
            },
...etc
```

###### Call:
_This call is the same as the first one, but adds a page key/value to only get the second page of results._
```json
{
    "operator_name_list": [
        "Intersection"
    ],
    "measures_range_list": [
        {
            "type": "imp",
            "min": 0
        }
    ],
    "page": 2,
    "page_size": 50001
}
```
###### Result:
_The second page result is the same as the first one, but for a smaller inventory count as this is the second and final page. The pagination object still included the overall count for the search._
```json
{
    "inventory_summary": {
        "inventory_count": 3358,
        "pagination": {
            "page": 2,
            "page_size": 50001,
            "number_of_pages": 2,
            "number_of_frames": 29960,
            "number_of_spots": 53359
        },
        "frame_list": [
            {
                "frame_id": 30542309,
                "spot_id_list": [
                    30542309
                ]
            },
etc...
```
 

