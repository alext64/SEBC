```
sudo less /var/kerberos/krb5kdc/kadm5.acl
```

```
*/admin@ALEXT64.SG      *
cloudera-scm@ALEXT64.SG admilc
```



```
sudo less /var/kerberos/krb5kdc/kdc.conf
```

```
[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88

[realms]
 ALEXT64.SG = {
  #master_key_type = aes256-cts
  acl_file = /var/kerberos/krb5kdc/kadm5.acl
  dict_file = /usr/share/dict/words
  admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
  supported_enctypes = aes256-cts:normal aes128-cts:normal des3-hmac-sha1:normal arcfour-hmac:normal des-hmac-sha1:normal des-cbc-md5:normal des-cbc-crc:normal
 }
```



```
sudo less /etc/krb5.conf
```



```
[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = ALEXT64.SG
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true

[realms]
 ALEXT64.SG = {
  kdc = sebx01.westeurope.cloudapp.azure.com
  admin_server = sebx01.westeurope.cloudapp.azure.com
 }

[domain_realm]
 .alext64.sg = ALEXT64.SG
 alext64.sg = ALEXT64.SG
```

