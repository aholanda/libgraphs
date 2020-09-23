# Description

This project studies various Linux source code versions as graphs.
The functions are considered vertices and function calls edges. All data are
stored in [data](data) directory.

[`cflow`](https://www.gnu.org/software/cflow/) is used to generate the function call 
flow and a script were developed to parse `cflow` output into data file.

# Troubleshooting

The following lines must be removed to avoid loops in `cflow`:

* linux-2.5.75.tar.xz
  + line 175: linux-2.5.75/drivers/ieee1394/nodemgr.c
  + line 198: linux-2.5.75/drivers/ieee1394/nodemgr.c
  + line 199: linux-2.5.75/drivers/ieee1394/nodemgr.c
* linux-4.14.14.tar.xz
  + line 996: linux-4.14.4/net/ceph/osd_client.c
  + line 2517: linux-4.14.4/net/ceph/osd_client.c

## References

### Simulators

- [LinSched](https://github.com/jontore/LinSched)
- [Emulate Linux Completely Fair Scheduler (CFS) using threads](https://github.com/ducminh296/Linux-CFS-Emulator).

### Writings

- [Linux Scheduler simulation](https://www.ibm.com/developerworks/library/l-linux-scheduler-simulator/) - Simulating the Linux Scheduler in user space with LinSched
  by M. Tim Jones. IBM Developer, February 23, 2011.
- [Completely Fair Scheduler](https://www.linuxjournal.com/node/10267) by Chandandeep Singh Pabla. Linux Journal, August 1, 2009.
- [CFS Scheduler - kernel documentation](https://www.kernel.org/doc/Documentation/scheduler/sched-design-CFS.txt).

