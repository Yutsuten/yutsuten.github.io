---
doc: https://taskwarrior.org/docs/syntax.html
update: 2021-07-22
---

## Usage

```shell
task FILTER COMMAND MODIFICATIONS
```

![Syntax](https://taskwarrior.org/docs/images/syntaxes.png)

### Common commands

| Command | Description |
| --- | --- |
| `list` | List all tasks |
| `information` | Shows all data and metadata |
| `add` | Add a new task |
| `edit` | Edit task(s) |
| `delete` | Delete task(s) |
| `start` | Start task(s) |
| `stop` | Remove the start time from a task |
| `done` | Mark the task as completed |
| `tags` | Shows a list of all tags used |
| `projects` | Shows a list of all project names used |
| `summary` | Shows a summary separated by projects |
| `help` | Display an usage help text |

### Common filter / modifiers

| Filter / modifier | Description |
| --- | --- |
| `project:Home` | Set the project |
| `status:pending` | Set the status of the task |
| `priority:H` | Set the priority of the task |
| `due:eom` | Set the due date of the task |
| `+garden` | Set a tag |
