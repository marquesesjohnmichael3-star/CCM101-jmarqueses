
# Mission 7 Reflection

Checking system resources is an important part of cloud operations because applications depend on the memory, processing power, and storage available on the machine. If a server runs out of memory or disk space, the application may become slow or stop working. By using `free -h` and `df -h /`, I learned how to check the condition of the environment before investigating an application problem.

Logs can also help explain complaints from users. For example, if someone reports that a page cannot be opened, I can inspect the Nginx access logs using `docker logs client-website`. The log entry can show the requested path and HTTP status code. In this activity, the request to `/hidden-admin-page` returned a 404 response. This helped me understand how logs provide evidence of requests handled by the server instead of relying only on what a user reports.

Logs and metrics have different purposes. Logs contain records of specific events, requests, and errors. Metrics provide numerical measurements such as CPU percentage, memory consumption, and network traffic. Using both gives an operator more information when checking an application's condition. A log may explain which request failed, while a metric may help reveal whether the container is using too many resources.

In a larger organization, tools such as Prometheus and Grafana can support monitoring. Prometheus collects and stores time-series metrics, while Grafana displays data through dashboards. These tools help teams notice changes in performance and investigate problems before they affect more users.

This activity improved my troubleshooting skills by giving me practice with Linux commands, Docker container management, HTTP testing, and log inspection. I also learned that a successful deployment is not the end of the task. The service must still be checked to confirm that it responds properly and uses resources as expected. In future cloud activities, I will use monitoring evidence to help identify problems instead of making assumptions about their cause.
