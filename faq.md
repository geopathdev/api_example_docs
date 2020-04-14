## This FAQ will point to links in the other documents that provide more information

##### Q: How do I get the impressions for a specific list of inventory?
###### A: _The Inventory Search endpoint allows you to provide a specific list of IDs to get impressions_

##### Q: How do I get targeted audience impressions for a specific list of inventory?
###### A: _The Inventory Search endpoint allows you to provide target segment ids, as well as a specific list of inventory ids._

##### Q: How do I get the Reach and Frequency for a specific list of inventory
###### A: _There are two methods depending on what you actually need:_
   * _When R/F for each spot in the list is required:_
     * _The Inventory Search endpoint provides a measures object that includes R/F based on the period_days parameter used when sending the search body (default is 7 days when parameter is not provided)._
   * _When R/F for the list as a whole is required:_
     * _The Summary/Search endpoint can be used to find all measures, including R/F for the inventory list as a whole_

##### Q: How can I download information to cache / use in my own system
###### A: _The Inventory Search endpoint can provide inventory and measures for all inventory (or a subset based on your search parameters). These JSON responses can be stored and used by your organization as you wish (in accordance with any Geopath licensing agreements). The data includes measures for global & target audiences and markets as well as R/F based on your specific search parameters._

##### Q: How do I find the best _________ for inventory?
###### A: 
  * Zip Code or DMA: 
    * Using the GET ```https://api.geopath.org/v2.1/inventory/measures/homes``` endpoint
    * Using the POST ```https://api.geopath.org/v2.1/inventory/measures/homes/spots``` endpoint
  * Audience Segment:
    * Using the ```https://api.geopath.org/v2.1/inventory/measures/summary/segments``` endpoint


