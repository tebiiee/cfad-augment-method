# Augment Develop Method: Technology Stack Rules

## 🎯 Purpose
Defines the technology stack preferences, constraints, and standards for this project.

## 🏗️ Default Stack Preferences

### Frontend Framework
- **Primary**: Next.js 14+ with App Router
- **Language**: TypeScript (strict mode)
- **Styling**: Tailwind CSS
- **State Management**: React Context + useReducer (simple) or Zustand (complex)
- **Forms**: React Hook Form + Zod validation

### Backend & Database
- **API**: Next.js API Routes or tRPC
- **Database**: 
  - **Simple Projects**: Convex (real-time, serverless)
  - **Complex Projects**: PostgreSQL + Prisma
  - **Prototypes**: SQLite + Prisma
- **Authentication**: NextAuth.js or Convex Auth

### Deployment & Infrastructure
- **Hosting**: Vercel (primary) or Netlify
- **Database Hosting**: 
  - Convex (managed)
  - Supabase (PostgreSQL)
  - PlanetScale (MySQL)
- **File Storage**: Vercel Blob or Supabase Storage
- **CDN**: Vercel Edge Network

### Development Tools
- **Package Manager**: npm (default) or pnpm
- **Linting**: ESLint + Prettier
- **Testing**: 
  - **Unit**: Jest + React Testing Library
  - **E2E**: Playwright (always configured)
  - **Component**: Storybook (if UI-heavy)
- **Type Checking**: TypeScript strict mode

## 🔧 Stack Detection & Configuration

### Auto-Detection Process:
1. **Scan package.json** for existing dependencies
2. **Check framework files** (next.config.js, etc.)
3. **Detect database** (schema files, env variables)
4. **Identify deployment** (vercel.json, netlify.toml)

### MCP Configuration Based on Stack:

#### Convex Projects:
- **Convex MCP**: Automatic if convex detected
- **Real-time Features**: WebSocket patterns
- **Schema Management**: Convex schema validation

#### Supabase Projects:
- **Supabase MCP**: For database operations
- **Auth Integration**: Supabase Auth patterns
- **Real-time**: Supabase subscriptions

#### PostgreSQL Projects:
- **Database MCP**: PostgreSQL operations
- **Migration Tools**: Prisma migrate
- **Connection Pooling**: PgBouncer patterns

## 📋 Stack-Specific Rules

### Next.js 14+ Rules:
- **App Router**: Always use app directory structure
- **Server Components**: Default to server components
- **Client Components**: Only when interactivity needed
- **API Routes**: Use route.ts in app directory
- **Metadata**: Use generateMetadata for SEO

### TypeScript Rules:
- **Strict Mode**: Always enabled
- **Type Imports**: Use `import type` for types
- **Interfaces**: Prefer interfaces over types for objects
- **Enums**: Use const assertions instead of enums
- **Any**: Never use `any`, use `unknown` instead

### Database Rules:

#### Convex:
- **Schema**: Define in `convex/schema.ts`
- **Mutations**: Pure functions, no side effects
- **Queries**: Reactive, real-time by default
- **Auth**: Use Convex Auth for authentication

#### PostgreSQL + Prisma:
- **Schema**: Define in `prisma/schema.prisma`
- **Migrations**: Always generate and review migrations
- **Queries**: Use Prisma Client, avoid raw SQL
- **Transactions**: Use Prisma transactions for complex operations

### Styling Rules:
- **Tailwind**: Use utility classes, avoid custom CSS
- **Components**: Create reusable component variants
- **Responsive**: Mobile-first approach
- **Dark Mode**: Support if specified in requirements

## 🚀 Performance Standards

### Core Web Vitals Targets:
- **LCP**: < 2.5 seconds
- **FID**: < 100 milliseconds
- **CLS**: < 0.1

### Optimization Strategies:
- **Images**: Use Next.js Image component
- **Fonts**: Use next/font for font optimization
- **Code Splitting**: Automatic with Next.js
- **Caching**: Leverage Vercel Edge Cache

## 🔒 Security Standards

### Authentication:
- **JWT**: Secure token handling
- **Sessions**: Secure session management
- **CSRF**: Protection enabled
- **Rate Limiting**: Implement for API routes

### Data Protection:
- **Environment Variables**: Never commit secrets
- **Input Validation**: Validate all inputs with Zod
- **SQL Injection**: Use parameterized queries
- **XSS**: Sanitize user inputs

## 🧪 Testing Standards

### Unit Testing:
- **Coverage**: Aim for 80%+ on new code
- **Test Files**: Co-locate with source files
- **Naming**: `*.test.ts` or `*.spec.ts`
- **Mocking**: Mock external dependencies

### E2E Testing:
- **Playwright**: Always configured
- **Test Files**: In `tests/` directory
- **Page Objects**: Use page object pattern
- **CI Integration**: Run on every PR

### Integration Testing:
- **API Routes**: Test all endpoints
- **Database**: Test database operations
- **Auth**: Test authentication flows
- **Real-time**: Test WebSocket connections

## 📦 Dependency Management

### Version Strategy:
- **Major Versions**: Pin major versions
- **Security Updates**: Apply immediately
- **Dependencies**: Minimize external dependencies
- **Bundle Size**: Monitor and optimize

### Allowed Dependencies:
- **UI**: shadcn/ui, Radix UI, Headless UI
- **Utilities**: lodash-es, date-fns, clsx
- **Validation**: Zod, yup
- **HTTP**: axios (if needed), fetch (preferred)

### Forbidden Dependencies:
- **jQuery**: Use modern alternatives
- **Moment.js**: Use date-fns instead
- **Lodash**: Use lodash-es for tree shaking
- **CSS Frameworks**: Avoid Bootstrap, use Tailwind

## 🔄 Migration Strategies

### Framework Updates:
- **Next.js**: Follow official migration guides
- **React**: Update incrementally
- **TypeScript**: Update with care, test thoroughly

### Database Migrations:
- **Schema Changes**: Always use migrations
- **Data Migrations**: Separate from schema migrations
- **Rollback**: Always have rollback strategy
- **Testing**: Test migrations on staging first

---

**Note**: These are default preferences. Project-specific requirements may override these standards. Document any deviations in `.augment/context/decisions.md`.
