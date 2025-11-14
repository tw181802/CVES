# CVES
Collections of CVES I have obtained


# CVE-2025-XXXX: WordPress CMS Stored XSS

## Information
**Description:** WordPress CMS is affected by Stored Cross-Site Scripting in permalinks/slug feature. An authenticated attacker with the lowest privileged role (contributor) can exploit this to redirect user to malicious site or control the account.. <br> 
**Versions Affected:** Confirmed on 6.8.3 but affects all versions <br> 
**Version Fixed:** [Pull Request #19646](#) (Open) <br> 
**Researcher:** Trenton Williams (https://youtube.com/@Infin1teXploit)  
**Disclosure Link:** https://#/ <br>
**NIST CVE Link:** https://nvd.nist.gov/vuln/detail/CVE-#

## Proof-of-Concept Exploit
### Description
WordPress CMS is affected by Stored Cross-Site Scripting in permalinks/slug feature. An authenticated attacker with the lowest privileged role (contributor) can exploit this to redirect user to malicious site or control the account.

### Usage/Exploitation
`Payload: ` <br>

![Alt-text that shows up on hover](#.png) 

This will output the malicious SVG file to upload as a profile picture. When this picture is viewed by the "Owner" of the tenant, it will transfer ownership to the attacker. 

![Alt-text that shows up on hover](#.gif) 

## Unofficial Patch
### Description
The vendor does not view this as a valid vector so will not be releasing an official patch, but it’s important to us at Rhino to not release unpatched vulnerabilities. While this is a unique case, we’ve decided to make the patch ourselves which is available at https://github.com/TryGhost/Ghost/pull/19646. 
