# Election_Analysis (Using Python)

## Overview of Election Audit

To assist a Colorado Board of Elections employee in an election audit of the tabulated results for the U.S. Congressional precinct in Colorado. The task is to review the data, in an automated way, to identify:

* Total overall number of votes
* A complete list of candidates who received votes
	* Total number of votes each candidate received
	* Percentage of votes each candidate won
	* The winner of the election based on popular vote
* The voter turnout for each county
	* The percentage of votes from each county out of the total count
	* The county with the highest turnout

The data provided was in .csv format and had more than 350,000 results. In order to provide this employee with the results quickly, the use of Python programming language allowed for a script to be created to answer the questions the Board of Elections was expecting.

## Resources

* **Data Source:** [election_results.csv](https://github.com/amylio/Election_Analysis/blob/main/Resources/election_results.csv)
* **Software:** Python version 3.7.6, VS Code version 1.51.1

## Election-Audit Results

The analysis showed that there were a total of 369,711 votes cast in the election. The results by county (reference county calculation script [here](https://github.com/amylio/Election_Analysis/blob/main/Resources/Source_Code_Counties.png)):

* Jefferson: 10.5% (38,855)
* Denver: 82.8% (306,055)
* Arapahoe: 6.7% (24,801)

***Denver*** had the largest voter turnout at 82.8% (306,055) of all the counties represented.

The results by candidate:

* Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
* Diana DeGette received 73.8% of the vote  and 272,892 number of votes.
* Raymon Anthony Doane 3.1% of the vote and 11,606 number of votes.

Of the candidates, ***Diana DeGette*** was the clear winner of the election with 73.8% (272,892) of the total votes cast.

## Election-Audit Summary


The script created to provide the Board of Elections with the final results of **Diana DeGette** being the winner and **Denver** being the county with the largest voter turnout can be used to calculate future and/or past elections. Depending on the data source, the script can be easily modified to add additional metrics to the results. For example, if someone wanted to know what the voter turnout by gender was, then:

* A list and dictionary would need to be added `gender()`, `gendor_votes[]`
* Extract gender from the dataset `gender_name = row[x]`
* Count the number of votes by gender `gender_votes[gender_name] += 1`,`gender = gender_votes.get(gender_name)`,`gender_percentage = float(gender) / float(total_votes) * 100`

Another modification can be made based in user input. For example, if you wanted to isolate the results by year, the following code can be added to the beginning of the script:

`print("What year would you like to see?")`,`Options = ("2017,"2018","2019")`,`user_choice = input("Make your Choice: 2017, 2018, or 2019?")`

The possibilities are endless!

**Election_Audit script can be found [here](https://github.com/amylio/Election_Analysis/blob/main/PyPoll_Challenge.py)**
