# ELK Stack with Docker

This repository contains a Docker-based ELK (Elasticsearch, Logstash, Kibana) stack setup for log aggregation and monitoring.

## Prerequisites

- Git
- Docker and Docker Compose
- VSCode (optional)

## Quick Start

1. Clone the repository:
   ```bash
   git clone git@github.com:michaeltansg/elk-docker.git
   cd elk-docker
   ```

2. Set up environment variables:
   ```bash
   cp .env.example .env
   ```
   Edit the `.env` file to configure your environment settings, especially the `ELASTIC_PASSWORD`.

3. Start the stack:
   ```bash
   docker compose up -d
   ```

4. Access Kibana:
   - URL: http://localhost:5601
   - Username: `elastic`
   - Password: Value of `ELASTIC_PASSWORD` from your `.env` file

## Components and Features

### Filebeat
- Real-time log streaming: http://localhost:5601/app/logs/stream
- Log exploration: http://localhost:5601/app/observability-logs-explorer/

### Logstash
- Batch processing configuration
- Search indices management: http://localhost:5601/app/enterprise_search/content/search_indices

### Metricbeat
- System and service monitoring: http://localhost:5601/app/monitoring

## Data Sources
This setup includes sample data for testing and development:
- Air quality metrics (CSV and log format)
- System metrics via Metricbeat
- Log data via Filebeat

## Additional Resources

### Documentation
- [Getting Started with Elastic Stack and Docker Compose](https://www.elastic.co/blog/getting-started-with-the-elastic-stack-and-docker-compose)
- [Elastic Stack Docker Tutorial](https://github.com/elkninja/elastic-stack-docker-part-one)

### Sample Data Sources
- [Elastic Examples Repository](https://github.com/elastic/examples)
- [Kaggle Datasets](https://www.kaggle.com/)

## License

See the [LICENSE](LICENSE) file for details.
