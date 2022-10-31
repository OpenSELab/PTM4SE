This dataset include 3 open source projects collected from github including:
1. [dbcli/pgcli](https://github.com/dbcli/pgcli)
2. [keras-team/keras] https://github.com/keras-team/keras
3. [pallets/flask] https://github.com/pallets/flask

Each folder is composed by 
1. commit.csv. Commits message and code changeset 
2. issue.csv. Issue title and summary
3. link.csv. Links between the issue and commits
   
We clean the above three files to produce the cleand files. 
- Removed very small commits (with less than 5 LOC). 
- Remove stacktrace from issue
- Keep only commits and issues that appeared in the link.csv


