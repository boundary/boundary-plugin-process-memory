Boundary Process Memory Plugin (Deprecated)
-------------------------------------------

### Note : This plugin is deprecated, use [Process plugin](https://help.truesight.bmc.com/hc/en-us/articles/214110829-Process-Plugin) instead.

Displays memory use (RSS) for specific processes. Use Regular Expressions to specify a process name, process full path, and/or the process current working directory. Currently only works for Linux based systems that support procfs (i.e. have a/proc directory). **Note**: to monitor processes with elevated priviledges requires running the meter as root, which is not recommended.

### Prerequisites

|     OS    | Linux | Windows | SmartOS | OS X |
|:----------|:-----:|:-------:|:-------:|:----:|
| Supported |   v   |    -    |    -    |  -   |


|  Runtime | node.js | Python | Java |
|:---------|:-------:|:------:|:----:|
| Required |    +    |        |      |

- [How to install node.js?](https://help.boundary.com/hc/articles/202360701)

### Plugin Setup

None

#### Plugin Configuration Fields

|Field Name        |Description                                                                                   |
|:-----------------|:---------------------------------------------------------------------------------------------|
|Source            |The source to display in the legend for the memory data.                                      |
|Process Name Regex|A regular expression to match the name of the process.                                        |
|Process Path Regex|A regular expression to match the full path of the process.                                   |
|Process CWD Regex |A regular expression to match the current working directory of the process.                   |
|Reconcile option  |How to reconcile in the case that multiple processes match.  Set to First Match to use the first matching process, Parent to choose the parent process (useful if process is forked), or Longest Running to pick the process that has been running the longest.|

### Metrics Collected

|Metric Name   |Description                   |
|:-------------|:-----------------------------|
|Memory Process|Process specific memory usage.|
