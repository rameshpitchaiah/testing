 <div class="center">
<p align="center"><img src="https://user-images.githubusercontent.com/523933/49741959-91a1da00-fc65-11e8-911f-521331f87174.png" align="center" width="20%" height="20%"></p>
  <h3 align="center">Clear Street</h3>
  <p align="center">
  SRE Developer Screening
</p>
</div>

---

This repository contains parts of your interview. You will be given your own private version of this repository to complete your work. Only you and and Clear Street members can view your repository.

You should take a branch of `master` to do your work. **Once you are satisified, create a pull-request to merge your work into `master`. The pull-request will let us know you are finished.**

## Q&A

The following sections contain questions that you should answer inline in this README.md file. Below each question, insert your response using tasteful Markdown choices.

### Tooling

Provide your perference for each of the categories below:

1. operating system?

1. text editor?

1. terminal type?

1. scripting languauge?

### Pros & Cons

Provide some salient pros and cons for each of the scenarios described below:

1. windows vs. linux

1. mono-repository vs. multi-repository

1. strongly typed vs. untyped languages

1. monolith vs. microservice architecture


### Git

Answer the following questions regarding git:

1. Describe your preferred git branching model

1. What is a git remote?

1. What is git LFS?

1. Provide the command you would use to stage, commit, and push local changes

1. What does `git config` do?

1. What does `git stash` do?

1. Is the `master` branch of a repository special?

### Docker

Answer the following questions regarding Docker:

1. What is Docker?

1. How would you compare Docker versus a virtual machine?

1. What is a Docker image?

1. What is a Docker container?

1. What is Docker Hub?

1. How do you create a Docker container?

1. Do I lose my data when the Docker container exits?

1. What, in your opinion, is the most exciting potential use for Docker?

1. What is `docker-compose`?

### Kubernetes

Answer the following questions regarding k8s:

1. What is the difference between a `Deployment` and a `StatefulSet`

1. What does k8s use to maintian its state, and how does this system work (2-3 sentences max)

1. What are some prominent differences between Docker Swarm and k8s, what is a good use case for each system

1. Describe k8s namespaces and how networking/service communication works inter/intra-namespace

1. What are the minimum requirements to build a high availability cluster in k8s?

1. Does `ImagePullPolicy: Always` do as the name impliies: always pull the image of the pod?

1. Do you have to use Docker with k8s? If not, what is an alternative and what are its pros/cons

### CICD and Cloud Deployments

Answer the following questions regarding testing, deployment, and CICD processes in general:

1. What is your preferred CICD tool?

1. Describe the challenges of building a CICD process with a monorepo. How does this contrast with a multirepo?

1. How do you manage deployments to a cloud provider such as AWS or GCE? Management includes deployment, maintainence and auditing an environment.

1. How do you deal with user management in a cloud environment?


## Project

Lets build a simple CICD Program (don't worry, it's not that complex).

Our CICD program will work as follows:

1. The user will give the link to a github repo
2. In this github repository, there will be a file called `cicd.sh` which will contain the script that your program will run
3. Your CICD program will start a Ubuntu Docker container with the provided repository, run the `cicd.sh` file, capture any output, and store it in a `cicd.log` file.
4. Your program should output the exit code of the CICD script as well.

Example usage/output of this program would be as follows:

```
$> # A proper repository
$> mycicd https://github.com/someuser/properrepo
Cloning https://github.com/someuser/properrepo...
Running CICD script...
(CICD output...)
CICD script exited with code 0
Storing output in cicd.log
$>
```

```
$> # A improper repository
$> mycicd https://github.com/someuser/badrepo
Cloning https://github.com/someuser/badrepo...
There is no cicd.sh! Exiting!
$>
```

You can chose to write your CICD program in any language. Please provide instructions for running your program, and also a short description of your thought process.

This repository contains a `cicd.sh`, so you can use this repository as your test.

Good Luck!
