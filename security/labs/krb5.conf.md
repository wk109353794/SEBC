	[logging]
	default = FILE:/var/log/krb5libs.log
	kdc = FILE:/var/log/krb5kdc.log
	admin_server = FILE:/var/log/kadmind.log
	
	[libdefaults]
	default_realm = WKSEBC.COM
	dns_lookup_realm = false
	dns_lookup_kdc = false
	ticket_lifetime = 24h
	renew_lifetime = 7d
	forwardable = true
	udp_preference_limit = 1
	default_tgs_enctypes = arcfour-hmac
	default_tkt_enctypes = arcfour-hmac 
	
	[realms]
	WKSEBC.COM = {
	kdc = 172.31.1.58
	admin_server = 172.31.1.58
	}
	
	[domain_realm]
	.example.com = WKSEBC.COM
	example.com = WKSEBC.COM
