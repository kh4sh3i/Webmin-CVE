# Webmin CVE
a Curated list of Webmin vulnerability.

## Shodan Dork
```
http.html:"webmin"
```

## default credential
root:unix_root_password
You should be able to login as root, using the same password as the root Unix user on your Linux system. However, if you change the Unix root password in future the Webmin root user will not change. This is because the package install just copies the current password from the /etc/shadow file.

## installing url
 http://_your-systems-hostname_:10000/


## CVE-2022-0824
Improper Access Control to Remote Code Execution in GitHub repository webmin/webmin prior to 1.990.

```
nuclei -u target.com:1000 -t CVE-2022-0824.yaml -v -V username=username -V password=password
```



## CVE-2022-36446
software/apt-lib.pl in Webmin before 1.997 lacks HTML escaping for a UI command.

```
nuclei -u target.com:1000 -t CVE-2022-36446.yaml -v -V username=username -V password=password
```



## references
* [CVE-2022-0824](https://nvd.nist.gov/vuln/detail/cve-2022-0824)
* [installing webmin](https://doxfer.webmin.com/Webmin/Installing_Webmin)
* [Webmin Security Vulnerabilities](https://www.cvedetails.com/vulnerability-list/vendor_id-358/Webmin.html)
* [CVE-2022-36446](https://www.tenable.com/cve/CVE-2022-36446)