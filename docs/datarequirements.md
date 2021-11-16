# Let's get started 

## Requirements
1. AWS account (kickstart working in the cloud)
- [Sign up the link](https://portal.aws.amazon.com/billing/signup?nc2=h_ct&src=header_signup&redirect_url=https%3A%2F%2Faws.amazon.com%2Fregistration-confirmation#/start)

- [Create IAM user to configure AWS CLI](https://console.aws.amazon.com/iam/) 

- [Create access keys](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-prereqs.html)

2. AWS CLI

- [Download installer](https://awscli.amazonaws.com/AWSCLIV2.msi)
- Or use command line
```
msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi
```

## Data through AWS CLI 

```AWS CLI
#list all files/datasets in the folder
aws s3 s3://h4g-hague4th/<challenge-name>/ --recursive --human-readable --summarize

#get files
aws s3 cp s3://h4g-hague4th/H4G_Hague_4thEdition/<challenge-name> LocalFolder --recursive

```

## Data through python script
```Python 

# install requirements 
import boto3
import os

# bucket name is h4g-hague4th and folder for challenges is added in
# Prefix='H4G_Hague_4thEdition/<your challenge>'

def download_all_objects_in_folder():
    s3_resource = boto3.resource('s3')
    my_bucket = s3_resource.Bucket('h4g-hague4th')
    objects = my_bucket.objects.filter(Prefix='H4G_Hague_4thEdition/<your-challenge>/')
    for obj in objects:
        path, filename = os.path.split(obj.key)
        my_bucket.download_file(obj.key, filename)
```
## Data through google colab 

```Python
!pip install s3fs 

import pandas 
import s3fs
df = pd.read_file('s3://h4g-hague4th/H4G_Hague_4thEdition/<your-challenge>/<file_name>')
```





