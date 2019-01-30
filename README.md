Ansible playbooks for system configuration

rhv_guest_agent:
---------------
Install and start RHV agent plugins.  When running, these agents report performance
statistics to the RHV manager and enable additional functionality.  This role works
for both RHEL 6 and 7 guests.


ssh_keys:
--------
Deploy SSH public keys.  This authorizes a client for SSH without passord.
To use, copy one (or multiple) SSH public key files to the roles/ssh_keys/files/
directory.  Note that if this directory doesn't exist, it needs to be created.
If using Tower, this must be owned by the "awx" user.  For example:

=> mkdir roles/ssh_keys/files/
=> chown awx:awx roles/ssh_keys/files/
=> cp /path/to/keys/*.pub roles/ssh_keys/files/


update-hostname.yml:
-------------------
Update host name for a system.  This role deploys a simple /etc/hosts file, and
manually sets the host name to the FQDN.

