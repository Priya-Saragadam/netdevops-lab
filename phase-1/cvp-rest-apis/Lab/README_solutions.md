# CVP REST APIs Lab

In this folder your skills will be tested on what you have learned about CVP REST APIs.

From the `Terminal` of `Programmability IDE` perform the following operations.

NOTE: Please feel free to login to CVP and take help from the `REST API Explorer`

## Challenge-1

- Delete any existing session cookie files
- Authenticate and obtain a new session cookie from CVP and store it into file named `cvpcookiefile`

API: cvpservice/login/authenticate.do
Solution: 
```
curl -X 'POST' 'https://cvp-url/cvpservice/login/authenticate.do' -H 'accept: application/json' -H 'Content-Type: application/json' -d '{ "password":"pwd", "userID":"username"}' -c cookiefile | jq
```
## Challenge-2

- Get the list of all containers currently on CVP

API: /cvpservice/inventory/containers
Solution: 
```
curl -X 'GET' 'https://cvp-url/cvpservice/inventory/containers' -H 'accept: application/json' -b cvpcookiefile | jq
```

## Challenge-3

- List of all devices that are in CVP inventory

API: cvpservice/inventory/devices
Solution: 
```
curl -X 'GET' 'https://cvp-url/cvpservice/inventory/devices' -H 'accept: application/json' -b cvpcookiefile | jq
```

## Challenge-4

- Get all configlets on CVP

API: cvpservice/configlet/getConfiglets.do
Solution: 
```
curl -X 'GET' 'https://cvp-url/cvpservice/configlet/getConfiglets.do?startIndex=0&endIndex=0&sortOrder=Ascending' -H 'accept: application/json' -b cvpcookiefile | jq
```

## Challenge-5

- Get list of all devices under container named `Leaf`

API: cvpservice/provisioning/getNetElementList.do
Solution: 
```
curl -X 'GET' \
  'https://cvp-url/cvpservice/provisioning/getNetElementList.do?nodeId=container_3b14f1a2-d5df-40e9-a778-35ef9ad0b9b0&startIndex=0&endIndex=0&ignoreAdd=true' \
  -H 'accept: application/json' -b cvpcookiefile.txt | jq
```

## Challenge-6

- Using `cvprac` in python script print the following information for all switches in  CVP inventory:
  - Hostname
  - Model Name
  - EOS Version
  - IP Address
  - MAC Address
Solution:
```
from pprint import pprint as pp
from cvprac.cvp_client import CvpClient
import ssl
ssl.create_default_https_context = ssl._create_unverified_context
import requests.packages.urllib3
requests.packages.urllib3.disable_warnings()

USERNAME = 'username'
PASSWORD = 'password'

if __name__ == '__main__':
    client = CvpClient()
    client.connect(nodes=['cvp'], username=USERNAME, password=PASSWORD)
    ans_part1=client.api.get_inventory()
    keys=["hostname", "modelName", "internalVersion", "ipAddress", "systemMacAddress"]
    for i in range(len(ans_part1)):
        for j in keys:
            print(ans_part1[i][j])
```

# Update the credentials based on your Lab Setup

The solutions for these challenges are present under `Solutions` folder, however we would encourage to try to figure our the solution from the REST API Explorer.
