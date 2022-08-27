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
nuclei -u target.com:1000 -t CVE-2022-36446.yaml -v -V username=username -V password=password
```


## references
* [CVE-2022-0824](https://nvd.nist.gov/vuln/detail/cve-2022-0824)
