# windows server fundamentals 1

### Peer - to - Peer network (workgroup)
- A peer to peer is a network that allows the user to share resources and information among themselves.
- user must remember which computer in the workgroup have have shared resources and information they want as there is no central location for authentocated users storing files or accessing resources.
- in order to access computers shared resources user must logon on to each computers.
- in most peer to peer network, the data is typically stored on multiple computers, making it difficult for user to track where the information is located.
- because multiple versions of same file exists in different computers in same workgroup, this makes backing up critical business information diffcult.
It freqently leads to small businesses failing to complete back up.

#### Slide 1:
<img width="950" height="465" alt="Screenshot 2026-03-26 at 8 56 57 PM" src="https://github.com/user-attachments/assets/f76bb0cc-976c-4fa7-9dfc-8c1375a4d64f" />

### networking basics
- service based network
-   server is a central location where users share and access network resources in a server-based network.
-   the level of access that users must share resources is controlled by the dedicated computer.
-   because shared data is in one place it is simple to backup important business data.
-   because users have only one user account & password to log on to the server and access to shared resources a server based network is the best
    network for sharing resources and data while providing centralised network security for those resources and data.
-   when multiple clients computers access the server based resources, the server operating system are designed to handle the load.


### server roles
A "server role" is a primary function performed by the server. a server can perform multiple functions.

Types of servers:
- file server
- print server
- werb server
- remote access
- application server
- email server
- database server
- monitoring server
- threat management server

### selecting server hardware
- Servers primary function to provide network services. It is designed to be used by multiple users at the same time hence it is typically more powerfull than client PCs.
- Choosing right harware is important in order to make server less prone to failures.
- following are main subsystems that make a server:
-    processor
-    memory
-    storage
-    network

### virtual servers
- with virtual machine and virtual server technology multiple operating system can run on single machine.
- server seperaton is enabled by the ability to run multiple operating systems on single machine, allowing changes on one virtual machine have no impact on other virtual machine.
- furthermore most of harware remains idle for most of time, it allows for better utilisation.
- by putting several virtual servers on a powerfull server, you can make better use of hardware while keeping costs low.
- it can also create windows test environment in a secure, self contained environment.

# windows server fundamentals 2

## naming resolution
- resolving name to one or more IPs is naming resolution
- DNS fully qulified domain names (FQDNs) and single label names can be resolved by windows
- DNS and NetBIOS can both resolbe single label names.

- Two types of names that need to be translated
  1. domain names / hostnames - which reside in domain name system.
  2. computer names also called NetBIOS name
- DNS manager
  - Type of computer program that manages DNS cluster. DNS data is spread across several servers. Its goals are to reduce human error when editing complex and repeatative DNS data.
- Universal naming convention (UNC)
  - method of identifying shared file on computer over a network, without having to specify the storage device it is on.
  - can be used instead of local naming system.
- DNS Globalname Zone
  - DNS database special zone used for single label naming resolution
  - TBD
 
- DHCP server (dynamic host configuration protocol) 
  - is a network server tht assigns IP address, default gateway and other network parameters to client devices on regular basis.
  - to respond to broadcast queries from client, it uses DHCP as a standard protocol.
  - when a DHCP client starts up and requires an IP address it broadcasts request to DHCP server to lease address.
  - messages are sent to UDP port 67 and UDP port 68 by the server.

## directory services 1
Also known as name service, connects names of network to their IP address. It stores, organises and makes info in directory accessible. Used to find, manage and organise common items and network. resources such as volumes, folders, files, printers, users, groups, devices, phone numbers and other objects.

Active directory services - provides a wide range network services such as:
- kerberos based authentication system
- single sign-on authentication
- DNS based naming and other network information
- a single point of administration and delegation of authority for the network


Lightweight directory access protocol (LDAP)
- Application protocol for querying and momdifing data in TCP/IP based directory services. TCP port 389 is used.
- TBD
- TBD

Kerberos
- computer network authentication protocol that allows hosts to authenticate themselves securely over insure networks.
- allows mutual authentication  for client and server to confirm each others identity.
- kerberos messages from protected from evesdropping and replay attacks for security reasons

Single Sign On (sso)
* it allows login once and access multiple related but seperate software systems without logging out.
* when you logon to windows using active directory, your given token to automatically sign on to other systems.

Active directory services have logical divisions:
- domain
  - windows domain is logical grouping of computers and networking resources that serves as a security perimeter.
  - a domain shares common security and user account information for all computers within the domain in a single active directory database,           allowing centralised administration for all user groups and resources on the network.
  - for orgs having thousands of user and computers it may be necessary for them to divide them into multiple domains.
- tree
  -  multiple domains with a contigious namespace, hirarchical namespace
  -  if abc.com is primary domain then more than one child domains can be associated with it eg: sales.abc.com and marketing.abc.com
- forest
  -  made up of mutiple trees
  -  
