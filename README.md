# Usage-lan2
Prerequisites:
* Your repo need to have 2 branches: `devlops` & `production` 1
* Create CodeDeply Application for each directory in repo (callcenter, work ..) and the EC2 target (for each environment)
# Workflow
1. Developer commit source code to `devlops` branch
1. Github create a trigger to CircleCI
1. CirlceCI call CodeDeploy Application to deploy source code to Dev Environment
1. After test Dev Environment, Developer create a pull request.
1. Administrator click approve for `Hold` job in CircleCI
1. Admin click `Merge` in Github for merge `devlops` to `production` branch.
1. CircleCI process job in production branch
1. CircleCI call CodeDeploy Application to delploy source code to Prod Enviroment

# Result
![screenshot for instruction](images/1.png)
![screenshot for instruction](images/2.png)
![screenshot for instruction](images/3.png)
![screenshot for instruction](images/4.png)
