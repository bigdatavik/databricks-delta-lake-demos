# Delta Lake Cloning and Time Travel Demo

An interactive educational notebook demonstrating Delta Lake's versioning and cloning capabilities through a healthcare payer storyline.

## 📖 Overview

This notebook showcases how to use Delta Lake's powerful features for data versioning, recovery, and environment management. Through the story of **HealthFirst Insurance** managing member claims data, you'll learn practical techniques for compliance, testing, and disaster recovery.

## ✨ Features Demonstrated

### 1. ⏰ Time Travel
- Query historical versions of data using `VERSION AS OF` and `TIMESTAMP AS OF`
- View complete table history with `DESCRIBE HISTORY`
- Understand Delta Lake's transaction log

### 2. 📋 Shallow Clone
- Create metadata-only clones for dev/test environments
- Understand dependencies between shallow clones and source tables
- Learn cost-effective strategies for test data management

### 3. 💾 Deep Clone
- Create fully independent table copies
- Implement disaster recovery strategies
- Prepare for major migrations and system upgrades

### 4. 🔄 UNDROP
- Recover accidentally dropped tables within 7-day retention window
- Understand Unity Catalog's safety net features
- Restore shallow clone functionality after source recovery

### 5. 🧹 VACUUM
- Manage storage and reclaim space from old data files
- Set appropriate retention periods
- Understand impact on time travel capabilities

## 🚀 Getting Started

### Prerequisites
- Azure Databricks workspace (DBR 11.3 LTS or higher)
- Unity Catalog enabled
- CREATE TABLE permissions in a catalog and schema

### Quick Start

1. **Import the Notebook**
   ```
   Delta_Lake_Cloning_TimeTravel_Payer_Education.ipynb
   ```
   Import this file into your Databricks workspace.

2. **Configure Your Environment**
   
   In Cell 3, update these parameters:
   ```python
   catalog_name = "your_catalog"      # Your Unity Catalog name
   schema_name = "your_schema"        # Your schema name
   table_name = "member_claims_prod"  # Table name (or customize)
   ```

3. **Run the Demo**
   - Execute cells sequentially from top to bottom
   - Follow the educational commentary in markdown cells
   - Observe the results of each operation

## 📊 What You'll Learn

### Core Concepts
- **Delta Lake Transaction Log**: How versioning works under the hood
- **Shallow vs Deep Clones**: When to use each approach
- **Time Travel Queries**: Accessing historical data for audits
- **Unity Catalog Retention**: 7-day safety net for dropped tables

### Real-World Scenarios

| Scenario | Feature Used | Business Value |
|----------|--------------|----------------|
| CMS Compliance Audit | Time Travel | Query data as it existed on specific dates |
| Dev/Test Environment | Shallow Clone | Cost-effective testing with production data structure |
| Pre-Migration Backup | Deep Clone | Guaranteed independent backup before major changes |
| Accidental Deletion | UNDROP + Time Travel | Recover from mistakes without data loss |
| Multi-Region DR | Deep Clone | Replicate critical data across regions |

### Best Practices Covered
✅ When to use shallow vs deep clones  
✅ Setting appropriate VACUUM retention periods  
✅ Managing dependencies between clones and source tables  
✅ Implementing disaster recovery strategies  
✅ Avoiding common pitfalls with dropped tables and clones  

## 🏥 Healthcare Payer Context

The notebook uses a relatable healthcare scenario:

**HealthFirst Insurance** needs to:
- Process member claims in production
- Test new adjudication rules safely
- Meet regulatory audit requirements (CMS, HIPAA)
- Maintain disaster recovery capabilities
- Recover from accidental data changes

This storyline demonstrates how Delta Lake features solve real business challenges in a regulated industry.

## 📁 Notebook Structure

The notebook contains 25 cells organized into:

1. **Introduction & Core Concepts** - Understand the fundamentals
2. **Real-World Scenarios** - See practical applications
3. **Configuration** - Set up your environment
4. **Step-by-Step Demo** - Hands-on exercises:
   - Create production claims table
   - Build version history
   - Query historical data (time travel)
   - Create shallow clone for dev/test
   - Create deep clone for backup
   - Test DROP behavior
   - Recover with UNDROP
   - Clean up with VACUUM
5. **Best Practices & Key Takeaways** - Actionable recommendations
6. **Additional Resources** - Links to official documentation

## 🔗 Key Documentation Links

- [Delta Lake Time Travel](https://learn.microsoft.com/en-us/azure/databricks/delta/time-travel)
- [Clone Tables in Azure Databricks](https://learn.microsoft.com/en-us/azure/databricks/delta/clone)
- [Shallow Clone for Unity Catalog](https://learn.microsoft.com/en-us/azure/databricks/delta/clone-unity-catalog)
- [UNDROP TABLE Command](https://docs.databricks.com/sql/language-manual/sql-ref-syntax-ddl-undrop-table.html)
- [VACUUM Command](https://learn.microsoft.com/en-us/azure/databricks/delta/vacuum)

## ⚙️ Databricks Asset Bundle

This demo includes a `databricks.yml` configuration file for easy deployment using Databricks Asset Bundles.

**To deploy:**
```bash
databricks bundle deploy
databricks bundle run
```

## 💡 Tips for Success

1. **Run cells sequentially** - Each cell builds on the previous one
2. **Read the markdown cells** - They provide essential context and explanations
3. **Experiment safely** - The demo uses a isolated table; feel free to modify and re-run
4. **Check DESCRIBE HISTORY** - Observe how each operation creates new versions
5. **Clean up after** - Run the cleanup cell to remove demo tables

## 🎯 Learning Outcomes

After completing this notebook, you will be able to:
- ✅ Query historical versions of Delta tables for compliance audits
- ✅ Create shallow clones for cost-effective dev/test environments
- ✅ Implement deep clone strategies for disaster recovery
- ✅ Recover dropped tables using Unity Catalog's UNDROP feature
- ✅ Optimize storage with VACUUM while preserving necessary history
- ✅ Understand the trade-offs between shallow and deep clones
- ✅ Apply best practices for table management in production environments

## 🤝 Feedback

Have suggestions for improving this demo? Open an issue in the main repository!

---

**[← Back to Main Repository](../README.md)**

