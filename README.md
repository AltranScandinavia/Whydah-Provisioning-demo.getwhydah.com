Singapore Emergency Provisioning
===================

Prerequisites
-------------
* Ansible [http://www.ansible.com/get-started] on local (via apt-get on ubuntu, yum on Red hat and brew on Mac)
* One or more Red Hat servers to be installed on
* SSH authentication keys (.pem /.ppk) available for servers

Getting started
---------------
This project requires configuration that is specific for your domain and may be sensitive.
The best alternative is to have these files in an own folder/project, and sym-link the files/folders in to avoid the possibility of erronously storing sensitive data the wrong place.

Given a project "My-Whydah-Config" located in the

Provisioning
------------
time ansible-playbook -i hosts provision-app.yml --private-timestamp=~/.ssh/...

Alternatives:

* --private-timestamp=~/mykeyfile.pem
* -vvvv <- For debugging
* --help
* --tags uib | sts | sso | adminapp <- To run one of the setups