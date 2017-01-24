Role Name
==========

boot_task

runs a task at system startup, by creating a @reboot crontab entry for root

Requirements
------------

none

Role Variables
--------------

boot_task_src_files: files to be copied
  default: []
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
