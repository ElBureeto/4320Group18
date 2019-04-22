# Group 18 Sprint 2 Design Document

## Deployment Environment

[ec2-18-223-33-215.us-east-2.compute.amazonaws.com:3333](ec2-18-223-33-215.us-east-2.compute.amazonaws.com:3333)

## Functional Requirements

1. User views data regarding pull requests that are proposed and merged into project
	- Provide visual of a repo shows how many pull requests are there and how many of them are merged
	- After choosing a repo, the system should be able to get number of commit, number of pull requests and the accept rate from database, and show on the site.
	- There should be a chart or figure in frontend showing the number of merged request, total request and the accept rate. 
	- Update visual every day to keep an accurate countdown.
2. User can identify inactive repos and either archive them or direct developers to them
	- Provide visual to user of how much time before repo has been inactive for a year
	- The system should be able to get last edited date of the project from database and judge it as active or unactive.
	- The system should provide buttons for user to archive the project or direct developers.
	- Updates visual each day to keep an accurate countdown
3. User wants to view the top contributors
  	- Show the user with highest commits number as the top contributer of the repo
	- The system should be able to get contributor username and commits from database and communicate with frontend
	- The system should provides a list of ranked contributors and mark the first place.
  	- Update every day to keep an accurate countdown
	
## Necessary for Whole System

1. Data Sources
	- We need the Augur data tables
2. Functions
	- We need SQL functions that send the data from the data tables to the server
	- We need VJS/Python scripts to interpret the data and put it into helpful graphics
3. Web Server
	- We need our EC2 instance to be up and running

## Visual Representation of System

![VRoS](VRoS.png)

## Visual Representation of Front End

![VRoFE](VRoFE.png)

