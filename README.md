[![LinkedIn][linkedin-shield-lapissoft]][linkedin-url-lapissoft]
[![Facebook-Page][facebook-shield-lapissoft]][facebook-url-lapissoft]
[![Youtube][youtube-shield-lapissoft]][youtube-url-lapissoft]

## Visit Us [Lapis Soft](http://www.lapissoft.com)

### GitHub Actions for DevOps Engineer Professional

GitHub Actions is a platform provided by GitHub that allows you to automate workflows directly within your GitHub repository. It enables you to define custom CI/CD (Continuous Integration/Continuous Deployment) workflows using YAML syntax. With GitHub Actions, you can automate tasks such as building, testing, and deploying your code. Here are some key concepts related to GitHub Actions:

- ***Workflow:*** A workflow is a set of automated processes that are triggered based on specific events in your GitHub repository. Common events include pushes to the repository, pull requests, or the creation of new issues.
- ***Job:*** A job is a set of steps that are executed on the same runner. You can define multiple jobs within a workflow, and they can run in parallel or sequentially.
- ***Step:*** A step is a single task within a job. It can be a shell command, a script, or an action. Actions are reusable units of code that encapsulate a task, and they can be created by the GitHub community or by yourself.
- ***Runner:*** A runner is a machine where your jobs are executed. GitHub provides hosted runners with various operating systems (Linux, macOS, Windows), or you can set up your own self-hosted runner.
- ***Workflow File (YAML):*** Workflows are defined using YAML files stored in the .github/workflows directory of your repository. These files specify the jobs, steps, and actions that should be executed when certain events occur.
Here's a simple example of a GitHub Actions workflow that runs on each push to the main branch:
```YAML
  name: CI

  on:
    push:
      branches:
        - master

  jobs:
    build:
      runs-on: ubuntu-latest

      steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install dependencies
        run: npm install

      - name: Run tests
        run: npm test
```
In this example, the workflow is triggered on each push to the main branch. It has one job (build) that runs on an Ubuntu-based runner. The steps include checking out the code, setting up Node.js, installing dependencies, and running tests.

You can customize GitHub Actions workflows to suit your specific needs, integrating them with various services and tools to automate your software development processes.

## Courtesy of Jakir

[![LinkedIn][linkedin-shield-jakir]][linkedin-url-jakir]
[![Facebook-Page][facebook-shield-jakir]][facebook-url-jakir]
[![Youtube][youtube-shield-jakir]][youtube-url-jakir]

### Have a good day, stay with me
<!-- Personal profile -->

[linkedin-shield-jakir]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url-jakir]: https://www.linkedin.com/in/jakir-ruet/
[facebook-shield-jakir]: https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white
[facebook-url-jakir]: https://www.facebook.com/jakir-ruet/
[youtube-shield-jakir]: https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white
[youtube-url-jakir]: https://www.youtube.com/@mjakaria-ruet/featured

<!-- Company profile -->

[linkedin-shield-lapissoft]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url-lapissoft]: https://www.linkedin.com/company/lapis-soft/
[facebook-shield-lapissoft]: https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white
[facebook-url-lapissoft]: https://www.facebook.com/GoLapisSoft/
[youtube-shield-lapissoft]: https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white
[youtube-url-lapissoft]: https://www.youtube.com/@LapisSoft/featured



