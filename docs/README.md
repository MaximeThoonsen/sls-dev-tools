---
id: README
title: Installation and use
sidebar_label: Installation and use
---

# sls-dev-tools

The Dev Tools for the Serverless World

[Docs Site](https://theodo-uk.github.io/sls-dev-tools)

![demo](assets/demo.png)

# To Run

- `npm install -g sls-dev-tools`
- Run `sls-dev-tools -n {YOUR_STACK_NAME} -r {YOUR_REGION} [-t {START_TIME}] [-i {INTERVAL}] [-p {PROFILE}]`
  - The start time defines when you want your graphs to start from. The format for the start time is as follows: `'30 March 2020 09:00 GMT'`
  - The interval defines the size of the buckets in seconds. This means if you give a interval of 3600, the line graph will group the invocations and errors into 1h chunks, and the bar chart will show the average response time over the hour for the last 6 hours during which invocations were made.
  - The profile option allows you to pass in an alternative aws profile to connect with if none is provided the default aws profile is used
  - To get the stack name, log on to AWS cloudformation and it is shown in the overview section of stack info. It may not be what you expected e.g. it might have `-dev` on the end, so worth checking if the dev tools are not working.
  - The region is the AWS region, for example, us-east-1.
- Choose a function with the arrow keys, and press enter to see the metrics for that function.
  - If you get an `AccessDenied` error in which case you must add the `GetMetricData` permission from CloudWatch in the IAM console on AWS.
  - If you're not seeing any data in the graphs, try changing your start date to make sure you have had invocations since then.
- The line graph shows the number of invocations and errors that occurred within the time interval.
- The bar chart shows the average response time of the invocations within the last 6 time intervals that had some invocations.

# Libs

Heavily based off the amazing [blessed](https://github.com/chjj/blessed) and [blessed-contrib](https://github.com/yaronn/blessed-contrib) projects.

## Core Team

| [Ben Ellerby](https://github.com/BenEllerby)                            | [Abbie Howell](https://github.com/abbiehowell)                           | [Rob Cronin](https://github.com/robcronin)                             |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------ | ---------------------------------------------------------------------- |
| ![Ben Ellerby](https://avatars2.githubusercontent.com/u/11080984?s=150) | ![Abbie Howell](https://avatars3.githubusercontent.com/u/41898453?s=150) | ![Rob Cronin](https://avatars3.githubusercontent.com/u/32868346?s=150) |
