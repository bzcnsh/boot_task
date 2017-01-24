Role Name
=========

run a task at system start up, using root's crontab

Requirements
------------

none

Role Variables
--------------

boot_task_src_files: files to be copied
boot_task_dest_dir: target directory for copied files
  default: /etc/boot_task
boot_task_command_text: command to be placed inside root's crontab

Dependencies
------------

none

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: boot_task, boot_task_src_files: msg_of_day, boot_task_command_text: "cat /etc/boot_task/msg_of_day > /tmp/log" }

License
-------

MIT

Author Information
------------------

bzcnsh at yahoo com
