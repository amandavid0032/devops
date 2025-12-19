## 📔 ES5
---
## 📘 Devops Learning 

---
## 📘 What is DevOps?

DevOps is an approach that improves collaboration between developers and operations teams to automate and streamline software development, testing, deployment, and maintenance.

```php
DevOps Lifecycle Diagram

 Plan
   ↓
 Code
   ↓
 Build
   ↓
 Test
   ↓
 Release
   ↓
 Deploy
   ↓
 Operate
   ↓
 Monitor
   ↺ (Feedback to Plan)

```
---

## 📘 What is Waterfall Model ?
In the context of DevOps, the Waterfall model is best understood as a **traditional software development methodology** The Waterfall model is a linear, sequential software development life cycle (SDLC) in which each phase must be completed fully before the next phase begins.

**Phases of the Waterfall Model**

1. Requirement Analysis
.Business and technical requirements are gathered and documented.
.Output: Software Requirement Specification (SRS)

2. System Design
.Architecture, database design, and system interfaces are defined.
.Output: Design documents

3. Implementation (Development)
.Code is written based on the design specifications.

4. Testing
.Unit, integration, system, and acceptance testing are performed.
.Defects are fixed before moving forward.

5. Deployment
.The application is released to production.

6. Maintenance
.Bug fixes, enhancements, and support activities occur post-release.

**Limitations of waterfall model**
1. High Amounts of risk and uncertainty 
2. No Working software is produced until late during the life cycle 
3. One an application is in the testing stage it is very difficult to go back and change something that was not well thought out in the concept stage 
4. Not a good model for complex and object-oriented projects 
5. Not suitable for the projects where requirements are at a moderate to high risk of changing 

```php
Waterfall Model Diagram

Requirement Analysis
        ↓
   System Design
        ↓
 Implementation
        ↓
     Testing
        ↓
    Deployment
        ↓
   Maintenance
```
---

## 📘 What Is Agile Methodology?
Agile methodology is an iterative and incremental software development approach that focuses on flexibility, customer collaboration, continuous feedback, and rapid delivery of working software.

Instead of delivering the entire product at the end, Agile delivers the software in small, usable increments called iterations or sprints.

**Key Characteristics of Agile**

1. Iterative Development
Work is divided into short cycles (typically 1–4 weeks), allowing frequent releases.

2. Customer Collaboration
Customers or stakeholders are involved continuously to provide feedback and clarify requirements.

3. Adaptive to Change
Requirements can change at any time, even late in development.

4. Early and Continuous Delivery
Working software is delivered frequently, reducing risk.

5. Cross-Functional Teams
Developers, testers, and operations work together closely.

**Agile vs Waterfall (Quick Comparison)**

| Aspect               | Agile      | Waterfall  |
| -------------------- | ---------- | ---------- |
| Development style    | Iterative  | Sequential |
| Change handling      | Easy       | Difficult  |
| Customer involvement | Continuous | Limited    |
| Delivery             | Frequent   | End-only   |
| Risk                 | Low        | High       |


```php
        ┌───────────────┐
        │  Requirements │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ Sprint Planning│
        └───────┬───────┘
                ↓
   ┌────────────────────────┐
   │ Design → Develop → Test │
   └───────────┬────────────┘
               ↓
        ┌───────────────┐
        │ Review & Demo │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ Release       │
        └───────┬───────┘
                ↓
        ┌───────────────┐
        │ Retrospective │
        └───────┬───────┘
                ↑
          (Next Sprint)
```
---

## 📘 What Is Source Code Management (SCM) in DevOps?
Source Code Management (SCM) is the practice of tracking, managing, and controlling changes to source code throughout the software development lifecycle.

In DevOps, SCM is the foundation of CI/CD pipelines and team collaboration.

**Key Functions of SCM**

1. Version control of code
2. Collaboration among multiple developers
3. Change history and traceability
4. Branching and merging
5. Rollback to previous versions
6. Integration with CI/CD tools

**Centralized Version Control System (CVCS)**

Definition
A Centralized Version Control System uses a single central repository that stores the entire codebase. All developers connect to this central server to access and commit code.
```js
          Central Repository
                 │
      ┌──────────┼──────────┐
      ↓          ↓          ↓
 Developer A  Developer B  Developer C

```

Advantages of CVCS

1. Simple and easy to understand
2. Centralized control and administration
3. Suitable for small teams

Limitations of CVCS

1. Single point of failure
2. Requires network connection
3. Limited branching and merging
4. Slower collaboration


