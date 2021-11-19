# Challenge

How can we help <ins>tech-aware people </ins> to distinguish real from fake online content (or parts of it: visuals, audio, text) by empowering them with effortless independent tools to spot deepfakes that are meant to pollute or cause harm in their information consumption and especially when there is uncertainty such as Covid-19, political elections, war, economic recession, etc. instead of being manipulated by or unintentionally perpetuating misinformation?


## Deepfake video and audio 

Here are 320 deepfake videos and their associated audio files as well. Forensics can be conducted on different parts of the evidence, 
video, audio, eye gaze, face movements and more.

``` avi, wav
```

<img width="300px" src="https://user-images.githubusercontent.com/62607582/139797015-f1044424-d697-4f72-854f-9fd85a560f86.gif">

<img width="300px" src="https://user-images.githubusercontent.com/62607582/139797124-1927c382-61ea-4986-ab72-a38378b8479f.gif"> 

<iframe width="300px" src="https://user-images.githubusercontent.com/62607582/139797151-244a5c68-b80c-4f5b-86b7-2119de1c0a6c.mp4"> 





## Deepfake text 

``` csv
0	zawvrk	justin timberlake really one of the goats if y...	human	human
1	narendramodi	Thank you @PMBhutan for your gracious prayers ...	human	human
2	ahadsheriff	Theory: the number of red lights you will hit ...	human	human
3	AINarendraModi	Respects on the Upt of the I good with the peo...	bot	rnn
4	kevinhooke	Might give the BASIC #10Liner game contest ano...	human	human
```

!> Explore the datasets in the AWS S3 bucket. 
```AWS CLI
aws s3 cp s3://h4g-hague4th/H4G_Hague_4thEdition/Deepfake_alert/ --recursive

aws s3 sync s3://h4g-hague4th/H4G_Hague_4thEdition/Deepfake_alert/ <local-folder> 
```