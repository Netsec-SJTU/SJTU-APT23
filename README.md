# SJTU-APT23
Considering the outdated and limited coverage of existing open-source APT traffic datasets, we have developed a comprehensive APT traffic database called SJTU-APT23, which includes over 700 traffic files from 25 APT organizations. The size of the dataset is 323G. It involves two main parts: building an APT malware sample corpus and collecting APT malicious traffic data.
## Construction of APT malware sample corpus
To ensure that the APT traffic we collect is up-to-date, we first obtain the latest and still valid APT samples. These samples are sourced from the open platforms VirusTotal and MalwareBazaar. By integrating samples from these two sources, we collected a total of 4696 APT samples from 68 organizations, achieving extensive coverage.
## Collect APT malicious traffic
We chose Falcon Sandbox and ANY. RUN, two open-source sandboxes. We have developed a crawler system that runs scripts daily from January to April 2023 to complete traffic collection.
Most of the crawled traffic is invalid or noisy, and some samples evade analysis by generating the smallest data packets. We filtered out pcap files smaller than 4KB. In addition, considering the unpredictability of APT malware and the presence of noisy ARP and NBNS requests, we have removed files that lack TCP/UDP protocol and TCP connection failures or have no further activity.
Finally, we obtained 726 valid pcap files from 4696 APT samples, totaling 427MB. Due to the high cost of manual screening, we only screened data from 25 organizations. The dataset, named SJTU-APT23, is the most comprehensive APT traffic dataset to date, covering the widest range of APT organizations. The composition of the dataset is shown in the table, and the organizational distribution is shown in the following figure.

<div align="center">
  
| Num | APT organization | APT traffic volume | Num | APT organization | APT traffic volume|
| :----: | :----: | :----: | :----: | :-----: | :----: |
| 1 | APT1 | 39 | 14 | APT-C-37 | 12 |
| 2 | APT10 | 60 | 15 | Bitter | 8 |
| 3 | APT19 | 8 | 16 | BlackTech | 28 | 
| 4 | APT21 | 13 | 17 | DarkHotel | 25 |
| 5 | APT28 | 57 | 18 | Donot | 38 |
| 6 | APT29 | 24 | 19 | EnergeticBear | 24 |
| 7 | APT30 | 19 | 20 | EquationGroup | 61 |
| 8 | APT32 | 24 | 21 | FIN7 | 5 |
| 9 | APT34 | 4 | 22 | GorgonGroup | 172 |
| 10 | APT-C-01 | 7 | 23 | MuddyWater | 13 |
| 11 | APT-C-23 | 9 | 24 | SideWinder | 7 |
| 12 | APT-C-27 | 16 | 25 | Winnti | 12 |
| 13 | APT-C-36 | 41 | 26 | Total | 726 |

</div>

<div align="center">
    <img align="center" src="https://github.com/Netsec-SJTU/SJTU-APT23/blob/main/APT_organization.png" width="500" height="350" />
</div>


## Non APT malicious traffic dataset
In addition to the APT traffic dataset SJTU-APT23, we also need to collect a non APT malware traffic dataset for subsequent experiments. This traffic was collected from Malware Traffic Analysis. net (MTA), an open-source malware traffic sharing website that provides over 1600 pcap files. These pcap files contain binary files marked as malicious by IDS and antivirus software, covering various types of malware such as ransomware, spam, and macro viruses. Many researchers have already used this dataset for malware detection. From June 2013 to October 2023, we captured a total of 2965 malware pcap files, with a total size of nearly 14GB. We refer to this dataset as the MTA dataset.

# Complete Dataset
The size of the full dataset is 323G and it is not possible to show all of it. Only part of the sample dataset is shown here, if you need the full dataset, contact：zhang_heming@sjtu.edu.cn
