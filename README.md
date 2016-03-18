## planner2taskwarrior
A bash script to add planner tasks to taskwarrior. Generate plans with planner and automatically add all tasks into taskwarrior. Tasks will use the start and due dates calculated in planner.

### Usage
planner2taskwarrior.sh /path/to/planner/file.xml

As of 2016-03-18 the script will pull out all the tasks from the planner xml. For each task:
* Task already completed - do nothing
* Task not completed - check if already added
  * If not added - add new task
    * New task will use 1) project name 2) task name 3) start date as wait 4) due date as wait
  * If task already added - update the wait and due dates

### Info
[Planner](https://wiki.gnome.org/action/show/Apps/Planner?action=show&redirect=Planner) is an (older) project planning sytem that is standalone and easy to use. Plans are saved in xml format.

[Taskwarrior](http://taskwarrior.org) is a command-line task management and prioritiation system.

### To do
* Read project dependencies to properly assign task order
* Code cleanup
* If task is removed in planner, remove in taskwarrior
* Import priority from planner
