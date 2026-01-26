# 🔐 Security Policy

## Supported Versions

This repository and all related projects are actively maintained. Security updates are applied to the latest versions.

| Version | Supported          |
| ------- | ------------------ |
| Latest  | ✅ Yes             |

## Reporting a Vulnerability

I take security seriously. If you discover a security vulnerability, please follow these steps:

### 📧 How to Report

1. **DO NOT** create a public GitHub issue for security vulnerabilities
2. Instead, please report via one of these methods:
   - **GitHub Private Vulnerability Reporting**: Use the "Security" tab → "Report a vulnerability"
   - **Email**: Create a private gist and share the link with me via GitHub

### 📋 What to Include

When reporting a vulnerability, please include:

- **Description**: A clear description of the vulnerability
- **Steps to Reproduce**: Detailed steps to reproduce the issue
- **Impact**: What could an attacker potentially do?
- **Suggested Fix**: If you have ideas on how to fix it (optional)

### ⏱️ Response Timeline

| Action | Timeline |
|--------|----------|
| Initial Response | Within 48 hours |
| Status Update | Within 7 days |
| Fix (if applicable) | Depends on severity |

### 🏆 Recognition

If you report a valid security vulnerability, I'll:
- Credit you in the fix commit (unless you prefer anonymity)
- Add you to a contributors list (if applicable)

## Security Best Practices

All projects in this organization follow these security practices:

### Authentication & Authorization
- ✅ JWT Authentication with token expiration
- ✅ bcrypt password hashing with automatic salting
- ✅ Token-based API protection for authenticated endpoints

### Rate Limiting
- ✅ Authentication endpoints: 5-10 requests/minute
- ✅ API endpoints: 20-60 requests/minute
- ✅ AI/external API endpoints: Limited per hour

### CORS Protection
- ✅ Explicit origin allowlist (no wildcard in production)
- ✅ Restricted HTTP methods and headers
- ✅ Credentials support with proper origin validation

### Data Protection
- ✅ Environment variables for sensitive configuration
- ✅ No secrets committed to repositories
- ✅ Input validation using Pydantic/Zod models
- ✅ Secret scanning enabled

## Scope

This security policy applies to:

| Project | Repository |
|---------|------------|
| AI Learning OS | [ai-learning-os](https://github.com/ankurkushwaha9/ai-learning-os) |
| FitTrack-Pro | [FitTrack-Pro](https://github.com/ankurkushwaha9/FitTrack-Pro) |
| Credit Card Transaction Extractor | [Credit-Card-Transaction-Extractor](https://github.com/ankurkushwaha9/Credit-Card-Transaction-Extractor) |
| Cold Outreach ComicHire AI | [cold-outreach-comichire-ai](https://github.com/ankurkushwaha9/cold-outreach-comichire-ai) |
| AI Request Desk | [ai-consulting](https://github.com/ankurkushwaha9/ai-consulting) |
| Discord Virtual Assistant | [Discord-Virtual-Assistant](https://github.com/ankurkushwaha9/Discord-Virtual-Assistant) |
| Lyzr Customer Support Agents | [lyzr-customer-support-agents](https://github.com/ankurkushwaha9/lyzr-customer-support-agents) |

## Security Implementation Checklist

For new projects, ensure the following:

### Backend Security
- [ ] JWT tokens with expiration (`exp` claim)
- [ ] JWT tokens with issued at (`iat` claim)
- [ ] bcrypt password hashing (min 10 rounds)
- [ ] Rate limiting on all public endpoints
- [ ] CORS with explicit origins (no `*` in production)
- [ ] Input validation on all endpoints
- [ ] No sensitive data in logs

### Frontend Security
- [ ] No hardcoded secrets
- [ ] Secure token storage
- [ ] XSS protection
- [ ] CSRF protection where applicable

### Repository Security
- [ ] `.gitignore` includes all sensitive files
- [ ] `.env.example` provided (no real values)
- [ ] No credentials in commit history
- [ ] Dependency updates regular

---

Thank you for helping keep these projects secure! 🙏
