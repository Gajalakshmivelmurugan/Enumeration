# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

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

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.Following searches for all the sites that is in the domain yahoo.com
## output:
![Screenshot 2024-04-17 180117](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/db7ca857-6edf-4de6-bd81-b3ba5615d03b)
filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.

Following searches for pdf file in the domain yahoo.com
![Screenshot 2024-04-17 180130](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/7a710115-52e0-4880-862a-ec9fc92ff1e9)



intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.

![Screenshot 2024-04-17 180142](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/82e5a31b-50e7-4326-98ae-c3a2e741c497)

inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.
![Screenshot 2024-04-17 180154](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/2a531bae-c6af-4686-b734-c27c517edc13)

intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.
![Screenshot 2024-04-17 180210](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/5387ea07-0a6f-449c-bc13-6ac1f1ed7c4c)


link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.
![Screenshot 2024-04-17 180221](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/b2771722-659d-4a96-88fc-61d4d4677902)


cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.
![Screenshot 2024-04-17 180235](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/88232187-c98f-4f98-a602-032a64c6dea1)

 
#DNS Enumeration


##DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:



![Screenshot 2024-04-17 180248](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/67889a33-9907-421c-b552-ec93345fad7e)

![Screenshot 2024-04-17 180259](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/3bb6b538-d11e-440c-90e6-51d9cafc9718)



##dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.
##output
![Screenshot 2024-04-17 180310](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/e9babb63-f2ed-4c04-8457-3a4d39bcecfc)


##smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.
##output

![Screenshot 2024-04-17 180322](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/e2aa8ec9-e277-4b6d-9939-716192121bdc)

In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:
##output
![Screenshot 2024-04-17 180335](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/de03e13b-60d0-4013-bdaa-ca160cc77c42)

select any username in the first column of the above file and check the same

##output
![Screenshot 2024-04-17 180344](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/a01699be-570c-4c37-8084-d626f0aa33ed)


#Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ## Output
![Screenshot 2024-04-17 180355](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/36447a51-eabb-4358-8f85-eee04fffbdb1)

  

## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:
![Screenshot 2024-04-17 180406](https://github.com/Gajalakshmivelmurugan/Enumeration/assets/144871940/ad12abfc-2315-4953-b800-219612fac1f1)


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

