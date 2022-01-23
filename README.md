# parallel-tasks

Execute laravel tasks in parallel by spawning multiple processes. Control the maximum processes to spawn and the timeouts. 

## How it works
Using symphony's process command, we just start up as many processes as required, and then check for them to all finish every second. Once they are all finished the parent task finishes.

Laravel's scheduler also uses the same Symphony process command under the hood.