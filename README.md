# ansible-role-systemd-tweaks
Ansible role for tweaking the defaults of systemd to better suit HPC

The default tmp.conf config file for systemd-tmpfiles deletes any files untouched for 10 days from /tmp.
This is a problem for temporary files from HPC jobs with max run times up to 30 days.

This role creates an overriding file in /etc/tmpfiles.d/ with configurable deletion times.

