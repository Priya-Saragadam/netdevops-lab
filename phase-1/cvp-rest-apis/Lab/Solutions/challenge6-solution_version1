#Challeng-6 solution copy-1

from pprint import pprint as pp
from cvprac.cvp_client import CvpClient
import ssl
ssl.create_default_https_context = ssl._create_unverified_context
import requests.packages.urllib3
requests.packages.urllib3.disable_warnings()

# Update the credentials based on your Lab Setup
USERNAME = 'arista'
PASSWORD = 'arista0kw4'

if __name__ == '__main__':
    client = CvpClient()
    client.connect(nodes=['cvp'], username=USERNAME, password=PASSWORD)
    ans_part1=client.api.get_inventory()
    keys=["hostname", "modelName", "internalVersion", "ipAddress", "systemMacAddress"]
    for i in range(len(ans_part1)):
        for j in keys:
            print(ans_part1[i][j])
