#Programs and Processes:

-Program: is a set of instructions in the main memory of the CPU
* Note: The OS Creates a counter to point on the next instruction, The value of the counter is stored in the main memory too.
In case of multi-tasking OS, Before switching between tasks the OS stores the last counter value for the task to start from it when it switches back to this task.

-Process: is a instance copy of a program in the main memory, it has (ID, Owner, Group, Parent Process)

#ps and pstree Commands:
$ ps     #show a snapshot of the current processes
$ pstree   #show a tree of running processes

#Processes:
- For Tereminate a Process (Close)   $ kill process-id
- For Force Tereminate a Process (Force Close)   $ kill -9 process-id
* kill Command can send more types of signals, check it by  $ kill -l

#Jobs:
- The Process Which it's parent is shell called "Job"
- Each Job has a number and Each Shell has a jobs list  $ jobs
- Terminating a Job (Close)  $ kill %(job-number)

#Foreground Jobs:
- The Default for programs/jobs to run in the foreground (in the shell)
- To Stop a job (Freeze) without clear a data: "Ctrl+Z"
- To Re-start a job in foreground: $ fg %(job-number)
- To Close a job and finish the process: "Ctrl+D"

#Background Jobs:
- To start a program/job in the background: $ (program-name) &
- To Re-start a foreground stopped program in the background: $ bg %(job-number)
