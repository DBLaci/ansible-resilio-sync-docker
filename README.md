Role Name
=========

Deploy Resilio Sync (rslsync / btsync) as Docker service.

This role deploys a basic config, all tracker/upnp etc. disabled. We assume `known_hosts` are set.

The directories will be created on the host.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Set `resilio_sync_shared_folders` to a list, see example in defaults/vars.yml

Set `resilio_sync_home_dir` to an absolute path on the server. This will be the base path for the directories set in the `dir` variable in the folder config.

known_hosts has to be set to at least one common server ip for rslsync to work as trackers are disabled in the role.


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-resilio-sync-docker }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