**Distributed Version Control System (DVCS)**
Definition
A Distributed Version Control System allows each developer to have a complete local copy of the repository, including full history.

```
 Developer A        Developer B        Developer C
 (Full Repo)        (Full Repo)        (Full Repo)
      │                 │                 │
      └────────────── Central Repo ───────────────┘
```

Examples of DVCS
1. Git
2. Mercurial

Advantages of DVCS

1. No single point of failure
2. Faster operations (local commits)
3. Strong branching and merging
4. Works offline
5. Ideal for DevOps and CI/CD

Limitations of DVCS

1. Slightly steeper learning curve
2. Larger local storage usage

---
# 📘 DevOps Linux Commands 

## 🔹 User & System Information
```bash
whoami            # Current logged-in user
uname -a          # Kernel and system info
uptime            # System running time and load
id                # User and group IDs
```

---

## 🔹 File & Directory Management
```bash
pwd                     # Present working directory
ls -l                   # Detailed file listing
ls -a                   # Show hidden files
cd /var/log             # Change directory
cd ..                   # Go to parent directory
mkdir app               # Create directory
mkdir -p a/b/c          # Create nested directories
rmdir empty_dir         # Remove empty directory
```

---

## 🔹 File Operations
```bash
touch config.txt        # Create empty file
cp file1 file2          # Copy file
cp -r dir1 dir2         # Copy directory
mv file.txt ..          # Move file to parent directory
mv ../file.txt .        # Move file from parent to current
mv old.txt new.txt      # Rename file
rm file.txt             # Delete file
rm -rf dir/             # Delete directory forcefully
```

---

## 🔹 File Viewing & Editing (Logs & Configs)
```bash
cat file.txt            # View file content
less file.txt           # Scrollable view
head file.txt           # First 10 lines
tail file.txt           # Last 10 lines
tail -f app.log         # Live log monitoring
nano config.yaml        # Edit file using nano
vi Dockerfile           # Edit file using vim
```

---

## 🔹 Permissions & Ownership (Critical for DevOps)
```bash
ls -ld file             # View permissions
chmod 755 script.sh     # Change permissions
chmod +x script.sh      # Make executable
chown user:user file    # Change owner
chown -R user:user dir/ # Recursive ownership
```

---

## 🔹 Process Management
```bash
ps -ef                  # List processes
ps -ef | grep nginx     # Find process
top                     # Live process view
htop                    # Enhanced process viewer
kill PID                # Kill process
kill -9 PID             # Force kill
```

---

## 🔹 Disk & Memory Monitoring
```bash
df -h                   # Disk usage
du -sh folder/          # Folder size
free -h                 # Memory usage
lsblk                   # Block devices
```

---

## 🔹 Networking & Connectivity
```bash
ip a                    # IP addresses
ping google.com         # Network check
curl http://localhost   # API/service test
wget URL                # Download file
ss -tuln                # Open ports
```

---

## 🔹 Search & Logs
```bash
grep "ERROR" app.log   # Search text
find /etc -name "*.conf" # Find files
journalctl -u nginx     # Service logs
```

---

## 🔹 Package Management (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install docker.io
sudo apt remove package
```

---
# 📘 What Is Configuration Management?
Configuration Management (CM) is the disciplined practice of systematically managing, controlling, and documenting changes to a system so that it maintains integrity, consistency, and reliability over time.

In DevOps, CM ensures that:
1. The current design, configuration, and build state of a system is:
 . Known
 . Verified
 . Trusted

2. Systems behave predictably across environments (dev, test, staging, prod).


1. Configuration management is the pratice of handling changes systematically so that system maintains its integrity over time 
2. configuratio management (CM) ensures that the current design and build state of the system is known, good & trusted
3. it doesn't rely on the tacit knowledge of the development team

```js
Plan → Code → Build → Test → Release → Deploy → Operate → Monitor
                                   ↑
                         Configuration Management

