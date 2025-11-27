# Architecture Overview

This document provides a high-level overview of the SuperGitSight system architecture based on the actual implementation.

## System Overview

SuperGitSight is built as a Next.js application with a layered architecture that processes GitHub data through multiple computation stages.

```
┌─────────────┐
│   Client    │
│  (Browser)  │
└──────┬──────┘
       │
       │ HTTPS
       │
┌──────▼─────────────────────────────────────┐
│         Next.js Application                │
│    (Server Actions + React Pages)          │
└──────┬─────────────────────────────────────┘
       │
       ├─────────────────┬─────────────────┐
       │                 │                 │
┌──────▼──────┐  ┌──────▼──────┐  ┌──────▼──────┐
│  GitHub API │  │  Processing │  │    Cache    │
│  (GraphQL)  │  │   Engine    │  │   (Redis)   │
└─────────────┘  └─────────────┘  └─────────────┘
       │                 │                 │
       └─────────────────┴─────────────────┘
                         │
              ┌──────────▼──────────┐
              │   Database          │
              │   (PostgreSQL)      │
              └─────────────────────┘
```

## Component Description

### Client Layer
- **Web Interface**: Next.js 16 + React 19 frontend
- **Server Actions**: Direct API calls from client to server
- **No Authentication**: Currently public-only access

### Application Layer (Next.js)

#### Server Actions
- Handle HTTP requests directly
- Request validation and sanitization
- Response formatting
- Error handling

#### Pages & Routes
- Public pages for profile search and viewing
- Profile analysis pages
- Comparison pages
- API routes for data fetching

### Processing Layer

#### GitHub API Integration
- GitHub GraphQL API calls
- Data fetching and normalization
- Rate limit management
- Username validation

#### Scoring Engine
- KCRISMAG algorithm execution
- ACID algorithm execution
- Score calculation
- Trend analysis
- Comparison logic

#### Computation Modules
- **Collaboration Analysis**: Team vs. solo work patterns
- **Contribution Analysis**: Monthly trends and patterns
- **Project Health**: Active vs. archived projects
- **Tech Stack**: Language and framework detection
- **Work Style**: Activity patterns and peak times

### Data Layer

#### Cache (Redis)
- Result caching for performance
- API response caching
- Cache invalidation
- TTL management

#### Database (PostgreSQL)
- Profile metadata storage
- Benchmark data storage
- Score history (if applicable)

### Data Flow

1. **User Request**: User submits GitHub username via web interface
2. **Cache Check**: System checks Redis cache for existing results
3. **Data Fetching**: If not cached, GitHub GraphQL API fetches profile/repo data
4. **Processing**: Data flows through multiple computation layers:
   - Normalization (adapters)
   - Computation (collaboration, contributions, tech stack, work style)
   - Scoring (KCRISMAG, ACID)
5. **Caching**: Results cached in Redis for future requests
6. **Storage**: Metadata stored in PostgreSQL (if needed)
7. **Response**: Results returned to user via Server Actions

## Architecture Layers

### Data Layer
- **Sources**: Fetch from GitHub GraphQL API or database
- **Adapters**: Normalize data to a common format
- **Purpose**: Abstract data sources and provide consistent data structure

### Processing Layer
- **Compute**: Transform data into metrics (collaboration, contributions, tech stack, work style)
- **Scoring**: Calculate scores (KCRISMAG, ACID)
- **Comparison**: Profile comparison logic
- **Purpose**: Pure functions, no I/O, reusable across domains

### Service Layer
- **Orchestration**: Coordinate data → processing → storage
- **Error Handling**: Custom error classes
- **Purpose**: Business logic coordination

### Presentation Layer
- **UI Components**: React components for visualization
- **Pages**: Next.js pages and routes
- **Purpose**: User interface and experience

## Technology Stack

### Frontend
- Next.js 16
- React 19
- TypeScript
- Tailwind CSS
- Shadcn/UI
- Framer Motion

### Backend
- Next.js Server Actions
- GitHub GraphQL API
- Prisma ORM
- PostgreSQL
- Redis

### Infrastructure
- Vercel for hosting and deployment
- CDN for static assets (via Vercel)
- Database hosted separately
- Redis cache hosted separately

### Security
- HTTPS everywhere (via Vercel)
- Encrypted data in transit
- No authentication system (public data only)
- Input validation and sanitization

## Scalability

### Current Approach
- Stateless application (can scale horizontally)
- Result caching reduces API calls
- Efficient GitHub API usage
- Database optimization

### Performance Optimization
- Result caching (Redis)
- Parallel processing where possible
- Efficient API usage patterns
- Database query optimization

## Security Measures

### Data Protection
- No permanent storage of sensitive data
- Encrypted data in transit (HTTPS)
- Input validation and sanitization
- No authentication system (public-only access)

### Privacy
- Public GitHub data only
- No private repository access
- No user data collection
- Privacy policy compliance


## Future Architecture Considerations

Potential improvements (not currently implemented):
- GitHub OAuth for private repo access
- Background job processing (message queues)
- Separate API service (if needed)
- User authentication and sessions
- Webhook support for real-time updates

---

**Note**: This architecture reflects the current implementation. The system is designed to be simple, maintainable, and scalable within the constraints of a Next.js application.

For more information, see:
- [Overview](overview.md)
- [Scoring Algorithms](scoring.md)
- [Features](features.md)
