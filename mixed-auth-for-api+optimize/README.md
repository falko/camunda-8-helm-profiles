A Helm profile for mixed mode authentication as a workaround to allow API access,
i.e. Operate and Tasklist use basic auth 
while Optimize uses Identity and Keycload because it cannot run without them.

Kick off the `core`. You may want to wait until Elasticsearch is running before starting `optimize`

You can get the cookie from Operate:

```sh
curl -c cookie.txt -X POST "http://localhost:8081/api/login?username=demo&password=demo"
```

should look like this:
```
# Netscape HTTP Cookie File
# https://curl.se/docs/http-cookies.html
# This file was generated by libcurl! Edit at your own risk.

#HttpOnly_localhost	FALSE	/	FALSE	0	OPERATE-SESSION	EF77B574A8377A9E269034EE88E1D244
```