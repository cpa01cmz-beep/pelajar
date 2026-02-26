# Backend Engineer Domain

## Domain Scope

The Backend Engineer domain covers:
- API design and implementation
- Database schema and migrations
- Authentication and authorization
- Business logic implementation
- Serverless functions
- Backend API integrations

## Current State

**Repository Status:** Initial bootstrap phase - no backend code yet

The repository currently only contains CI/CD workflow configuration. Application code needs to be implemented based on the existing issues.

## Issues Analysis

Existing issues requiring backend work:
- F1: Authentication System
- F2: Database Schema & RLS Policies  
- INF2: Supabase Integration

## Guidelines

1. **API Design**: RESTful principles, proper error handling
2. **Security**: RLS policies, input validation, secure auth flows
3. **Performance**: Efficient queries, proper indexing
4. **Code Quality**: TypeScript strict mode, consistent patterns
5. **Testing**: Unit tests for business logic, integration tests for APIs

## Tech Stack (Expected)

Based on the workflow and issues:
- Supabase (Database & Auth)
- Next.js API Routes (Serverless)
- TypeScript

## Notes

- Wait for Architect to create backend-specific issues
- Coordinate with Platform Engineer for infrastructure needs
- Coordinate with Security Engineer for auth patterns

## Current Dependencies

- **F1: Authentication System** → Blocked by INF2 (Supabase Integration)
- **F2: Database Schema & RLS Policies** → Blocked by INF2 (Supabase Integration)

## Repository Health

- No application code exists yet (empty repository)
- Project needs: package.json, Next.js setup, Supabase configuration
- This is an Architect/Platform responsibility, not Backend Engineer
