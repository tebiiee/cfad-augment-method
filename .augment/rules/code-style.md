# CFAD 2.0: Code Style Guidelines

## 🎯 Purpose
Defines consistent code style, formatting, and naming conventions for the project.

## 📝 General Formatting

### Indentation & Spacing:
- **Indentation**: 2 spaces (no tabs)
- **Line Length**: 80 characters (soft limit), 120 (hard limit)
- **Trailing Spaces**: Remove all trailing whitespace
- **Final Newline**: Always end files with newline

### Semicolons & Quotes:
- **Semicolons**: Always use semicolons
- **Quotes**: Single quotes for strings, double quotes for JSX attributes
- **Template Literals**: Use for string interpolation and multiline strings

## 🏷️ Naming Conventions

### Variables & Functions:
- **camelCase**: For variables, functions, methods
- **PascalCase**: For classes, components, types, interfaces
- **SCREAMING_SNAKE_CASE**: For constants and environment variables
- **kebab-case**: For file names, CSS classes, HTML attributes

### Examples:
```typescript
// Variables and functions
const userName = 'john_doe';
const calculateTotalPrice = (items: Item[]) => { ... };

// Components and types
const UserProfile = () => { ... };
interface UserData { ... }
type ApiResponse = { ... };

// Constants
const MAX_RETRY_ATTEMPTS = 3;
const API_BASE_URL = process.env.NEXT_PUBLIC_API_URL;

// Files
user-profile.tsx
api-client.ts
user-settings.module.css
```

### File Naming:
- **Components**: `PascalCase.tsx` (UserProfile.tsx)
- **Utilities**: `kebab-case.ts` (api-client.ts)
- **Pages**: `kebab-case.tsx` (user-settings.tsx)
- **Types**: `kebab-case.types.ts` (user.types.ts)
- **Tests**: `ComponentName.test.tsx` or `utility-name.test.ts`

## ⚛️ React/Next.js Specific

### Component Structure:
```typescript
// 1. Imports (external libraries first, then internal)
import React from 'react';
import { NextPage } from 'next';
import { Button } from '@/components/ui/button';
import { UserService } from '@/services/user-service';

// 2. Types and interfaces
interface UserProfileProps {
  userId: string;
  onUpdate?: (user: User) => void;
}

// 3. Component definition
const UserProfile: React.FC<UserProfileProps> = ({ 
  userId, 
  onUpdate 
}) => {
  // 4. Hooks (useState, useEffect, custom hooks)
  const [user, setUser] = useState<User | null>(null);
  const [loading, setLoading] = useState(true);

  // 5. Event handlers
  const handleUpdate = useCallback((updatedUser: User) => {
    setUser(updatedUser);
    onUpdate?.(updatedUser);
  }, [onUpdate]);

  // 6. Effects
  useEffect(() => {
    UserService.getUser(userId).then(setUser);
  }, [userId]);

  // 7. Early returns
  if (loading) return <LoadingSpinner />;
  if (!user) return <ErrorMessage />;

  // 8. Render
  return (
    <div className="user-profile">
      {/* Component JSX */}
    </div>
  );
};

// 9. Export
export default UserProfile;
```

### JSX Guidelines:
- **Self-closing tags**: Use for components without children
- **Prop ordering**: Boolean props first, then others alphabetically
- **Conditional rendering**: Use ternary for simple conditions, && for existence checks
- **Event handlers**: Prefix with `handle` (handleClick, handleSubmit)

```typescript
// Good
<Button 
  disabled 
  loading
  className="primary-button"
  onClick={handleSubmit}
  type="submit"
>
  Submit
</Button>

// Conditional rendering
{isLoading && <LoadingSpinner />}
{error ? <ErrorMessage error={error} /> : <SuccessMessage />}
```

## 🎨 CSS/Tailwind Guidelines

### Tailwind Class Organization:
```typescript
// Order: Layout → Spacing → Typography → Colors → Effects
<div className="
  flex flex-col items-center justify-center
  p-4 m-2 space-y-4
  text-lg font-semibold text-center
  bg-white text-gray-900 border border-gray-200
  rounded-lg shadow-md hover:shadow-lg
  transition-shadow duration-200
">
```

