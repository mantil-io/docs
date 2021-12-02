# API Configuration

APIs come preconfigured with some default settings for memory size, timeout and environment variables. You can customize these settings using the `config/environment.yml` file. Values can be defined on a project, stage or function level. If the same value is defined on multiple levels the lowest level will take precedence. The final values will be visible in `config/state.yml` after deployment.

For example, let's say we created a project with two functions called `one` and `two` and deployed it to two stages called `development` and `production`. After creating both stages the `config/state.yml` file will look like this:
```
name: my-project
stages:
- name: development
  ...
  functions:
  - name: one
    ...
    memory_size: 128
    timeout: 900
    env:
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoiZGV2ZWxvcG1lbnQiLCJNQU5USUxfV09SS1NQQUNFIjoiN2Vub2o1TjVRby0yZVNwQkhWVEJlQSJ9LCJXc0ZvcndhcmRlck5hbWUiOiJtYW50aWwtbXktcHJvamVjdC1kZXZlbG9wbWVudC13cy1mb3J3YXJkZXItYzVjNjM2ZTAiLCJOYW1pbmdUZW1wbGF0ZSI6Im15LXByb2plY3QtZGV2ZWxvcG1lbnQtJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: development
  - name: two
    ...
    memory_size: 128
    timeout: 900
    env:
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoiZGV2ZWxvcG1lbnQiLCJNQU5USUxfV09SS1NQQUNFIjoiN2Vub2o1TjVRby0yZVNwQkhWVEJlQSJ9LCJXc0ZvcndhcmRlck5hbWUiOiJtYW50aWwtbXktcHJvamVjdC1kZXZlbG9wbWVudC13cy1mb3J3YXJkZXItYzVjNjM2ZTAiLCJOYW1pbmdUZW1wbGF0ZSI6Im15LXByb2plY3QtZGV2ZWxvcG1lbnQtJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: development
- name: production
  ...
  functions:
  - name: one
    ...
    memory_size: 128
    timeout: 900
    env:
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoicHJvZHVjdGlvbiIsIk1BTlRJTF9XT1JLU1BBQ0UiOiI3ZW5vajVONVFvLTJlU3BCSFZUQmVBIn0sIldzRm9yd2FyZGVyTmFtZSI6Im1hbnRpbC1teS1wcm9qZWN0LXByb2R1Y3Rpb24td3MtZm9yd2FyZGVyLWM1YzYzNmUwIiwiTmFtaW5nVGVtcGxhdGUiOiJteS1wcm9qZWN0LXByb2R1Y3Rpb24tJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: production
  - name: two
    ...
    memory_size: 128
    timeout: 900
    env:
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoicHJvZHVjdGlvbiIsIk1BTlRJTF9XT1JLU1BBQ0UiOiI3ZW5vajVONVFvLTJlU3BCSFZUQmVBIn0sIldzRm9yd2FyZGVyTmFtZSI6Im1hbnRpbC1teS1wcm9qZWN0LXByb2R1Y3Rpb24td3MtZm9yd2FyZGVyLWM1YzYzNmUwIiwiTmFtaW5nVGVtcGxhdGUiOiJteS1wcm9qZWN0LXByb2R1Y3Rpb24tJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: production
```
Since we have not yet defined any custom values in `config/environment.yml` all values will be set to their defaults. Note that Mantil also sets some default environment variables which always start with `MANTIL_`. Now we can define some custom values:
```
project:
  memory_size: 128
  timeout: 30
  env:
    KEY: project
  stages: 
    - name: development
      functions:
      - name: one
        memory_size: 256
        timeout: 60
        env:
          KEY: function
    - name: production
      memory_size: 512
      timeout: 120
      env:
        KEY: stage
```
Now after deploying both stages again the final state will look like this:
```
name: my-project
stages:
- name: development
  ...
  functions:
  - name: one
    ...
    memory_size: 256
    timeout: 60
    env:
      KEY: function
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoiZGV2ZWxvcG1lbnQiLCJNQU5USUxfV09SS1NQQUNFIjoiN2Vub2o1TjVRby0yZVNwQkhWVEJlQSJ9LCJXc0ZvcndhcmRlck5hbWUiOiJtYW50aWwtbXktcHJvamVjdC1kZXZlbG9wbWVudC13cy1mb3J3YXJkZXItYzVjNjM2ZTAiLCJOYW1pbmdUZW1wbGF0ZSI6Im15LXByb2plY3QtZGV2ZWxvcG1lbnQtJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: development
  - name: two
    ...
    memory_size: 128
    timeout: 30
    env:
      KEY: project
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoiZGV2ZWxvcG1lbnQiLCJNQU5USUxfV09SS1NQQUNFIjoiN2Vub2o1TjVRby0yZVNwQkhWVEJlQSJ9LCJXc0ZvcndhcmRlck5hbWUiOiJtYW50aWwtbXktcHJvamVjdC1kZXZlbG9wbWVudC13cy1mb3J3YXJkZXItYzVjNjM2ZTAiLCJOYW1pbmdUZW1wbGF0ZSI6Im15LXByb2plY3QtZGV2ZWxvcG1lbnQtJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: development
- name: production
  ...
  functions:
  - name: one
    ...
    memory_size: 512
    timeout: 120
    env:
      KEY: stage
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoicHJvZHVjdGlvbiIsIk1BTlRJTF9XT1JLU1BBQ0UiOiI3ZW5vajVONVFvLTJlU3BCSFZUQmVBIn0sIldzRm9yd2FyZGVyTmFtZSI6Im1hbnRpbC1teS1wcm9qZWN0LXByb2R1Y3Rpb24td3MtZm9yd2FyZGVyLWM1YzYzNmUwIiwiTmFtaW5nVGVtcGxhdGUiOiJteS1wcm9qZWN0LXByb2R1Y3Rpb24tJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: production
  - name: two
    ...
    memory_size: 512
    timeout: 120
    env:
      KEY: stage
      MANTIL_GO_CONFIG: eyJSZXNvdXJjZVRhZ3MiOnsiTUFOVElMX0tFWSI6ImM1YzYzNmUwIiwiTUFOVElMX1BST0pFQ1QiOiJteS1wcm9qZWN0IiwiTUFOVElMX1NUQUdFIjoicHJvZHVjdGlvbiIsIk1BTlRJTF9XT1JLU1BBQ0UiOiI3ZW5vajVONVFvLTJlU3BCSFZUQmVBIn0sIldzRm9yd2FyZGVyTmFtZSI6Im1hbnRpbC1teS1wcm9qZWN0LXByb2R1Y3Rpb24td3MtZm9yd2FyZGVyLWM1YzYzNmUwIiwiTmFtaW5nVGVtcGxhdGUiOiJteS1wcm9qZWN0LXByb2R1Y3Rpb24tJXMtYzVjNjM2ZTAifQ==
      MANTIL_KEY: c5c636e0
      MANTIL_PROJECT: my-project
      MANTIL_STAGE: production
```

## Scheduled execution

Using the `cron` field you can set up a rule to execute an API on a schedule. For example, with the following setup the default method of the `one` API will be executed every minute:
```
project:
  stages: 
    - name: development
      functions:
      - name: one
        cron: "* * * * ? *"
        env:
          KEY: function
```
For more information about the cron syntax please refer to the AWS docs:
https://docs.aws.amazon.com/AmazonCloudWatch/latest/events/RunLambdaSchedule.html
