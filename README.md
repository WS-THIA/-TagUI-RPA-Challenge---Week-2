# -TagUI-RPA-Challenge---Week-2
# https://community.aisingapore.org/groups/tagui-rpa/forum/discussion/rpa-challenge-submissions/

Here is my general approach using a mix of RPA (TagUI in turbo mode) and Selenium from Python:

1) Access ‘Purchase Order Tracking’ webpage with error handling on login failure [Selenium]
2) Access ‘Supply Chain Management’ webpage [TagUI]
3) Extract URL to Agent Territory Spreadsheet from href attribute [TagUI]
4) Access ‘Agent Territory Spreadsheet’ and store data in key:value pairs
5) Count total number of PONumber in ‘Supply Chain Management’ webpage [TagUI]
6) Iterate thru each ‘PONumber’
    6.1) Get ‘PONumber’ from ‘Supply Chain Management’ webpage [TagUI]
    6.2) Get ‘State’, ‘ShipDate’ and ‘OrderTotal’ from ‘Purchase Order Tracking’ webpage [Selenium]
    6.3) Input ‘ShipDate’, ‘OrderTotal’ and ‘Agent’ into ‘Supply Chain Management’ webpage [TagUI]
7) Click ‘submit’ button [TagUI]
8) Read and print results [TagUI]
9) Click ‘logout’ button and close ‘Purchase Order Tracking’ webpage [Selenium]
