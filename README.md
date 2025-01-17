# Google Dorks for Bug Bounty

A list of Google Dorks for Bug Bounty, Web Application Security, and Pentesting

[Live Tool](https://saksham.thedev.id/google-dorks-bug-bounty/)

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
site:example.com 
(inurl:url= OR inurl:return= OR inurl:next= OR inurl:redirect= OR inurl:redir= OR inurl:ret= OR inurl:r2= OR inurl:page= OR inurl:go= OR inurl:dest= OR inurl:target= OR intitle:"Redirecting..." OR intitle:"Redirect")
```

### SQLi Prone Parameters

```
site:example.com (inurl:id= OR inurl:pid= OR inurl:category= OR inurl:cat= OR inurl:action= OR inurl:sid= OR inurl:dir= OR inurl:page= OR inurl:p= OR inurl:num= OR inurl:offset= OR inurl:limit= OR inurl:start= OR inurl:end= OR inurl:mode= OR inurl:view= OR inurl:type= OR inurl:section= OR inurl:menu= OR inurl:lang= OR inurl:language= OR inurl:ref= OR inurl:referrer= OR inurl:token= OR inurl:key= OR inurl:order= OR inurl:sort= OR inurl:filter=)
```

### SSRF Prone Parameters

```
site:example.com 
(inurl:http OR inurl:https inurl:url OR inurl:path OR inurl:dest OR inurl:target OR inurl:redirect OR inurl:location OR inurl:goto OR inurl:link inurl:file OR inurl:load OR inurl:get OR inurl:include OR inurl:source OR inurl:resource OR inurl:lookup OR inurl:resolve OR inurl:open OR inurl:read OR inurl:access OR inurl:retrieve OR inurl:obtain OR inurl:acquire OR inurl:procure)
```

### LFI Prone Parameters

```
site:example.com 
(inurl:include OR inurl:inc OR inurl:require OR inurl:load OR inurl:source OR inurl:page OR inurl:file OR inurl:doc OR inurl:conf OR inurl:config OR inurl:xml OR inurl:php OR inurl:txt inurl:dir OR inurl:path OR inurl:folder OR inurl:file OR inurl:page OR inurl:view)
```

### RCE Prone Parameters

```
site:example.com (inurl:cmd OR inurl:exec OR inurl:execute OR inurl:run OR inurl:shell OR inurl:system OR inurl:os inurl:query OR inurl:search OR inurl:find OR inurl:lookup OR inurl:locate OR inurl:get OR inurl:fetch inurl:data OR inurl:input OR inurl:param OR inurl:arg OR inurl:value OR inurl:option OR inurl:mode OR inurl:type)
```

### File upload endpoints

```
site:example.com ”choose file”
```

### API Docs

```
site:"example[.]com" (inurl:apidocs OR inurl:api-docs OR inurl:swagger OR inurl:api-explorer OR inurl:openapi OR inurl:apispec OR inurl:api-spec OR inurl:api-reference OR inurl:api-guide OR inurl:api-documentation OR inurl:restapi OR inurl:rest-api OR inurl:graphql OR inurl:api-schema OR inurl:api-def OR inurl:apidef OR inurl:api-endpoints OR inurl:endpoints OR inurl:api-console OR inurl:apiconsole OR inurl:api-playground OR inurl:apiplayground)
```

### Login Pages

```
site:example[.]com (inurl:login OR inurl:signin OR inurl:log-in OR inurl:sign-in OR inurl:access OR inurl:secure OR inurl:portal OR inurl:account OR inurl:auth OR inurl:authentication OR intitle:login OR intitle:signin OR intitle:log-in OR intitle:sign-in OR intitle:authentication OR intitle:secure OR intitle:portal)
```

### Test Environments

```
site:example.com (inurl:test OR inurl:env OR inurl:dev OR inurl:staging OR inurl:sandbox OR inurl:debug OR inurl:temp OR inurl:internal OR inurl:demo OR inurl:beta OR inurl:qa OR inurl:development OR inurl:prototype OR inurl:experimental OR inurl:trial OR inurl:rc OR inurl:preview OR inurl:nonprod OR inurl:staging-env OR inurl:test-env OR inurl:devenv)
```

### Sensitive Documents

```
site:example.com (ext:txt OR ext:pdf OR ext:xml OR ext:xls OR ext:xlsx OR ext:ppt OR ext:pptx OR ext:doc OR ext:docx OR ext:rtf OR ext:csv OR ext:log OR ext:json OR ext:config OR ext:ini)
(intext:"confidential" OR intext:"Not for Public Release" OR intext:"internal use only" OR intext:"do not distribute" OR intext:"restricted" OR intext:"private" OR intext:"sensitive" OR intext:"classified" OR intext:"proprietary")
```

### Sensitive Parameters

```
site:example[.]com (inurl:email= OR inurl:phone= OR inurl:password= OR inurl:secret= OR inurl:token= OR inurl:key= OR inurl:credentials= OR inurl:login= OR inurl:user= OR inurl:username= OR inurl:pwd= OR inurl:pass= OR inurl:auth= OR inurl:api-key= OR inurl:apikey= OR inurl:access-token= OR inurl:accesstoken=)
```

### Adobe Experience Manager (AEM)

```
site:example[.]com (inurl:/content/usergenerated OR inurl:/content/dam OR inurl:/jcr:content OR inurl:/libs/granite OR inurl:/etc/clientlibs OR inurl:/content/geometrixx OR inurl:/bin/wcm OR inurl:/crx/de OR inurl:/system/console OR inurl:/cf OR inurl:/apps/cq OR inurl:/etc/designs OR inurl:/etc/workflow OR inurl:/etc/replication OR inurl:/etc/commerce OR inurl:/etc/tags OR inurl:/etc/segmentation OR inurl:/libs/cq OR inurl:/libs/foundation)
```

### Disclosed XSS and Open Redirects

```
site:openbugbounty.org (inurl:reports OR inurl:vulnerability OR inurl:bugs OR inurl:disclosures intext:"example.com")
```

### Google Groups

```
site:groups.google.com "example.com"
```

### Code Leaks

```
(site:codepen.io OR site:codebeautify.org OR site:pastebin.com OR site:jsfiddle.net OR site:repl.it OR site:glitch.com OR site:codesandbox.io OR site:ideone.com OR site:hastebin.com OR site:gist.github.com) 
"example.com"
```

### Cloud Storage

```
(site:s3.amazonaws.com OR site:blob.core.windows.net OR site:googleapis.com OR site:drive.google.com OR site:dev.azure.com OR site:onedrive.live.com OR site:digitaloceanspaces.com OR site:sharepoint.com OR site:s3-external-1.amazonaws.com OR site:s3.dualstack.us-east-1.amazonaws.com OR site:dropbox.com/s OR site:box.com/s OR site:docs.google.com) 
(inurl:"/d/" OR inurl:"/s/" OR inurl:"/file/") 
"example[.]com"
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
