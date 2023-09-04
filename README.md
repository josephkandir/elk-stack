# elk-stack
Elastick Search + Logstash + Kibana Stack Docker Compose

# Note:
You can use your own password but password should contain atleat 6 characters and should be alphanumeric
Replace **changem1**, **changem2** and **your_userame** with your desired set value

# Steps
1. docker compose up -d (or docker-compose up -d)
2. You may see kibana is refussing to connect elastixsearch and that is because of credentials, please run below command
  ```
curl -XPOST -u elastic:changeme1 -k 'http://0.0.0.0:9200/_security/user/your_username' -H "Content-Type: application/json" -d '{
  "password" : "changeme2",
  "roles" : [ "kibana_system" ]
}'
  ```
3. 
