# Master Consolidated Program Status Report Generation Query

## **Complete Request for Multi-Format Program Status Report System**

Using the Atlassian MCP, create a comprehensive program status report system from the following Jira tickets: **PBE-XXXX, PBE-XXXX**. Create simultaniously the eml file and the confluence page. The confluence page should be created in the space with key "milieva".

### **Required Data Fields:**
- **Domain Areas** (customfield_32380)
- **Executive Status** / **Execution Status** (customfield_30698) 
- **Executive Summary** (customfield_34883)

---

## **Report Generation Requirements:**

### **1. EML Email Report (`program_report_YYYYMMDD.eml`)**

Convert the Jira data to EML format with the **MODERN STREAMLINED DESIGN**:

#### **Email Headers (Updated Format):**
```
From: Your NAME <name.surname@autodesk.com>
To: Recipient name_ or list <name.surname@autodesk.com>
Subject: Program Status Report - [Current Date]
Date: [Current Date in UTC format: Thu, 12 Sep 2025 12:00:00 +0000]
MIME-Version: 1.0
Content-Type: multipart/alternative; boundary="----=_NextPart_000_0001_01D9F2B3.12345678"
```

#### **Plain Text Structure (Streamlined Format):**
```
PROGRAM STATUS REPORT
Generated on [Current Date]

PROGRAM SUMMARY
===============

1. [Program Name] ([Ticket])
   Status: [Status] | Assignee: [Name] | Domain: [Domain]
   Jira: [Jira URL]

2. [Next Program...]

DETAILED PROGRAM INFORMATION
============================

[PROGRAM NAME] ([TICKET])
---------------------------
[Executive Summary Content - Clean formatting]
```

#### **HTML Structure :**
- **DOCTYPE**: `<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN">`
- **MSO Optimization**: Enhanced conditional comments and Office namespaces
- **Modern CSS Architecture**:
  ```css
  body {
      background-color: #f4f4f4 !important;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, Arial, sans-serif !important;
      font-size: 14px !important;
      line-height: 1.6 !important;
  }
  
  .email-container {
      max-width: 600px !important;
      margin: 0 auto !important;
      background-color: #ffffff !important;
  }
  
  .header-table {
      background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%) !important;
      background-color: #1e3c72 !important; /* Fallback for Outlook */
  }
  
  .header-cell {
      padding: 30px 20px !important;
      text-align: center !important;
  }
  
  .header-title {
      color: #ffffff !important;
      font-size: 28px !important;
      font-weight: 300 !important;
      margin: 0 0 10px 0 !important;
      line-height: 1.2 !important;
  }
  
  .header-date {
      color: #e6f2ff !important;
      font-size: 16px !important;
      font-weight: 300 !important;
      margin: 0 !important;
  }
  
  .content-wrapper {
      padding: 30px 20px !important;
  }
  
  .section-title {
      color: #1e3c72 !important;
      font-size: 22px !important;
      font-weight: 600 !important;
      margin: 0 0 20px 0 !important;
      padding-bottom: 8px !important;
      border-bottom: 3px solid #2a5298 !important;
  }
  
  .summary-table {
      width: 100% !important;
      border-collapse: collapse !important;
      margin: 0 0 30px 0 !important;
      background-color: #ffffff !important;
  }
  
  .summary-table th {
      background-color: #f8f9fa !important;
      color: #1e3c72 !important;
      padding: 12px 8px !important;
      text-align: left !important;
      font-weight: 600 !important;
      font-size: 13px !important;
      border-bottom: 2px solid #e0e0e0 !important;
  }
  
  .summary-table td {
      padding: 12px 8px !important;
      border-bottom: 1px solid #e0e0e0 !important;
      font-size: 13px !important;
      vertical-align: top !important;
  }
  
  .program-link {
      color: #2a5298 !important;
      text-decoration: none !important;
      font-weight: 600 !important;
  }
  
  .jira-link {
      color: #0052cc !important;
      text-decoration: none !important;
      font-weight: 500 !important;
      padding: 2px 6px !important;
      border-radius: 3px !important;
      background-color: #e6f3ff !important;
      font-size: 12px !important;
  }
  
  .status-badge {
      background-color: #4caf50 !important;
      color: #ffffff !important;
      padding: 4px 8px !important;
      border-radius: 16px !important;
      font-size: 11px !important;
      font-weight: 600 !important;
      text-transform: uppercase !important;
  }
  
  .program-section {
      margin: 0 0 25px 0 !important;
      padding: 20px !important;
      background-color: #f8f9ff !important;
      border-left: 4px solid #2a5298 !important;
      border-radius: 0 6px 6px 0 !important;
  }
  
  .program-title {
      color: #1e3c72 !important;
      font-size: 18px !important;
      font-weight: 600 !important;
      margin: 0 0 10px 0 !important;
  }
  
  .program-meta {
      color: #666666 !important;
      font-size: 13px !important;
      margin: 0 0 15px 0 !important;
  }
  
 
  .executive-summary {
      line-height: 1.7 !important;
      font-size: 14px !important;
  }
  
  .footer-section {
      background-color: #f8f9fa !important;
      padding: 20px !important;
      text-align: center !important;
      color: #666666 !important;
      font-size: 13px !important;
  }
  
  /* Mobile Responsive */
  @media only screen and (max-width: 600px) {
      .email-container {
          width: 100% !important;
          max-width: 100% !important;
      }
      
      .content-wrapper {
          padding: 20px 15px !important;
      }
      
      .header-title {
          font-size: 24px !important;
      }
      
      .summary-table th,
      .summary-table td {
          padding: 8px 5px !important;
          font-size: 12px !important;
      }
      
      .program-section {
          padding: 15px !important;
      }

  }
  ```

