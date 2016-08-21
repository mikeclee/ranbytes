Notes about Docker 

## Docker-Machine: Boot2Docker

* user: docker
* password: tcuser - [ref](https://github.com/boot2docker/boot2docker)

## Docker-Machine: VirtualBox

[Ubuntu Manage VMS](http://askubuntu.com/questions/457329/shutting-down-all-virtualbox-vagrant-vms-in-one-easy-to-use-bash-command-that)

* VBoxManage list runningvms
    * VBoxManage controlvm <name|uuid> savestate
    * VBoxManage controlvm <name|uuid> poweroff
    * VBoxManage controlvm <name|uuid> acpipowerbutton

<pre>
VBoxManage controlvm <uuid>|<name>
     pause|resume|reset|poweroff|savestate|
     acpipowerbutton|acpisleepbutton|
</pre>

* Use NAT port forward between the VM and Host
     * VBoxManage modifyvm <machine_name> --natpf1 "<forward_name>,tcp,127.0.0.1,2376,,2376"
     * use `controlvm` if the VM is already started

## Docker over VPN (Anyconnect)

* [Jonathan Li's Hack](https://github.com/onejli/docker-vpn-helper)
* [Ian Collington Information](https://www.iancollington.com/docker-and-cisco-anyconnect-vpn/)
* [Stackoverflow 1](http://stackoverflow.com/questions/32174560/port-forwarding-in-docker-machine)

### References

* [Official Docker Repository](https://github.com/docker/docker)
* [Other Cheatsheet Repositories](https://github.com/search?utf8=%E2%9C%93&q=docker+cheatsheet&type=Repositories&ref=searchresults)
