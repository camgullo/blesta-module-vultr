# Changelog

All notable changes to the Vultr module will be documented in this file.

## [2.1.0] - 2025-11-29

## Added

● Network Tab: Added a dedicated tab for both Admin and Client views to list IPv4 and IPv6 addresses.  
● Reverse DNS: Added functionality to update Reverse DNS (rDNS) directly from the Network tab.  
● Password Capture: The new root password is now captured and displayed immediately after a server reinstall.  
● Password Sync: The new root password is now automatically saved to the local Blesta database after a reinstall, ensuring it remains visible on the dashboard.  
● Click-to-Copy: Added copy-to-clipboard buttons for Server ID, IP Addresses, Password, and Hostname in the service information tables.

## Changed

● UI Overhaul: Redesigned the "Service Information" table on the Dashboard and Admin Service page to display Server ID, Root Password, IPv4, IPv6, and Hostname in a cleaner layout.  
● Reinstall Workflow: Combined "Reinstall" and "Change Template" into a single "Reinstall / Change OS" button with a confirmation popup to prevent accidental data loss.  
● Performance: Removed legacy usleep delays and optimized API rate limiting to 25 requests/second, significantly speeding up package configuration and page loads.  
● Data Display: Implemented smart CSS truncation for long fields (IPv6, Server ID) to prevent table layout breakage while keeping data accessible via tooltip and copy button.

## Fixed


● Fixed an issue where the "Statistics" tab would hide the password row if the API returned a null value (added fallback to local database).  
● Fixed "Internal Error" messages during reinstall by properly handling API response timeouts.