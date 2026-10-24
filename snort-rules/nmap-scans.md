# Nmap Scan Testing

These commands were used to test scan-related detection in an isolated, authorized lab environment.

Replace `TARGET_IP` with the IP address of your lab target.

## 1. TCP SYN Scan
```bash
sudo nmap -sS -p 1-100 TARGET_IP
```

## 2. TCP ACK Scan
```bash
sudo nmap -sA -p 1-100 TARGET_IP
```

## 3. TCP FIN Scan
```bash
sudo nmap -sF -p 1-100 TARGET_IP
```

## 4. TCP NULL Scan
```bash
sudo nmap -sN -p 1-100 TARGET_IP
```

## 5. TCP Xmas Scan

sudo nmap -sX -p 1-100 TARGET_IP


## 6. UDP Scan

sudo nmap -sU -p 1-100 TARGET_IP


## Validation
After each test, review the Snort alert log and Kibana Discover to check which signatures fired.

## Notes
- Run these commands only against systems you own or are explicitly authorized to test.
- ACK packets and scan signatures can produce false positives; an alert alone does not prove malicious activity.
- Results depend on network configuration, firewall behavior, and Snort rule settings.
