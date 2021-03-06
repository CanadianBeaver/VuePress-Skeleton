---
title: Report1
lang: en-US
---

# Report1

presents the current situation related to company's job.

## Displayed columns

The report contains the folowing columns:

| Position | Column caption          | Group summary | Displayed value                                                          | Remark                                      |
|:--------:|-------------------------|---------------|--------------------------------------------------------------------------|---------------------------------------------|
|     1    | Number                  |               | Number of job                                                            |                                             |
|     2    | Name                    |               | Name of job                                                              |                                             |
|     3    | Type                    |               | Type of job                                                              |                                             |


## Filtering the data

The report contains the folowing filters with the logical operation between them is `AND`:

| Position | Filter caption | Required | Initial value | Filter columns                                          | Multiple selected | Filter applicability                                                                                                | Description                                                     |
|:--------:|:---------------|----------|---------------|---------------------------------------------------------|-------------------|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
|     1    | Open/Close     | Yes      | Opened        | General status of job&#x00B9;                           | No                | Drop down list with predefined values: `Opened`, `Closed`, `All`                                                    | Display opened jobs or closed jobs or display all jobs          |
|     2    | From Received  | Optional | Nothing       | Jobs with `Received Date` which is after selected date  | No                | Drop down calendar without time                                                                                     | If nothig selected display all jobs                             |


&#x00B9; Closed jobs are the jobs that has `Dead Lead`, `Non-Accepted`, `Rejected` or `Closed` alternative status, related to `Production closed` or `Closed Date` status. Opened jobs are everything else.  
&#x00B2; Applying this filtering will implement grouping by Employee.

## Grouping the data

The report is divided into the following groups:

| Level | Group by           | Sorting by                                     | Displaying                                                                                                                                                                             | Remark                                                                                                  |
|:-----:|:-------------------|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| 1     | Employee           | Alphabetically                                 | Each job can have several `Employees`, therefore these jobs should be displayed in each related group of employee. The displayed value is combination of `First Name` and `Last Name`. | this grouping will be displayed on the report only if the filtering by `Employee Type` has been applied |

## Sorting the data in groups

The displayed rows should be sorted by the following columns in each group:

| Level | Order by column | Direction                                       | Remark                                                 |
|:-----:|:----------------|-------------------------------------------------|--------------------------------------------------------|
| 1     | Received Date   | From the past to the future with truncated time | jobs without `Received Date` should be displayed first |
| 2     | Job Number      | Alphabetically                                  |                                                        |
