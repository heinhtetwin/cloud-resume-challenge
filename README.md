# cloud-resume-challenge
The Github repository for participating in [Cloud Resume Challenge](https://github.com/heinhtetwin/cloud-resume-challenge.git). This repository contains all the code and configuration needed for Cloud Resume API where you can get my resume data in JSON format through API.

## Contents
- [Introduction](#introduction)
- [Features](#features)
- [Deployment](#deployment)
- [Usage](#usage)
- [License](#license)
- [Contact](#contact)

## Introduction
This sample project contains 3 lambda funtions integrated with AWS API Gateway. The deployment is done via GitHub actions using SAM framework from AWS. You can create a new resume in json type, get all the resumes and get a single resume by id in this project. This project is intended for practicing AWS services and CICD integration between GitHub and AWS so there is no crazy code logic involved. I will briefly describe which features this project has in the next section. 

## Features
- **Adding New Resume**: You can create a new Resume object by calling the root URL with a POST method and defining JSON object in the body of HTTP call. I've also included the postman collection [here](./Cloud%20Resume%20Challenge.postman_collection.json).
- **Get All Resumes**: You can get all resume objects stored in this API by calling a GET method call to root URL. 
- **Get a Resume by ID**: You can get a single resume object stored in this API by calling a GET method call to ```{{base_url}}/{{id}}``` path. 

## Deployment
The deployment of this project is handled by [GitHub Actions](https://docs.github.com/en/actions). This project will be deployed whenever new commit is pushed to main branch. It typically includes only one stage and makes use of [setup-sam action](https://github.com/marketplace/actions/setup-aws-sam-cli) to deploy AWS resources such as Lambda functions, API Gateway methods and stages to our environment.

The secrets required to interact with AWS account are stored in [repository secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-a-repository) and securely referenced them in the workflow file.

## Usage
You can call my API from the web browser [here]() or use command line tool like curl ```curl -X GET "https://iz15tg1yjg.execute-api.ap-southeast-1.amazonaws.com/Prod/"``` or you can use any API client like [Postman](https://www.postman.com/) or [Insomnia](https://insomnia.rest/) .

## License
Distributed under the Apache License. See LICENSE for more information.

## Contact

Contact me through [Linkedin](https://www.linkedin.com/in/hein-htet-win/) or [Email](mailto:heinhtetwin386@gmail.com) to know more about this project and how you participated in this challenge also.

## References

You can find more details about this challenge in this link - https://cloudresumeapi.dev and this github repo - https://github.com/rishabkumar7/cloud-resume-api

You can find JSON Schema that I referenced for this API here - https://jsonresume.org/schema.