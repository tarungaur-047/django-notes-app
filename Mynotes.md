I have aligned Database host name = db in .env  with mysql container name = db which is also described as db in service section of docker compose file.

I have also added ports - "3306:3306" in db which is mysql container and checkd database volume if it is there or not.
at last I have added a driver: bridge under the network name so that they can communicate efficiently. 

while deploying I was facing a issue with error Code = 137 which is OOM issue because free instances come up with only limited memory (RAM). 

but it ss deployable as containers were made smoothly and only mysql container was unable to run due to OOM issue. 
