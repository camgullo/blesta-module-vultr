# Improved Vultr Module for Blesta

This is a modified version of the official Vultr module for Blesta. It integrates with Vultr via API
v2 and includes significant enhancements for client management, UI improvements, and
performance optimizations.

## Key Features

● API v2 Integration: Fully compatible with Vultr's modern API.  
● Network Management Tab: New tab for clients and admins to view IPv4/IPv6 details and manage Reverse DNS (rDNS).  
● Smart Reinstall: Unified "Reinstall / Change OS" workflow with immediate root password display upon success.  
● Performance Tuning: Optimized API rate limiting (25 req/s) and removed artificial delays for faster page loads.  
● Enhanced UI:  
○ Dashboard service info matches modern standards (Server ID, Root Password, IPv4, IPv6, Hostname).  
○ "Click-to-Copy" buttons for all key fields. 
○ Smart truncation for long IDs and IPv6 addresses to keep the interface clean.  
● Password Sync: Automatically updates the root password in Blesta's database after a reinstall.

## Install the Module

1. Upload the source code to a ```/components/modules/vultr/``` directory within your Blesta
    installation path.
    For example:
    ```/var/www/html/blesta/components/modules/vultr/```
2. Log in to your admin Blesta account and navigate to:Settings > Company > Modules
3. Find the **Vultr** module and click the "Install" (or "Upgrade" if updating) button.
4. Configure the module by adding your Vultr API Key under "Add Account".

## Configuration

To ensure the best performance, it is recommended to enable Caching in Blesta:
Settings > System > General > Cache: Enable

## Blesta Compatibility


```
Blesta Version Module Version
>= v5.0.0 v2.1.0+
```
## License

This software is released under the MIT License.