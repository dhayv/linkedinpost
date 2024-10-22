From Paycheck Stress to Automated Success: Building a Solution (1/5)"
"Why I Built an App to Replace My Budget Spreadsheet (1/5)"
"Goodbye Excel, Hello Automation: A Budget App Journey (1/5)"]

Payday. Time for my bi-weekly ritual:

Open Excel
List all bills due before next paycheck
Add them up
Subtract from my paycheck
Figure out what's left for savings/discretionary spending
Repeat in two weeks

As a developer, I realized I was solving the same equation repeatedly: "From this paycheck, what's the total of upcoming bills before my next payday?"
I built a solution using:

React (Create React App) frontend
Python (FastAPI) backend
Docker for containerization
SQLite database
Nginx reverse proxy with SSL
All hosted on a single EC2 instance

The result? A simple dashboard message:
"You'll need $1,200 for expenses until your next paycheck on Oct 17th"
One glance tells me exactly what to set aside, letting me immediately know what's available for savings and spending. No more Excel, no more manual calculations.
Initial deployment was basic: SSH into the server, sync the changes, restart Docker. Not sophisticated, but it solved my paycheck planning problem while letting me experiment with containerization and API design.
Next post: How this evolved into a proper cloud architecture with S3, CloudFront, and automated deployments.
#SoftwareEngineering #FullStack #PersonalProjects #Automation