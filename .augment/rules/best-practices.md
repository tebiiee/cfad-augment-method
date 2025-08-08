# CFAD 2.0: Development Best Practices

## 🎯 Purpose
Defines development philosophy, patterns to follow, anti-patterns to avoid, and decision-making guidelines.

## 🏗️ Architecture Principles

### Design Philosophy:
- **KISS**: Keep It Simple, Stupid - prefer simple solutions
- **DRY**: Don't Repeat Yourself - extract common patterns
- **YAGNI**: You Aren't Gonna Need It - build what's needed now
- **Composition over Inheritance**: Favor composition patterns
- **Separation of Concerns**: Each module has a single responsibility

### Component Architecture:
- **Atomic Design**: Build from atoms → molecules → organisms → templates
- **Single Responsibility**: Each component has one clear purpose
- **Props Interface**: Clear, typed interfaces for all props
- **Controlled Components**: Prefer controlled over uncontrolled components
- **Error Boundaries**: Implement error boundaries for robust UIs

## 🧪 Testing Philosophy

### Test-Driven Development (TDD):
- **Red → Green → Refactor**: Write failing test, make it pass, refactor
- **Test First**: Write tests before implementation when possible
- **Behavior Testing**: Test behavior, not implementation details
- **Fast Feedback**: Tests should run quickly and provide clear feedback

### Testing Pyramid:
```
    E2E Tests (Few)
   ↗              ↖
Integration Tests (Some)
↗                      ↖
Unit Tests (Many)
```

### Testing Patterns:
```typescript
// Good: Testing behavior
it('should display error message when login fails', async () => {
  const { getByRole, getByText } = render(<LoginForm />);
  
  fireEvent.click(getByRole('button', { name: /login/i }));
  
  await waitFor(() => {
    expect(getByText(/invalid credentials/i)).toBeInTheDocument();
  });
});

// Avoid: Testing implementation
it('should call setError when handleSubmit is called with invalid data', () => {
  // This tests implementation, not user-facing behavior
});
```

## 🔄 State Management

### State Strategy:
- **Local First**: Use local state (useState) when possible
- **Lift Up**: Lift state up when shared between components
- **Context**: Use React Context for app-wide state
- **External**: Use Zustand/Redux for complex state management

### State Patterns:
```typescript
// Good: Derived state
const [users, setUsers] = useState<User[]>([]);
const activeUsers = users.filter(user => user.status === 'active');

// Avoid: Duplicate state
const [users, setUsers] = useState<User[]>([]);
const [activeUsers, setActiveUsers] = useState<User[]>([]);
```

### State Updates:
- **Immutable**: Always update state immutably
- **Batch Updates**: Use functional updates for dependent state
- **Optimistic Updates**: Update UI optimistically, rollback on error

## 🚀 Performance Best Practices

### React Performance:
- **Memoization**: Use React.memo, useMemo, useCallback judiciously
- **Code Splitting**: Split code at route and component level
- **Lazy Loading**: Lazy load components and routes
- **Virtual Scrolling**: For large lists (react-window)

### Next.js Performance:
- **Static Generation**: Use SSG when possible
- **Server Components**: Default to server components
- **Image Optimization**: Always use Next.js Image component
- **Font Optimization**: Use next/font for font loading

### Performance Monitoring:
```typescript
// Performance measurement
const startTime = performance.now();
// ... expensive operation
const endTime = performance.now();
console.log(`Operation took ${endTime - startTime} milliseconds`);

// React Profiler for component performance
<Profiler id="UserList" onRender={onRenderCallback}>
  <UserList users={users} />
</Profiler>
```

## 🔒 Security Best Practices

### Input Validation:
- **Client + Server**: Validate on both client and server
- **Schema Validation**: Use Zod for runtime type checking
- **Sanitization**: Sanitize user inputs
- **SQL Injection**: Use parameterized queries (Prisma handles this)

### Authentication & Authorization:
- **JWT Security**: Secure token storage and transmission
- **Session Management**: Proper session handling
- **Role-Based Access**: Implement proper authorization
- **CSRF Protection**: Enable CSRF protection

### Data Protection:
```typescript
// Good: Environment variables for secrets
const apiKey = process.env.API_KEY;

// Avoid: Hardcoded secrets
const apiKey = 'sk-1234567890abcdef'; // Never do this

// Good: Input validation
const userSchema = z.object({
  email: z.string().email(),
  age: z.number().min(0).max(120),
});

const validatedUser = userSchema.parse(userInput);
```

## 🐛 Error Handling

