# TPM Weekly Report via Jira and Cursor

## 🧭 What This Repository Demonstrates

This repository showcases a transformative workflow for Technical Program Managers (TPMs) that automates the generation of weekly status reports using Jira tickets, MCP (Model Context Protocol) servers, and Cursor. It replaces manual reporting with a scalable, AI-assisted system that extracts program health, risks, and progress directly from Jira and Slack, producing consistent, executive-ready summaries.

## ⚙️ The TPM Reporting Workflow

### 🔄 **From Manual to Automated**
- **Before**: TPMs spent 1–3 hours weekly compiling Jira data, formatting updates, and emailing reports manually.
- **After**: Reports are generated between 5 tyo 10 minutes using MCP and Cursor integrations.
- **Output**: Structured, risk-aware status reports with embedded Jira ticket references and Slack context.

### 🔥 **What is the Innovation**: Jira MCP + Cursor Integration
- **JIRA MCP**: Automated Jira data access
- **Confluence MCP**: Instant wiki page creation
- **AI Structure**: Summarizes risks, ownership, and timelines into digestible formats aligned with TPM templates.

## ✨ What This Workflow Achieves

### 🤖 AI-Powered Automation
- **Automated Jira Ticket Parsing**: Pulls status, risk flags, and delivery health from Jira dashboards.
- **Consistent Report Format**: Aligns with the weekly cadence and structure used in TPM reporting templates.
- **Instant Wiki Creation**: Professional pages in Confluence automatically

### 📊 Report Sections Generated
- **Program Summary**: Program Summary table with all 5 programs
- **Programs Details**: Status indicators and navigation links
- _**Risks & Considerations**: _Detailed risk analysis_; _could be added to the query if needed._
- **Actionable recommendations**: Structured action plan with priorities
  
## 📁 Repository Contents

```
tpmweekreport/
├── README.md                    # This comprehensive workflow guide
├── requirements.txt             # Minimal dependencies
├── Templates/                  # Working directory for examples
│   └── weekly_report_template.md # Reusable AI prompt template
└── .playwright-mcp/            # Browser automation cache (excluded from Git)
```

## 🛠️ Prerequisites for Implementation

### Required MCP Servers
1. **JIRA MCP**: Jira data rendering
2. **Confluence MCP**: Wiki page creation
3. **AI Assistant**: Claude, GPT, or similar for content analysis

### System Requirements
- **OS**: Windows 11 (optimized), macOS (compatible)
- **Docker**: For Confluence MCP server
- **Access**: Confluence wiki

## 🚀 Quick Start - 3-Step Process

### Step 1: Copy the AI Prompt Template
```Copy the Promp template located here(https://git.autodesk.com/ilievam/TPMWeekReport/blob/main/templates/weekly_report_template.md)
```

### Step 2: Customize for Your Ticket IDs
- **Replace `[PBE-XXXX]`** with your Jira Ticket ID; Add a more ticket IDs as needed divided by a comma
- **Replace details in the email heather`** 
    ```Sender, Recipients; From: Your NAME <name.surname@autodesk.com>
    To: Recipient name_ or list <name.surname@autodesk.com>
    Subject: Program Status Report - [Current Date]
    Date: [Current Date in UTC format: Thu, 12 Sep 2025 12:00:00 +0000]
    MIME-Version: 1.0
    Content-Type: multipart/alternative; boundary="----=_NextPart_000_0001_01D9F2B3.12345678"
    ```
- **Customize sections** based on report type (see templates below)

### Step 3: Execute and Get Results
- **Paste into Claude/Cursor** with MCP servers configured
- **Wait 5 minutes** for complete automation
- **Get professional formatted report** with instant wiki page creation and e-mail format ready to be sent

## 📋 Report Templates

### Program Summary
```markdown
- Summarize in a compact table view the status of the chosen programs from Jira.
```

### Detailed Program Information
```markdown
- Provides detailed status on each program with the posibility to navigate to the summary on top of the email once done. 
```

### 🎯 **Real Success Example**
- **Report**: Weekly PD Report
- **Duration**: 1 hour report preparation, data gathering, wiki creation
- **Processing Time**: < 10 minutes
- **Output**: Professional wiki page with all sections; ready to send email 

### 📈 **Performance Metrics**
- **Time Savings**: 1-2 hours → 5 minutes (30% to 50% reduction in time)
- **Accuracy Rate**: 30% to 50% for key information capture
- **Format Consistency**: 100% standardized output
- **User Satisfaction**: Dramatically reduced manual work

### 💰 **ROI Impact**
- **Productivity Gain**: 3x faster meeting documentation
- **Quality Improvement**: Consistent, comprehensive notes
- **Knowledge Retention**: Better decision tracking and follow-up
- **Team Efficiency**: Faster action item resolution

## 🔧 Implementation Guide

### MCP Server Configuration
Create `~/.cursor/mcp.json` with:

```json
{
  "mcpServers": {
    "playwright": { 
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    },
    "mcp-atlassian": {
      "command": "docker",
      "args": [
         "run",
        "--rm",
        "-i",
        "-e", "CONFLUENCE_URL",
        "-e", "CONFLUENCE_PERSONAL_TOKEN",
        "-e", "CONFLUENCE_SSL_VERIFY",
        "-e", "JIRA_URL",
        "-e", "JIRA_PERSONAL_TOKEN",
        "-e", "JIRA_SSL_VERIFY",
        "ghcr.io/sooperset/mcp-atlassian:latest"
      ],
      "env": {
        "CONFLUENCE_URL": "https://api.wiki.autodesk.com",
        "CONFLUENCE_PERSONAL_TOKEN": "YOUR_TOKEN",
        "CONFLUENCE_SSL_VERIFY": "true",
        "JIRA_URL": "https://jira.autodesk.com",
        "JIRA_PERSONAL_TOKEN": YOUR_TOKEN",
        "JIRA_SSL_VERIFY": "true"
      }
    }
  }
}
```

### Setup Steps
1. **Install Node.js** for Playwright MCP
2. **Install Docker** for Confluence MCP
3. **Configure MCP servers** in Cursor
4. **Get API tokens** for Confluence
5. **Test the workflow** with a sample Jira ticket

## Content Validation:
1. **All Jira tickets included**
2. **All custom fields extracted and formatted**
3. **Executive summaries complete and properly formatted**
4. **All external Jira links functional**
5. **Status indicators consistent across formats**

### Success Criteria
- **Functional Requirements**
✅ Data Completeness: All Jira custom fields extracted and formatted
✅ Navigation: Full internal navigation (summary ↔ sections)
✅ External Links: All Jira ticket links functional
✅ Multi-Format: EML and Confluence page versions created
✅ Professional Design: Executive-ready presentation quality

## 🤝 Contributing

### How to Contribute
1. **Test the workflow** with different Jira content
2. **Share your results** and lessons learned
3. **Improve templates** for specific use cases
4. **Document MCP server** configurations
5. **Create examples** for different industries
