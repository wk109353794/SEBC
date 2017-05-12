	[logging]
	 default = FILE:/var/log/krb5libs.log
	 kdc = FILE:/var/log/krb5kdc.log
	 admin_server = FILE:/var/log/kadmind.log
	
	[libdefaults]
	 default_realm = WK109353794.CN
	 dns_lookup_realm = false
	 dns_lookup_kdc = false
	 ticket_lifetime = 24h
	 renew_lifetime = 7d
	 forwardable = true
	
	[realms]
	 WK109353794.CN = {
	  kdc = 172.31.1.194
	  admin_server = 172.31.1.194
	 }
	
	[domain_realm]
	 .example.com = WK109353794.CN
	 example.com = WK109353794.CN