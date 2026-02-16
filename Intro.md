1. HTTP protocol 
2. Routing 
3. Serialization & deseralization 


Story and philosophy 
Implementations 



Port 80, 443 
serves some content 
DNS 
Firewall security groups we can alllow that what ports we want to allow. 

22, 80, 443 - inbound rules 
reverse proxy - nginx 

pm2 list  - see what process are running 

browser - dns server - aws server firewall - aws instance - nginx - localhost 

CORS is to make the browser like a sandbox. 


Why not backend logic in frontend? 
1. Security 
2. CORS 
3. Database
4. Compute power. 

PUT 
POST
GET
PATCH
DELETE 

intent of the action 
PATCH vs PUT - 
complete replacement vs append only 


idempotent vs non idempotent 
get, put, delete - idempotent 

post - non idempotent, we change the results for same results 

options - 
CORS - same origin policy 
browsers will prevent the frontend to make any request to servers that is not within that domain 

simple
preflight 

the return response will have access control allow origin 
now that should return the particular origin domain or *[for all the domains]


preflight request flow 
the method is not get, post or head
or the request includs non simple headers like auth, x custom headers 
or
the request has content type other than application/www-form-urlencoded, multipart/form-data or text/plain 


204 - no content 
do you allow the clients origin 
max age for caching 

information - continue large payloads, update from http to websocket 
sucess - 200 sucessfull, 201 new resource has been created, 204 no content 
redired 301 moved premanently maintain backwords compactibility, 302 temp redirect, 304
client 200 bad request, 401 - unauth, 403 - forbidden, 404 not found, 405 - method not allowed, 409 - conflicts, 429 - too many requests
server 500 - internal server error, 501 - not implemented, 502 - bad gateway, 503 - service unavailable 504 - gateway timeout

