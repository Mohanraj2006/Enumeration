# Explore Google hacking and enumeration 
## NAME:MOHAN RAJ C
## REG NO:212223040114
# AIM:
To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

| Operator    | Description                        | Example Usage           |
| ----------- | ---------------------------------- | ----------------------- |
| `site:`     | Search within a specific domain    | `site:example.com`      |
| `inurl:`    | Search in URL                      | `inurl:admin`           |
| `intitle:`  | Search in page title               | `intitle:"index of"`    |
| `filetype:` | Search by file type                | `filetype:pdf`          |
| `intext:`   | Search inside page text            | `intext:"confidential"` |
| `link:`     | Pages that link to a specific site | `link:example.com`      |
| `cache:`    | View cached version of a site      | `cache:example.com`     |
| `ext:`      | Same as filetype                   | `ext:xls`               |

 ## Architecture 
 ```
+----------------------+
|   Attacker / Hacker  |
|   (Browser & Google) |
+----------+-----------+
           |
           | Google Dork Queries
           v
+---------------------------+
|       Google Search       |
+---------------------------+
           |
           | Indexed Public Content
           v
+---------------------------+
|   Target Websites / Data  |
| - Leaked files            |
| - Open directories        |
| - Sensitive info          |
+---------------------------+

```

# Output:
# SITE:

<img width="1913" height="976" alt="image" src="https://github.com/user-attachments/assets/b204636d-0713-4f8e-8942-a794dd246214" />



# INURL
<img width="1916" height="972" alt="image" src="https://github.com/user-attachments/assets/cc3f26ae-8ace-49fd-a128-018b75231ca0" />


# INTITLE
<img width="1918" height="971" alt="image" src="https://github.com/user-attachments/assets/821b8ed8-255c-4174-81a1-2acab6f7e527" />



# FILETYPE
<img width="1911" height="970" alt="image" src="https://github.com/user-attachments/assets/c4c11c34-2384-45d7-872a-cbca749cf3e1" />


# INTEXT
<img width="1919" height="969" alt="image" src="https://github.com/user-attachments/assets/017b71d8-f97f-4483-9a96-2aa2b1fa226c" />


# LINK
<img width="1919" height="970" alt="image" src="https://github.com/user-attachments/assets/e10e6cdd-5def-4769-8e88-2a5f2ac9cbe2" />


# CACHE
<img width="1919" height="966" alt="image" src="https://github.com/user-attachments/assets/0c4a848c-d8c6-44e3-acc0-9725a2dbe979" />


# EXT
<img width="1919" height="974" alt="image" src="https://github.com/user-attachments/assets/6e205bfc-0cc5-447e-b4f0-644214a59805" />

# DNS Enumeration
<img width="682" height="786" alt="image" src="https://github.com/user-attachments/assets/6cb23fb4-2427-4765-996f-02a54678d04c" />

## DNS Recon
<img width="624" height="498" alt="image" src="https://github.com/user-attachments/assets/61673c8e-0d4d-4c93-8aef-65dc9c5b1fbd" />


| Record Type | Meaning                        | Example Output                   |
| ----------- | ------------------------------ | -------------------------------- |
| A           | Host to IPv4 address           | `example.com -> 93.184.216.34`   |
| AAAA        | Host to IPv6 address           | `example.com -> ::1`             |
| MX          | Mail server info               | `mail.example.com`               |
| NS          | Name servers                   | `ns1.example.com`                |
| TXT         | Misc data (SPF, verifications) | `v=spf1 include:_spf.google.com` |
| CNAME       | Canonical names (aliases)      | `www -> example.com`             |

## Common Tools Used (Kali Linux)

