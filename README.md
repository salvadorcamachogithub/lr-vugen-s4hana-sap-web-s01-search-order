Updated: 05.2025  
Script created by Salvador Camacho

This SAP script requires SoftEther VPN Client Manager to connect to DEMONET

It goes against SAP S/4HANA Fiori LaunchPad, https://sap-hana.mfdemoportal.com:44300/sap/bc/ui2/flp?sap-client=100&sap-language=EN#Shell-home

This script was created with best practices, so it is more resilient, such as:
* Transaction naming
* No third party
* One validation per transaction
* Think times at the end of each transaction to better simulate user behavior
* SAP credentials parametrized

This SAP Web script logs on, enters Tcode VA03 to search for an order, searches an order, goes to it, then signs out

Runtime Settings were set to log only on errors and generate snapshot on errors, think times 75% to 150%

This script has 5 transactions:  
S4HANA-SAP Web-S01-01 Starting URL  
S4HANA-SAP Web-S01-02 Log On  
S4HANA-SAP Web-S01-03 Enter Tcode in Apps (VA03)  
S4HANA-SAP Web-S01-04 Search Order  
S4HANA-SAP Web-S01-05 Sign Out  