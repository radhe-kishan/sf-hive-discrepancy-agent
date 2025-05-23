# SF-Hive Discrepancy Agent

A tool for detecting and resolving discrepancies between Snowflake and Hive data sources.

## Overview

The SF-Hive Discrepancy Agent automatically monitors and reports differences between data stored in Snowflake and Hive environments, helping ensure data consistency across platforms.

## Prerequisites

- Docker
- Snowflake account credentials
- Python 3.8+
- OpenAI API Key

## Setup and Installation

### Quick Setup

1. Make the setup script executable and run it:
   ```bash
   chmod +x setup.sh
   ./setup.sh
   ```

2. Build the Docker image:
   ```bash
   ./build_docker.sh
   ```

### Manual Setup

If you prefer manual setup, you'll need to:
1. Configure your environment variables
2. Install required dependencies
3. Build the Docker image using `build_docker.sh`

## Usage

```bash
./run_docker.sh
```

## Configuration

Configure the agent by setting the following environment variables:

- `SNOWFLAKE_USER` - Snowflake username
- `SNOWFLAKE_ACCOUNT` - Your Snowflake account identifier
- `SNOWFLAKE_WAREHOUSE` - Snowflake warehouse to use
- `SNOWFLAKE_DATABASE` - Snowflake database name
- `SNOWFLAKE_SCHEMA` - Snowflake schema name
- `HIVE_SCRIPT_DIR` - Path to directory containing Hive SQL scripts
- `SNOWFLAKE_SCRIPT_DIR` - Path to directory containing Snowflake SQL scripts
- `OPENAI_API_KEY` - Your OpenAI API key for LLM integration

## Scripts

- `setup.sh` - Prepares the environment, installs dependencies, and validates configurations
- `build_docker.sh` - Builds the Docker image for the agent

## Contributing

Please read CONTRIBUTING.md for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.