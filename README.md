# FR_DBVulnScan_and_Report

Last Updated: 12/1/23

-Problem-
As part of the RA-5 control FedRAMP requires databases be scanned for vulnerabilities and this requirement presents a unique challenge when operating in a cloud environment. As cloud customers don't control the DB engine it can be difficult to know if that engine version has active CVEs. FedRAMP is requiring CSPs to "scan" their cloud databases and report upon DB engine versions with active CVEs. To date there are no commerical off the shelf tooling that provides this functionaltiy. The following Python scripts aim to solve this problem.

-Basic Functionality-
1. Ingests a inventory of cloud databases either from a CSV or by quering the APIs of major cloud providers
2. Extracts the DB engine version applicable to each db instance in the inventoruy and searches vulnerability sources for CVEs applicable to that engine version
3. Reports on in-use DB engine versions with active CVEs
4. Can send emails or open support tickets with the associated cloud providers to inquire on the status of vulnerable DB-engine versions
