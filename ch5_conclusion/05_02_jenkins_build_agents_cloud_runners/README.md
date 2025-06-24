# 05_02 Build agents and cloud runners

In this lesson, you'll learn how Jenkins uses build agents and cloud runners to distribute work across multiple machines. This approach improves scalability and flexibility for real-world automation projects.

While this course focuses on a single-machine setup for learning, exploring build agents and cloud runners is essential for real-world Jenkins implementations.

Distributed agents enable scalability, flexibility, and better resource management for CI/CD pipelines.

- **What Are Build Agents:**
  - Build agents are additional machines that Jenkins can delegate work to.
  - Agents can be physical servers, virtual machines, or cloud-based resources.
  - Helps distribute workloads across multiple machines for better performance.

- **Why Use Distributed Build Agents:**
  - Run jobs in parallel (e.g., tests on one agent, builds on another).
  - Use different operating systems or toolsets tailored to specific projects.
  - Scale Jenkins to meet the needs of larger or more complex teams.

- **Cloud Runners:**
  - Build agents that run in cloud environments like AWS, Azure, or Google Cloud.
  - Cloud-specific plugins allow Jenkins to spin up agents on demand.
  - After jobs complete, the agents are automatically decommissioned to save costs.

<!-- FooterStart -->
---
[← 05_01 Pipeline as code](../05_01_pipeline_as_code/README.md) | [05_03 Next Steps with Jenkins →](../05_03_continuing_on_with_jenkins/README.md)
<!-- FooterEnd -->
