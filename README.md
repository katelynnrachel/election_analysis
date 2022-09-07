# Election Audit Challenge

## Project Overview
"A Colorado board of elections employee has given you the following task to complete sthe election audit of a recent logal congressional election." 

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

## Resources
- Data Source: election_results.csv
- Software: Python 3.10, Visual Studio Code

## Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election.
-  The candidates were:
  - Charles Casper Stockham
  - Diana DeGette
  - Raymon Anthony Doane
- The candidate results were:
  - Charles Casper Stockham received "23.0%" of the vote and "85,213" number of votes.
  - Diana DeGette received "73.8%" of the vote and "272,892" number of votes.
  - Raymon Anthony Doane received "3.1%" of the vote and "11,606" number of votes.
- The winner of the election was:
  - Diana DeGette who received "73.8%" of the vote and "272,892" number of votes.
  
  
## Challenge Overview
The purpose of the challenge was to find the voter turnout for each county, the percentage of votes from each county, and the county with the highest turnout. Using python script, such as conditional statements, decision statements, and equations, we can find the more information about the "election." 

## Challenge Summary -- Results
- How many votes were cast in this congressional election?
  - To find the total votes cast in the congressional election, I first initialized a variable, "total_votes = 0." I then used the script "total_votes = total_votes + 1" so that each vote would be added to the total count.
- Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
  <img width="387" alt="Screen Shot 2022-09-07 at 10 32 01 AM" src="https://user-images.githubusercontent.com/107594280/188942389-2d135e30-47c6-47c1-8046-911b8e81d40c.png">
 
  - Using a "for loop," I was able to retreive the name of each county from the csv file. I then able to retreive the vote count and perform an equation that then gives he percentage of total votes for each county before printing the information. 
  ```
  for county_name in county_votes:
        c_votes = county_votes.get(county_name)
        county_percentage = float(c_votes) / float(total_votes) * 100

        county_results = (
            f"{county_name}: {county_percentage:.1f}% ({c_votes:,})\n")
        print(county_results, end="")
        txt_file.write(county_results) 
  ```
- Which county had the largest number of votes?
  - The results show that Denver had 82% of the total vote at 306,055 votes, making Denver the county with the largest number of votes. 
- Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
  <img width="383" alt="Screen Shot 2022-09-07 at 10 51 54 AM" src="https://user-images.githubusercontent.com/107594280/188945626-1c0826ae-334f-4d58-9292-562956078a56.png">

  - To find the breakdown of votes for the candidates, I used a similar script and format that was used to find the breakdown of county votes.
  ```
  for candidate_name in candidate_votes:
        votes = candidate_votes.get(candidate_name)
        vote_percentage = float(votes) / float(total_votes) * 100
        candidate_results = (
            f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")

        print(candidate_results)
        txt_file.write(candidate_results)
  ```
- Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
  - The results show that Diana DeGette won the election at 272,892 votes, which was 73.8% of the total vote.
- Election-Audit Summary: In a summary statement, provide a business proposal to the election commission on how this script can be used—with some modifications—for any election. Give at least two examples of how this script can be modified to be used for other elections.
  - This script could prove to be useful for any election given certain modifications, where it can then analyze other data sets. If newer data sets collected wider information about each voter, such as gender, the script could be adjusted to find what percentage of male/female/non-binary persons voted for each candidate and from which county. This script can also be used to find other demographics, such as which counties favored each candidate.

## Overall Results
<img width="361" alt="Screen Shot 2022-09-07 at 11 06 27 AM" src="https://user-images.githubusercontent.com/107594280/188948140-5d6be7c3-57ef-43d7-b62e-787cf91527f9.png">
