
# System Baseline Report

## Purpose

This report records the available memory and disk capacity of the Ubuntu environment before monitoring the Nginx web container. These measurements provide a starting point for checking system resources during the activity.

## Memory Information

The `free -h` command showed the following results:

| Resource | Observed Value |
|---|---:|
| Total memory | 1.9 GiB |
| Used memory | 425 MiB |
| Free memory | 1.1 GiB |
| Shared memory | 1.1 MiB |
| Buffer/cache | 513 MiB |
| Available memory | 1.4 GiB |
| Total swap | 1.0 GiB |
| Used swap | 0 B |

The system had approximately 1.5 GiB of available memory. Swap usage was zero during this measurement.

## Disk Information

The `df -h /` command showed the following results:

| Resource | Observed Value |
|---|---:|
| Filesystem | /dev/vda1 |
| Total capacity | 19 GiB |
| Used space | 5.5 GiB |
| Available space | 13 GiB |
| Usage percentage | 30% |

The root filesystem had approximately 13 GiB available, with 30% of its capacity in use.

## Process Monitoring

The `top` command was used to view active processes and their resource consumption. This provides a quick way to check whether a process is using an unusually large amount of CPU or memory.

## Conclusion

These measurements establish the initial resource condition of the environment. They can be compared with container monitoring results to help identify possible resource pressure while the web service is running.
