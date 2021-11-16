# Challenge

How can we help <ins>water managers</ins> to better understand and monitor saltwater intrusion in the IJsselmeer by combining satellite data with existing point monitoring resulting in an alert (early warning) tool which considers the changes in weather and water quality including their potential consequences instead of relying solely on in-situ data?


## Bathymetry shows the shape of land below water

<img width="auto" src="https://raw.githubusercontent.com/Hackathon-for-Good/H4G_Hague_4thEdition/main/remote%20sensing%20for%20water%20salinity/qgis-bin_FHno26cE2E.png"> 


## Salt measurements and land displacement data can be combined to identify hotspots of saltwater intrusion

https://www.satellietdataportaal.nl/?base=brtachtergrondkaart&res=0.5&datemin=27-09-2020&loc=52.27488%2C4.405518%2C8z

https://waterinfo.rws.nl/#!/kaart/zouten/


!> Explore the datasets in the AWS S3 bucket. 
```AWS CLI
aws s3 cp s3://h4g-hague4th/H4G_Hague_4thEdition/Remote_sensing_for_water_salinity_monitoring/ --recursive
```
