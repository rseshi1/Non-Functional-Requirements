# Non-Functional Requirements (NFRs), Service Level Objectives (SLOs), and Service Level Indicators (SLIs)

Non-functional requirements (NFRs), Service Level Objectives (SLOs), and Service Level Indicators (SLIs) are all important concepts in software engineering and system design, but they serve different purposes and are used in different contexts. Here's a breakdown of each:

---

## 1. Non-Functional Requirements (NFRs)

### **Definition**
Non-functional requirements describe the qualities or constraints of a system rather than specific behaviors or functionalities. They define **how the system should perform**, rather than what it should do.

### **Examples**
- **Performance** (e.g., response time, throughput)
- **Scalability** (e.g., ability to handle increased load)
- **Availability** (e.g., uptime percentage)
- **Security** (e.g., encryption standards, authentication mechanisms)
- **Usability** (e.g., user interface responsiveness)
- **Maintainability** (e.g., ease of code updates)

### **Purpose**
NFRs are typically used during the design and development phases to ensure that the system meets certain quality standards. They are often documented in requirements specifications and used to guide architectural decisions.

---

## 2. Service Level Indicators (SLIs)

### **Definition**
SLIs are specific metrics that measure the performance, reliability, or availability of a service. They are **quantitative measures** that reflect the health or performance of a service from the user's perspective.

### **Examples**
- **Latency** (e.g., time taken to process a request)
- **Error rate** (e.g., percentage of failed requests)
- **Availability** (e.g., percentage of time the service is up)
- **Throughput** (e.g., number of requests processed per second)

### **Purpose**
SLIs are used to monitor and evaluate the performance of a service in real-time. They provide the raw data that can be used to assess whether a service is meeting its objectives.

---

## 3. Service Level Objectives (SLOs)

### **Definition**
SLOs are specific, measurable goals that define the acceptable level of service performance. They are typically based on SLIs and represent the **target values or ranges** that a service is expected to meet.

### **Examples**
- "The service should have a latency of less than 200ms for 99% of requests."
- "The service should have an availability of 99.9% over a 30-day period."
- "The error rate should be less than 0.1% of all requests."

### **Purpose**
SLOs are used to set clear expectations for service performance and to guide decisions about when to take corrective action. They are often used in conjunction with SLIs to monitor and manage service quality.

---

## Key Differences

### **Scope**
- **NFRs** are broad and cover a wide range of system qualities.
- **SLIs and SLOs** are more focused on specific aspects of service performance and reliability.

### **Usage**
- **NFRs** are used during the design and development phases to guide system architecture and implementation.
- **SLIs and SLOs** are used during the operation and maintenance phases to monitor and manage service performance.

### **Nature**
- **NFRs** are qualitative or descriptive, often specifying what is expected without always providing exact metrics.
- **SLIs** are quantitative metrics that provide raw data.
- **SLOs** are quantitative targets derived from SLIs, specifying acceptable performance levels.

---

## Relationship

### **NFRs to SLIs/SLOs**
NFRs can inform the selection of SLIs and the setting of SLOs. For example, if an NFR specifies that the system should be highly available, this could translate into an SLO that targets 99.9% availability, measured by an SLI that tracks uptime.

### **SLIs to SLOs**
SLIs provide the data that is used to evaluate whether SLOs are being met. For example, if an SLO specifies that latency should be under 200ms for 99% of requests, the corresponding SLI would measure the actual latency of requests.

---

## Summary
- **NFRs** define the overall quality attributes of a system.
- **SLIs** are the specific metrics used to measure those attributes.
- **SLOs** are the targets that define acceptable performance levels based on those metrics.
