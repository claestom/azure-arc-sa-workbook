# Azure Arc Software Assurance Dashboard

A comprehensive Azure Workbook for monitoring Software Assurance compliance across your hybrid infrastructure with Arc-enabled servers and SQL Server instances.

## Overview

This workbook provides real-time visibility into your Azure Arc-enabled infrastructure licensing status, helping you:

- Track Software Assurance compliance across Windows Servers
- Monitor SQL Server licensing types (Paid vs License-Only/BYOL)
- Identify potential licensing gaps
- Generate compliance reports for hybrid infrastructure

## Features

### 📊 Key Metrics Dashboard
- **Software Assurance Enabled/Disabled** servers count
- **Paid License** SQL Server instances
- **License-Only (BYOL)** SQL Server instances

### 📋 Detailed Server Inventory
- Complete list of Arc-enabled servers and SQL instances
- License status indicators with visual formatting
- Filterable by server type (Windows Server, SQL Server)
- Sortable by various attributes

### 🎯 Compliance Tracking
- Visual indicators for compliance status
- Resource group and subscription organization
- Location-based server distribution

## Prerequisites

- Azure subscription with Arc-enabled servers
- Azure Monitor Workbooks access
- Appropriate RBAC permissions to view hybrid compute resources

## Installation

1. **Clone this repository:**
   ```bash
   git clone https://github.com/yourusername/azure-arc-sa-dashboard.git
   ```

2. **Import the workbook:**
   - Navigate to Azure Monitor > Workbooks in the Azure portal
   - Click "New" and select "Advanced Editor"
   - Copy the contents of `workbooks/arc-sa-overview.json`
   - Paste into the Gallery Template editor
   - Click "Apply" and save the workbook

3. **Configure parameters:**
   - Select your subscription(s) from the dropdown
   - Choose server type filters as needed

## Usage

### Quick Start
1. Open the workbook in Azure Monitor
2. Select your subscriptions from the parameter dropdown
3. Use the server type filter to focus on specific infrastructure
4. Review the tile summaries for quick compliance overview
5. Examine the detailed server inventory table for specific licensing status

### Interpreting Results

| Status | Icon | Meaning |
|--------|------|---------|
| ✓ Yes | Green | Software Assurance/Paid licensing active |
| ⚠ No | Orange | No Software Assurance/License-only model |
| Unknown | Gray | Status cannot be determined |

## Workbook Structure

```
workbooks/
└── arc-sa-overview.json    # Main workbook template
```

The workbook includes:
- **Parameters section**: Subscription and server type filters
- **Tile visualizations**: Quick compliance metrics
- **Table visualization**: Detailed server inventory with licensing status
- **Documentation**: Usage instructions and compliance guidance

## Customization

You can modify the workbook to:
- Add additional server properties
- Include custom licensing fields
- Extend filtering capabilities
- Add compliance thresholds and alerts

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/enhancement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/enhancement`)
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For issues and questions:
- Create an [issue](https://github.com/yourusername/azure-arc-sa-dashboard/issues) in this repository
- Review [Azure Arc documentation](https://docs.microsoft.com/azure/azure-arc/)
- Check [Azure Monitor Workbooks documentation](https://docs.microsoft.com/azure/azure-monitor/platform/workbooks-overview)

## Disclaimer

This workbook is provided as-is for monitoring purposes. Always consult with your licensing team and review Microsoft licensing terms for official compliance requirements.

---

**Built with ❤️ for the Azure Arc community**