## More About Me – [Take a Look!](http://www.mjakaria.me) 

### [GitHub Actions](https://docs.github.com/en/actions/about-github-actions/understanding-github-actions)
GitHub Actions is a automation (CI/CD) service by GitHub. It's automated all kind of repository related process & actions that will run one or more jobs. Workflows are defined in the `.github/workflows` directory in a repository. It's has two main areas
- Continuous Integration (CI/CD) - Code `Test`, `Build`, `Deployment`, new app release. 
- Source Code Management (SCM) - Automate `code reviews`, `issues management` etc.

 It lets you automate workflows like `testing code`, `building applications`, `deploying to servers`, `sending notifications`, and more — all triggered by GitHub events like `push`, `pull` `request`, `release`, etc.

#### The `three` main building blocks in GitHub Actions are:
1. **[Workflows](https://docs.github.com/en/actions/about-github-actions/understanding-github-actions)**
   A workflow is a set of automated processes that are triggered based on specific events in your GitHub repository. Common events include pushes to the repository, pull requests, or the creation of new issues.
   - A workflow is a YAML file that defines what should happen (CI/CD logic).
   - It lives in `.github/workflows/` in your repo.
   - You can have multiple workflows for different purposes (`test`, `deploy`, `release`).
```yaml
name: Deploy Website
on: push
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - run: echo "Deploying site..."
```

2. [Jobs](https://docs.github.com/en/actions/about-github-actions/understanding-github-actions)
   A job is a set of steps in a workflow that is executed on the same runner. Each step is either a shell script that will be executed, or an action that will be run.
   - A job is a set of steps that run in the same runner (environment).
   - Jobs can run in parallel or sequentially.
   - Each job runs on its own VM or container.
```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - run: echo "This is a job"
```

3. [Steps](https://docs.github.com/en/actions/about-github-actions/understanding-github-actions)
   - Steps are individual tasks inside a job (`checkout code`, `run tests`).
   - They can run commands or use actions (reusable pieces of code).
```yaml
steps:
  - name: Checkout Code
    uses: actions/checkout@v3
  - name: Install Dependencies
    run: npm install
```

#### Others building blocks in GitHub Actions are:
##### Events
An event is a specific activity in a repository that triggers a workflow run. For example, an activity can originate from GitHub when someone creates a pull request, opens an issue, or pushes a commit to a repository.
- `push` – When someone pushes to the repo.
- `pull_request` – When a PR is opened or updated.
- `schedule` – Runs on a cron schedule.
- `workflow_dispatch` – Manual trigger via GitHub UI
```yaml
on:
  push:
    branches: [main]
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
A runner is a server that runs your workflows when they're triggered. Each runner can run a single job at a time. GitHub provides Ubuntu Linux, Microsoft Windows, and macOS runners to run your workflows.
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