```
---


## 📘 CI/CD

# GitHub Actions – Developer Workflows Summary

## Overview

**GitHub Actions** is a platform provided by GitHub to **automate developer workflows** directly within a repository. While **CI/CD (Continuous Integration / Continuous Deployment)** is one of the most common use cases, GitHub Actions supports many other workflows related to development, collaboration, and repository management.

---

## CI/CD Is One of Many Workflows

CI/CD focuses on:
- Automatically building code
- Running tests
- Packaging applications (e.g., Docker images)
- Deploying to servers or cloud platforms

However, GitHub Actions goes beyond CI/CD and can automate **non-build, non-deployment workflows** as well.

---

## Common Developer Workflows Automated by GitHub Actions

### 1. Adding New Contributors

When a new contributor joins a project, GitHub Actions can automate tasks such as:
- Sending a welcome message on the first pull request
- Automatically labeling the contributor as `first-time-contributor`
- Assigning reviewers or mentors
- Enforcing contribution guidelines

**Trigger examples:**
- `pull_request` (opened)
- `issues` (opened)

---

### 2. Pull Request Creation Workflow

When a pull request (PR) is created, GitHub Actions can:
- Run automated checks (linting, tests, build)
- Validate code formatting and standards
- Check commit messages
- Add labels based on changed files
- Notify reviewers

**Trigger example:**
- `pull_request`

This ensures that every PR meets quality and compliance standards before review.

---

## Organizational and Team Workflows

GitHub Actions is widely used to automate **organizational and collaboration tasks**, not just code execution.

### Review the Pull Request

Automated actions can:
- Assign reviewers automatically
- Block merging if checks fail
- Enforce mandatory approvals
- Add review reminders

---

### Fix the Issue

Issue-related workflows can:
- Automatically assign issues to team members
- Link issues to pull requests
- Move issues across project boards
- Add labels based on issue content

**Trigger examples:**
- `issues`
- `issue_comment`

---

### Merge to Master Branch

Before merging to the `master` branch, GitHub Actions can ensure:
- All CI checks have passed
- Required reviews are completed
- No merge conflicts exist
- Branch protection rules are satisfied

After merge, Actions can:
- Trigger deployment pipelines
- Create releases and tags
- Notify stakeholders

---

## Summary

- GitHub Actions is a **workflow automation platform**, not just a CI/CD tool.
- CI/CD is only one part of a broader automation ecosystem.
- Actions can automate:
  - Contributor onboarding
  - Pull request validation
  - Code review processes
  - Issue management
  - Secure and controlled merges to `master`

By automating both **technical** and **organizational** workflows, GitHub Actions improves code quality, team productivity, and project consistency.

```js
# =========================================================
# File: .github/workflows/php-composer-ci.yml
# Purpose: CI pipeline for PHP projects using Composer
# Triggered on: push & pull request to master branch
# =========================================================

name: PHP Composer CI

# ---------------------------------------------------------
# WHEN THIS WORKFLOW RUNS
# ---------------------------------------------------------
# 1. Every time a commit is pushed to the `master` branch
# 2. Every time a Pull Request is opened/updated for `master`
# ---------------------------------------------------------

on:
  push:
    branches: [ "master" ]
  pull_request:
    branches: [ "master" ]

# ---------------------------------------------------------
# PERMISSIONS (SECURITY BEST PRACTICE)
# Read-only access to repository contents
# ---------------------------------------------------------

permissions:
  contents: read

# ---------------------------------------------------------
# JOB DEFINITIONS
# ---------------------------------------------------------

jobs:
  build:
    name: Build & Validate PHP Project

    # -----------------------------------------------------
    # RUNNER (GitHub-hosted Virtual Machine)
    # A fresh Ubuntu machine is created for every run
    # -----------------------------------------------------
    runs-on: ubuntu-latest

    steps:
      # ---------------------------------------------------
      # STEP 1: CHECKOUT SOURCE CODE
      # This pulls the repository code into the runner
      # ---------------------------------------------------
      - name: Checkout repository
        uses: actions/checkout@v4

      # ---------------------------------------------------
      # STEP 2: VALIDATE COMPOSER FILES
      # Fails if composer.json or composer.lock is invalid
      # --strict makes warnings fail the build
      # ---------------------------------------------------
      - name: Validate composer.json and composer.lock
        run: composer validate --strict

      # ---------------------------------------------------
      # STEP 3: CACHE COMPOSER DEPENDENCIES
      # Speeds up CI by reusing vendor directory
      # Cache is invalidated when composer.lock changes
      # ---------------------------------------------------
      - name: Cache Composer dependencies
        id: composer-cache
        uses: actions/cache@v3
        with:
          path: vendor
          key: ${{ runner.os }}-php-${{ hashFiles('**/composer.lock') }}
          restore-keys: |
            ${{ runner.os }}-php-

      # ---------------------------------------------------
      # STEP 4: INSTALL DEPENDENCIES
      # Uses cached dependencies if available
      # --prefer-dist for faster downloads
      # --no-progress for clean CI logs
      # ---------------------------------------------------
      - name: Install Composer dependencies
        run: composer install --prefer-dist --no-progress

      # ---------------------------------------------------
      # STEP 5: RUN TESTS (OPTIONAL)
      # Uncomment after adding test script in composer.json
      # Example script:
      # "scripts": { "test": "vendor/bin/phpunit" }
      # ---------------------------------------------------
      # - name: Run test suite
      #   run: composer run-script test

