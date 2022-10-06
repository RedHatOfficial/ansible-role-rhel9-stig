DRAFT DISA STIG for Red Hat Enterprise Linux 9
=========

Ansible Role for DRAFT DISA STIG for Red Hat Enterprise Linux 9  
  
Profile Description:  
This is a draft profile based on its RHEL8 version for experimental purposes.  
It is not based on the DISA STIG for RHEL9, because this one was not available at time of  
the release.  
In addition to being applicable to Red Hat Enterprise Linux 9, DISA recognizes this  
configuration baseline as applicable to the operating system tier of  
Red Hat technologies that are based on Red Hat Enterprise Linux 9, such as:  
- Red Hat Enterprise Linux Server  
- Red Hat Enterprise Linux Workstation and Desktop  
- Red Hat Enterprise Linux for HPC  
- Red Hat Storage  
- Red Hat Containers with a Red Hat Enterprise Linux 9 image

The tasks that are used in this role are generated using OpenSCAP.
See the OpenSCAP project for more details on Ansible playbook generation at [https://github.com/OpenSCAP/openscap](https://github.com/OpenSCAP/openscap)

To submit a fix or enhancement for an Ansible task that is failing or missing in this role,
see the ComplianceAsCode project at [https://github.com/ComplianceAsCode/content](https://github.com/ComplianceAsCode/content)

Requirements
------------

- Ansible version 2.9 or higher

Role Variables
--------------

To customize the role to your liking, check out the [list of variables](defaults/main.yml).

Dependencies
------------

N/A

Example Role Usage
----------------

Run `ansible-galaxy install RedHatOfficial.rhel9_stig` to
download and install the role. Then, you can use the following playbook snippet to run the Ansible role:

    - hosts: all
      roles:
         - { role: RedHatOfficial.rhel9_stig }

Next, check the playbook using (on the localhost) the following example:

    ansible-playbook -i "localhost," -c local --check playbook.yml

To deploy it, use (this may change configuration of your local machine!):

    ansible-playbook -i "localhost," -c local playbook.yml

License
-------

BSD-3-Clause

Author Information
------------------

This Ansible remediation role has been generated from the body of security
policies developed by the ComplianceAsCode project. Please see
[https://github.com/complianceascode/content/blob/master/Contributors.md](https://github.com/complianceascode/content/blob/master/Contributors.md)
for an updated list of authors and contributors.
