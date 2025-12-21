# 🤖 Case Study: AI Request Desk

> Centralized AI Resource Management for Enterprise Teams

---

## 📋 Overview

| Field | Details |
|-------|---------|
| **Project Name** | AI Request Desk |
| **Category** | Enterprise SaaS Platform |
| **Duration** | 2 weeks |
| **Status** | ✅ Complete & Live |
| **Repository** | [ai-consulting](https://github.com/ankurkushwaha9/ai-consulting) |
| **Live Demo** | [Replit](https://ai-consulting--ankur0609.replit.app) |

---

## 🎯 The Challenge

### Problem Statement
Organizations are rapidly adopting AI tools, but without centralized management, they face:
- **Shadow AI** - Employees using unapproved AI tools
- **No visibility** - Leadership can't track AI adoption or ROI
- **Security risks** - Unmanaged AI usage creates compliance concerns
- **Budget waste** - Multiple overlapping subscriptions without oversight

### Key Pain Points
- IT teams lack visibility into AI tool usage
- No standardized process for requesting new AI tools
- Difficult to measure ROI on AI investments
- Compliance and data security concerns

### Target Users
- **Employees** - Need easy access to approved AI tools
- **Managers** - Need to approve team AI requests
- **IT/Admin** - Need to manage organization-wide AI access
- **Leadership** - Need visibility into AI adoption

---

## 💡 The Solution

### Concept
Build a centralized platform where employees can request AI tool access through a streamlined workflow, managers can approve requests, and leadership gains visibility into AI adoption across the organization.

### Key Features

| Feature | Description |
|---------|-------------|
| 📝 **Request Management** | Submit, track, and manage AI tool access requests |
| 🏢 **Multi-Department** | Support for Sales, Marketing, Customer Success, Product, Engineering |
| ✅ **Approval Workflow** | Manager approval system with audit trails |
| 🔐 **Authentication** | Secure session-based auth with Passport.js |
| 📊 **Usage Tracking** | Monitor AI tool adoption (planned) |
| 🤖 **AI Catalog** | Browse and request approved AI tools |

### User Flows

**Employee Flow:**
1. Browse AI tool catalog
2. Submit access request with justification
3. Track request status
4. Receive approval notification

**Manager Flow:**
1. Review pending requests
2. Approve/reject with comments
3. Monitor team AI usage

---

## 🛠️ Technical Implementation

### Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                        CLIENT (React + Vite)                     │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────────────┐ │
│  │  Pages   │  │Components│  │  Hooks   │  │  TanStack Query  │ │
│  └──────────┘  └──────────┘  └──────────┘  └──────────────────┘ │
└─────────────────────────────┬───────────────────────────────────┘
                              │ HTTP / WebSocket
┌─────────────────────────────▼───────────────────────────────────┐
│                      SERVER (Express + Node.js)                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────────────┐ │
│  │  Routes  │  │   Auth   │  │ Storage  │  │    WebSocket     │ │
│  └──────────┘  └──────────┘  └──────────┘  └──────────────────┘ │
└─────────────────────────────┬───────────────────────────────────┘
                              │ Drizzle ORM
┌─────────────────────────────▼───────────────────────────────────┐
│                        DATABASE (PostgreSQL)                     │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────────────┐ │
│  │  Users   │  │ Requests │  │ AI Agents│  │    Sessions      │ │
│  └──────────┘  └──────────┘  └──────────┘  └──────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
```

### Tech Stack

| Layer | Technology | Purpose |
|-------|------------|---------|
| **Frontend** | React 18 | UI Framework |
| **Language** | TypeScript | Type Safety |
| **Styling** | Tailwind CSS | Utility-First CSS |
| **Components** | Radix UI + shadcn/ui | Accessible UI Components |
| **State** | TanStack Query | Server State Management |
| **Routing** | Wouter | Lightweight Routing |
| **Forms** | React Hook Form + Zod | Form Handling & Validation |
| **Animations** | Framer Motion | Smooth Animations |
| **Backend** | Express.js | Web Framework |
| **Database** | PostgreSQL | Relational Database |
| **ORM** | Drizzle ORM | Type-Safe Database Access |
| **Auth** | Passport.js | Authentication |
| **Sessions** | Express Session | Session Management |
| **Build** | Vite 5 | Fast Development |
| **Platform** | Replit | Hosting & Development |

### Database Schema

```typescript
// Users Table
users {
  id: serial (PK)
  username: varchar(255) UNIQUE
  password: varchar(255)
  email: varchar(255)
  department: varchar(100)
  role: varchar(50)
  createdAt: timestamp
}

// AI Tool Requests
requests {
  id: serial (PK)
  userId: integer (FK)
  toolName: varchar(255)
  justification: text
  status: enum('pending', 'approved', 'rejected')
  approvedBy: integer (FK)
  createdAt: timestamp
  updatedAt: timestamp
}

// AI Agents Catalog
aiAgents {
  id: serial (PK)
  name: varchar(255)
  description: text
  category: varchar(100)
  isActive: boolean
}
```

### Key Technical Decisions

1. **Drizzle ORM over Prisma**
   - Better TypeScript inference
   - Lighter weight for this use case
   - Seamless PostgreSQL integration

2. **TanStack Query for Server State**
   - Automatic caching and revalidation
   - Optimistic updates for better UX
   - Built-in loading and error states

3. **Radix UI + shadcn/ui**
   - Accessible by default
   - Unstyled primitives for customization
   - Production-ready components

4. **Session-based Authentication**
   - Simpler than JWT for this use case
   - Server-side session storage
   - Easy integration with Passport.js

---

## 📊 Results & Impact

### Technical Achievements
- ✅ Full-stack application with authentication
- ✅ PostgreSQL database with proper schema
- ✅ RESTful API with proper error handling
- ✅ Responsive design for all devices
- ✅ Production deployment on Replit

### Code Quality
- 🎯 TypeScript throughout (83.9% of codebase)
- 🎯 Proper separation of concerns
- 🎯 Shared types between client and server
- 🎯 Form validation with Zod schemas

### User Experience
- 🎯 Clean, modern interface
- 🎯 Department-based navigation
- 🎯 Quick access to request forms
- 🎯 Real-time status updates

---

## 📚 Key Learnings

### Technical Learnings

1. **Full-Stack TypeScript**
   - Sharing types between frontend and backend
   - End-to-end type safety with Drizzle
   - Zod schemas for runtime validation

2. **PostgreSQL + Drizzle**
   - Schema definition in TypeScript
   - Migration-free development with `db:push`
   - Type-safe queries and mutations

3. **Session Authentication**
   - Passport.js local strategy
   - Secure session management
   - CSRF protection considerations

4. **Modern React Patterns**
   - Server state vs client state
   - Optimistic UI updates
   - Proper loading/error boundaries

### Architecture Learnings

1. **Monorepo Structure**
   - Shared code between client/server
   - Single deployment unit
   - Simplified dependency management

2. **API Design**
   - RESTful conventions
   - Proper HTTP status codes
   - Consistent error responses

### Process Learnings

1. **Replit Development**
   - Quick deployment workflow
   - Built-in PostgreSQL hosting
   - Collaborative editing capabilities

2. **Documentation**
   - README as first impression
   - Architecture docs for maintainability
   - Environment variable documentation

---

## 🔮 Future Enhancements

| Enhancement | Priority | Complexity |
|-------------|----------|------------|
| Admin dashboard with analytics | High | High |
| Email notifications | High | Medium |
| Role-based access control (RBAC) | High | High |
| Usage analytics per tool | Medium | Medium |
| AI agent marketplace | Medium | High |
| Audit logging | Medium | Medium |
| API rate limiting | Low | Low |
| SSO integration | Low | High |

---

## 📸 Screenshots

*[Screenshots would be added here]*

- Landing page with feature sections
- AI tool catalog view
- Request submission form
- Request tracking dashboard
- User profile page

---

## 🔗 Links

- **Repository:** [github.com/ankurkushwaha9/ai-consulting](https://github.com/ankurkushwaha9/ai-consulting)
- **Live Demo:** [ai-consulting--ankur0609.replit.app](https://ai-consulting--ankur0609.replit.app)
- **Author:** [@ankurkushwaha9](https://github.com/ankurkushwaha9)

---

*Case Study Created: December 21, 2025*
