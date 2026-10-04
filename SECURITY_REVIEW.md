# TIB ILA — Security Review at Batch 15

## Application decisions
- Uses a publishable browser key only; no service-role secret is embedded.
- Academy materials and submissions are private buckets.
- Course materials use time-limited signed URLs.
- Enrollment is checked before the trainee course is entered.
- Enrollment expiry is enforced.
- Instructor-only materials are excluded from trainee queries.
- Database-derived filename/status/reviewer-comment text is escaped before HTML display.
- User uploads are placed under the authenticated user's ID path.

## Supabase security advisor findings
The project-wide advisor currently reports issues outside and potentially adjacent to TIB ILA. These were NOT silently changed because they can affect other existing TIB applications.

High-priority review before production:
1. Four SECURITY DEFINER views reported by the advisor.
2. Eight SECURITY DEFINER functions reported callable by anon and/or authenticated roles.
3. Leaked-password protection is disabled.
4. Eight tables have RLS enabled but no policies; those tables become inaccessible through the Data API unless policies are intentionally added.
5. One function has a mutable search_path.

These findings require an owner-aware remediation pass because this Supabase project serves more than this one application. Batch 15 therefore records rather than destructively changes them.

## Required go-live verification
Explicitly test RLS for:
- enrollments
- academy_progress
- academy_materials
- academy_submissions
- storage.objects policies for academy-materials
- storage.objects policies for academy-submissions

A successful UI test alone is not sufficient; verify cross-user denial with two test trainee accounts.
