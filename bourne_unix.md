﻿Bourne, Stephen, R. The Unix System V Environment, Addison-Wesley Publishing Company, 1987

The system call fork creates two nearly identical copies of a process. One copy is called the parent and the other the child. In the parent process, fork returns the process number of the child. The value returned in the child is zero. If fork cannot create a new process the a -1 is returned. This can happen, for example, when the system process table is full, or if the fork call is interrrupted. 135 {#platform-making}
