# BA_Preprocessing
Processing of Seoul Bike Rental Station Information

## File Information
- **seoul_bicycle_master.json**<br/>
  : [Master data of Seoul Bike rental stations](http://data.seoul.go.kr/dataList/OA-21235/S/1/datasetView.do)
- **master_preprocessing.ipynb**<br/>
  : Normalizes the coordinates in the master data where they are recorded as 0.0 using the Google API
- **seoul_bicycle_maser_preprocessed.csv**<br/>
  : File containing data processed using master_preprocessing.ipynb
- **master_info_with_nearby.ipynb**<br/>
  : Adds columns of data for the nearest rental station and its distance using seoul_bicycle_maser_preprocessed.csv
- **master_info_with_nearby.csv**<br/>
  : File containing data with added information about nearby rental stations using master_info_with_nearby.ipynb
- **master_final.ipynb**<br/>
  : Processes rows where the district data has not been correctly recorded due to differences in address formatting
- **master_final.csv**<br/>
  : File containing data where 'stn_gu' has been appropriately added to all data using master_final.ipynb

## master_final.csv
- **stn_id** : Represents the id of the rental station and is of object type
- **stn_addr** : Represents the full address of the rental station and is of object type
- **stn_lat** : Represents the latitude of the rental station and is of float64 type
- **stn_lng** : Represents the longitude of the rental station and is of float64 type
- **nearby_id** : Represents the id of the nearest rental station and is of object type
- **nearby_km** : Represents the distance to the nearest rental station in km and is of float64 type
- **stn_gu** : A district data column was added for analysis as the weather data classification is done by district. This is of object type
  
ex)<br/>
<img width="791" alt="Screenshot 2023-11-10 PM 6 23 21" src="https://github.com/cyl0424/BA_Preprocessing/assets/63573867/226225b4-2d06-4b89-ac3b-1313cd888e37">
