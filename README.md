# Project Management Templates

This repository contains Excel-based templates for project managers, specifically designed for tracking conversion, migration, and testing projects.

## 📋 Contents

- **Conversion_Tracker.csv** - Main tracking spreadsheet with 28 columns
- **Excel_Setup_Guide.md** - Detailed setup instructions for Excel
- **Formula_Reference.md** - Complete formula documentation
- **Sample_Data.csv** - Additional test data

---

## 🚀 Quick Start

### Option 1: Use in Excel

1. **Download** `Conversion_Tracker.csv`
2. **Open** in Microsoft Excel
3. Follow the **Excel_Setup_Guide.md** to:
   - Add dropdown lists
   - Apply the Overall Status formula
   - Set up conditional formatting
   - Configure date formats

### Option 2: Use in Google Sheets

1. **Download** `Conversion_Tracker.csv`
2. **Upload** to Google Drive
3. **Open with** Google Sheets
4. Most features work automatically (with minor formula adjustments)

### Option 3: Connect to Power BI

1. **Download** the CSV file
2. **Open Power BI Desktop**
3. **Get Data** → **Text/CSV**
4. Load the file and create dashboards

---

## 📊 What's Tracked

### Conversion Phases

This tracker monitors 6 major phases:

1. **Pre-requisites** - Initial setup and dependencies
2. **Auto Conversion** - Automated conversion processes
3. **Manual Conversion** - Manual migration work
4. **Dry Run** - Test runs before production
5. **Unit Testing** - Individual component testing
6. **Integration Testing** - End-to-end testing

### For Each Phase:
- ✅ Start Date
- ✅ End Date
- ✅ Status (Not Started, In Progress, Completed, Blocked, On Hold, Not Applicable)
- ✅ Comments

### Additional Tracking:
- Resource assignment
- Artifact type and name
- Overall project status (auto-calculated)

---

## 🎯 Key Features

### 1. Smart Overall Status
The tracker automatically determines the overall status based on the current active phase:
- If Unit Testing is "In Progress" → Overall Status = "Unit Testing In Progress"
- If all phases are "Completed" → Overall Status = "Completed"
- Prioritizes the latest phase in the workflow

### 2. Dropdown Lists
Pre-configured status dropdowns ensure data consistency:
- Not Started
- In Progress
- Completed
- Blocked
- On Hold
- Not Applicable

### 3. Visual Status Indicators
Color-coded statuses (when using Excel):
- 🟢 Green = Completed
- 🟡 Yellow = In Progress
- 🔴 Red = Blocked
- 🟠 Orange = On Hold
- ⚪ Gray = Not Started
- ⚫ Light Gray = Not Applicable

### 4. Flexible Artifact Types
Track different types of work:
- Reports
- Dashboards
- ETL Jobs
- Stored Procedures
- APIs
- Scripts
- Database Schemas
- Other

---

## 📈 Use Cases

### Migration Projects
Track data or application migrations through all phases from prerequisites to final testing.

### Conversion Projects
Monitor conversion of legacy systems, reports, or processes to new platforms.

### Testing Projects
Manage comprehensive testing workflows with dry runs, unit tests, and integration tests.

### Multi-Resource Projects
Track work across multiple team members with clear status visibility.

---

## 🔧 Customization

### Add More Phases
You can add additional phases by:
1. Adding new Start/End/Status/Comments columns
2. Updating the Overall Status formula
3. Applying data validation to new status columns

### Modify Status Options
Edit the dropdown list values to match your workflow:
- Add custom statuses like "Pending Review", "Approved", etc.
- Remove statuses you don't need

### Add Calculated Fields
Enhance with additional formulas:
- Duration calculations (End Date - Start Date)
- Progress percentage
- Days remaining
- Resource utilization

---

## 💡 Best Practices

1. **Update Regularly**: Update statuses daily or weekly for accuracy
2. **Use Comments**: Document blockers, decisions, and key information
3. **Mark N/A**: Use "Not Applicable" for phases that don't apply
4. **Track Dates**: Enter start dates when work begins, end dates when complete
5. **Review Overall Status**: Check that overall status reflects actual progress
6. **Export for Reporting**: Save as Excel and connect to Power BI for dashboards

---

## 📊 Power BI Integration

### Connect Your Data

1. Save the CSV file in a shared location (SharePoint, OneDrive, etc.)
2. Open Power BI Desktop
3. Get Data → Text/CSV
4. Select your file
5. Load data

### Recommended Visualizations

**Executive Dashboard:**
- Pie chart: Artifacts by Overall Status
- Bar chart: Artifacts by Resource
- Timeline: Start/End dates
- KPI cards: Total, Completed, Blocked, In Progress

**Phase Analysis:**
- Stacked bar: Status by Phase
- Funnel: Progression through phases
- Table: Artifacts with status details

**Resource View:**
- Matrix: Resources vs. Artifacts
- Bar chart: Workload by resource
- Timeline: Resource assignments

---

## 🤝 Contributing

Feel free to:
- Fork this repository
- Suggest improvements
- Add your own templates
- Share customizations

---

## 📝 Version History

**v1.0** (2026-01-30)
- Initial release
- 28-column conversion tracker
- Overall status formula
- Sample data with 10 artifacts

---

## 📧 Support

For questions or issues:
- Review the **Excel_Setup_Guide.md** for detailed instructions
- Check **Formula_Reference.md** for formula help
- Open an issue in this repository

---

## 📄 License

Free to use and modify for your project management needs.

---

**Happy Tracking! 📊**