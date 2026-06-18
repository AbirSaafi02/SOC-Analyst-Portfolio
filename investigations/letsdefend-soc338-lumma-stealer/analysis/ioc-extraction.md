# IOC Extraction - SOC338

## Phishing / Web Indicators
- Malicious domain: `windows-update.site`
- URL: `https://windows-update.site/`
- Referrer: `https://mail.letsdefend.io/`
- User-Agent: `Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:122.0) Gecko/20100101 Firefox/122.0`
- Phishing lure: Click Fix / Windows Update prompt

## Malware Indicators
- Malware family: Lumma Stealer
- Tag: `Lumma.Lumma Stealer`
- File hash: `15c80b5be235bf2a8c38291eb697a702c07dde08...`
- Behavior: DLL side-loading
- Payload type: credential theft / data exfiltration

## Endpoint / Process Indicators
- Process: `chrome.exe` accessing malicious URL
- Technique: DLL side-loading from a trusted binary context
- Suspicious DLL load patterns in same folder as legitimate executable
- Unusual child process behavior after download

## Detection / Hunting Rules
- Search for email/web alerts containing `windows-update.site`
- Hunt for process chains where `chrome.exe` or browser processes access unknown update domains
- Look for DLL side-loading indicators in endpoint logs
- Correlate with Lumma Stealer tags or hashes
- Monitor for suspicious files placed beside legitimate loaders

## Recommended Blocking
- Block `windows-update.site` at DNS/web proxy
- Block the identified file hash in endpoint protections
- Block suspicious Click Fix / Windows Update phishing email patterns
- Enforce application whitelisting for update utilities
- Alert on DLL loads from non-standard locations for trusted binaries

## Notes
- Evidence screenshots will be added in `../evidence/`
- Use the collected raw log and search screenshot as supporting artifacts