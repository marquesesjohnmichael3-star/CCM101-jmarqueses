
# Container Observability Report

## Container Details

- **Container Name:** `client-website`
- **Service:** Nginx web server
- **Host Port:** `8080`
- **Container Port:** `80`
- **Monitoring Commands:** `docker ps`, `docker logs`, and `docker stats`

## Request Testing

The Nginx website was tested with two requests to the root page and one request to a nonexistent path.

| Request | Expected Result |
|---|---|
| `/` | HTTP 200 OK |
| `/hidden-admin-page` | HTTP 404 Not Found |
| `/` | HTTP 200 OK |

The nonexistent page returned a 404 response because the requested resource was not available at that path.

## Access Log Evidence

**Actual access-log line for the 404 request:**

Paste the real line from `docker logs client-website` that contains `GET /hidden-admin-page` and status code `404`.

**Explanation:**

The access log records the requested path and the server's response status. This entry confirms that Nginx received the request but could not find the requested resource. Logs are useful for investigating failed requests and checking what happened during a reported problem.

## Container Resource Metrics

Record the values displayed by `docker stats client-website`.

- **Memory Usage:** 2.715MiB / 1.859GiB
- **CPU Percentage:** 0.14%
- **Network I/O:** 3.14kB / 3.73kB

These values describe the container's resource usage at the time of observation. They can help identify unusual memory consumption, CPU activity, or network traffic.

## Conclusion

Combining request tests, access logs, and live container statistics gives a clearer picture of the web service. The request results show whether the expected pages are available, while the logs and metrics provide additional evidence for troubleshooting.
