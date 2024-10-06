API
---
<p>Application programming interfaces.</p>
<p>It is a intermediate between client and server.</p>
<p>It is platform independent</p>
<p>It support only XML/JSON</p>

XML (Extensible markup languages)
---------------------------------
```xml
<search>
    <from>Chennai</from>
    <to>Delhi</to>
    <travelDate>2024-10-03</travelDate>
</search>
```
JSON (JavaScript object notation)
---------------------------------
combination of key and values
```json
{
  "search": {
    "from": "Chennai",
    "to": "Delhi",
    "travelDate": "2024-10-03"
  }
}
```
SOAP (Simple object access protocol)
----
<p>It accept only xml formats. by default it secured.</p>

REST (Representational State Transfer)
----
<p>It accept both XML/JSON we have create won security.</p>

Operation (CRUD)
---------
<p>GET (Retrieve)</p>
<p>PUT (Modify)</p>
<p>POST (Create)</p>
<p>DELETE (Resource delete)</p>

Response code (HTTP status code)
-------------
<p>100 - 199 (information response)</p>
<p>200 - 299 (successful response)</p>
<p>300 - 399 (redirects)</p>
<p>400 - 499 (client error)</p>
<p>500 - 599 (server error)</p>

URL
---
```
https://www.facebook.com/
```
Endpoint
--------
```
/login
```
Path param
----------
```
https://www.facebook.com/google
```
Quarry param
------------
```
https://www.facebook.com/v10.0/dialog/oauth?client_id={app-id}&redirect_uri={redirect-uri}&state={state-param}
```
URL
---
```
URL + Endpoint
https://www.facebook.com/login
 ```

