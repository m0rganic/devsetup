This is a work in progress...

Personal Development Box
========================

This is a [Vagrant][vagrant], [Ansible][ansible] and [Docker][docker] setup
for my personal development environment. 

Included Packages
-----------------

This environment will set up dev customizations on top of a basebox image 
with Ansible and Docker installed for further specialization, take a look 
at `ansible/setup.yml`. It's simple to add more -- just edit the file and 
run `ansible-playbook` -- see the "Executing" section.

Host System Prerequisites
-------------------------

1. Install [Vagrant][vagrant] from a binary package
2. Install [Ansible][ansible]: `sudo easy_install pip && sudo pip install ansible`
3. Install VirtualBox from a binary package

Setup
-----

TODO

Executing Ansible Commands
---------------------------

To run commands on your Vagrant box using the `ansible` binary, you need
to pass in the private key from vagrant. Here's an example 

    ansible-playbook -i ansible/hosts \
    --private-key=~/.vagrant.d/insecure_private_key \
    ansible/setup.yml --verbose


Author
------

Morgan Bickle, morgan.bickle@gmail.com

License
-------

The MIT License (MIT)

Copyright (c) [2013] [Morgan Bickle]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[vagrant]: http://www.vagrantup.com/
[ansible]: http://www.ansibleworks.com/
