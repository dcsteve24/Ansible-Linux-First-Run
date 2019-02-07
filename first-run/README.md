Role Name
=========

Uses the raw command to install python as required for ansible. Should be inserted as a role for the very first run on the target.

The main play in /etc/playbooks/ must have gather_facts:false for this to work since gather_facts pieces uses python.

Author Information
------------------

Steven Craig, ISSM, BESL
