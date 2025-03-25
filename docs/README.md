K8s Pod Metrics Collector
Overview
This script collects real-time metrics from Kubernetes pods within a specified namespace and saves them to a CSV file for analysis. It integrates with Prometheus for performance data and the Kubernetes API for status information.

Features
Comprehensive Monitoring: Tracks CPU usage, memory consumption, network traffic, pod status, and events
Selective Monitoring: Excludes specified pods from data collection
Real-time Updates: Captures metrics at regular intervals (customizable)
Event Tracking: Records the latest events for pods and nodes
Detailed Logging: Captures container errors and last log entries
Requirements
Python 3.7+
kubernetes Python client
pandas
requests
Access to a Kubernetes cluster
Prometheus instance
Installation
bash

Copy
# Clone repository
git clone https://github.com/yourusername/k8s-pod-metrics.git
cd k8s-pod-metrics

# Install dependencies
pip install kubernetes pandas requests python-dateutil
Configuration
Edit these variables at the top of the script:

PROMETHEUS_URL: URL for your Prometheus instance
NAMESPACE: Kubernetes namespace to monitor
OUTPUT_FILE: CSV file path for storing metrics
SLEEP_INTERVAL: Time between data collection cycles
EXCLUDE_POD_NAMES: List of pods to exclude from monitoring
Usage
bash

Copy
python metrics_collector.py
The script will continuously collect metrics and append them to the specified CSV file until interrupted.

Output Format
The CSV file contains timestamps and detailed metrics for each pod including:

Resource usage (CPU, memory, network)
Pod status and container health
Event information and error messages
Node-related events
Notes
This is my project for the Guidewire Hackathon 2025! I built this tool to help with the AI/ML model that predicts Kubernetes failures. It's still a work in progress, but I'm hoping to integrate it with our prediction system to provide the real-time data our model needs.