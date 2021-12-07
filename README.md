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

## Things Patrick Needs to do
- add andrew to azure account
  - give correct permissions
  - app admin
  - devops admin
- see if josh can add github repo to function app > deployment center

## Steps that Patrick did to get here
```
    brew install azure-cli 
    az group create --location eastus --resource-group PatricksResourceGroup ## we deploy stuff to our resource groups?
    az deployment group create --resource-group PatricksResourceGroup --template-file ./azure-arm.json
```

### Notes
- I created ```./azure-pipelines.yml``` according to [this doc](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/add-template-to-azure-pipelines)
  - believe this kicks off a build on commit
  - was also following along with [a CI/CD doc for Azure Functions](https://www.azuredevopslabs.com/labs/vstsextend/azurefunctions/)
- Did not end up deploying a successful function, will continue to play with
- The above ```steps that patrick did``` were needed to create base framework for infra?
- On commit, GitHub Action kicks off
  - ```./github/workflows/main_XXXX.yml``` was auto-generated when I linked github source for function app
  - fine with me if this is how he does it, but would press on what it does