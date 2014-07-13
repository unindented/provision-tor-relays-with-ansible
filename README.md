# Provision Tor Relays With Ansible

This repository contains the playbook discussed in my article [Provision Tor Relays With Ansible](http://unindented.org/articles/provision-tor-relays-with-ansible/).

Install [VirtualBox](https://www.virtualbox.org/), [Vagrant](https://www.vagrantup.com/) and [Ansible](http://www.ansible.com/) on your machine, and then run:

```
$ vagrant up
```

You will end up with two [Tor](https://www.torproject.org/) relays listening to port *9001*, and advertising their directory service on port *9030*.

If you browse to `http://localhost:9031` and `http://localhost:9032` you will see their respective notices.


## Contributors

* Daniel Perez Alvarez ([unindented@gmail.com](mailto:unindented@gmail.com))


## License

Copyright (c) 2014 Daniel Perez Alvarez ([unindented.org](http://unindented.org/)). This is free software, and may be redistributed under the terms specified in the LICENSE file.
