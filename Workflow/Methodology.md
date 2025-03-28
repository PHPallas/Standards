code: SWDA-7001  version: **1.0**  status: **active**

---
# Teamwork Methodology

## Introduction

This document outlines the workflow for our team as we adopt a Scrum framework for project management. The aim is to provide clarity on roles, responsibilities, and processes to ensure efficient collaboration and delivery of high-quality products.

## Project Overview

- **Project Duration**: Ongoing
- **Sprint Length**: 7 days
- **Story Points**: 
  - XS: 0-4 hours work
  - S: 4-8 hours work
  - M: 1-2 days work
  - L: 2-4 days work
  - XL: Full sprint length work
  - 2XL: 2 sprint length work
  - 3XL: One season work length
  - 4XL: One year work length

## Team Roles

1. **Project Manager**
   - Responsible for planning the project roadmap.
   - Selects tasks from the backlog to be included in upcoming sprints.

2. **Repository Admin**
   - Acts as the leader of the repository.
   - Maintains the repository and oversees DevOps tasks related to the product.

3. **Developers**
   - Responsible for developing features, fixing bugs, and conducting unit tests.
   - Must work on tasks assigned in the to-do list.

4. **SQA Agent**
   - Tests products for quality and functionality.
   - Ensures that all features meet the required standards before deployment.

## Workflow Process

### 1. Backlog Management
- All tasks are initially placed in the **backlog**.
- The **Project Manager** reviews the backlog and selects tasks to be prioritized for each sprint.

### 2. Sprint Planning
- At the beginning of each sprint, the **Project Manager** and **Repository Admin** determine which tasks from the backlog will be moved to the **to-do list**.
- Tasks are assigned story points based on their estimated effort.

### 3. Task Execution
- **Developers** begin work on tasks from the **to-do list**.
- Upon starting a task, the status is updated to **In Progress**.
- When a task is completed, the status changes to **Done**.

### 4. Code Review and Quality Assurance
- After finishing a task, the **Developer** creates a **Pull Request** (PR) and assigns it to the **Repository Admin**.
- The **Repository Admin** reviews the code and, if satisfactory, assigns the task to the **SQA Agent** for testing.
  
### 5. Testing and Merging
- The **SQA Agent** conducts thorough testing to verify functionality and quality.
- If the SQA Agent approves the changes, the **Repository Admin** merges the branches into the main codebase.

### 6. Continuous Improvement
- At the end of each sprint, the team conducts a retrospective to discuss what went well, what could be improved, and any adjustments needed for future sprints.

## Conclusion

This workflow is designed to facilitate clear communication and efficient task management within the team. By adhering to these processes, team members can ensure that they are aligned with project goals and contribute effectively to the delivery of high-quality products.

For any questions or clarifications regarding this workflow, please feel free to reach out to the **Project Manager** or **Repository Admin**.