| Tool           | Description                                | Usage Example                           |
| -------------- | ------------------------------------------ | --------------------------------------- |
| `nslookup`     | DNS lookup tool (simple queries)           | `nslookup example.com`                  |
| `dig`          | DNS lookup utility (detailed)              | `dig example.com any`                   |
| `host`         | Simple DNS querying tool                   | `host example.com`                      |
| `dnsenum`      | Perl script to enumerate DNS info          | `dnsenum example.com`                   |
| `fierce`       | DNS scanner to locate non-contiguous IPs   | `fierce -dns example.com`               |
| `dnsrecon`     | Powerful DNS enumeration script            | `dnsrecon -d example.com -a`            |
| `theHarvester` | Subdomain enumeration using search engines | `theHarvester -d example.com -b google` |


## OUTPUT:
# NSLOOKUP
<img width="597" height="769" alt="image" src="https://github.com/user-attachments/assets/0771ec89-79f3-4bf3-a637-2a528d61ba51" />


# DIG
<img width="589" height="580" alt="image" src="https://github.com/user-attachments/assets/c7d74108-2028-41e6-88b1-30bca923c470" />


# HOST
<img width="558" height="390" alt="image" src="https://github.com/user-attachments/assets/466f5505-7ca2-440a-b22a-864e286aee62" />


# DNSSENUM
<img width="650" height="452" alt="image" src="https://github.com/user-attachments/assets/5d7f8f3c-b55b-4c92-94cd-f03bca8bf6ab" />


# DNSRECON
<img width="661" height="505" alt="image" src="https://github.com/user-attachments/assets/89156ffd-240d-473c-8674-c705be7a104a" />

# FIERCE
<img width="615" height="325" alt="image" src="https://github.com/user-attachments/assets/fd8872c1-1f0a-438c-b67e-33f2a2b3a8f5" />

# HARVESTER
<img width="602" height="331" alt="image" src="https://github.com/user-attachments/assets/30c868a5-8735-4cd2-b74d-91e71dc941af" />


## Architecture Diagram 
```
+-------------------+        +------------------+       +------------------+
|                   |        |                  |       |                  |
|   Attacker (You)  +------->|   Target Server   +<----->+    DNS Server    |
| Kali Linux / Parrot|       | (Mail / DNS Host) |       |  (Authoritative) |
+---------+---------+        +---------+--------+       +---------+--------+
          |                            ^                          ^
          |                            |                          |
          |                            |                          |
          |           +-----------------------------+            |
          |           |      Information Tools      |            |
          |           |-----------------------------|            |
          |           | smtp-user-enum              |            |
          |           | nmap --script smtp-enum-*   |            |
          |           | dnsenum                     |<-----------+
          |           +-----------------------------+
          |
          v
+-----------------------------+
|   Output/Report             |
|  - Usernames Found          |
|  - MX Records / Zones       |
|  - Subdomains / IPs         |
+-----------------------------+

```

## dnsenum
**Purpose:** A multithreaded Perl script to enumerate information from DNS servers.

**Use case:** Performs DNS zone transfers, brute force subdomains, and gather host IPs.

```
dnsenum example.com
```

## Output:
<img width="668" height="461" alt="image" src="https://github.com/user-attachments/assets/eee4150d-b2d6-4f8f-a6e7-1ea57a4fa660" />




## smtp-user-enum
**Purpose:** Standalone tool used to enumerate valid users by using the VRFY, EXPN, or RCPT TO commands.

**Use case:** Brute-forces SMTP to find users.

```
smtp-user-enum -M VRFY -U users.txt -t <target-ip>
```
  
 ## Output
<img width="702" height="359" alt="image" src="https://github.com/user-attachments/assets/64ff9a7e-e40f-42e7-8cd3-373c1872af80" />



## nmap –script smtp-enum-users.nse <hostname>

**Purpose:** Uses smtp-enum-users NSE script to enumerate valid users on an SMTP server.

**Use case:** Helps identify email accounts on mail servers.

```
nmap -p 25 --script smtp-enum-users.nse <target-ip>
```
## OUTPUT:
<img width="677" height="177" alt="image" src="https://github.com/user-attachments/assets/6cc19572-672e-43e9-9ae2-0387869c92a7" />



## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
