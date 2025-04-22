## More About Me – [Take a Look!](http://www.mjakaria.me) 

### GitHub Actions?
GitHub Actions is a Continuous Integration/Continuous Deployment `CI/CD` platform built into GitHub. It lets you automate workflows like `testing code`, `building applications`, `deploying to servers`, `sending notifications`, and more — all triggered by GitHub events like `push`, `pull` `request`, `release`, etc.

#### Core Concepts

| Term         | Description                                                                                                                      |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| **Workflows** | A YAML file that defines the automation process, triggered by GitHub events like push, PR, release, etc.                         |
| **Events**    | A specific activity on GitHub that triggers a workflow (e.g., `push`, `pull_request`, `release`, `schedule`).                    |
| **Jobs**      | A set of steps that execute on the same runner. Jobs run in parallel by default.                                                 |
| **Steps**     | A single task within a job. Steps can run shell commands or use actions.                                                         |
| **Actions**   | A reusable piece of code or script that can be shared across workflows. GitHub and the community provide many pre-built actions. |
| **Runners**   | A server that runs your workflow jobs. GitHub provides hosted runners, or you can host your own.                                 |

##### Workflows
A workflow is a set of automated processes that are triggered based on specific events in your GitHub repository. Common events include pushes to the repository, pull requests, or the creation of new issues. A workflow is the top-level configuration file that defines `what automation you want to run` and when to run it. Some important bullet points;
- It’s written in YAML and stored in `.github/workflows/`.
- Each workflow can have multiple jobs, and each job has multiple steps.
- You can have as many workflow files as you want in a repository.
```yaml
name: Deploy Website
on: push
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - run: echo "Deploying site..."
```
##### Events
An event is what triggers a workflow to run. Some important bullet points;
- `push` – When someone pushes to the repo.
- `pull_request` – When a PR is opened or updated.
- `schedule` – Runs on a cron schedule.
- `workflow_dispatch` – Manual trigger via GitHub UI
```yaml
on:
  push:
    branches: [main]
```
##### Jobs
A job is a set of steps that are executed on the same runner. You can define multiple jobs within a workflow, and they can run in parallel or sequentially.
- A job is a group of steps that run together on the same runner (machine).
- Jobs run in parallel by default (unless you set dependencies between them).
- Each job runs in a clean environment unless you persist data using artifacts or caching.
```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - run: echo "This is a job"
```
##### Steps
A step is a single task within a job. It can be a shell command, a script, or an action. Actions are reusable units of code that encapsulate a task, and they can be created by the GitHub community or by yourself.
```yaml
steps:
  - name: Checkout Code
    uses: actions/checkout@v3
  - name: Install Dependencies
    run: npm install
```
##### Actions
An action is a custom application for the GitHub Actions platform that performs a complex but frequently repeated task. Use an action to help reduce the amount of repetitive code that you write in your workflow files.
```yaml
- name: Set up Node.js
  uses: actions/setup-node@v3
  with:
    node-version: '18'
```
##### Runners
A runner is a machine where your jobs are executed. GitHub provides hosted runners with various operating systems (Linux, macOS, Windows), or you can set up your own self-hosted runner.
```yaml
runs-on: ubuntu-latest
```

## With Regards, `Jakir`

[![LinkedIn][linkedin-shield-jakir]][linkedin-url-jakir]
[![Facebook-Page][facebook-shield-jakir]][facebook-url-jakir]
[![Youtube][youtube-shield-jakir]][youtube-url-jakir]

### Wishing you a wonderful day! Keep in touch.

<!-- Personal profile -->

[linkedin-shield-jakir]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url-jakir]: https://www.linkedin.com/in/jakir-ruet/
[facebook-shield-jakir]: https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white
[facebook-url-jakir]: https://www.facebook.com/jakir.ruet/
[youtube-shield-jakir]: https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white
[youtube-url-jakir]: https://www.youtube.com/@mjakaria-ruet/featured
