## planner2taskwarrior
A bash script to add planner tasks to taskwarrior. Generate plans with planner and automatically add all tasks into taskwarrior.

### Usage
planner2taskwarrior.sh /path/to/planner/file.xml

As of 2016-03-18 the script will pull out all the tasks from the planner xml. For each task:
* Task already completed - do nothing
* Task not completed - check if already added
  * If not added - add new task
    * New task will use 1) project name 2) task name 3) start date as wait 4) due date as wait
  * If task already added - update the wait and due dates

### Info
Planner is a (older) project planning sytem that is standalone and easy to use. Plans are saved in xml format.
Planner [website](https://wiki.gnome.org/action/show/Apps/Planner?action=show&redirect=Planner)

[Taskwarrior](http://taskwarrior.org) is a command-line task management and prioritiation system.
