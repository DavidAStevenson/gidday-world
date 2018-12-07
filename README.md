# gidday-world
A slightly novel take on the classic

This project is part of my catching up on my technology:

- SCM
  - GitHub (DONE)

- Virtualization / Deployment
  - Vagrant VMs (DONE)
  - Docker Containers (DONE)

- Container Orchestration
  - docker-compose (DONE)
  - Kubernetes (IN PROGRESS)
    - Reading through kuard (currently reading chapter 7)
    - run exercises through page 62 in minikube

- Messaging
  - NATS (DONE)
  - RabbitMQ
  - Apache Kafka

- API tooling
  - OpenAPI (fka Swagger)
  - AsyncAPI maybe

- Programming Languages
  - Golang
  - Java 
    - Spring Framework (DONE)
    - Unit testing
      - JUnit (DONE)
      - Mockito
    - Guice (for DI, related to Governator, which has retired Karyon)
  - C++ (REVISION IN PROGRESS)
    - C++11
    - C++14
    - C++17
  - Python
    - Python 3
      - pytest
      - unittest, nose
    - Python 2

- Web Service
	- design a simple OpenAPI spec
		- something that could run as a side-car to alphabet-pingpong?
	- implement in python
		- use python3, flask, connexion to implement it
		- dockerize it in a smallish image (e.g. python3 alpine?)
	- implement in golang
		- find some examples of how to do equivalent in golang, and do it
		- go-swagger? 
		- API-First tooling for golang?

- Build tools
  - Maven (DONE)
  - Gradle

- Continuous Integration & Continuous Delivery
  - Jenkins (DONE)
  - Circle CI
  - Travis CI
  - GoCD?
  - GitHub integration with Slack (DONE)
  - GitHub integration with Jenkins, etc

- Configuration Management
  - Ansible 
    - Reading Tettei Nyumon
      - https://github.com/h-hirokawa/tettei-nyumon-playbooks 
      - read through to end of chapter 3 of the book
  - Chef

- HashiCorp tools
  - Consul
  - Vault
  - Terraform

- Serverless
  - AWS Lambda
  - GCP functions?

- Cloud providers
  - GCP (IN PROGRESS)
  - AWS (IN PROGRESS)
  	- AWS Lambda
		- (DONE) https://aws.amazon.com/getting-started/tutorials/run-serverless-code/
		- Developer Guide: https://docs.aws.amazon.com/lambda/latest/dg/welcome.html
    - https://aws.amazon.com/jp/ec2/
    - https://aws.amazon.com/jp/elasticloadbalancing/
    - https://aws.amazon.com/jp/cloudformation/
    - https://aws.amazon.com/jp/cli
    - http://docs.ansible.com/ansible/intro_dynamic_inventory.html

```
                      +
                      | requests
                      |
          +-----------v-----------+
          |          ELB          |
          | (distribute between   |
          |       blue/green)     |
          +-+------------------+--+
            |                  |
            |                  |
+-----------v------+     +-----v------------+
|                  |     |                  |
|       Blue       |     |       Green      |
| +-----+  +-----+ |     | +-----+  +-----+ |
| |     |  |     | |     | |     |  |     | |
| |     |  |     | |     | |     |  |     | |
| +-----+  +-----+ |     | +-----+  +-----+ |
|  Web 1    Web 2  |     |  Web 1    Web 2  |
+----------^-------+     +------^-----------+
           |                    |
           |                    |
     +-----+--------------------+------+
     |         +--------+              |
     |         |        |              |
     |         |   CI   | Ansible      |
     |         | Server | (config      |
     |         |        |  management) |
     |         +--------+              |
     +---------------------------------+
```
