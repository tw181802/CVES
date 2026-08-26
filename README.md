# CVES
Collections of CVES I have obtained


# CVE-2026-39070: WordPress PLugin (Bit Assist) Stored XSS

## Information
**Description:** WordPress plugin (Bit Assist) is affected by Stored Cross-Site Scripting in Call-To-Action feature. An authenticated attacker with the  privileged role (administrator) can exploit this to redirect user to malicious site or control the account. The javascript will execute for unauthenticated users visiting the site <br> 
**Versions Affected:** Confirmed on 1.7.1 and lower <br> 
**Version Fixed:** 1.7.2(#) (Open) <br> 
**Researcher:** Trenton Williams (https://youtube.com/@Infin1teXploit)  
**Disclosure Link:** https://#/ <br>
**NIST CVE Link:** https://nvd.nist.gov/vuln/detail/CVE-#

## Proof-of-Concept Exploit
### Description
WordPress plugin (Bit Assist) is affected by Stored Cross-Site Scripting in Call-To-Action feature. An authenticated attacker with the  privileged role (admin) can exploit this to redirect user to malicious site or control the account. The javascript will execute for unauthenticated users visiting the site.

### Usage/Exploitation
``` 
Payload: javascript:/*–></title></style></textarea></script></xmp><details/open/ontoggle='+/`/+/"/+/onmouseover=1/+/[*/[]/+alert(/@PortSwiggercalltoactionRes/)//'>
```

To help you reproduce the issue in version 1.7.1, I’ve attached step-by-step screenshots. The process is as follows:
Navigate to the plugin dashboard.
Select the widget (in my example, the widget is named “test”)
<img width="1153" height="173" alt="image" src="https://github.com/user-attachments/assets/c5177fe0-0544-4ab8-b27a-833a1536ca52" />


Click into the widget and go to the Settings section (as shown in the screenshot).
Locate the Call to Action form field.
<img width="621" height="614" alt="image" src="https://github.com/user-attachments/assets/45cc0339-db71-463b-9ce8-3b804c880ad7" />

Insert the provided payload into this field.
```
javascript:/*–></title></style></textarea></script></xmp><details/open/ontoggle='+/`/+/"/+/onmouseover=1/+/[*/[]/+alert(/@PortSwiggercalltoactionRes/)//'>
```
Save/update the widget and observe the behavior when the input is rendered.

<img width="585" height="447" alt="image" src="https://github.com/user-attachments/assets/48faa6db-6e64-48d9-9970-112a8c042557" />



The attached screenshots walk through each of these steps and demonstrate the issue clearly.

## Unofficial Patch
### Description
The vendor have patched this in version 1.7.2. 



# CVE-2026-39071: WordPress PLugin (Spiffy Plugin) Stored XSS

## Information
**Description:** WordPress plugin (Spiffy Plugin) is affected by Stored Cross-Site Scripting in Event Title field. An authenticated attacker with the lowest privileged role (contributor) can exploit this to redirect user to malicious site or control the account. <br> 
**Versions Affected:** Confirmed on 5.0.8 and lower <br> 
**Version Fixed:** 5.0.9(#) (Open) <br> 
**Researcher:** Trenton Williams (https://youtube.com/@Infin1teXploit)  
**Disclosure Link:** https://#/ <br>
**NIST CVE Link:** https://nvd.nist.gov/vuln/detail/CVE-#

## Proof-of-Concept Exploit

Navigate to the Event Title and Enter the Payload
```
<image/src/onerror=prompt(10)>
```
<img width="1060" height="673" alt="Screenshot 2026-04-01 015456" src="https://github.com/user-attachments/assets/be3c0541-3820-420f-8b93-a7522603122f" />
<img width="722" height="130" alt="Screenshot 2026-04-01 015727" src="https://github.com/user-attachments/assets/c02a2508-9766-4e2d-835e-1aee632dbf53" />


And Navigate to the Page
<img width="1157" height="513" alt="Screenshot 2026-04-01 015445" src="https://github.com/user-attachments/assets/eda281b4-702f-4908-bd5a-3ae5ad62c904" />


### Description
WordPress plugin (Spiffy Calendar) is affected by Stored Cross-Site Scripting in Event Title field. An authenticated attacker with the  privileged role (admin) can exploit this to redirect user to malicious site or control the account

### Description
The vendor have patched this in version 5.0.9

