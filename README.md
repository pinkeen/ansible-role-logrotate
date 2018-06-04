# Universal role for adding new logs to logrotate. (Centos6/7)

Supported vars:
 - logrotate_logs - each item should contain:
   - name - name of the log/program - used for conf file naming
   - path - path to the log file / can be a glob
   - reload_service (optional) - service to reload post_rotate
   - max_size (default: '10M') - max log size before being rotated
   - max_count (default: 5) - nr of old log files kept
   - email (optional) - the email address which is mailed the log files being rotated out of existence
   - su_user (optional) - Required when rotating logs not owned by root,
                          or located in a world-writable directory.
   - su_group (required if `su_user`) - same as above.
