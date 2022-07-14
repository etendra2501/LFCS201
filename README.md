# LFCS201
E-Learning

#Unit 4
What Are Signals?

Signals are one of the oldest methods of Inter-Process Communication (IPC) and are used to notify processes about asynchronous events (or exceptions).

By asynchronous, we mean the signal-receiving process may:

    Not expect the event to occur.
    Expect the event, but not know when it is most likely to occur.

For example, if a user decides to terminate a running program, it could send a signal to the process through the kernel to interrupt and kill the process.

There are two paths by which signals are sent to a process:

    From the kernel to a user process, as a result of an exception or programming error.
    From a user process (using a system call) to the kernel which will then send it to a user process. The process sending the signal can actually be the same as the one receiving it.

Signals can only be sent between processes owned by the same user or from a process owned by the superuser to any process.

When a process receives a signal, what it does will depend on the way the program is written. It can take specific actions, coded into the program, to handle the signal or it can just respond according to system defaults. Two signals: 

    SIGKILL (#9)
    SIGSTOP (#19)

cannot be handled and will always terminate the program.