# =========================================================
# WHAT HAPPENS ON COMMIT / PULL REQUEST
# ---------------------------------------------------------
# 1. Developer pushes code or opens PR to master
# 2. GitHub triggers this workflow
# 3. Ubuntu runner starts
# 4. Code is checked out
# 5. Composer files are validated
# 6. Dependencies are cached/restored
# 7. Dependencies are installed
# 8. (Optional) Tests are executed
# 9. Workflow succeeds or fails
# =========================================================

```
---

##  GitLab CI/CD 

- Single tool for **Git + CI/CD**
- No extra CI server (unlike Jenkins)
- YAML-based pipelines stored with code
- Built-in Docker registry
- Built-in DevSecOps scans
- By default gitlab use rubby to run the conatiner 

**Real-world usage:**
Startups and enterprises use GitLab CI/CD to deploy microservices, APIs, and web apps.

---

## 3. GitLab CI/CD Architecture (With Flow)

### Components

#### GitLab Server
- Stores source code
- Reads `.gitlab-ci.yml`
- Creates and manages pipelines

#### GitLab Runner
- Executes jobs
- Can run on VM, Docker, Kubernetes

#### Executor (Execution Environment)
- **Shell** → runs directly on host
- **Docker** → isolated container
- **Kubernetes** → scalable pods

**Flow Example:**
```
Code Push → GitLab → Runner → Job Execution → Result
```

---

## 4. Pipeline (Core Concept)

A pipeline is a **collection of stages and jobs** that run automatically.

### Common Triggers
- Push to branch
- Merge Request
- Tag creation
- Scheduled run
- Manual trigger

---

## 5. `.gitlab-ci.yml` (Base Example)

```yaml
stages:
  - test
  - build
  - deploy
```

This defines the **order of execution**.

---

## 6. Jobs (With Example)

```yaml
unit_test_job:
  stage: test
  image: node:18
  script:
    - npm install
    - npm test
```

**Explanation:**
- Uses Node.js container
- Installs dependencies
- Runs test cases

---

## 7. Stages (Parallel Execution)

```yaml
stages:
  - test
  - build
```

Jobs inside the same stage run **in parallel** if runners are available.

---

## 8. Variables (With Practical Usage)

```yaml
variables:
  APP_ENV: production
```

```yaml
script:
  - echo "Environment is $APP_ENV"
```

### Types
- Predefined (`CI_COMMIT_BRANCH`)
- Custom
- Secret (masked)

---

## 9. Rules (Modern Job Control)

```yaml
deploy_prod:
  stage: deploy
  rules:
    - if: '$CI_COMMIT_BRANCH == "main"'
  script:
    - echo "Deploying to production"
```

Runs **only on main branch**.

---

## 10. Artifacts (Passing Files Between Stages)

```yaml
build_job:
  stage: build
  script:
    - npm run build
  artifacts:
    paths:
      - dist/
    expire_in: 7 days
```

**Use-case:**
- Build output used in deploy stage

---

## 11. Cache (Speed Optimization Example)

```yaml
cache:
  paths:
    - node_modules/
```

Speeds up pipelines by avoiding repeated downloads.

---

## 12. Docker Image Build Example

```yaml
build_docker:
  stage: build
  image: docker:latest
  services:
    - docker:dind
  script:
    - docker build -t myapp:$CI_COMMIT_SHA .
    - docker push myapp:$CI_COMMIT_SHA
```

**Explanation:**
- Uses Docker-in-Docker
- Builds and pushes image

---

## 13. Environments (Deployment Tracking)

```yaml
deploy_prod:
  stage: deploy
  script:
    - echo "Deploying..."
  environment:
    name: production
    url: https://example.com
```

Tracks deployments visually in GitLab.

---

## 14. Job Dependencies (`needs`)

```yaml
deploy_job:
  stage: deploy
  needs:
    - build_job
```

Allows faster pipelines by skipping stage waits.

---

## 15. Parallel & Matrix Jobs

```yaml
test_matrix:
  stage: test
  parallel:
    matrix:
      - NODE_VERSION: [14, 16, 18]
```

Runs tests on multiple Node versions.

---

## 16. Merge Request Pipelines (Example)

```yaml
rules:
  - if: '$CI_PIPELINE_SOURCE == "merge_request_event"'
```

Prevents broken code from being merged.

---

## 17. Security & DevSecOps Example

```yaml
sast:
  stage: test
  script:
    - echo "Running SAST scan"
