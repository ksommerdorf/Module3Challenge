# Election Audit Analysis
## Overview of Election Audit
The Colorado Board of Elections has asked for an audit of the tabulated election results for US Congressional precinct in Colorado. In this project we are teaming up with Tom, a Colorado Board of Elections' employee and Seth, Tom's manager, to create an automated audit using Python. The three primary voting methods included in this data are mail-in ballots, punch cards, and direct recording electronic (DRE) counting machines. The election results produced by the code include total vote count, county vote counts, largest county turnout, candidate vote count, and the winning candidate vote count and percentage. These results from this election audit will be submitted to the election commission for review. The overall goal is for this code to not only audit the congressional district elections but to audit senatorial districts and local elections as well.

## Analysis and Challenges
The election_results.csv file was downloaded and read into Python 3.10.4 Visual Studio Code 1.65.2.

![SS0](https://user-images.githubusercontent.com/57520471/160316678-d1884fb1-b671-4bdc-bd92-85ea0326348a.png)

Step 1: Initialized a county list that will hold the names of the counties and a dictionary that will hold the county as the key and the votes cast for each county as the values.

![SS1](https://user-images.githubusercontent.com/57520471/160316704-cba25828-eeca-44a2-90b4-a6f1faf4ddc2.png)

Step 2: Initialized an empty string that will hold the county names for the county with largest turnout and a variable that will hold the number of votes of the county that had the largest turnout.

![SS2](https://user-images.githubusercontent.com/57520471/160316717-efdf3fe0-d836-471a-bb04-525843989cf9.png)

Step 3: Created a for loop that reads the election results and produces the names of the county from each row.

![SS3](https://user-images.githubusercontent.com/57520471/160316754-88b68ed4-354f-4248-8e7d-88a0045ef8a8.png)

Step 4: Created a decision statement with a logical operator to check if the county name in Step 3 is located in the county list created in Step 1. 

![SS4](https://user-images.githubusercontent.com/57520471/160316726-07b8e8f2-709c-4830-9dd0-8b96ee468700.png)

Step 5: Created a second decision statement that tracks each county's vote count and adds the results to the dictionary created in Step 1.

![SS5](https://user-images.githubusercontent.com/57520471/160316765-1095a74c-9417-4f08-bb81-6341e4af755e.png)

Step 6a-d: Created a repetition statement to get the county from the county dictionary created in Step 1 and prints a statement with the current county, its percentage of the total votes, and its total votes to the command line.

![SS6 1](https://user-images.githubusercontent.com/57520471/160316773-f6cbd469-5329-4f88-9a7c-997f9e9bebf1.png)

Step 6e-f: Created another decision statement that determines the county with the largest vote count and then adds that county and its vote count to the variables created in Step 2.

![SS6 2](https://user-images.githubusercontent.com/57520471/160316778-8095096f-3512-4412-be42-2e709d235bb1.png)

Step 7: Created a final print out statement with the county with the largest turnout. 

![SS7](https://user-images.githubusercontent.com/57520471/160317287-ef7920c8-b20d-40ea-84b8-c1203b5ba8c3.png)


Step 8: Created a for loop that saves the largest county turnout, each candidate's vote count and percentage, and the winning candidate vote count and percentage to a text file. 

![SS8](https://user-images.githubusercontent.com/57520471/160316794-a1bad085-60d4-4039-851e-59661f485be1.png)

## Election-Audit Results
* There were 369,711 votes casted in this congressional election.
* Number of votes and percentage of total votes for each county in the precinct:
  * Jefferson: 38,855 votes; 10.5%
  * Denver: 306,055 votes; 82.8%
  * Arapahoe: 24,801 votes; 6.7%
* Denver had the largest number of votes.
* The number of votes and the percentage of the total votes each candidate received:
  * Charles Casper Stockham: 85,213 votes; 23.0%
  * Diana DeGette: 272,892 votes; 73.8%
  * Raymon Anthony Doane: 11,606 votes; 3.1%
* Diana DeGette won the election with 272,892 votes which is 73.8% of the total votes.

Election-Audit Results On Text File

![textfileSS](https://user-images.githubusercontent.com/57520471/160316842-6d0330a8-ae81-4a32-a5dc-423fb336e9fe.png)

Election-Audit Results In Terminal

![terminalSS](https://user-images.githubusercontent.com/57520471/160316848-2f1586a1-fa2d-4873-8924-a70fd5f708f1.png)

## Election-Audit Summary
This script can be used, with modifications, to produce results for any election. For example, with local elections, the code can be modified to break down the number of votes and percentage by city within each county. Also with senatorial district elections, the code can be modified to break down the voting statistics not only by county but by voting district. The code can also be modified to show the percentage of vote based on political parties, rural vs urban areas, and age group. The potential of this code could be an easy, automated solution for all future election audit analysis needs. 
