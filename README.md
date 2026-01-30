# PM Templates - Conversion Tracker

A comprehensive Excel-based tracking system for managing project conversions, migrations, and testing phases with Power BI integration.

---

## 📋 Overview

This repository contains a complete project tracking template designed for project managers overseeing technical conversions, migrations, or multi-phase delivery projects. Track your artifacts through every phase from pre-requisites to integration testing with automatic status updates and visual indicators.

### Key Features

✅ **28 Comprehensive Columns** covering all phases of conversion projects
✅ **Automatic Overall Status Calculation** based on phase completion
✅ **6 Distinct Phases:** Pre-requisite, Auto Conversion, Manual Conversion, Dry Run, Unit Testing, Integration Testing
✅ **Built-in Dropdowns** for consistent data entry
✅ **Conditional Formatting** for visual status tracking
✅ **Power BI Ready** - CSV format for easy dashboard creation
✅ **10 Sample Records** with realistic scenarios

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `Conversion_Tracker.csv` | Main tracker template with sample data (10 artifacts) |
| `Excel_Setup_Guide.md` | Complete step-by-step setup instructions for Excel |
| `Formula_Reference.md` | Detailed documentation of all formulas and logic |
| `README.md` | This file - overview and quick start guide |

---

## 🚀 Quick Start

### Option 1: Direct Excel Use (5 minutes)

1. **Download** `Conversion_Tracker.csv` from this repository
2. **Open in Excel**
3. **Follow setup guide** in `Excel_Setup_Guide.md` to add:
   - Dropdowns for status columns
   - Overall Status formula
   - Conditional formatting
   - Date formatting

### Option 2: Power BI Direct Import (2 minutes)

1. **Open Power BI Desktop**
2. **Get Data** → **Web** → Enter raw GitHub URL:
   ```
   https://raw.githubusercontent.com/Rekhaikkurti/PM-templates/main/Conversion_Tracker.csv
   ```
3. **Load** and start creating dashboards

---

## 📊 Column Structure

The tracker includes 28 columns organized into these categories:

### 1. Basic Information
- S.No
- Resource Name
- Type of Artifact
- Artifact Name

### 2. Phase Tracking (6 Phases x 3-4 columns each)

Each phase includes:
- Start Date
- End Date
- Status (dropdown)
- Comments

**Phases:**
1. **Pre-requisite** - Initial setup and requirements
2. **Auto Conversion** - Automated conversion process
3. **Manual Conversion** - Manual conversion work
4. **Dry Run** - Test run in safe environment
5. **Unit Testing** - Individual component testing
6. **Integration Testing** - End-to-end testing

### 3. Automatic Calculation
- **Overall Status** - Auto-calculated based on all phase statuses

---

## 🎯 Status Values

All status columns use these standardized values:

| Status | Meaning | Color Code |
|--------|---------|------------|
| **Not Started** | Phase hasn't begun | Gray |
| **In Progress** | Currently working on this phase | Yellow |
| **Completed** | Phase finished successfully | Green |
| **Blocked** | Phase stopped due to dependency/issue | Red |
| **On Hold** | Temporarily paused | Orange |
| **Not Applicable** | Phase doesn't apply to this artifact | Light Gray |

---

## 🔄 Overall Status Logic

The **Overall Status** column automatically shows the current phase status based on this priority:

1. **Integration Test** status (highest priority - last phase)
2. **Unit Testing** status
3. **Dry Run** status
4. **Manual Conversion** status
5. **Auto Conversion** status
6. **Pre-requisite** status (lowest priority - first phase)

**Examples:**
- If Unit Testing = "In Progress" → Overall Status = "Unit Testing In Progress"
- If all phases = "Completed" or "Not Applicable" → Overall Status = "Completed"
- If Pre-requisite = "Blocked" → Overall Status = "Pre-requisite Blocked"

---

## 📝 Sample Data

The template includes 10 sample artifacts showing various scenarios:

- ✅ Fully completed artifacts
- 🟡 Artifacts in different phases of progress
- 🔴 Blocked artifacts requiring attention
- 🟠 Artifacts on hold
- ⚪ Artifacts not yet started

---

## 💡 Use Cases

This tracker is perfect for:

- **System Migrations** - Track legacy to new system conversions
- **Database Migrations** - Monitor schema, data, and procedure migrations
- **Report Conversions** - Manage BI report migrations (e.g., Crystal → Power BI)
- **API Transitions** - Track API versioning and updates
- **Platform Upgrades** - Oversee multi-phase technical upgrades
- **Code Refactoring Projects** - Monitor systematic code improvements

---

## 🔌 Power BI Integration

### Recommended Dashboards

