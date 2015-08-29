# ansible
Ansible is a configuration management solution developed by Michael DeHaan.

Topics:
* Cloud Provisioning (vSphere, EC2 and Openstack)
* Windows Server management:
	* Install 3rd-party apps
	* Enabling Windows Features
	* Working with Services
	* Copy files
	* Windows Templating
	* Running PowerShell scripts
* Dynamic inventories (hosts file management)

## Windows Server Management setup

How do I get set up?
* You will need a Linux Control Machine
* Latest ansible version from EPEL repository
* Windows boostraping:
	* .NET Framework 4.0
	* Enable execution of scripts ($ Set-ExecutionPolicy RemoteSigned)
	* Power Shell 3.0 or higher
	* Run the "ConfigureRemoteforAnsible" script https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1
	* A local administrator account
	* On Windows 7 and Server 2008 R2 machines, due to a bug in Windows Management Framework 3.0, it may be necessary to install this hotfix http://support.microsoft.com/kb/2842230 to avoid receiving out of memory and stack overflow exceptions.
	* Hack --> you may need new version of both files: win_feature.ps1 and win_feature.py
