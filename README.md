# Github-Actions
This repository consists of the Github Actions certification course hands-on


**Github Actions**
1. Fully integrated with GitHub
2. Github Actions can be triggered with any response on the Github
3. You can easily login the logs
4. Easy to write and share and action workflows are based on yaml files and Actions are based on js (or other languages that compile to js)

**Components of Actions**
1. Events -> (triggers) -> Workflows -> (uses) -> Actions

Event triggers the Workflow and each workflow has number of jobs present. Each job has number of steps present which holds the code for different actions that gets triggered simultaneously.
Actions basically have tasks that will be performed such as : checkout the code, build the app, deploy the app, create issues.
You can also use "Shell" commands if you want to perform all the above actions via shell commands
