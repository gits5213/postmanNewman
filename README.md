# postman Newman Learing from Scratch 

## Youtub Video Tutorials 
- [GITS - API test Series-00 | What is API? | POSTMAN | Sample Request & Response](https://youtu.be/qniB-uDonDk)
- [GITS - API test Series-01 | What is API? | POSTMAN | GET Request & Response | Assertion | Test | Schema Validation](https://youtu.be/tHoiBne7SIE)
- [GITS - API test Series-02 | What is API? | POSTMAN | POST Request & Response | Assertion | Test | Schema Validation](https://youtu.be/yOnJhjyqY34)
- [GITS - API test Series-03 | What is API? | POSTMAN | Customize Assertion | Global Variable](https://youtu.be/biOUwIcEFPA)
- [GITS - API test Series-04 | POSTMAN Runner | Newman | CLI | Newman HTML Report](https://youtu.be/5W8Eu01gW_M)
- [GITS - API test Series-05 | Github Action | Newman | CLI | CICD | Newman HTML Report](https://youtu.be/oA2ZMAEeGV0)
- [GITS - API test Series-5a | Github Action | Newman | CLI | CICD | Github Workflow Debug](https://youtu.be/uzHgAJQsYd8)
- [GITS - API test Series-5ab | Github Action | Newman | CLI | CICD | Artifact Newman HTML Report ](https://youtu.be/hFMgJDD0x9g)

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
