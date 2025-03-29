code: SWDA-7010  version: **1.0**  status: **active**

---
# Linear Git Flow

## Introduction

This document outlines the rules and guidelines for implementing a Linear Git Flow, characterized by the use of a single branch named **main**. This approach is particularly suitable for specific use cases, such as *documentation repositories* and *simple scripts*.

## Definition

Linear Git Flow is a simplified version control strategy where all development occurs on the **main** branch, avoiding the complexities of multiple branches. This model is designed for projects that do not require extensive collaboration or feature branching.

## Rules

1. This model **MUST** be used only for projects focused on maintaining *documentation*, where changes are straightforward and can be made directly on the **main** branch.

2. Updates must be incremental and do not require extensive testing or reviews. Otherwise, linear git follow **MUST** be avoided.

3. This model **MAY** be applied to small, single-script programs that do not involve complex features or dependencies.

4. Commit messages **MUST** be clear and descriptive, summarizing the changes made. It is RECOMMENDED to keep description between 10 - 40 characters.

5. Prefixing the commit message **MUST** be avoided.

6. All changes **MUST** be commited directly to the **main** branch.

7. Repository **MUST** have only one branch named **main**.

8. Basic functionality **SHOULD** be verified before committing changes.

9. Any changes to scripts or documentation **SHOULD** be accompanied by relevant updates to ensure clarity and accuracy.

10. Simple versioning practices **MUST** be used, such as tagging releases on the **main** branch, to track significant changes. Each tag **MUST** include a brief description of the changes made.

11. In case of errors, it is **RECOMMENDED** to revert previous commits on the **main** branch. Commiting a revision is possible but NOT **RECOMMENDED**.

## Conclusion

The Linear Git Flow model is designed for projects with limited complexity, such as documentation repositories and simple scripts. By adhering to this rule manifest, developers must maintain a streamlined and efficient workflow, focusing on rapid iterations and straightforward updates.