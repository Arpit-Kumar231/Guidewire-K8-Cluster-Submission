# K8s Pod Metrics Collector
Overview
This script collects real-time metrics from Kubernetes pods within a specified namespace and saves them to a CSV file for analysis. It integrates with Prometheus for performance data and the Kubernetes API for status information.

Copy
python metrics_collector.py
The script will continuously collect metrics and append them to the specified CSV file until interrupted.

Output Format
The CSV file contains timestamps and detailed metrics for each pod including:

Resource usage (CPU, memory, network)
Pod status and container health
Event information and error messages
Node-related events


### This code monitors Kubernetes pods in a specified namespace by collecting comprehensive metrics and health data. It integrates with Prometheus to gather performance metrics (CPU usage, memory consumption, network traffic) while using the Kubernetes API to track pod statuses, container health, restart counts, and events. The script detects and logs status changes, captures the latest pod and node events, and collects recent log entries from each pod. It also calculates memory usage percentages and monitors network errors. Operating in a continuous loop with configurable intervals, the code filters pods based on an exclusion list and writes all collected data to a CSV file for historical analysis and potential use in predictive failure detection systems