### Custom CSS (when needed):
- **CSS Modules**: For component-specific styles
- **Global Styles**: Only for base styles and Tailwind customizations
- **BEM Methodology**: If using custom CSS classes

## 📁 Import Organization

### Import Order:
1. **React/Next.js**: React, Next.js core imports
2. **External Libraries**: Third-party packages
3. **Internal Utilities**: Services, utilities, helpers
4. **Components**: UI components, page components
5. **Types**: Type definitions and interfaces
6. **Relative Imports**: Local files

```typescript
// 1. React/Next.js
import React, { useState, useEffect } from 'react';
import { NextPage } from 'next';
import Link from 'next/link';

// 2. External libraries
import { z } from 'zod';
import { useForm } from 'react-hook-form';

// 3. Internal utilities
import { ApiClient } from '@/services/api-client';
import { formatDate } from '@/utils/date-utils';

// 4. Components
import { Button } from '@/components/ui/button';
import { UserCard } from '@/components/user-card';

// 5. Types
import type { User, ApiResponse } from '@/types/user.types';

// 6. Relative imports
import './UserProfile.module.css';
```

## 🔧 TypeScript Guidelines

### Type Definitions:
```typescript
// Interfaces for object shapes
interface User {
  id: string;
  name: string;
  email: string;
  createdAt: Date;
}

// Types for unions and computed types
type UserStatus = 'active' | 'inactive' | 'pending';
type UserWithStatus = User & { status: UserStatus };

// Generic types
interface ApiResponse<T> {
  data: T;
  success: boolean;
  message?: string;
}

// Function types
type EventHandler<T = void> = (event: Event) => T;
```

### Type Safety:
- **Strict Mode**: Always use TypeScript strict mode
- **No Any**: Avoid `any`, use `unknown` for truly unknown types
- **Type Guards**: Use type guards for runtime type checking
- **Assertion**: Use type assertions sparingly and with care

## 🧪 Testing Style

### Test Structure:
```typescript
describe('UserProfile Component', () => {
  // Setup
  const mockUser: User = {
    id: '1',
    name: 'John Doe',
    email: 'john@example.com',
    createdAt: new Date(),
  };

  beforeEach(() => {
    // Reset mocks
  });

  describe('when user is loading', () => {
    it('should display loading spinner', () => {
      // Test implementation
    });
  });

  describe('when user is loaded', () => {
    it('should display user information', () => {
      // Test implementation
    });

    it('should handle update events', () => {
      // Test implementation
    });
  });
});
```

### Test Naming:
- **Describe blocks**: Use "Component/Function Name" and "when/given" scenarios
- **Test cases**: Use "should [expected behavior]"
- **Variables**: Use descriptive names with "mock" prefix for mocks

## 📋 Comments & Documentation

### When to Comment:
- **Complex Logic**: Explain why, not what
- **Business Rules**: Document business logic and constraints
- **Workarounds**: Explain temporary solutions
- **Public APIs**: Document function parameters and return values

### JSDoc for Functions:
```typescript
/**
 * Calculates the total price including tax and discounts
 * @param items - Array of items to calculate total for
 * @param taxRate - Tax rate as decimal (0.1 for 10%)
 * @param discountCode - Optional discount code to apply
 * @returns Total price after tax and discounts
 */
const calculateTotal = (
  items: Item[], 
  taxRate: number, 
  discountCode?: string
): number => {
  // Implementation
};
```

## 🚨 Code Quality Rules

### Avoid:
- ❌ Deep nesting (max 3 levels)
- ❌ Long functions (max 20 lines)
- ❌ Magic numbers (use named constants)
- ❌ Duplicate code (extract to functions/components)
- ❌ Unused imports/variables

### Prefer:
- ✅ Early returns to reduce nesting
- ✅ Pure functions when possible
- ✅ Composition over inheritance
- ✅ Explicit over implicit
- ✅ Readable over clever

---

**Enforcement**: These styles are enforced by ESLint and Prettier. Run `npm run lint` and `npm run format` before committing.
