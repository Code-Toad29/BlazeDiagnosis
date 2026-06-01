# Cyber Security Analyst Learning Path

## Week 1 Focus

- Web application security basics
- OWASP Top 10 awareness
- Authentication and authorization
- Role-based access control
- Customer data exposure risks
- GitHub secret safety
- API security basics
- Clear security reporting

## Priority Files to Review

- `docs/access-control.md`
- `docs/api-contracts.md`
- `docs/security/STUDENT_SECURITY_RULES.md`
- `docs/security/SECURITY_REVIEW_CHECKLIST.md`
- `backend/src/shared/middleware/auth.ts`
- `backend/src/shared/middleware/authorization.ts`
- `backend/src/shared/middleware/tenant-scope.ts`
- `.env.example`
- `backend/.env.example`
- `frontend/.env.example`
- `.gitignore`

## Starter Tasks

- Check that `.env` files are ignored.
- Review what customer data exists in the schema.
- Identify where role-based access is required.
- Create a security checklist for customer tracking links.
- Review API contracts for access-control risks.
- Document possible risks in quote approval flows.
- Document safe testing boundaries.

## Security Report Format

```markdown
# Security Finding

## Area Reviewed

## Risk Level
Low / Medium / High

## Finding

## Why It Matters

## Recommended Fix

## Evidence

## Notes
```

## Rules

- Do not test production systems.
- Do not attack third-party systems.
- Do not attempt password guessing.
- Do not access data you were not given permission to access.
- Report risks clearly and professionally.
