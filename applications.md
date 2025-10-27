# Application Configuration

## Definitions

## Statements
### Log Files
1. An application should have just one configuration for their application log files
2. An application may have one configuration when they are run on a cluster or server and another configuration when they are run on a client log
3. Applications should not send log data to both a log file and the console
4. Application must rotate their log files and should limit their logs to 10 files of 20 megabytes or thirty days of logs
5. Application log files that fall outside of the rotation policy must be deleted
