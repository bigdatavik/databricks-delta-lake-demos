# Databricks Delta Lake Demos

A collection of educational Databricks notebooks demonstrating Delta Lake features with real-world scenarios and best practices.

## 📚 Notebooks

### Delta Lake Cloning and Time Travel
**File:** `Delta_Lake_Cloning_TimeTravel_Payer_Education.ipynb`

An interactive educational demo showcasing Delta Lake's powerful versioning and cloning capabilities through a healthcare payer storyline.

**Topics Covered:**
- ⏰ **Time Travel**: Query and restore historical versions of your data
- 📋 **Shallow Clone**: Create metadata-only clones for dev/test environments
- 💾 **Deep Clone**: Create independent copies for disaster recovery
- 🔄 **UNDROP**: Recover accidentally dropped tables (Unity Catalog 7-day retention)
- 🧹 **VACUUM**: Manage storage and data retention

**Key Features:**
- Configurable catalog, schema, and table names
- Real-world healthcare payer scenarios
- Step-by-step demonstrations with PySpark SQL
- Comprehensive documentation and best practices
- Links to official Azure Databricks documentation

## 🚀 Getting Started

### Prerequisites
- Azure Databricks workspace (DBR 11.3 LTS or higher recommended)
- Unity Catalog enabled
- Access to a catalog and schema where you can create tables

### Usage

1. **Import the Notebook**
   - Download the `.ipynb` file
   - Import into your Databricks workspace
   - Attach to a cluster with Unity Catalog access

2. **Configure Parameters**
   - Update `catalog_name`, `schema_name`, and `table_name` in Cell 3
   - Ensure you have CREATE TABLE permissions

3. **Run the Demo**
   - Execute cells sequentially
   - Follow along with the educational commentary
   - Experiment with the examples

## 📊 What You'll Learn

### Core Concepts
- Understanding Delta Lake's transaction log and versioning
- When to use shallow vs deep clones
- Time travel queries with `VERSION AS OF` and `TIMESTAMP AS OF`
- Unity Catalog's dropped table retention policies

### Real-World Use Cases
1. **Compliance Audits**: Query historical data for regulatory requirements
2. **Dev/Test Environments**: Create cost-effective sandboxes with shallow clones
3. **Disaster Recovery**: Implement backup strategies with deep clones
4. **Accidental Data Recovery**: Use UNDROP and time travel for mistake recovery
5. **Multi-Region DR**: Replicate data across regions

### Best Practices
- Storage optimization with VACUUM
- Setting appropriate retention periods
- Avoiding common pitfalls with clones
- Managing dependencies between shallow clones and source tables

## 🏥 Healthcare Payer Storyline

The notebook uses a relatable scenario: **HealthFirst Insurance** managing member claims data. This context demonstrates how Delta Lake features solve real business challenges:

- **Production claims processing** with audit requirements
- **Developer testing** without duplicating production data
- **System migrations** with guaranteed backups
- **Regulatory compliance** with historical data access

## 📁 Repository Structure

```
databricks-delta-lake-demos/
├── README.md                                          # This file
├── databricks.yml                                     # Databricks asset bundle config
└── Delta_Lake_Cloning_TimeTravel_Payer_Education.ipynb  # Main educational notebook
```

## 🔗 Additional Resources

### Official Documentation
- [Delta Lake Time Travel](https://learn.microsoft.com/en-us/azure/databricks/delta/time-travel)
- [Clone Tables in Azure Databricks](https://learn.microsoft.com/en-us/azure/databricks/delta/clone)
- [Unity Catalog Best Practices](https://learn.microsoft.com/en-us/azure/databricks/data-governance/unity-catalog/best-practices)
- [VACUUM Command](https://learn.microsoft.com/en-us/azure/databricks/delta/vacuum)
- [UNDROP TABLE](https://docs.databricks.com/sql/language-manual/sql-ref-syntax-ddl-undrop-table.html)

### Delta Lake Resources
- [Delta Lake Official Site](https://delta.io/)
- [Delta Lake GitHub](https://github.com/delta-io/delta)

## 🤝 Contributing

Contributions are welcome! If you have ideas for new demos or improvements:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see below for details.

```
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 💡 Feedback & Questions

Have questions or feedback? Feel free to open an issue in the repository.

---

**Happy Learning!** 🎓✨

