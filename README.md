# Exploring github actions

## Github actions flow:

1. Name of the workflow using keyword `name: <workflow name>`
2. Trigger type using keyword `on: <[type]> | <type>` Example of types: `push, pull_requests(opened, closed, merged), issues(created, closed), external events, schedule
3. One or more jobs using keyword `jobs`
4. Each job runs on a virtual machine specified by keyword `runs-on: <machine type>`
5. Jobs have steps in array form using keyword `steps: array of steps`

### Example of simple workflow

```yml
name: Introduction to github actions

on: [push]

jobs:
  run-greetings-command:
    runs-on: ubuntu-latest
    steps:
      - name: Greet github actions from shell command
        run: echo "Hello github actions"
```
