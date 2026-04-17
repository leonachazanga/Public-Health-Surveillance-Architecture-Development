# Public-Health-Surveillance-Architecture-Development
This project models a COVID-19 disease outbreak monitoring system which has 4 hospitals. It leverages synthetic healthcare data, along with OpenEMR and a HAPI-FHIR server, to collect, integrate and share patient data to ensure interoperability.  Visualization of COVID-19 patient information in near real time was done through Google Looker Studio. 

# System Architecture
* Five Virtual Hospital Environments: Baraga, Aspirus, Marquette, Portage, and UPHIE were each deployed in separate virtual machines
* Electronic Medical Records: OpenEMR was installed on every VM and configured with firewall protections and secure MySQL settings
* Central HAPI-FHIR Server: Hosted on the UPHIE VM to enable standardized data exchange across all sites to ensure interoperability
* Synthetic Data Generation: Synthea was used to create patient records in FHIR format 
* Data Processing: Python scripts were developed to extract and combine JSON dataset files containing the health records from the hospitals
* Visualization: A dashboard built in Google Looker Studio displays COVID-19 trends and metrics 

# Technologies Utilized
•	OS- Ubuntu Linux 
•	EMR- OpenEMR with MySQL 
•	Interoperability- HAPI-FHIR Server (customized interface) 
•	API- Postman for FHIR resource management 
•	Data generation-  Synthea 
•	Data processing- Python (including Pandas, NumPy, and Matplotlib libraries) 
•	Visualization- Google Looker Studio 

##  Setup & Workflow
# 1. Environment Setup
•	Create and deploy 5 Ubuntu-based virtual machines for each hospital
•	Configure firewall rules and secure MySQL on each node 
•	Ping and ensure all VMs communicate
2. Install Core Systems
•	Install and configure OpenEMR on each hospital VM 
•	Set up the centralized HAPI-FHIR Server 
# 3. Generate Data
•	Use Synthea to simulate patient data 
•	Export records in FHIR JSON format 
4. Data Integration
•	Use Python scripts to extract and combine datasets 
•	Send FHIR resources via Postman or API pipelines 
# 5. Visualization
•	Connect aggregated data to Google Looker Studio 
•	Build dashboards to monitor COVID-19 cases across hospitals
Challenges Encountered
•	Generating location-specific demographic data with Synthea 
•	Maintaining consistent security configurations across multiple virtual machines and MySQL 
•	Managing high memory consumption during aggregation of the large JSON datasets 

## Results
•	Built and deployed a functional multi-site health information exchange (HIE) system using OpenEMR and HAPI-FHIR 
•	Successfully generated, stored, and secured patient records derived from synthetic datasets 
•	Built a dashboard for monitoring disease trends across the multiple locations with visualization. 

# Future Improvements
•	Automate data pipelines for real-time processing
•	Enhance the dashboard with predictive analytics (e.g., outbreak forecasting) 
•	Integrate additional FHIR resources for more detailed clinical insights
•	Use a higher performing hardware

LINK- https://datastudio.google.com/s/lsTdLV2qUmQ
