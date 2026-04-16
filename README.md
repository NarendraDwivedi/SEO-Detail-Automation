# SEO Detail Automation

An automated, serverless time-series database designed to monitor, log, and visualize Core Web Vitals and SEO metrics without the overhead of traditional backend infrastructure.

## 🏗️ Architecture Overview

This project bypasses standard database hosting by utilizing Git as a highly reliable, version-controlled JSON storage layer. 

A scheduled serverless edge function queries target URLs daily, extracts raw application performance data, and commits the structured payload to this repository. The resulting architecture forms an immutable, zero-maintenance time-series database.

### Directory Structure Protocol
Data is partitioned dynamically to ensure scalability and rapid frontend retrieval:
```text
/
├── index.html          # Data aggregation and visualization dashboard
├── year/
│   └── month/
│       └── date/
│           └── detail.json  # Daily metric payload
