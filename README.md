# Elastic SIEM Home Lab

## Objective
The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps
First step we will be Connecting our Elastic Agent to our host

![CYB4bqa](https://github.com/danielgee0415/ElasticSIEM/assets/20386303/dad1c0d3-521a-4045-826f-8a4b29bc8a87)

After successfully connecting to our Kali Linux host i use nmap commands to generate tasks

![image](https://github.com/danielgee0415/ElasticSIEM/assets/20386303/34d8af89-9bbb-4882-84d8-2ad513763e6e)

Then we look for our nmap scans in our logs

![image](https://github.com/danielgee0415/ElasticSIEM/assets/20386303/73876a17-ec7e-44a5-8276-827e1fdf8fb3)

And we view details and confirm that it indeed was our entry

![image](https://github.com/danielgee0415/ElasticSIEM/assets/20386303/2cf2d789-d39a-49df-a894-7ff0d76738eb)

Now we set up a visualisation with the horizontal axis being timestamp and vertical axis beinr count of records

![image](https://github.com/danielgee0415/ElasticSIEM/assets/20386303/053ec562-9932-4334-a799-eb5f3af8b710)

We move on to setting up a new rule to alert us when the nmap command was used

![image](https://github.com/danielgee0415/ElasticSIEM/assets/20386303/e2644f73-6c4d-497c-b9a6-389e1f0a1d0d)

We successfully created our Nmap Scan Detection rule which will send an alert to our email whenever an nmap command has been used

![image](https://github.com/danielgee0415/ElasticSIEM/assets/20386303/596cf4ef-42d8-43f7-9a85-a8ee0e1a4233)
