# ELK-Florida-US-Demo (Need actual file to test)

1. Clone/download this project into local system and copy the Senthilkumar1.json file to some other location and delete the base file from the logstash folder.
2. Open Docker container  
3. Open the command prompt from the root folder where you copied the files and then run the below command
                                 **docker-compose up -d**
4. Once the all the instances are up and running, Before placing the json data file inside logstash folder, we need to use the script(create_loanbook_index.json) to create the loan book data structure in elasticsearch. This need to run from Postman. Following are the parameters need to considered. 
    ######    HTTP Request Type : PUT 
    ######    URL Pattern : http://localhost:9200/_template/loanbook_index   <br>
5. Once the structure is created in the ElasticSearch, Need to place the Senthilkumar1.json file into logstash folder. <br>
6. This is a ELK stack implementation to read Json files from a shared location using Logstash and pushing the same to Elasticsearch. <br>
7. The Logstash will read the files, creates the index with index _id for each record in Elasticsearch. <br>
8. Kibana is used to create a Map and view the loan book data with Geolocation information. We can search and view the specific customer details based on latitude and longitude.<br>
9. The recording steps to create a geo location map is available in the below path: (https://fdplc.sharepoint.com/sites/CMCDataServices/Shared%20Documents/Forms/AllItems.aspx?ct=1651245711673&or=OWA%2DNT&cid=6b3444e5%2De47e%2D75cc%2Dc971%2D7271593a8979&ga=1&OR=Teams%2DHL&CT=1694517894736&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiIyNy8yMzA4MDQwODYzNiIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D&id=%2Fsites%2FCMCDataServices%2FShared%20Documents%2FData%20Engineering%20and%20Data%20Science%2F3%2D%20Deliveries%2FCustomers%2FIBM%20sustainable%20cloud%20%2D%20Projects%2FDEMO%2FESG%20%2DELKstack%2Dlocal%2DDemo%2D27%2D04%2D2023%2Emp4&viewid=df39eeff%2Dc6b2%2D4c89%2Dba44%2D8d92da4de5ac&parent=%2Fsites%2FCMCDataServices%2FShared%20Documents%2FData%20Engineering%20and%20Data%20Science%2F3%2D%20Deliveries%2FCustomers%2FIBM%20sustainable%20cloud%20%2D%20Projects%2FDEMO)

###### Elastic Search URL : https://localhost:9200 (to test whether the server is up and running )
###### Kibana URL : http://localhost:5601/ (to create a Map )