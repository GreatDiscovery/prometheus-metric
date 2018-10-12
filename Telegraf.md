# Metrics collected by telegraf

## cpu metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
cpu_load_average_1m | 
cpu_time_system | Time spent running a virtual CPU for guest operating systems under the control of the Linux kernel |
cpu_time_user | Time spent in user mode |
cpu_time_idle | Time spent in the idle task.  This value should be USER_HZ times
cpu_time_active (must be explicitly enabled by setting report_active = true) | 
cpu_time_nice | Time spent in user mode with low priority (nice).
cpu_time_iowait | Time waiting for I/O to complete.
cpu_time_irq | Time servicing interrupts.
cpu_time_softirq | Time servicing softirqs.
cpu_time_steal | Stolen time, which is the time spent in other operating systems,when running in a virtualized environment
cpu_time_guest | Time spent running a virtual CPU for guest operating systems under the control of the Linux kernel.
cpu_time_guest_nice | Time spent running a niced guest (virtual CPU for guest operating systems under the control of the Linux kernel).

## memory metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
mem_active | integer
available
buffered
cached
free
inactive
slab
total
used
available_percent | float
used_percent | float
wired
commit_limit
committed_as
dirty
high_free
high_total
huge_page_size
huge_pages_free
huge_pages_total
low_free
low_total
mapped
page_tables
shared
swap_cached
swap_free
swap_total
vmalloc_chunk
vmalloc_total
vmalloc_used
write_back
write_back_tmp

## disk metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
free | integer, bytes
total | integer, bytes
used | integer, bytes
used_percent | float, percent
inodes_free | integer, files
inodes_total | integer, files
inodes_used | integer, files

## diskio metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
reads/writes | These values increment when an I/O request completes.
read_bytes/write_bytes | These values count the number of bytes read from or written to this block device.
read_time/write_time | These values count the number of milliseconds that I/O requests have waited on this block device. If there are multiple I/O requests waiting, these values will increase at a rate greater than 1000/second; for example, if 60 read requests wait for an average of 30 ms, the read_time field will increase by 60*30 = 1800.
io_time | This value counts the number of milliseconds during which the device has had I/O requests queued.
weighted_io_time | This value counts the number of milliseconds that I/O requests have waited on this block device. If there are multiple I/O requests waiting, this value will increase as the product of the number of milliseconds times the number of requests waiting (see read_time above for an example).
iops_in_progress | This value counts the number of I/O requests that have been issued to the device driver but have not yet completed. It does not include I/O requests that are in the queue but not yet issued to the device driver.

## net metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
net_bytes_sent | The total number of bytes sent by the interface
net_bytes_recv | The total number of bytes received by the interface
net_packets_sent | The total number of packets sent by the interface
net_packets_recv | The total number of packets received by the interface
net_err_in  | The total number of receive errors detected by the interface
net_err_out | The total number of transmit errors detected by the interface
net_drop_in  | The total number of received packets dropped by the interface
net_drop_out  | The total number of transmitted packets dropped by the interface