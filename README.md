# Databricks Delta Lake Demos

A curated collection of educational Databricks notebooks demonstrating Delta Lake features, Unity Catalog capabilities, and real-world data engineering patterns.

## 🎯 Purpose

This repository provides hands-on, production-ready examples for learning Databricks and Delta Lake through interactive notebooks. Each demo includes:
- 📖 Comprehensive documentation and explanations
- 🏢 Real-world business scenarios and use cases
- ✅ Best practices and common pitfalls
- 🔗 Links to official documentation
- 💻 Ready-to-run code with configurable parameters

## 📚 Available Demos

### 1. [Delta Lake Cloning and Time Travel](./delta-lake-cloning-timetravel/)

**Level:** Intermediate | **Duration:** 30-45 minutes

Learn how to leverage Delta Lake's versioning and cloning capabilities for dev/test, disaster recovery, and compliance.

**Topics Covered:**
- ⏰ Time Travel: Query historical versions of data
- 📋 Shallow Clone: Create metadata-only clones for dev/test
- 💾 Deep Clone: Create independent copies for DR
- 🔄 UNDROP: Recover dropped tables (Unity Catalog)
- 🧹 VACUUM: Manage storage and retention

**Use Cases:**
- Healthcare payer managing member claims data
- Compliance audits and regulatory requirements
- Safe testing of new data processing logic
- Disaster recovery and backup strategies

**[View Demo →](./delta-lake-cloning-timetravel/)**

---

## 🚀 Getting Started

### Prerequisites

Before running any demo, ensure you have:
- ✅ Azure Databricks workspace (or AWS/GCP Databricks)
- ✅ Unity Catalog enabled (for most demos)
- ✅ Appropriate permissions (CREATE TABLE, etc.)
- ✅ Databricks Runtime 11.3 LTS or higher (recommended)

### How to Use

1. **Clone the Repository**
   ```bash
   git clone https://github.com/bigdatavik/databricks-delta-lake-demos.git
   cd databricks-delta-lake-demos
   ```

2. **Choose a Demo**
   - Browse available demos above
   - Navigate to the demo folder
   - Read the demo-specific README

3. **Import to Databricks**
   - Open your Databricks workspace
   - Go to Workspace → Import
   - Upload the `.ipynb` file from the demo folder
   - Attach to a cluster with appropriate runtime

4. **Configure and Run**
   - Update configuration parameters (catalog, schema, table names)
   - Execute cells sequentially
   - Follow along with the educational commentary

## 📂 Repository Structure

```
databricks-delta-lake-demos/
├── README.md                              # This file - main repository overview
├── .gitignore                             # Git ignore rules
│
├── delta-lake-cloning-timetravel/        # Demo 1: Time Travel & Cloning
│   ├── README.md                          # Demo-specific documentation
│   ├── Delta_Lake_Cloning_TimeTravel_Payer_Education.ipynb
│   └── databricks.yml                     # Databricks asset bundle config
│
└── [future-demos]/                        # Additional demos will be added here
    ├── README.md
    └── *.ipynb
```

## 🎓 Learning Path

If you're new to Delta Lake and Databricks, we recommend following this sequence:

1. **Start Here:** [Delta Lake Cloning and Time Travel](./delta-lake-cloning-timetravel/)
   - Foundational concepts: versioning, ACID transactions
   - Essential operations: clones, time travel, recovery

2. **Coming Soon:** Delta Lake Performance Optimization
   - Z-ordering and data skipping
   - Partition management
   - Optimize and auto-optimize

3. **Coming Soon:** Unity Catalog Governance
   - Fine-grained access control
   - Data lineage and discovery
   - Attribute-based access control (ABAC)

4. **Coming Soon:** Delta Live Tables
   - Declarative ETL pipelines
   - Data quality expectations
   - Change data capture (CDC)

## 🏢 Industry Scenarios

Our demos use relatable business contexts:

| Demo | Industry | Scenario |
|------|----------|----------|
| Time Travel & Cloning | Healthcare | Payer managing claims data with compliance requirements |
| *More coming soon* | Finance, Retail, Manufacturing | Various real-world use cases |

## 🔗 Resources

### Official Documentation
- [Azure Databricks Documentation](https://learn.microsoft.com/en-us/azure/databricks/)
- [Delta Lake Official Site](https://delta.io/)
- [Unity Catalog Documentation](https://docs.databricks.com/data-governance/unity-catalog/index.html)
- [Databricks Academy (Free Training)](https://www.databricks.com/learn/training/home)

### Community
- [Databricks Community Forums](https://community.databricks.com/)
- [Delta Lake GitHub](https://github.com/delta-io/delta)
- [Databricks Blog](https://www.databricks.com/blog)

## 🤝 Contributing

Contributions are welcome! Whether you want to:
- 🐛 Fix a bug or typo
- 📝 Improve documentation
- ✨ Add a new demo
- 💡 Suggest enhancements

**How to Contribute:**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-demo`)
3. Make your changes
4. Test thoroughly in a Databricks workspace
5. Commit with clear messages
6. Submit a pull request

### Guidelines for New Demos
- Follow the existing folder structure (`demo-name/README.md + notebooks`)
- Include comprehensive markdown documentation
- Use realistic business scenarios
- Provide configurable parameters
- Link to official documentation
- Test on recent DBR versions

## 📝 License

This project is licensed under the MIT License.

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

## 🌟 Star This Repository

If you find these demos helpful, please consider starring this repository to help others discover it!

## 💬 Feedback & Questions

- 🐛 **Found a bug?** Open an issue
- 💡 **Have a suggestion?** Open an issue or discussion
- 📧 **Need help?** Check the demo-specific README or Databricks Community Forums

## 🔄 Updates

This repository is actively maintained. Check back regularly for:
- New demos and tutorials
- Updates for new Databricks features
- Improved documentation
- Community contributions

---

**Happy Learning!** 🎓✨

*Built with ❤️ for the Databricks community*
