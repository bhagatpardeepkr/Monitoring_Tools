echo | openssl s_client -connect <domain>:443 2>/dev/null | openssl x509 -noout -dates
