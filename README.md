# Google Dorks for Bug Bounty

A list of Google Dorks for Bug Bounty, Web Application Security, and Pentesting

[Live Tool](https://taksec.github.io/google-dorks-bug-bounty/)

[![tool screenshot](https://github.com/TakSec/google-dorks-bug-bounty/assets/27094033/3ff009d7-f402-4eb2-8321-ce22eeeb5605)](https://taksec.github.io/google-dorks-bug-bounty/)

[![Twitter URL](https://img.shields.io/twitter/url/https/twitter.com/TakSec.svg?style=social&label=Follow%20%40TakSec)](https://twitter.com/TakSec)
</p>

---

### Broad domain search w/ negative search <!--omit-->

```
site:example.com -www -shop -share -ir -mfa
```

### PHP extension w/ parameters

```
site:example.com ext:php inurl:?
```

### API Endpoints

```
site:example.com (inurl:api OR inurl:/rest OR inurl:/v1 OR inurl:/v2 OR inurl:/v3)
```

### Juicy Extensions

```
site:example.com (ext:log OR ext:txt OR ext:conf OR ext:cnf OR ext:ini OR ext:env OR ext:sh OR ext:bak OR ext:backup OR ext:swp OR ext:old OR ext:~ OR ext:git OR ext:svn OR ext:htpasswd OR ext:htaccess OR ext:json)
```

### High % inurl keywords

```
site:example.com (inurl:conf OR inurl:env OR inurl:cgi OR inurl:bin OR inurl:etc OR inurl:root OR inurl:sql OR inurl:backup OR inurl:admin OR inurl:php OR inurl:websql)
```

### Server Errors

```
site:example.com (intitle:"exception" OR intext:"Warning: mysql_connect()" OR intitle:"failure" OR intext:"on * using password:" OR intitle:"server at" OR inurl:exception OR "database error" OR "SQL syntax" OR "undefined index" OR "unhandled exception" OR "stack trace")
```

### XSS prone parameters

```
site:example.com (inurl:q= OR inurl:s= OR inurl:"search=" OR inurl:"query=" OR inurl:"keyword=" OR inurl:lang=)
```

### Open Redirect prone parameters

```
site:example.com (inurl:url= OR inurl:return= OR inurl:next= OR inurl:redirect= OR inurl:redir= OR inurl:ret= OR inurl:r2= OR inurl:page= OR inurl:go= OR inurl:dest= OR inurl:target=) OR (intitle:"Redirecting..." OR intitle:"Redirect")
```

### SQLi Prone Parameters

```
site:example.com (inurl:id= OR inurl:pid= OR inurl:category= OR inurl:cat= OR inurl:action= OR inurl:sid= OR inurl:dir= OR inurl:page= OR inurl:p= OR inurl:num= OR inurl:offset= OR inurl:limit= OR inurl:start= OR inurl:end=)
```

### SSRF Prone Parameters

```
site:example.com (inurl:http OR inurl:https) (inurl:url OR inurl:path OR inurl:dest OR inurl:target OR inurl:redirect OR inurl:location OR inurl:goto OR inurl:link) (inurl:file OR inurl:load OR inurl:get OR inurl:include OR inurl:source OR inurl:resource OR inurl:lookup OR inurl:resolve OR inurl:open OR inurl:read OR inurl:access OR inurl:retrieve OR inurl:obtain OR inurl:acquire OR inurl:procure)
```

### LFI Prone Parameters

```
site:example.com (inurl:include OR inurl:inc OR inurl:require OR inurl:load OR inurl:source OR inurl:page OR inurl:file OR inurl:doc OR inurl:conf OR inurl:config OR inurl:xml OR inurl:php OR inurl:txt) (inurl:dir OR inurl:path OR inurl:folder OR inurl:file OR inurl:page OR inurl:view)
```

### RCE Prone Parameters

```
site:example.com (inurl:cmd OR inurl:exec OR inurl:execute OR inurl:run OR inurl:shell OR inurl:system OR inurl:os) (inurl:query OR inurl:search OR inurl:find OR inurl:lookup OR inurl:locate OR inurl:get OR inurl:fetch) (inurl:data OR inurl:input OR inurl:param OR inurl:arg OR inurl:value OR inurl:option)
```

### File upload endpoints

```
site:example.com ”choose file”
```

### API Docs

```
site:"example[.]com" inurl:apidocs | inurl:api-docs | inurl:swagger | inurl:api-explorer
```

### Login Pages

```
site:example[.]com inurl:login | inurl:signin | intitle:login | intitle:signin | inurl:secure | inurl:sign-in | inurl:portal
```

### Test Environments

```
inurl:test | inurl:env | inurl:dev | inurl:staging | inurl:sandbox | inurl:debug | inurl:temp | inurl:internal | inurl:demo site:example.com
```

### Sensitive Documents

```
site:example.com ext:txt | ext:pdf | ext:xml | ext:xls | ext:xlsx | ext:ppt | ext:pptx | ext:doc | ext:docx
intext:“confidential” | intext:“Not for Public Release” | intext:”internal use only” | intext:“do not distribute”
```

### Sensitive Parameters

```
inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:example[.]com
```

### Adobe Experience Manager (AEM)

```
inurl:/content/usergenerated | inurl:/content/dam | inurl:/jcr:content | inurl:/libs/granite | inurl:/etc/clientlibs | inurl:/content/geometrixx | inurl:/bin/wcm | inurl:/crx/de site:example[.]com
```

### Disclosed XSS and Open Redirects

```
site:openbugbounty.org inurl:reports intext:"example.com"
```

### Google Groups

```
site:groups.google.com "example.com"
```

### Code Leaks

```
site:pastebin.com "example.com"
```

```
site:jsfiddle.net "example.com"
```

```
site:codebeautify.org "example.com"
```

```
site:codepen.io "example.com"
```

### Cloud Storage

```
site:s3.amazonaws.com "example.com"
```

```
site:blob.core.windows.net "example.com"
```

```
site:googleapis.com "example.com"
```

```
site:drive.google.com "example.com"
```

```
site:dev.azure.com "example[.]com"
```

```
site:onedrive.live.com "example[.]com"
```

```
site:digitaloceanspaces.com "example[.]com"
```

```
site:sharepoint.com "example[.]com"
```

```
site:s3-external-1.amazonaws.com "example[.]com"
```

```
site:s3.dualstack.us-east-1.amazonaws.com "example[.]com"
```

```
site:dropbox.com/s "example[.]com"
```

```
site:box.com/s "example[.]com"
```

```
site:docs.google.com inurl:"/d/" "example[.]com"
```

### JFrog Artifactory

```
site:jfrog.io "example[.]com"
```

### Firebase

```
site:firebaseio.com "example[.]com"
```

### JWT Token

```
site:example.com intext:Bearer
```

```
site:example.com inurl:token=
```

```
site:example.com ext:json intext:jwt
```

## Dorks that work better w/o domain

### Bug Bounty programs and Vulnerability Disclosure Programs <!--omit-->

```
"submit vulnerability report" | "powered by bugcrowd" | "powered by hackerone"
```

```
site:*/security.txt "bounty"
```

### Apache Server Status Exposed <!--omit-->

```
site:*/server-status apache
```

### WordPress <!--omit-->

```
inurl:/wp-admin/admin-ajax.php
```

### Drupal <!--omit-->

```
intext:"Powered by" & intext:Drupal & inurl:user
```

### Joomla <!--omit-->

```
site:*/joomla/login
```


---

Medium articles for more dorks:

https://thegrayarea.tech/5-google-dorks-every-hacker-needs-to-know-fed21022a906

https://infosecwriteups.com/uncover-hidden-gems-in-the-cloud-with-google-dorks-8621e56a329d

https://infosecwriteups.com/10-google-dorks-for-sensitive-data-9454b09edc12

Top Parameters:

https://github.com/lutfumertceylan/top25-parameter

Proviesec dorks:

https://github.com/Proviesec/google-dorks
