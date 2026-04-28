# KQL

A collection of useful KQL queries for security monitoring, suspicious activity detection, and event analysis in Microsoft and related technology environments.

This repository contains queries for working with data from areas such as Active Directory, Azure AD, Microsoft Defender for Endpoint, and Fortigate.

## Repository Contents

```text
.
├── AD
├── AzureAD
├── Fortigate
└── MDE
```

## Query Categories

### AD

Queries focused on on-premises Active Directory and related security events.

Examples of included queries:

- Detection of remote PowerShell activity
- Overview of failed logons
- Failed logons followed by a successful login
- RDP connections to multiple devices

### AzureAD

Queries for Azure Active Directory / Microsoft Entra ID.

Examples of included queries:

- Failed logins followed by a successful login
- Inactive users
- Successful authentication from a new or foreign country
- Successful authentication from a new country blocked by MFA
- Logins from unknown countries

### Fortigate

Queries for analyzing logs from Fortigate devices.

Examples of included queries:

- Brute-force attack detection

### MDE

Queries for Microsoft Defender for Endpoint.

Examples of included queries:

- Finding untrusted executable files blocked by ASR rules
- Checking active or passive device state
- Last completed antivirus scan
- Last logged-on user on a device

## Usage

1. Select the required `.kql` file based on the technology or scenario.
2. Open the query in an environment that supports Kusto Query Language, such as:
   - Microsoft Sentinel
   - Microsoft Defender XDR Advanced Hunting
   - Log Analytics Workspace
   - Azure Data Explorer
3. Adjust table names, time ranges, or filters according to your environment.
4. Run the query and analyze the results.

## Requirements

To use these queries, you need:

- Access to the relevant logs and tables
- An environment that supports KQL
- Permissions to run queries against security data
- Properly configured data collection from the relevant source

## Recommendations

Before using these queries in production monitoring, it is recommended to:

- Verify table and column names in your environment
- Adjust time ranges according to your data volume
- Tune thresholds for your specific environment
- Test the queries against historical data
- Add custom exclusions for known legitimate activity

## Contributing

Contributions are welcome. If you want to add a new query or modify an existing one:

1. Fork the repository.
2. Add or update a `.kql` file in the appropriate folder.
3. Use a descriptive file name.
4. Add comments directly in the query where appropriate.
5. Open a pull request.

## File Naming Convention

Recommended file name format:

```text
Scenario-description.kql
```

Example:

```text
Failed-logins-followed-by-successful-login-AzureAD.kql
```

## Disclaimer

The queries in this repository are intended as starting templates and examples. Results should always be interpreted in the context of your specific environment.

Some queries may require adjustments depending on:

- Available data sources
- Configured connectors
- Log retention period
- Internal security rules
- Specific table or column names

## License

No license is currently specified in this repository. Before redistributing or using the content outside your own environment, verify the terms of use with the repository owner.

## Author

This repository is maintained by [luberan](https://github.com/luberan).
