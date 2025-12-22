# 💳 Credit Card Transaction Extractor

**Category:** Medium Project  
**Status:** ✅ Complete  
**Started:** December 2025  
**Repository:** [github.com/ankurkushwaha9/Credit-Card-Transaction-Extractor](https://github.com/ankurkushwaha9/Credit-Card-Transaction-Extractor)  
**Live Demo:** [Replit App](https://credit-card-transaction-extractor.replit.app)

---

## 🎯 Overview

### Problem Statement
Managing credit card transactions from PDF statements is tedious. Manually copying transactions for expense tracking, budgeting, or record-keeping takes hours and is error-prone.

### Solution
Built a web application that automatically extracts transactions from credit card PDF statements and exports them to Excel or Word documents for easy editing, sharing, and analysis.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| TypeScript | Primary language |
| React 18 | Frontend framework |
| Node.js | Backend runtime |
| Express | Server framework |
| pdf-parse | PDF text extraction |
| ExcelJS | Excel file generation |
| docx | Word document generation |
| Tailwind CSS | Styling |
| Vite | Frontend build tool |
| Replit | Development & hosting |

---

## ✨ Features Built

- [x] PDF file upload with drag & drop
- [x] Automatic transaction extraction
- [x] Multi-bank support (Citibank, American Express)
- [x] Smart date and amount parsing
- [x] Transaction preview table
- [x] Export to Excel (.xlsx)
- [x] Export to Word (.docx)
- [x] Dark/light theme support
- [x] Responsive design
- [x] Privacy-focused (no data storage)

---

## 🏦 Supported Banks

| Bank | Status |
|------|--------|
| Citibank (Costco Anywhere Visa) | ✅ Full Support |
| American Express (AMEX) | ✅ Full Support |
| Other Banks | 🔄 Generic Parser |

---

## 💡 Key Learnings

### Technical
1. **PDF Parsing** - Extracting structured data from unstructured PDF text
2. **Pattern Recognition** - Building regex patterns for different bank formats
3. **Document Generation** - Creating formatted Excel and Word files programmatically
4. **File Handling** - Processing uploads in memory for privacy

### Process
1. **Iterative Development** - Started with one bank format, expanded to others
2. **Edge Case Handling** - Credit card statements have many format variations
3. **AI-Assisted Coding** - Used Replit Agent for rapid prototyping

### What Worked Well
- Breaking down parsing logic into small, testable functions
- Using TypeScript for type safety across the stack
- Memory-only processing for user privacy

### Challenges Faced
- Different banks use vastly different PDF formats
- Multi-line transactions require special handling
- Distinguishing transactions from summary information

---

## 📊 How It Works

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Upload PDF │ ──▶ │ Parse Text  │ ──▶ │  Extract    │
│  Statement  │     │ from PDF    │     │ Transactions│
└─────────────┘     └─────────────┘     └─────────────┘
                                              │
                                              ▼
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  Download   │ ◀── │  Generate   │ ◀── │   Preview   │
│  File       │     │  Document   │     │   Table     │
└─────────────┘     └─────────────┘     └─────────────┘
```

---

## 🔮 Future Improvements

- [ ] Support for more bank formats
- [ ] CSV export option
- [ ] Transaction categorization
- [ ] Date range filtering
- [ ] Batch processing multiple statements
- [ ] Transaction search/filter
- [ ] Summary statistics (totals by category)

---

## 🔗 Links

- **GitHub:** [Credit-Card-Transaction-Extractor](https://github.com/ankurkushwaha9/Credit-Card-Transaction-Extractor)
- **Built on:** Replit

---

## 🏷️ Tags

`typescript` `react` `nodejs` `pdf-parsing` `excel` `word` `finance` `document-generation` `replit`

---

*Created: December 2025*  
*Part of: [AI Learning OS](https://github.com/ankurkushwaha9/ai-learning-os)*
