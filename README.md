Kubernetes Monitoring Exercise
------------------------------
The goal of today's exercise is to deploy the Prometheus & Grafana stack to our Kubernetes cluster and use it to create a dashboard for our Kubernetes cluster.
1. Install the Prometheus+Grafana stack onto our cluster (use official Helm chart!).
   Note: The official chart may take a minute to install, don't worry.
2. Install the juice-shop application (available from https://artifacthub.io/packages/helm/securecodebox/juice-shop) onto your cluster (including an Nginx ingress).
3. Import dashboards from Grafana’s registry (https://grafana.com/grafana/dashboards), for Nginx ingress, look inside the dashboards (especially inside the “edit” view) to get a hang of how PromQL queries work and how they create their visualizations.
4. Learn how to query PromQL - write PromQL queries to get useful metric data from our cluster.
5. Create a dashboard, make a few panels in it (average CPU usage percent, remaining disk space, days until TLS cert is expired, etc... be creative!).

While being able to see the live metrics of our cluster and applications is nice, we need to be alerted once something is abnormal, let’s talk alerting!
6. Create an “alerting” dashboard, create several visualizations for it (you can use the same queries from before).
   Note: We can only create alerts for time-series visualizations.
7. Create an alerting channel (any kind you want).
8. Create alerts for surpassing certain thresholds on the alerting dashboard, and send them to your alerting channel, try and see if you can test them.