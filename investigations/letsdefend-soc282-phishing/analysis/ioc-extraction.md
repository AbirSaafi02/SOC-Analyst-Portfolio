# IOC (Indicators) - Simple Version

## Email info (what to look for)
- Sender: look for strange or misspelled emails
- Subject: offers like "Free Coffee Voucher" are suspicious
- Headers: SPF/DKIM/DMARC may fail for spoofed emails

## File info
- Attachment name: `free-coffee.zip` (password: `infected`)
- Inside: `Coffee.exe` (Windows executable)
- VirusTotal: 61/75 vendors flagged the file
- Use MD5/SHA256 hashes from the case for exact blocking rules

## Endpoint signs (what to hunt for)
- Process name: `Coffee.exe` running
- Parent process: usually `explorer.exe` (user double-clicked)
- File path: often in `C:\Users\<user>\Downloads\`
- Check for network connections from that host after execution

## Simple hunting rules
- Search SIEM for password-protected ZIP attachments with EXE inside
- Search for process executions from `Downloads` with unusual names
- Cross-check suspicious files with VirusTotal

## Quick blocking suggestions
- Email gateway: block password-protected ZIPs that contain EXEs
- Endpoint: block the file hash (MD5/SHA256) after confirming
- Network: block known C2 IPs/domains if found
