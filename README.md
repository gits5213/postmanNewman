# postmanNewman


## Pre-requisites
> POSTMAN
> Node.js 

## Newman
Install the Newman from Command Line using the command 
> npm install -g newman


## Newman reporter
Install Newman HTML report by the following command
> npm install -g newman-reporter-htmlextra

## Newman CLI Command
-  [Newman CLI Commands](https://learning.postman.com/docs/collections/using-newman-cli/newman-options/)

## Generate Postman CLI Configuration Github Action
    - Select on 3 dot on the collection
    - Select Run collection 
    - Click on Configure Commands under Run on CI/CD on the Choose how to run your collection pannel 
    - Select CI/CD provider as GtiHub Action 
    - Generate API Key
    - Copy the snippet code 
    - Create .yml file under workflow under .github folder 
    - ${{ secrets.POSTMAN_API_KEY }} replace with Generated API Key 
    - Push your code 
    - Build Success in github action 

## [Newman Github action](https://github.com/marketplace/actions/newman-action)
    - Copy Example workflow file
    - Replace the API Key 
    - Replace the collection 

## Newman CLI end point execution through the github action and deploy report to github page
```
    > mkdir -p testResults
    > npm install -g newman
    > npm install -g newman-reporter-htmlextra
    > newman run "LearingRESTFULService.json" -r htmlextra --reporter-htmlextra-export testResults/htmlreport.html
    - Output the results in the testResults
    - Test marketplace action for report 
    -  Publish Github Page
```




