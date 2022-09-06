# CI/CD tools

In this guide, you will learn about tools to help you improve your experience in your development process using docker.

## Authors

- Jefferson Oña @jeffqev

## Topics

- [CI CD Tools](#ci-cd-tools)
- [on-cloud tools vs on-premise tools vs self-hosted](#on-cloud-tools-vs-on-premise-tools-vs-self-hosted)
  - [on-cloud tools](#on-cloud-tools)
  - [on-premise](#on-premise-tools)
  - [self-hosted](#self-hosted)
- [Some Tools you can use](#some-tools-you-can-use)

### CI CD Tools

Understanding what is CI/CD and how pipelines works is the hardest part the tools only facilitate the execution and order of the jobs and each tool has its syntax but they are very similar

### on-cloud tools vs on-premise tools vs self-hosted

As we know the job execution in a pipeline is the execution of one or several commands so we need a place where this command is going to be executed and to do that exist several types of servers execute it.

#### on-cloud tools

these types of servers run in the cloud and the cost of execution depends on how many minutes it takes for the command to execute.

Example: [Travis CI](https://docs.travis-ci.com/user/tutorial/).

#### on-premise tools

In this type of server, the tool is installed on a server and if you are the owner of the server this would have no cost, however, it can also be installed on amazon instances or its equivalent to the cloud provider and the cost would depend on the instance.

Example: [Jenkins](https://www.jenkins.io/doc/).

#### self-hosted

This is a mix of the previous types, you can use the tool in the cloud however you can specify the server to execute the commands on, this can be your server or one in the cloud.

Most on-cloud tools have this option to reduce costs on commands that take a long time to execute

Example: [Github actions](https://docs.github.com/es/actions/hosting-your-own-runners/about-self-hosted-runners).

### Some Tools you can use

- Jenkins
- CircleCI
- TeamCity
- Bamboo
- GitLab
- Buddy
- Travis CI
- Codeship
- GoCD
- Wercker

[Read more about these tools on](https://katalon.com/resources-center/blog/ci-cd-tools)

## References

- [ci/cd tools](https://katalon.com/resources-center/blog/ci-cd-tools)
