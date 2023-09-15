# roundcube


### SSL

If hostnames do not match the SSL certs, such as a docker aliases, ssl connection will fail.  

Add this to `/var/www/html/config/config.docker.inc.php`.  

```
$config['imap_conn_options'] = [
	'ssl' => [
		'verify_peer' => false,
		'verify_peer_name' => false,
		'allow_self_signed' => true,
	],
	'tls' => [
		'verify_peer' => false,
		'verify_peer_name' => false,
		'allow_self_signed' => true,
	]
];
	
$config['smtp_conn_options'] = [
	'ssl' => [
		'verify_peer' => false,
		'verify_peer_name' => false,
		'allow_self_signed' => true,
	],
	'tls' => [
	'verify_peer' => false,
	'verify_peer_name' => false,
	'allow_self_signed' => true,
	]
];
```
