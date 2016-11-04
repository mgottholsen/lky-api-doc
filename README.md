# lky-api
Documentation and examples for accessing various Louisville Metro public API endpoints.


Louisville Metro City News Feed
https://louisvilleky.gov/government/all/news/feed
This RSS returns the last 30 news items from all Louisville Metro Departments. This feed can be filtered by department by replacing "all" in the URL with the department ID retrieved from the departments_list.json endpoint.

Louisville Metro Events Feed
https://louisvilleky.gov/government/all/events/feed
This RSS returns the last 30 event items from all Louisville Metro Departments. This feed can be filtered by department by replacing "all" in the URL with the department ID retrieved from the departments_list.json endpoint.

Louisville Metro Departments
https://louisvilleky.gov/services/departments_list.json?limit=0
This JSON endpoint returns department name and site ID from LouisvilleKy.gov. 

Louisville Metro Forms
https://louisvilleky.gov/services/toolbox_forms.json?limit=0
All Louisville Metro Forms (both online, and print) listed on LouisvilleKy.gov. This feed can be filtered via the field "og_group_ref", which is the Department ID from the "Departments" feed.

Louisville Metro Online Services
https://louisvilleky.gov/services/toolbox_services.json?limit=0
All Louisville Metro Online Services listed on LouisvilleKy.gov. This feed can be filtered via the field "og_group_ref", which is the Department ID from the "Departments" feed.

Louisville Metro Air Quality Feed (selected for development focus)
https://sss-api-metro.smartlouisville.com/
This feed provides data from APCD, which returns Air Quality Information from multiple sites in the Louisville Metro Area, in addition to a "city-wide" AQI score. Different physical sites have varying sensors.

Services Info Lookup (selected for development focus)
api.louisvilleky.gov/api/geo/FindQuickServiceLookup?address=' + address + '&city=Louisville',
Example: https://api.louisvilleky.gov/api/geo/FindQuickServiceLookup?address=121%20FREEMAN%20AVE&city=Louisville
This API endpoint returns Metro Service information for an address. Currently this information is as follows:
LocationTableID: Unique GUID for address
InServiceDistrict: Is this address in the Metro Services Area? (Does it receive normal city services such as trash, junk and recycling services)
PoliceDivision: Louisville Metro Police Division
PoliceBeat: Louisville Metro Police Beat, sub area of Sector
PoliceSector: Louisville Metro Police Sector, subarea of Zone
PoliceZone: Louisville Metro Police Zone, area of Jefferson County
FireDistrict: Louisville Metro Fire District
CounsilDistrict: Louisville Metro Council District (see: http://louisvilleky.gov/government/metro-council, https://louisvilleky.gov/government/metro-council-district-10)
GarbageDay: Day of Garbage Pickup in Metro Services Area
YardWasteRecycleDay: Day of Yard Waste Pickup in Metro Services Area
JunkSetOutBegin: Date range start of Junk Pick Up activity by Louisville Metro
JunkSetOutEnd: Date range end of Junk Pick Up activity by Louisville Metro
LojicNeighborhoodName: Historic name of neighborhood
Address: Address matched
City: City matched
County: County matched
State: State Matched
ZipCode: Zipcode of address
Latitude: Latitiude of address
Longitude: Longitude of address

School closure sources: (selected for development focus)
No known API or method for retrieval. 
https://twitter.com/jcpsky?lang=en
