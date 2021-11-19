# Challenge 

How can we help a <ins>drone airspace control center</ins> to provide and monitor the best path possible per drone by creating a smooth link between one map tile to another when a drone has to complete an operation over a bigger distance instead of calculating separate parts of the flight path within each single tile?

## Would the location of existing transport infrastructure help drone flights? 


!> Explore the datasets in the AWS S3 bucket. 
```AWS CLI
aws s3 cp s3://h4g-hague4th/H4G_Hague_4thEdition/Drone_flight_control/ --recursive

aws s3 sync s3://h4g-hague4th/H4G_Hague_4thEdition/Drone_flight_control/ <local-folder> 
```
