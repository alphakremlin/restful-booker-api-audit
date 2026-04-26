# Restful Booker — REST API Audit Report

**Type:** REST API Testing
**Site:** restful-booker.herokuapp.com
**Auditor:** Ramone Scott — QA Engineer

## Summary
Full REST API audit covering all CRUD endpoints, authentication flows, edge cases, input validation, and security headers. Live curl testing against all endpoints.

## Findings
- 7 bugs documented with severity ratings
- 2 critical bugs (server crashes on bad input)
- API quality score: 5/10

## Key Bugs Found
- POST /auth returns 200 OK on failed login (should be 401 Unauthorized)
- POST /booking returns 500 Internal Server Error on missing required fields (should be 400)
- GET /booking?checkin=not-a-date crashes the server with 500
- POST /booking accepts negative totalprice values (-999) with no validation
- POST /booking returns 200 instead of 201 Created on resource creation
- X-Powered-By header exposes Express.js version to attackers

## Endpoints Tested
GET /booking, GET /booking/:id, POST /booking, PUT /booking/:id, PATCH /booking/:id, DELETE /booking/:id, POST /auth

---
*Ramone Scott · QA Engineer · Jamaica · Available for freelance audits*
