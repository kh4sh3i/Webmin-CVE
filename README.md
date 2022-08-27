# Webmin CVE
a Curated list of Webmin vulnerability.

## Shodan Dork
```
http.html:"webmin"
```


## CVE-2022-0824
Improper Access Control to Remote Code Execution in GitHub repository webmin/webmin prior to 1.990.

```
nuclei -u target.com:1000 -t CVE-2022-36446.yaml -v -V username=username -V password=password
```


## references
* [CVE-2022-0824](https://nvd.nist.gov/vuln/detail/cve-2022-0824)
