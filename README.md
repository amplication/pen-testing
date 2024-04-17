# pen-testing
Automated penetration testing CI


## local

```sh
docker run --rm -v $(pwd):/zap/wrk/:rw -e   -t ghcr.io/zaproxy/zaproxy:stable zap-api-scan.py \
    -t https://server.amplication-sandbox.com/api-json -f openapi -g amplication.conf -r testrest.html -O https://server.amplication-staging.com -n /zap/wrk/amplication.context
```