# sysvconf
This script aims to provide the functionality and ease of use of Red Hat's chkconfig for Devuan using SysVInit.

#### Limitations:
- update-rc.d doesn’t support all chkconfig nuances (e.g., exact sequence numbers like S20). The script uses defaults, which may differ from Red Hat’s behavior.
- Status checks (/etc/init.d/$service status) are not fully implemented; add parsing if needed based on your init scripts.
- Customization: Adjust update-rc.d options (e.g., start 20 2 3 4 5 . stop 20 0 1 6 .) for precise control.
- Testing: Test with other services to ensure compatibility across your system.
#### Conclusion
This script provides a robust replacement for chkconfig, supporting its primary flags and adapting to Devuan’s sysvinit. 
### Webmin ConfigServer Security check & csf compatible
 [WebminCSFCompatability](WebminCSFCompatability.md)

### Setup
- clone the repo
- EX:(Using https) 
- $ git clone https://github.com/landNull/sysvconf.git
- $ cd sysvconf
- $ sudo or su - mv sysvconf /usr/local/bin
- $ sudo chmod +x /usr/local/bin/sysvconf
- $ sysvconf --help
  
"Usage: /usr/local/bin/sysvconf [--list] [service] [on|off] [--level <levels>]
  --list           List all services and their runlevel statuses
  --add <service>  Add a new service to the init process
  --del <service>  Remove a service from the init process
  <service> on     Enable service for default runlevels
  <service> off    Disable service for default runlevels
  --level <levels> Specify runlevels (e.g., 2 3 5) for on/off"
