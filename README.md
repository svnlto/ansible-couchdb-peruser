ansible-couchdb-peruser
========

Install CouchDB including per-user CouchDB plugin.

Requirements
------------

git, curl, build-essential. Requirements are installed by the role.

Role Variables
--------------

Dependencies
------------

No dependencies.

Example Playbook
-------------------------

    - hosts: servers
      roles:
        - role: couchdb-peruser
          couchdb:
            version: 1.6.0
            src: "/home/couchdb/src/couchdb"
            dest: "/home/couchdb/opt/couchdb"
            ini: "templates/couchdb/local.ini"
            repo: "git://github.com/apache/couchdb.git"
            host: "0.0.0.0"
            port: 5984
            peruser_version: 1.0.1
            peruser_src: "/home/couchdb/src/couchdb-1.0.1"
            peruser_dst: "${couchdb.dest}/lib/couchdb/plugins/couchperuser"
            peruser_repo: "git://github.com/etrepum/couchperuser.git"
            rebar_version: 2.5.1
            rebar_src: "/home/couchdb/src/rebar-2.5.1"
            rebar_repo: "git://github.com/rebar/rebar.git"

License
-------

BSD

Author Information
------------------

Sven Lito
