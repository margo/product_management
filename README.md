## Product Management Team
The product management team (aka PM team)  is a subteam of Margo's Steering Committee.
It's mission is to set technical directions aligned with project objectives, and to assure marketing enablement for Margo's deliverables.
The product management team owns the roadmap planning and defines the requirements, both inputs for Margo's Technical Working Group.

In a spirit of openness, the roadmap and the collection of requirements are shared in public (read-only). Github Issues and Github Project view are used to structure these deliverables.
The Specification Update Process can be used to make suggestions to the PM team. 


### Documentation Support
- User Journey Steps - Deploy Workload At Scale - [Step-by-step scenario](https://github.com/margo/product_management/blob/main/UserJourneySteps-DeployWorkloadAtScale.md)
- Use the [Project Dashboard](https://github.com/orgs/margo/projects/13) to track the current status of requirements and roadmap planning
- [Product Management collaboration space : MSTeams channel (Margo members only)](https://teams.microsoft.com/l/channel/19%3A7970d4523d194838bcb8b29e45df02bd%40thread.tacv2/Product%20Management?groupId=c2e91119-2dca-467c-a982-a9e732dd6d9a&tenantId=2c3f4c59-fa82-47a7-a9a5-7c0ec5558786)

***
### Requirments workflow
![image](https://github.com/user-attachments/assets/0d59b491-1c2c-4efe-82f9-a6dd99b6ed81)


| Steps |     Requirement Responsibility  | Action                                                                                                            | Assigned Label on Completion   | Comments |
|-------|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------|
| 1     | PM member Submits Draft Requirement            | [Click here](https://github.com/margo/product_management/issues/new?template=requirements.yaml)                           | ```PM-Requirement in Draft```        |          |
| 2     | PM Requirement Review               | PM Group reviews submitted Requirements to gain consensus; once approved, the requirement Issue is assigned to the TWG (@ajcraig) for feedback | ```TWG - Feedback```                 |          |
| 3     | TWG Feedback                        | TWG review the proposed requirement.                                                                                                           |                                |          |
|       | a. No Comments                      |  No Comments: TWG accepts the requirement and is placed into the TWG requirement backlog. Move to **Step 6**                                   | ```TWG - Requirements Backlog```     |          |
|       | b. Comments raised                  | Reassigned to the PMG (@abbottjb)                                                                                                              | ```PM - Reviewing TWG Feedback```    |          |
| 4.    | PM Reviews TWG requirement Feedback | PM Group assesses the feedback and adjusts requirements accordingly - once approved, the requirement Issue is assigned to the TWG (@ajcraig)   | ```TWG - Requirements Review```      |          |
| 5.    | TWG Feedback                        |                                                                                                                                                |                                |          |
|       | a. No Comments                      | TWG accepts the requirement and is placed into the TWG requirement backlog. Move to **Step 6**                                                 | ```TWG - Requirements Backlog```     |          |
|       | b. Comments Raised                  | Reassigned to the PMG (@abbottjb)                                                                                                              | ```PM - Reviewing TWG Feedback```    |          |
| 6.    | TWG Initiate work on Requirement    | TWG starts work on the requirement                                                                                                             | ```TWG - Requirements in progress``` |          |
| 7.    | Requirement Completed               |                                                                                                                                                |                                |          |
|       | a. Yes                                 | Issue/PR assigned to the PMG for final review before the requirement is merged into the Spec baseline                                       | ```PM - Requirement Final Review```  |          |
|       | b. No                                  | Requires TWG feedback - Assign the issue to PWG (@abbottjb) - **Move to Step 4**                                                            | ```PM - Reviewing TWG Feedback```    |          |

***

## Issue Management

This repository uses a structured issue management process:

### Who Can Create Issues?
Only members of the **Project Management Team** are authorized to create new issues.

### Who Can Comment?
All **Technical Working Group (TWG)** members can:
- Comment on existing issues
- Provide feedback and suggestions
- Participate in discussions

### Automated Enforcement
An automated workflow monitors issue creation. Issues created by unauthorized users will be:
- Automatically labelled with `unauthorized-creation` and `policy-violation`
- Closed with an explanation
- Logged for audit purposes

### Need to Report Something?
If you're a TWG member and need to report an issue:
1. Search for existing related issues first
2. Add your comments to the relevant issue
3. Contact a PM team member if a new issue is genuinely needed
