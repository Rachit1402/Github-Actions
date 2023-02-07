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

**Events**
1. Web hook events -> PR, Issues, pushes
2. Scheduled Events -> Via cronx sequence
3. Manual Events -> Very useful when developing actions to test it. -> workflow_dispatch events

**Runner**
1. Github_hosted_runner
2. Self_hosted_runner -> You need to configure this hosted runner with the required configurations.

**Actions**
1. Reusable unit of codes
2. NodeJS runtime or docker container environments
3. Can be public or locally

Conditional statements can also be used in the yaml files

**Dependent Jobs**
By default all job runs independently but there are certain scenarios where you are required to run the jobs sequentialls or in a pre-definde order. In that scenario you could use the **needs** keyword

**Build Matrix**
This is very useful when we have to test the same code accross multiple versions.
This is defined in the following ways : 
  strategy:
  matrix:
    node: [6,8,10]
  steps:
    - uses: actions/setup-node@v2
      with:
        node-version: {{matrix.node}}
