# Performance Testing Report – Himalayan Circuit Tours and Travel

**Full Report here** -- https://docs.google.com/document/d/17KV2s7dSEzZiaLvFEUmZHdouS1jG19AKJ-mQxqKO0c8
Performance testing conducted on the **Himalayan Circuit Tours and Travel** website using **Apache JMeter** to evaluate the application's responsiveness, stability, and scalability under different load conditions.

## Project Overview

This project demonstrates performance testing of the website hosted on shared hosting infrastructure. The tests were designed to measure:

- ⚡ Responsiveness under normal user traffic
- 🔄 Stability during continuous load
- 📈 Scalability with increasing concurrent users

## Tools Used

- Apache JMeter
- Java
- Windows 11

## Test Environment

| Component | Configuration |
|-----------|---------------|
| Operating System | Windows 11 |
| Testing Tool | Apache JMeter |
| Test Script | `HC-Homepage.jmx` |
| Server Type | Shared Hosting |
| Target Website | https://himalayancircuit.de/ |

## Test Scenarios

### 1. Responsiveness Test

**Objective**

Measure how quickly the homepage responds under light user traffic.

**Configuration**

- Users: **5**
- Ramp-up: **10 seconds**
- Loop Count: **5**

**Result Summary**

| Metric | Value |
|--------|------:|
| Total Samples | 30 |
| Average Response Time | 334 ms |
| Maximum Response Time | 2260 ms |
| Minimum Response Time | 71 ms |
| Error Rate | 0.0% |
| Throughput | 1.7 requests/min |

**Outcome**

- No errors detected
- Stable response times
- Good performance under normal load

---

### 2. Stability Test

**Objective**

Evaluate system stability during sustained traffic.

**Configuration**

- Users: **10**
- Ramp-up: **20 seconds**
- Loop Count: Infinite
- Duration: **15 minutes**

**Result Summary**

| Metric | Value |
|--------|------:|
| Total Samples | 12,357 |
| Average Response Time | 719 ms |
| Maximum Response Time | 14,793 ms |
| Minimum Response Time | 0 ms |
| Error Rate | 0.09% |
| Throughput | 13.7 requests/sec |

**Outcome**

- Website remained stable during continuous testing
- Very low error rate
- Response times remained within acceptable limits

---

### 3. Scalability Test

**Objective**

Measure performance as concurrent users increase.

| Concurrent Users | Samples | Avg Response | Max | Error Rate | Throughput |
|----------------:|--------:|-------------:|----:|-----------:|-----------:|
| 50 | 100 | 116 ms | 259 ms | 0.00% | 5.1/sec |
| 100 | 200 | 123 ms | 278 ms | 0.00% | 6.7/sec |
| 200 | 400 | 125 ms | 399 ms | 0.00% | 10.0/sec |

**Outcome**

- Response time increased gradually as expected
- No errors during scalability testing
- Website handled concurrent users efficiently for a shared hosting environment

---

## Repository Structure

```
├── HC-Homepage.jmx                 # Apache JMeter test script
├── Performance Testing Report.docx # Complete performance testing report
├── README.md
└── screenshots/                    # Test result screenshots
```

## Full Report

The complete report includes:

- Test objectives
- Detailed configurations
- JMeter listener screenshots
- Summary reports
- Aggregate reports
- View Results Tree
- Result analysis
- Observations and conclusions

Please refer to **`Performance Testing Report.docx`** for the complete documentation.

## Author

**Suyog Sharma**

---

> This project was created for learning and demonstrating web performance testing using Apache JMeter.
