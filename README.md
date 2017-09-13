## Installs auditd and configures it according to CIS benchmark ##

Works only for arch64, but with minor modifications for files under the roles/linux-hardening/files/ directory - basically changing arch=b64 to b32 would make this work on 32-bit systems as well.

Tested on Centos 7 and Ubuntu Trusty 64.

Usage:

- Configure variables under vars/main.yml
- Configure files/privileged.rules with the help provided in the file
- Auditd rules are divided into separate files under the files directory for easier maintenance. In the target machine, /etc/audit/audit.rules will show them in one file afterwards, if you prefer that format.
- Configure the playbook as needed
- Test with vagrant up. Change operating system in Vagrantfile as needed. Afterwards you should ssh to the box and verify results with 'auditctl -l'


