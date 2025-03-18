# DoT

45.90.28.0,45.90.30.0

sudo nano /etc/systemd/resolved.conf

[Resolve]
DNS=45.90.28.0#.dns.nextdns.io
DNS=2a07:a8c0::#.dns.nextdns.io
DNS=45.90.30.0#.dns.nextdns.io
DNS=2a07:a8c1::#.dns.nextdns.io
DNSOverTLS=yes
FallbackDNS=
DNSSEC=yes
Cache=no-negative

sudo systemctl enable systemd-resolved;
sudo systemctl restart systemd-resolved;
sudo systemctl restart NetworkManager;
sudo resolvectl status;
