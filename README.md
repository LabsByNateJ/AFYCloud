# AFYCloud

Azure engineering labs by [LabsByNateJ](https://github.com/LabsByNateJ), covering networking, identity, compute, storage, monitoring, and automation. On-premises Windows infrastructure lives in [AFYSystems](https://github.com/LabsByNateJ/AFYSystems).

## Project roadmap

These labs are planned; this index does not claim deployment or validation. Track implementation in [repository issues](https://github.com/LabsByNateJ/AFYCloud/issues) and the private AFYCloud Project board. Workflow: Todo → In Progress → Done.

| Project | Tracking | Intended folder |
|---|---|---|
| Azure baseline and cost controls | [#1](https://github.com/LabsByNateJ/AFYCloud/issues/1) | projects/lab-baseline/ |
| Networking | [#2](https://github.com/LabsByNateJ/AFYCloud/issues/2) | projects/networking/ |
| IAM: users, groups, RBAC, PIM | [#3](https://github.com/LabsByNateJ/AFYCloud/issues/3) | projects/iam-access/ |
| IAM: MFA and Conditional Access | [#4](https://github.com/LabsByNateJ/AFYCloud/issues/4) | projects/iam-authentication/ |
| IAM: applications, managed identities, lifecycle | [#5](https://github.com/LabsByNateJ/AFYCloud/issues/5) | projects/iam-workloads/ |
| Compute, monitoring, recovery | [#6](https://github.com/LabsByNateJ/AFYCloud/issues/6) | projects/compute-monitoring/ |
| Storage | [#7](https://github.com/LabsByNateJ/AFYCloud/issues/7) | projects/storage/ |
| Spot VM snapshot automation review and consolidation | [#8](https://github.com/LabsByNateJ/AFYCloud/issues/8) | projects/spot-vm-snapshots/ |

The [existing snapshot automation repository](https://github.com/LabsByNateJ/spotvm-snapshot-automation) remains the source until its implementation is reviewed and history-preserving consolidation is completed.

## Project documentation

Keep each project's README, SOPs, KBs, diagrams, scripts or infrastructure code, and validation evidence together under its project folder. Create folders when content is available; the paths above describe the intended organization.

A project README should cover:

1. Objective and current status
2. Architecture and prerequisites, including licensing
3. Deployment or configuration steps
4. Validation and observed results
5. Troubleshooting and lessons learned
6. Costs and cleanup

Use the [SOP template](docs/templates/sop-template.md) and [KB template](docs/templates/kb-template.md). Close tasks only after linking evidence of validation.

## Lab operations

Establish naming, tags, budgets, access controls, and cleanup procedures before deployments. Check required Entra licensing for PIM, Conditional Access, and governance scenarios. Cost alerts are notifications, not automatic spending limits.

This repository is public. Use lab examples and sanitized screenshots; keep credentials and private working configuration outside it.

## Legacy material

`Githubcodeforafy.txt` contains an older AFYCloud website concept. It is retained for now and is separate from the Azure lab roadmap. The current portfolio is [labsbynatej.com](https://labsbynatej.com).
