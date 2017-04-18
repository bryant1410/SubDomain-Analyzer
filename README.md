SubDomain Analyzer
==================

The "SubDomain Analyzer" tool written in Python language.
The purpose of "SubDomain Analyzer" getting full detailed information of selected domain.
The "SubDomain Analyzer" gets data from domain by following steps:

1. Trying to get the `zone tranfer` file.
2. Gathers all information from DNS records.
3. Analyzing the DNS records (Analyzing all IP's addresses from DNS records and test class C range from IP address (For example: 127.0.0.1/24) and getting all data that containing the domain being analyzed).
4. Tests subdomains by dictionary attack.

The Subdomain Analyzer can keep new addresses which found on DNS records or IP's analyzer.
The Subdomain Analyzer can brings a very qualitative information about the domain being analyzed,
additionally, he shows a designed report with all the data.

##### Examples:
* Analyzing `example.com` domain:
`subdomain-analyzer.py example.com`
* Analyzing `example.com` domain, save the records on log file by name `log.txt`, works with 100 threads and use by another dictionary file by name `another-file.txt`:
`subdomain-analyzer.py example.com --output log.txt --threads 100 --sub-domain-list another-file.txt`
* Analyzing `example.com` domain, save the records on log file by name `log.txt` and append a new sub-domains to sub-domains list file:
`subdomain-analyzer.py example.com -o log.txt --sub-domain-list`

Requirements:
===============
### Linux Installation:
1. sudo apt-get install python-dev python-pip
2. sudo pip install -r requirements.txt
3. easy_install prettytable

### MacOSx Installation:
1. Install Xcode Command Line Tools (AppStore)
2. sudo easy_install pip, prettytable
3. sudo pip install -r requirements.txt

### Windows Installation:
1. Install [dnspython](http://www.dnspython.org/)
2. Install [gevent](http://www.lfd.uci.edu/~gohlke/pythonlibs/#gevent)
3. Install [prettytable](https://pypi.python.org/pypi/PrettyTable)
4. Open Command Prompt(cmd) as Administrator -> Goto python folder -> Scripts (cd c:\Python27\Scripts)
5. pip install -r (Full Path To requirements.txt)
6. easy_install prettytable