#### 1. Executive Overview
- Total artifacts by status (pie chart)
- Phase completion percentage (bar chart)
- Timeline view (Gantt-style)
- Resource allocation (table)

#### 2. Phase Analysis
- Artifacts per phase (stacked bar)
- Average duration by phase (line chart)
- Blocked items list (table with drill-down)
- Completion trend over time

#### 3. Resource Dashboard
- Workload per resource (bar chart)
- Artifacts by type (pie chart)
- My tasks view (filtered table)
- Team performance metrics

### Key Metrics to Calculate in Power BI

```DAX
Total Artifacts = COUNTROWS('Conversion_Tracker')

Completed = CALCULATE(COUNTROWS('Conversion_Tracker'), 
                      'Conversion_Tracker'[Overall Status] = "Completed")

Completion % = DIVIDE([Completed], [Total Artifacts], 0) * 100

In Progress = CALCULATE(COUNTROWS('Conversion_Tracker'), 
                        CONTAINSSTRING('Conversion_Tracker'[Overall Status], "In Progress"))

Blocked = CALCULATE(COUNTROWS('Conversion_Tracker'), 
                    CONTAINSSTRING('Conversion_Tracker'[Overall Status], "Blocked"))
```

---

## 🛠️ Customization Options

### Adding New Phases

1. Insert new columns for: Start Date, End Date, Status, Comments
2. Add data validation dropdown
3. Update Overall Status formula (see `Formula_Reference.md`)
4. Apply conditional formatting

### Adding New Status Values

1. Update dropdown lists in all status columns
2. Add new conditional formatting rules
3. Update Overall Status formula if needed
4. Document changes in comments

### Changing Artifact Types

Edit the dropdown list in Column C:
```
Current: Report, Dashboard, ETL Job, Stored Procedure, API, Script, Database Schema, Other
Add your own: View, Trigger, Function, Package, etc.
```

---

## 📚 Documentation

- **[Excel_Setup_Guide.md](Excel_Setup_Guide.md)** - Complete Excel setup instructions with formulas
- **[Formula_Reference.md](Formula_Reference.md)** - Detailed formula documentation and customization guide

---

## 🎓 Best Practices

### Data Entry
1. ✅ Always use dropdown values for status columns
2. ✅ Fill in dates when phase starts/completes
3. ✅ Use "Not Applicable" for skipped phases (don't leave blank)
4. ✅ Add meaningful comments for blocked or on-hold items
5. ✅ Update status regularly (daily or weekly)

### Team Collaboration
1. 📤 Store in SharePoint for multi-user access
2. 🔒 Protect formula columns to prevent accidental changes
3. 📊 Export to Power BI for stakeholder reporting
4. 💬 Use comments columns for team communication
5. 🔔 Set up alerts for blocked items

### Progress Tracking
1. 📈 Review overall status weekly in team meetings
2. 🚨 Flag blocked items for immediate attention
3. ⏱️ Track duration to identify bottlenecks
4. 📊 Create burndown charts in Power BI
5. 🎯 Set phase-wise completion targets

---

## 🤝 Contributing

Have suggestions for improving this template? 

- Open an issue with your ideas
- Submit a pull request with enhancements
- Share your customizations

---

## 📄 License

This template is provided as-is for project management use. Feel free to customize and adapt for your organization's needs.

---

## 🆘 Support

### Common Issues

**Q: Overall Status shows "Check Status"**
A: One or more status columns has an invalid value. Use only dropdown values.

**Q: Formulas not calculating**
A: Ensure cell format is "General" not "Text". Re-paste formula if needed.

**Q: Dropdowns not appearing**
A: Reapply Data Validation following steps in `Excel_Setup_Guide.md`

**Q: Dates showing as numbers**
A: Format columns as Date (right-click → Format Cells → Date)

### Need Help?

1. Check the `Excel_Setup_Guide.md` for setup steps
2. Review `Formula_Reference.md` for formula details
3. Examine the sample data for examples
4. Open an issue in this repository

---

## 🔗 Related Resources

- [Power BI for Project Management Guide](https://learn.microsoft.com/en-us/power-bi/)
- [Excel Data Validation](https://support.microsoft.com/en-us/office/apply-data-validation-to-cells-29fecbcc-d1b9-42c1-9d76-eff3ce5f7249)
- [Power BI DAX Reference](https://learn.microsoft.com/en-us/dax/)

---

## 📊 Version History

- **v1.0** (2026-01-30) - Initial release
  - 28 columns with 6 phases
  - Automatic overall status calculation
  - 10 sample records
  - Complete documentation

---

**Ready to start tracking?** Download `Conversion_Tracker.csv` and follow the `Excel_Setup_Guide.md`!

For Power BI dashboards, import the CSV and start visualizing your project progress today! 🚀