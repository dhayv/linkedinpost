
# From Paycheck Stress to Automated Success: Building a Solution (1/5)"
-   "Why I Built an App to Replace My Budget Spreadsheet (1/5)"
-   "Goodbye Excel, Hello Automation: A Budget App Journey (1/5)"]

Payday. Time for my bi-weekly ritual:

1.  Open Excel
2.  List all bills due before next paycheck
3.  Add them up
4.  Subtract from my paycheck
5.  Figure out what's left for savings/discretionary spending
6.  Repeat in two weeks

As a developer, I realized I was solving the same equation repeatedly: "From this paycheck, what's the total of upcoming bills before my next payday?"

I built a solution using:

-   React (Create React App) frontend
-   Python (FastAPI) backend
-   Docker for containerization
-   SQLite database
-   Nginx reverse proxy with SSL
-   All hosted on a single EC2 instance

The result? A simple dashboard message: "You'll need $1,200 for expenses until your next paycheck on Oct 17th"

One glance tells me exactly what to set aside, letting me immediately know what's available for savings and spending. No more Excel, no more manual calculations.

Initial deployment was basic: SSH into the server, sync the changes, restart Docker. Not sophisticated, but it solved my paycheck planning problem while letting me experiment with containerization and API design.

Next post: How this evolved into a proper cloud architecture with S3, CloudFront, and automated deployments.

#SoftwareEngineering #FullStack #PersonalProjects #Automation


## Architecture diagram

[![](https://mermaid.ink/img/pako:eNp1UlFrwjAQ_ishe9nAgZOxYR8Gtp1DGOJ0g0HrQ0wutqxNSprOifjfd7G1VtkOkkvuvvvucpcd5VoA9ajM9IYnzFjy7seKoJTVam1YkZDnYBDhIhNVWqY4LGu_E5Ea4DbVqo1yMn2ZTD-jw07m8A2mBDIz-mfbiWzZQ82_wES1IoFWlqUKTAfqZDSbRGNWWtTEZwhV4gIR-tH14u01tYDHm44ToadLMB9FgQGGqDkwbsmoKMjYYNZzxrr429snF_GXGQs5mV1Vzhg2TWhTfpT4NN_oDerlAXJgqJ31zjNWliFIAnxAZJpl3pWUw2G_3-M608ZbZfjcCyg_dqkJGNwPH0A0AZsEe3ARIFZH6kch7-AfajdpV0bX1MylzXjm85GY9mgOJmepwF-0c-6Y2gRyiKmHRwGSVZmNaaz2CGWV1Yut4tSzpoIeNbpaJ9STLCvxVhUCJxOmDL9G3lj3v7IazD8?type=png)](https://mermaid.live/edit#pako:eNp1UlFrwjAQ_ishe9nAgZOxYR8Gtp1DGOJ0g0HrQ0wutqxNSprOifjfd7G1VtkOkkvuvvvucpcd5VoA9ajM9IYnzFjy7seKoJTVam1YkZDnYBDhIhNVWqY4LGu_E5Ea4DbVqo1yMn2ZTD-jw07m8A2mBDIz-mfbiWzZQ82_wES1IoFWlqUKTAfqZDSbRGNWWtTEZwhV4gIR-tH14u01tYDHm44ToadLMB9FgQGGqDkwbsmoKMjYYNZzxrr429snF_GXGQs5mV1Vzhg2TWhTfpT4NN_oDerlAXJgqJ31zjNWliFIAnxAZJpl3pWUw2G_3-M608ZbZfjcCyg_dqkJGNwPH0A0AZsEe3ARIFZH6kch7-AfajdpV0bX1MylzXjm85GY9mgOJmepwF-0c-6Y2gRyiKmHRwGSVZmNaaz2CGWV1Yut4tSzpoIeNbpaJ9STLCvxVhUCJxOmDL9G3lj3v7IazD8)