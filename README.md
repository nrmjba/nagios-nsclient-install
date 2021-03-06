# NSClient++ Unattended Installation for Windows
Installs NSClient (32/64 bit) in NRPE mode with your favorite settings and plugins.

## Installation

### Download this repo as zip file to your windows server
https://github.com/gardart/nagios-nsclient-install/archive/master.zip

### Change configuration settings

* Change the file `files/allowed_hosts.ini`
```
[/settings/default]
allowed hosts = 127.0.0.1,{ip_address_of_your_nagios_server}
```

* `Optional:` Make your changes in `files/nsclient.ini` . This configuration is currently configured for NRPE mode

### Install NSClient++

Run Unattended_Setup.vbs to begin silent unattended installation. 

The installation script will do the following:

* Stop NSClient++ service
* Install the correct package depending on your system architecture (32/64 bit)
* Install Firewall Rules for NSClient++
* Install your custom plugins and config files
* Start the NSClient++ service

If you have older msi setup of NSClient++, it will be updated.

