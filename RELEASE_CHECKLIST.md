# TIB ILA — Batch 15 Release Checklist

## Build scope
Development scope is locked and ends at Batch 15.

## Completed application layers
- Course Player: SEE → LISTEN → OBSERVE → BUILD → COMPARE → CONNECT
- Supabase email/password authentication
- PM → Controls Lead entitlement check
- Enrollment-expiry enforcement
- Correct separation of enrollment course code and Academy app-course ID
- Remote progress + resume behavior
- Real Academy material retrieval
- Private signed material access
- Activity-to-material mapping
- Narration player + production-audio manifest + browser fallback
- Full-screen document viewer shell
- Secure trainee uploads
- Academy submission records
- Self-review persistence and completion
- Instructor status/score/comment display
- Responsive desktop/mobile behavior

## Production acceptance tests
1. Valid enrolled trainee signs in.
2. Non-enrolled trainee is blocked from the course.
3. Expired enrollment is blocked.
4. Course resumes at latest remotely saved activity.
5. Private trainee material opens only while authenticated/authorized.
6. Instructor-only material never appears in trainee material query.
7. Workbook upload succeeds to academy-submissions.
8. academy_submissions record is created for the signed-in user.
9. Another trainee cannot read another trainee's submission (verify RLS).
10. Self-review requires all configured questions.
11. Progress survives sign-out/sign-in.
12. Desktop and Android/mobile layouts remain usable.
13. Wide tables/files are not forced into narrow columns.
14. Sign out clears the authenticated course session.
15. Production audio uses signed private access when configured.

## Deployment
Intended Vercel project: tib-academy-interactive-learning

Deployment is NOT claimed by this package. Deploy only after the security items in SECURITY_REVIEW.md are reviewed.
