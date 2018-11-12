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
    - Python 2

- Build tools
  - Maven (DONE)
  - Gradle

- Continuous Integration & Continuous Delivery
  - Jenkins (DONE)
  - Circle CI
  - Travis CI
  - GitHub integration with Slack (DONE)
  - GitHub integration with Jenkins, etc

- Cloud providers
  - GCP (IN PROGRESS)
  - AWS
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
