# TeraForge 🔨

### *Your Personal Big Data Foundry*

[![Hadoop](https://img.shields.io/badge/Hadoop-3.3.6-green)](https://hadoop.apache.org/)
[![Hive](https://img.shields.io/badge/Hive-3.1.3-blue)](https://hive.apache.org/)
[![Spark](https://img.shields.io/badge/Spark-3.5.0-orange)](https://spark.apache.org/)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

> Transform massive datasets into actionable insights from the comfort of your home server

---

## 🎯 What is TeraForge?

**TeraForge** is a complete, production-ready Hadoop ecosystem setup designed for single-node deployment. Perfect for learning big data technologies, prototyping data pipelines, or running analytics on your home server without the complexity of multi-node cluster management.

**Key Highlights:**
- 🐘 Full Apache Hadoop stack (HDFS, YARN, MapReduce)
- 🔍 SQL-like queries with Apache Hive
- ⚡ Real-time processing with Apache Spark
- 🔄 Database integration via Apache Sqoop
- 📊 Three ready-to-run analysis projects
- 🚀 Setup in under 30 minutes

## ✨ Features

- **Single-Node Simplicity**: Pseudo-distributed mode - all daemons on one machine
- **Complete Toolchain**: Hadoop, Hive, Spark, Sqoop pre-configured and integrated
- **Sample Projects**: Log analysis, sentiment analysis, retail analytics
- **Web Dashboards**: Access HDFS and YARN through browser interfaces
- **Production Patterns**: Following industry best practices and standards
- **Fully Documented**: Step-by-step guides for setup, configuration, and troubleshooting

## 📋 System Requirements

| Component | Requirement |
|-----------|------------|
| OS | Ubuntu Server 20.04+ |
| RAM | 8GB minimum (16GB recommended) |
| CPU | Multi-core processor (2+ cores) |
| Storage | 50GB+ free space |
| Java | OpenJDK 8 |

## 🚀 Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/teraforge.git
cd teraforge

# 2. Run environment setup (as root)
cd scripts/installation
sudo bash setup_environment.sh

# 3. Switch to hadoop user
su - hadoop

# 4. Configure SSH and install Hadoop
cd /path/to/teraforge/scripts/installation
bash configure_passwordless_ssh.sh
bash install_hadoop.sh
source ~/.bashrc

# 5. Copy configurations
cp /path/to/teraforge/configs/hadoop/*.xml $HADOOP_HOME/etc/hadoop/

# 6. Format and start cluster
cd ../cluster-management
bash format_namenode.sh
bash start_cluster.sh

# 7. Access web UIs
# NameNode: http://localhost:9870
# ResourceManager: http://localhost:8088
```

## 📦 What's Included

### Core Components
- **Apache Hadoop 3.3.6** - Distributed storage and processing
- **Apache Hive 3.1.3** - Data warehouse and SQL queries
- **Apache Spark 3.5.0** - Fast in-memory processing
- **Apache Sqoop 1.4.7** - Relational database integration

### Sample Projects
1. **Log File Analysis** - Parse and analyze server access logs
2. **Twitter Sentiment Analysis** - Real-time sentiment classification with PySpark
3. **Retail Data Analysis** - Customer segmentation and sales trends

### Scripts & Tools
- Automated installation scripts for all components
- Cluster management (start/stop/status)
- HDFS operations reference guide
- Configuration templates optimized for single-node

## 🎓 Learning Path

1. **Beginners**: Start with [QUICKSTART.md](../QUICKSTART.md)
2. **Configuration**: Tune performance with [CONFIGURATION.md](../CONFIGURATION.md)
3. **Sample Projects**: Run analyses in `projects/` directory
4. **Advanced**: Scale to multi-node cluster (see [ROADMAP.md](../ROADMAP.md))

## 📊 Sample Use Cases

- **Educational**: Learn Hadoop ecosystem hands-on
- **Prototyping**: Test data pipelines before cloud deployment
- **Analytics**: Process personal data collections (photos, logs, documents)
- **Portfolio**: Showcase big data skills with real projects
- **Research**: Experiment with distributed algorithms

## 🌐 Web Interfaces

| Service | URL | Purpose |
|---------|-----|---------|
| NameNode | http://localhost:9870 | HDFS browser and status |
| ResourceManager | http://localhost:8088 | YARN applications |
| DataNode | http://localhost:9864 | Node information |
| JobHistory | http://localhost:19888 | MapReduce job history |

## 📖 Documentation

- **[Full README](../README.md)** - Comprehensive guide
- **[Quick Start](../QUICKSTART.md)** - Get running in 5 steps
- **[Configuration](../CONFIGURATION.md)** - Tuning and optimization
- **[Roadmap](../ROADMAP.md)** - Future features and ideas

## 🔧 Example Commands

```bash
# HDFS Operations
hdfs dfs -mkdir -p /user/hadoop/data
hdfs dfs -put myfile.txt /user/hadoop/data/
hdfs dfs -ls /user/hadoop/data

# Hive Query
hive -e "SELECT * FROM my_table LIMIT 10;"

# Spark Job
spark-submit --master local[*] analysis.py

# Cluster Management
bash scripts/cluster-management/start_cluster.sh
bash scripts/cluster-management/cluster_status.sh
```

## 🤝 Contributing

Contributions welcome! Areas of interest:
- Additional sample datasets and analysis projects
- Performance optimizations
- Multi-node deployment guides
- Integration with modern tools (Kafka, Airflow, etc.)

## 📝 License

This project is licensed under the Apache License 2.0 - see LICENSE file for details.

## 🙏 Acknowledgments

Built with:
- Apache Hadoop and the entire Apache Software Foundation ecosystem
- Community tutorials and best practices
- Real-world production patterns

## 🔗 Resources

- [Apache Hadoop](https://hadoop.apache.org/)
- [Apache Hive](https://hive.apache.org/)
- [Apache Spark](https://spark.apache.org/)
- [Hadoop Documentation](https://hadoop.apache.org/docs/current/)

---

**TeraForge** - *Forging Big Data Solutions, One Node at a Time* 🔨

Made with ❤️ for the big data community