#### **Enhanced Outlook Optimization:**
- **Enhanced MSO conditional comments** with better Office namespace support
- **Improved table structure** with optimized cellspacing and cellpadding
- **Better border-collapse** properties for consistent rendering
- **Streamlined inline styling** with proper !important declarations
- **Cross-platform compatibility**: Outlook Classic, macOS Outlook, mobile clients
- **High DPI support**: Proper rendering on retina displays

#### **Content Transfer Encoding:**
- Use `Content-Transfer-Encoding: 7bit` for both plain text and HTML
- Remove `quoted-printable` encoding for better compatibility

---

### **2. Confluence Page (API Creation)**

Create a Confluence page in the **milieva/Performance and Scale SVF1 to SVF2/Deprecation/Reports** personal space with:

#### **Page Details:**
- **Space**: milieva
- **Title**: "Program Status Report [Current Date]"
- **Content Format**: Markdown
- **Parent**: None (create in root of personal space)
- **URL Format**: https://wiki.autodesk.com/pages/viewpage.action?pageId=[PAGE_ID] (remove "api" from URL)

#### **Confluence Formatting:**
- **Professional Header**: Main title with generation date
- **Summary Table**: Markdown table with all programs
- **Status Indicators**: Green circle emojis (🟢) for visual status
- **Internal Navigation**: Markdown links to sections within page
- **External Jira Links**: Direct links to all Jira tickets
- **Structured Sections**: Each program with consistent formatting

#### **Content Structure:**
```markdown
# Program Status Report
*Generated on [Current Date]*

**📧 Download Email Format:**
- [📧 Email Version](program_report_YYYYMMDD.eml) - Outlook-compatible email format

## Program Summary
| Program | Ticket | Status | Assignee | Domain Area |
|---------|--------|--------|----------|-------------|
| [Program Name](#anchor) | [TICKET](jira-link) | 🟢 Status | Assignee | Domain |

## Program Name
**Ticket:** [TICKET](jira-link) | **Status:** 🟢 Status | **Assignee:** Name | **Domain:** Area

### Executive Summary
[Formatted content from Jira]
```

---

## **Technical Implementation Steps:**

### **Step 1: Data Extraction**
```
1. Fetch all 5 Jira tickets using parallel API calls
2. Extract required custom fields: customfield_32380, customfield_30698, customfield_34883
3. Process and format executive summary content
4. Map status values to color codes
5. Generate current date in multiple formats (email, markdown)
```