### Error Strategy:
- **Fail Fast**: Catch errors early and fail fast
- **Graceful Degradation**: Provide fallbacks for non-critical features
- **User-Friendly**: Show meaningful error messages to users
- **Logging**: Log errors for debugging and monitoring

### Error Patterns:
```typescript
// Good: Comprehensive error handling
const fetchUser = async (id: string): Promise<User | null> => {
  try {
    const response = await api.get(`/users/${id}`);
    return response.data;
  } catch (error) {
    if (error.status === 404) {
      return null; // User not found is expected
    }
    
    logger.error('Failed to fetch user', { id, error });
    throw new Error('Unable to load user data');
  }
};

// Error boundaries for React
class ErrorBoundary extends React.Component {
  componentDidCatch(error: Error, errorInfo: ErrorInfo) {
    logger.error('React error boundary caught error', { error, errorInfo });
  }
}
```

## 📦 Code Organization

### File Structure:
```
src/
├── components/          # Reusable UI components
│   ├── ui/             # Basic UI components (buttons, inputs)
│   └── features/       # Feature-specific components
├── pages/              # Next.js pages
├── services/           # API clients and external services
├── utils/              # Pure utility functions
├── hooks/              # Custom React hooks
├── types/              # TypeScript type definitions
├── constants/          # Application constants
└── styles/             # Global styles and themes
```

### Import Patterns:
- **Barrel Exports**: Use index.ts files for clean imports
- **Absolute Imports**: Use path mapping (@/components)
- **Dependency Direction**: Higher-level modules import lower-level ones

## 🔄 Git Workflow

### Commit Practices:
- **Atomic Commits**: Each commit represents one logical change
- **Clear Messages**: Use conventional commit format
- **Frequent Commits**: Commit early and often
- **Clean History**: Use interactive rebase to clean up history

### Branch Strategy:
- **Feature Branches**: Create branches for each feature/story
- **Short-Lived**: Keep branches short-lived (< 1 week)
- **Descriptive Names**: Use descriptive branch names
- **Clean Merges**: Squash commits when merging

### Code Review:
- **Self-Review**: Review your own code before requesting review
- **Small PRs**: Keep pull requests small and focused
- **Context**: Provide context in PR descriptions
- **Responsive**: Respond to feedback promptly

## 🚨 Anti-Patterns to Avoid

### React Anti-Patterns:
```typescript
// ❌ Avoid: Mutating state directly
state.users.push(newUser);
setState(state);

// ✅ Good: Immutable updates
setState(prevState => ({
  ...prevState,
  users: [...prevState.users, newUser]
}));

// ❌ Avoid: Using array index as key
{items.map((item, index) => 
  <Item key={index} data={item} />
)}

// ✅ Good: Using stable unique keys
{items.map(item => 
  <Item key={item.id} data={item} />
)}
```

### General Anti-Patterns:
- ❌ **God Components**: Components that do too much
- ❌ **Prop Drilling**: Passing props through many levels
- ❌ **Magic Numbers**: Hardcoded values without explanation
- ❌ **Premature Optimization**: Optimizing before measuring
- ❌ **Copy-Paste Programming**: Duplicating code instead of abstracting

## 🎯 Decision-Making Framework

### When to Abstract:
- **Rule of Three**: Abstract after third duplication
- **Clear Interface**: Can define a clear, stable interface
- **Genuine Reuse**: Multiple genuine use cases exist
- **Maintenance Benefit**: Abstraction reduces maintenance burden

### Technology Choices:
1. **Start Simple**: Choose the simplest solution that works
2. **Proven Solutions**: Prefer battle-tested technologies
3. **Team Expertise**: Consider team's existing knowledge
4. **Future Needs**: Consider likely future requirements
5. **Exit Strategy**: Ensure you can migrate away if needed

### Performance vs. Readability:
- **Readability First**: Optimize for readability unless performance is critical
- **Measure First**: Profile before optimizing
- **Document Trade-offs**: Explain performance optimizations
- **Incremental**: Make incremental improvements

## 📋 Quality Gates

### Before Committing:
- ✅ All tests pass
- ✅ Linting passes
- ✅ Type checking passes
- ✅ Code reviewed (self-review minimum)
- ✅ Documentation updated

### Before Deploying:
- ✅ E2E tests pass
- ✅ Performance tests pass
- ✅ Security scans pass
- ✅ Accessibility checks pass
- ✅ Browser compatibility verified

---

**Remember**: These are guidelines, not rigid rules. Use judgment and document deviations in `.augment/context/decisions.md`.
