# azure-interview

## Project Definition
Welcome to the trials and tribulations of Vint! For this round, we are asking you to create a CI/CD pipeline for an Azure function. On commit to this repo, we would like a build to kickoff and re-deploy an Azure function.

## Reqs
* Infra-as-Code (reproducibility is great!)

## Non-reqs
* Wizard knowledge
  * You are more than welcome to use any resources to get the job done! Most of the battle is knowing where to go, and being able to communicate your work. Plagiarism is encouraged but not at the expense of understanding :-)

## Asks
* ARM / terraform templates for all related infra (Function / Pipeline)
* After you have completed the task, we will ask you to teardown and re-provision your infra on a demo call, where you will walk us through your code and demo your capabilities.

# Steps
1. Create an Azure function that prints 'Hello, Vint!' in your favorite programming language
2. Create an ARM template to build and deploy the Azure Function
3. Create a pipeline that takes in the above ARM template and builds/re-deploys the Function
4. Have the pipeline trigger a build on commits from repo
5. Put pipeline into an ARM template

~You will have 2 hours from the time you start reading this to complete~