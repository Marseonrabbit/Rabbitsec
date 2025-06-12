## Active Directory 
- its a phone book for windows.
- non-windows devices, like Linux, firewall can also authenticate to AD via RADIUS or LDAP.
- There are 2 components physical and logical.
- ## Physical
	- data store 
	- domain controller 
	- global catalog server
	- Read-only domain(RODC
- ## Logical
- Partitions 
- schema Domains
	- defines every type of object that can be stored in the directory
	- Enforces rules regarding object createion and configuration
	- object types 
		- class object - what objects can be create in the dir - user, computer.
		- attribute object information that can be attached to an object - display name
- domain trees
- forests
- sites
-  Organization Units(OUs)
---
### Domain controllers
- Host a copy of the AD DS directory store 
- Provide authentication and authorization services
- Replicate updates to other DC in the domain and forest
- Allow admin to access to manage user accounts and network resources
---
### AD DS data store
- consists of the Ntds.dit file
- is stored by default in the %systemrroot%\NTDS folder on all domain controllers 
- is accessible only through the DC processes and protocols
---

