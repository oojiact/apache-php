# apache-php


1. 

$yum install mod_security

edit file /etc/httpd/conf.d/mod_security.conf


SecServerSignature "My Web"



2.

edit file /etc/httpd/conf/httpd.conf

add line 



</IfModule>
<IfModule security2_module>
SecRuleEngine on
ServerTokens Prod
</IfModule>

3.


$systemctl restart httpd 


4.


$curl -s -D - http://localhost -o /dev/null


HTTP/1.1 403 Forbidden
Date: Wed, 22 Aug 2018 11:38:12 GMT
Server: My Web
Last-Modified: Mon, 28 May 2018 16:16:42 GMT
ETag: "f91-56d4671722e80"
Accept-Ranges: bytes
Content-Length: 3985
Content-Type: text/html; charset=UTF-8

