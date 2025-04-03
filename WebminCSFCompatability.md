### Installation Steps

1. **Create the Script**:
    - Save the script to /usr/local/bin/sysvconf:
        
        bash
        
        CollapseWrapCopy
        
        `sudo nano /usr/local/bin/sysvconf`
        
        - Paste the script content, save (Ctrl+O, Enter), and exit (Ctrl+X).
2. **Set Permissions**:
    - Make it executable:
        
        bash
        
        CollapseWrapCopy
        
        `sudo chmod +x /usr/local/bin/sysvconf`
        
3. **Create Symbolic Link** (for CSF compatibility):
    - Link to /usr/sbin/chkconfig:
        
        bash
        
        CollapseWrapCopy
        
        `sudo ln -sf /usr/local/bin/sysvconf /usr/sbin/chkconfig`

This solves this warning and enables the security check to complete in Webmin
[](WebminChkConfigWarning.png)