### **Step 2: EML Generation **
```
1. Create multipart MIME structure with 7bit encoding
2. Generate streamlined plain text version with numbered format
3. Create email-optimized version using the html above:
   - Add XHTML DOCTYPE and enhanced Office namespaces
   - Include improved MSO conditional comments
   - Apply modern CSS architecture with streamlined styling
   - Use optimized table-based layout
   - Add proper email headers with UTC date format
4. Ensure cross-platform compatibility with enhanced Outlook support
5. Save as program_report_YYYYMMDD.eml
```

### **Step 3: Confluence Page Creation**
```
1. Convert content to Confluence markdown format
2. Use Confluence API to create page in milieva space
3. Apply proper formatting with status emojis
4. Add download link section at top linking to EML file only
5. Ensure internal navigation works
6. Return page URL for reference (use wiki.autodesk.com format, not api.wiki.autodesk.com)
```

### **Step 4: Cross-Format Linking**
```
1. After Confluence page is created, get the page URL (remove "api" from URL)
2. Update EML file to add Confluence link at bottom (wiki.autodesk.com format)
3. Ensure EML references Confluence page only (no confluence file download)
```

---

## **File Management:**

### **File Naming Convention:**
- EML: `program_report_YYYYMMDD.eml` (e.g., program_report_20250912.eml) based on the today's date
- Directory: Save all files in point to your directory of choice.

### **Output Directory Structure:**
```
weekly_report_dmd/
├── program_report_YYYYMMDD.eml
```

---

## **Quality Assurance Checklist:**

### **Content Validation:**
- [ ] All  Jira tickets included
- [ ] All custom fields extracted and formatted
- [ ] Executive summaries complete and properly formatted
- [ ] All external Jira links functional
- [ ] Status indicators consistent across formats

### **Navigation Testing:**
- [ ] Summary table links to program sections work
- [ ] External Jira links open in new tabs
- [ ] Confluence internal navigation functional

### **Format-Specific Validation:**
- [ ] **EML**: Outlook compatibility, mobile rendering, plain text fallback, Confluence link at bottom (wiki.autodesk.com format)
- [ ] **Confluence Page**: Proper markdown rendering, emoji status indicators, download link to EML at top

### **Cross-Platform Testing:**
- [ ] EML renders correctly in Outlook Classic, macOS Outlook, mobile clients 
- [ ] Confluence page displays properly in browser and mobile app

---

## **Success Criteria:**

### **Functional Requirements:**
✅ **Data Completeness**: All Jira custom fields extracted and formatted  
✅ **Navigation**: Full internal navigation (summary ↔ sections)  
✅ **External Links**: All Jira ticket links functional  
✅ **Multi-Format**: EML and Confluence page versions created  
✅ **Professional Design**: Executive-ready presentation quality  

### **Technical Requirements:**
✅ **Email Compatibility**: Outlook Classic, macOS, mobile clients 
✅ **Responsive Design**: Mobile-friendly layouts  
✅ **Status Indicators**: Color-coded badges and emojis across formats  
✅ **Clean Code**: Maintainable email CSS structure  
✅ **API Integration**: Confluence page created via API with correct URL format  

### **User Experience:**
✅ **Intuitive Navigation**: Easy movement between summary and details  
✅ **Professional Appearance**: Suitable for executive distribution  
✅ **Cross-Platform**: Consistent experience across devices/clients  
✅ **Accessibility**: Proper semantic markup and contrast ratios  

---

## **CRITICAL DESIGN REQUIREMENT:**

1. **Enhanced MIME structure** with 7bit encoding
2. **Streamlined plain text format** with numbered program list
3. **Modern CSS architecture** with improved MSO compatibility
4. **Optimized responsive design** with better mobile breakpoints
5. **Professional visual hierarchy** with refined spacing and typography
6. **Enhanced Outlook optimization** with better conditional comments
7. **Improved cross-platform compatibility** across all email clients
8. **Confluence URL format**: Use wiki.autodesk.com (not api.wiki.autodesk.com)
9. **No confluence file downloads**: Only link to Confluence page

Open the Confluence page right after creating the report.
Open the ".eml" file created as well right after the execution of the query is completed.
