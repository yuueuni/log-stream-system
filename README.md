# Log Stream System

**Log Stream System**는 다양한 애플리케이션과 시스템에서 생성되는 로그 데이터를 실시간으로 수집, 처리, 저장하고 분석할 수 있는 로그 수집 서비스입니다. 시스템 모니터링, 오류 탐지, 사용자 활동 분석 등의 기능을 제공하여 효율적이고 신속한 운영을 지원합니다.

**Log Stream System** is a comprehensive log collection service that enables real-time collection, processing, storage, and analysis of log data from various applications and systems. It provides capabilities for system monitoring, error detection, and user activity analysis, helping ensure efficient and rapid operations.

---

## 기능 및 특징 (Features)

- **실시간 로그 수집 및 분석** (Real-Time Log Collection & Analysis): 다양한 서비스와 애플리케이션에서 발생하는 로그 데이터를 실시간으로 수집하고 분석하여 시스템 이상을 빠르게 감지합니다.  
- **다양한 로그 유형 지원** (Support for Multiple Log Types): HTTP 요청 로그, 에러 로그, 사용자 활동 로그 등 다양한 유형의 로그 데이터를 수집하고 분류합니다.  
- **임계값 감지 및 알림** (Threshold Alerting): 설정된 임계값을 초과하는 이벤트가 발생하면 즉시 알림을 전송하여 신속하게 대응할 수 있도록 지원합니다.  
- **안정적인 데이터 저장 및 백업** (Reliable Data Storage & Backup): 로그 데이터를 NoSQL 데이터베이스에 저장하고, 주기적으로 HDFS에 백업하여 안정성을 보장합니다.  
- **데이터 시각화** (Data Visualization): 대시보드에서 실시간 데이터와 통계를 시각화하여 시스템 상태를 직관적으로 파악할 수 있습니다.

## Features

- **Real-Time Log Collection & Analysis**: Collects and analyzes log data from various services and applications in real time, enabling quick detection of system anomalies.
- **Support for Multiple Log Types**: Handles a range of log data types, including HTTP request logs, error logs, and user activity logs, and categorizes them for more effective analysis.
- **Threshold Alerting**: Sends alerts when predefined thresholds are exceeded, allowing teams to respond swiftly to critical issues.
- **Reliable Data Storage & Backup**: Stores log data in NoSQL databases and performs periodic backups to HDFS for enhanced reliability.
- **Data Visualization**: Visualizes real-time data and statistics on dashboards, providing an intuitive view of system health and activity.

## 아키텍처 (Architecture)

Log Stream System의 핵심 아키텍처는 다음과 같습니다:

1. **로그 수집** (Log Collection): Kafka Producer가 다양한 서비스와 애플리케이션에서 로그 데이터를 수집하고, Kafka Broker에 저장합니다.
2. **스트림 처리** (Stream Processing): Apache Flink가 Kafka의 로그 데이터를 실시간으로 처리하여 이상 감지 및 데이터 변환을 수행합니다.
3. **저장소** (Data Storage): Flink는 처리된 데이터를 Cassandra나 MongoDB와 같은 데이터베이스에 저장하여 빠른 조회와 분석이 가능합니다.
4. **백업** (Backup): HDFS를 통해 로그 데이터를 주기적으로 백업하여 장애 상황에서 복구할 수 있도록 합니다.
5. **알림 시스템** (Alerting System): 설정된 임계값이 초과될 경우 사용자에게 실시간으로 알림을 전송합니다.

## Architecture

The core architecture of LogVerse is structured as follows:

1. **Log Collection**: A Kafka Producer collects log data from various services and applications, storing it in Kafka Brokers.
2. **Stream Processing**: Apache Flink processes log data from Kafka in real-time, performing anomaly detection and data transformation.
3. **Data Storage**: Flink stores processed data in databases such as Cassandra or MongoDB, enabling fast retrieval and analysis.
4. **Backup**: Periodically backs up log data to HDFS, ensuring data can be recovered in case of failure.
5. **Alerting System**: Sends real-time alerts to users when predefined thresholds are exceeded or critical events occur.

---

## License
This project is distributed under the MIT License.
See the LICENSE file for details.
