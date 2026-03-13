# ThesysExamples Development Patterns

> Auto-generated skill from repository analysis

## Overview

This codebase contains TypeScript-based examples focusing on C1Chat (Claude AI) integrations, primarily built with Next.js. The repository demonstrates various patterns for creating AI-powered chat applications with different levels of complexity, from basic implementations to advanced setups with tools, message persistence, and context management.

## Coding Conventions

**File Naming:**
- Use camelCase for file names: `messageStore.ts`, `TableContext.tsx`
- Component files use PascalCase with .tsx extension
- API routes follow Next.js convention: `route.ts` in directory structure

**Import/Export Style:**
```typescript
// Mixed import styles - prefer named imports for utilities
import { NextRequest, NextResponse } from 'next/server'
import React from 'react'

// Default exports for components and API routes
export default function Page() { ... }
```

**Project Structure:**
```
project-name/
├── src/app/
│   ├── api/chat/
│   │   ├── route.ts
│   │   ├── messageStore.ts
│   │   └── tools.ts
│   ├── components.tsx
│   ├── page.tsx
│   └── globals.css
├── public/
├── package.json
└── next.config.ts
```

**Commit Style:**
- Freeform commit messages
- Average 39 characters
- Focus on what changed rather than why

## Workflows

### New Next.js C1Chat Project Setup
**Trigger:** When creating a new C1Chat-powered Next.js application from scratch
**Command:** `/new-c1-project`

1. **Initialize project configuration**
   ```json
   // package.json - include Next.js, TypeScript, C1Chat dependencies
   {
     "name": "project-name",
     "scripts": {
       "dev": "next dev",
       "build": "next build"
     }
   }
   ```

2. **Create build configuration files**
   - `tsconfig.json` with strict TypeScript settings
   - `next.config.ts` for Next.js configuration
   - `eslint.config.mjs` and `postcss.config.mjs` for tooling
   - `.gitignore` with Node.js and Next.js ignores

3. **Set up app structure**
   ```typescript
   // src/app/layout.tsx - Root layout component
   // src/app/page.tsx - Main page component
   // src/app/globals.css - Global styles
   ```

4. **Create C1Chat API route**
   ```typescript
   // src/app/api/chat/route.ts
   export async function POST(request: NextRequest) {
     // C1Chat integration logic
   }
   ```

5. **Add public assets** (favicon.ico, SVG icons)

6. **Set up environment configuration** for API keys

### Iterative UI Development
**Trigger:** When actively developing and refining user interface components
**Command:** `/refine-ui`

1. **Target specific component changes**
   ```typescript
   // src/app/components.tsx - Make focused component updates
   export function ChatComponent() {
     // Incremental improvements
   }
   ```

2. **Adjust styling for specific features**
   ```css
   /* src/app/globals.css - Feature-specific style changes */
   .chat-container {
     /* Updated styles */
   }
   ```

3. **Test changes in main page component**
   ```typescript
   // src/app/page.tsx - Integration testing
   ```

4. **Commit incremental improvements** with descriptive messages

5. **Repeat cycle** for different UI aspects (layout, interactions, responsive design)

### Advanced C1Chat API Integration
**Trigger:** When adding sophisticated C1Chat capabilities with tools and persistence
**Command:** `/setup-c1chat-advanced`

1. **Create comprehensive API chat route**
   ```typescript
   // src/app/api/chat/route.ts
   import { messageStore } from './messageStore'
   import { tools } from './tools'
   
   export async function POST(request: NextRequest) {
     // Advanced C1Chat setup with tools
   }
   ```

2. **Implement message storage system**
   ```typescript
   // src/app/api/chat/messageStore.ts
   export class MessageStore {
     // Message persistence logic
   }
   ```

3. **Define tool configurations**
   ```typescript
   // src/app/api/chat/tools.ts
   export const tools = [
     {
       name: "tool_name",
       description: "Tool description",
       // Tool implementation
     }
   ]
   ```

4. **Add context management components**
   ```typescript
   // src/app/TableContext.tsx (or similar)
   export const TableContext = React.createContext(...)
   ```

5. **Set up specialized API endpoints**
   ```typescript
   // src/app/api/table/route.ts (or similar)
   export async function GET/POST() {
     // Specialized endpoint logic
   }
   ```

### Dependency Updates
**Trigger:** When updating project dependencies to latest versions
**Command:** `/bump-deps`

1. **Update package.json dependencies**
   ```json
   {
     "dependencies": {
       "next": "^latest",
       "@anthropic-ai/sdk": "^latest"
     }
   }
   ```

2. **Regenerate lock file** (`npm install` or `npm update`)

3. **Update API configurations for new versions**
   ```typescript
   // src/app/api/chat/route.ts - Update model names, endpoints
   const response = await anthropic.messages.create({
     model: "claude-3-5-sonnet-20241022", // Updated model
   })
   ```

4. **Test for breaking changes** and adjust code accordingly

5. **Commit updates** with version information

### Project Restructuring
**Trigger:** When reorganizing project structure or renaming projects
**Command:** `/restructure-project`

1. **Plan new structure** - decide on naming and organization

2. **Remove old project directories** completely
   ```bash
   # Remove entire old project folders
   rm -rf old-project-name/
   ```

3. **Create new project structure** with updated names
   ```bash
   mkdir new-project-name/
   # Recreate directory structure
   ```

4. **Migrate and refactor existing code**
   - Update import paths
   - Rename components and files
   - Update package.json project names

5. **Update all configuration files** for new project layout

6. **Test migrated functionality** to ensure nothing broke

## Testing Patterns

**Test File Pattern:**
- Use `*.test.*` naming convention for test files
- Framework: Unknown/Variable (appears to be project-specific)
- Tests likely focus on API endpoints and component functionality

**Example Test Structure:**
```typescript
// components.test.tsx (hypothetical)
describe('ChatComponent', () => {
  it('should render chat interface', () => {
    // Test implementation
  })
})
```

## Commands

| Command | Purpose |
|---------|---------|
| `/new-c1-project` | Create complete Next.js project with C1Chat integration |
| `/refine-ui` | Iteratively improve UI components and styling |
| `/setup-c1chat-advanced` | Add advanced C1Chat features with tools and persistence |
| `/bump-deps` | Update project dependencies to latest versions |
| `/restructure-project` | Reorganize and rename project structure |