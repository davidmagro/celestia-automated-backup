## Celestia Automated Backup and Recovery Tool

The Celestia Automated Backup and Recovery Tool is a command-line tool that automates the process of backing up and recovering Celestia node data. The tool is designed to provide a convenient and reliable way for validators, node operators, and developers to protect their Celestia node data from loss or corruption and recover it in case of issues.

The tool includes the following features:

1. Multi-node support: Back up and restore data for multiple Celestia nodes simultaneously.
2. Backup scheduling: Schedule automatic backups on a regular basis, such as daily or weekly.
3. Cloud integration: Upload backup files to AWS S3 for secure storage and remote accessibility.
4. Notifications: Send notifications to the user when backups are taken or when a restore operation is completed.
5. Disaster recovery: Restore data to a different server or cloud instance in case of a catastrophic failure.

### Prerequisites

Before using this tool, you will need the following:

- A Celestia node running on a server or cloud instance.
- Python 3.6 or later installed.
- Boto3 library installed (for AWS integration).

### Installation

To install the Celestia Automated Backup and Recovery Tool, follow these steps:

1. Clone the repository to your server or cloud instance:

    ```
    git clone https://github.com/celestiaorg/backup-tool.git
    ```

2. Navigate to the directory:

    ```
    cd backup-tool
    ```

3. Configure the tool by editing the variables at the top of the `backup.py` file:

    ```
    # Define backup directory
    BACKUP_DIR = "/backup/"

    # Define AWS credentials
    AWS_ACCESS_KEY_ID = "<AWS_ACCESS_KEY_ID>"
    AWS_SECRET_ACCESS_KEY = "<AWS_SECRET_ACCESS_KEY>"
    AWS_REGION = "<AWS_REGION>"
    AWS_BUCKET_NAME = "<AWS_BUCKET_NAME>"
    ```

    Replace the values in angle brackets with your own values.

4. Install the Boto3 library using pip:

    ```
    pip install boto3
    ```

### Usage

To use the Celestia Automated Backup and Recovery Tool, simply run the `backup.py` file:

python backup.py

The tool will automatically create backups, upload them to AWS S3, and schedule regular backups. In case of a catastrophic failure, you can use the tool to restore node data from a backup file.

### Support

If you have any questions or issues with the Celestia Automated Backup and Recovery Tool, please contact the Celestia team on Discord or create an issue on the GitHub repository.