```

Used for early vulnerability detection.

---

## 18. Secrets Management (Best Practice)

```yaml
script:
  - echo "$DB_PASSWORD"
```

Store `DB_PASSWORD` in GitLab CI/CD variables (masked).

---

## 19. Failure Handling

```yaml
allow_failure: true
retry: 2
```

Used for non-critical jobs.

---

## 20. Production-Grade Pipeline Example (Complete)

```yaml
stages:
  - test
  - build
  - deploy

unit_test:
  stage: test
  script:
    - npm test

build_app:
  stage: build
  script:
    - npm run build
  artifacts:
    paths:
      - dist/

deploy_prod:
  stage: deploy
  rules:
    - if: '$CI_COMMIT_BRANCH == "main"'
  script:
    - echo "Deploying to production"
```

---

## 21. Common Mistakes

- Hardcoding secrets
- No caching
- No MR pipelines
- No manual approvals

---

**example of pipeline .gitlab.yml**
```js
# ==========================================================
# GitLab CI/CD Pipeline Configuration
# This single file is enough to TEST, BUILD, PUSH, and DEPLOY
# your application WITHOUT restarting the server.
# ==========================================================

# ------------------------------
# Global variables (used in all jobs)
# ------------------------------
variables:
  # Docker Hub repository name
  IMAGE_NAME: amanplaxonic/aman-pratice

  # Image tag = current Git commit short SHA
  # This makes every image unique and traceable
  IMAGE_TAG: $CI_COMMIT_SHORT_SHA

# ------------------------------
# Pipeline stages (execution order)
# ------------------------------
stages:
  - test    # Run automated tests
  - build   # Build & push Docker image
  - deploy  # Deploy container to server via SSH

# ==========================================================
# STAGE 1: TEST
# ==========================================================
run_tests:
  stage: test

  # Use official Node.js image
  image: node:20-alpine

  script:
    # Install dependencies exactly from package-lock.json
    - npm ci --legacy-peer-deps

    # Run tests once (no watch mode in CI)
    - npm test -- --watchAll=false

# ==========================================================
# STAGE 2: BUILD
# Build Docker image and push to Docker Hub
# ==========================================================
build_image:
  stage: build

  # Docker CLI image
  image: docker:20.10.16

  # Docker-in-Docker service (required to build images)
  services:
    - docker:20.10.16-dind

  # Required for Docker-in-Docker security
  variables:
    DOCKER_TLS_CERTDIR: "/certs"

  before_script:
    # Login to Docker Hub using GitLab CI variables
    - docker login -u "$REGISTRY_USER" -p "$REGISTRY_PASS"

  script:
    # Build Docker image from Dockerfile
    - docker build -t "$IMAGE_NAME:$IMAGE_TAG" .

    # Push image to Docker Hub
    - docker push "$IMAGE_NAME:$IMAGE_TAG"

# ==========================================================
# STAGE 3: DEPLOY
# Deploy the container to the server via SSH
# NOTE: The SERVER IS NOT RESTARTED.
# Only the Docker container is replaced.
# ==========================================================
deploy:
  stage: deploy

  # Lightweight Linux image
  image: alpine:latest

  before_script:
    # Install SSH client and Docker CLI
    - apk add --no-cache openssh docker-cli

    # Fix permissions for SSH private key (File variable)
    - chmod 600 "$SSH_KEY"

  script:
    # Use HEREDOC to safely run multiple commands on the server
    - |
      ssh -o StrictHostKeyChecking=no -i "$SSH_KEY" root@68.183.84.250 << EOF

        # Login to Docker Hub from the server
        docker login -u "$REGISTRY_USER" -p "$REGISTRY_PASS"

        # Stop and remove old container if it exists
        docker stop app || true
        docker rm app || true

        # Pull the new image built by CI
        docker pull "$IMAGE_NAME:$IMAGE_TAG"

        # Run the new container
        docker run -d \
          --name app \
          -p 3000:3000 \
          "$IMAGE_NAME:$IMAGE_TAG"

      EOF

# ==========================================================
# REQUIRED GITLAB CI/CD VARIABLES (Settings > CI/CD > Variables)
# ----------------------------------------------------------
# SSH_KEY        -> Type: File (SSH private key)
# REGISTRY_USER  -> Masked (Docker Hub username)
# REGISTRY_PASS  -> Masked (Docker Hub password)
# ==========================================================

# RESULT:
# - No server restart
# - Only container restarts
# - Fully automated CI/CD pipeline
# ==========================================================

```