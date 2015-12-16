#`waitx` System Call

- The files which were modified are in the `modified files` directory.
- Replace the original files in the xv6 source with these files, `make` and then run in `qemu`

This question was about implementing the `waitx` system call. This was done mainly by changing the `proc structure` and `trap call`.

Four new variables `stime` (start time), `etime` (end time), `rtime` (run time) and `iotime` (I/O time) have been added.

- The variable stime is updated when the command is first scheduled on the CPU.
- End time is called when the program exits.
- The runtime is calculated by appropriately calculating the stime, etime and the iotime(the time when the process is sleeping and I/O is going on)

`Ticks` have been used to calculate the time.
