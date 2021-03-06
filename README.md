NextAction
==========

A more GTD-like workflow for Todoist. Uses the REST API to add and remove a `@next_action` label from tasks.

This program looks at every list in your Todoist account.
Any list that ends with `--` or `=` is treated specially, and processed by NextAction.

Activating NextAction
======

Sequential list processing
------
If a list ends with `--`, the top level of tasks will be treated as a priority queue and the most important will be labeled `@next_action`.
Importance is determined by:
 1. Priority
 2. Due date
 3. Order in the list

`@next_action` waterfalls into indented regions. If the top level task that is selected to receive the `@next_action` label has subtasks, the same algorithm is used. The `@next_action` label is only applied to one task.

Parallel list processing
------
If a list name ends with `=`, the top level of tasks will be treated as parallel `@next_action`s.
The waterfall processing will be applied the same way as sequential lists - every parent task will be treated as sequential. This can be overridden by appending `=` to the name of the parent task.


Howto install (python) and Run
==========
1) The NextAction script is based on Python2, so install Python 2.7.6 or newer.
2) Then install the package manager pip: http://www.pip-installer.org/en/latest/installing.html. 
3) Then install the package dateutil: 'pip install python-dateutil'. 
4) Then run the script: 'python nextaction.py' and apparently let it run in the background.