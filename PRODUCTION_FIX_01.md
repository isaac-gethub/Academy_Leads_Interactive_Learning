# Batch 15 Production Fix 01

## Fixed
1. OBSERVE > SHOW ME now has an explicit **← Back to Course** control.
2. Closing/back returns to the exact course/activity/stage already on screen; it does not restart navigation.
3. DOCX files are fetched through the authenticated private signed URL and rendered directly inside TIB ILA with Mammoth.js.
4. The trainee no longer depends on Microsoft Office Online merely to read a Word training document.
5. **Download Original** is retained for the real DOCX/Office artifact.
6. Trainee-facing Batch 13 development/technical explanation was removed from the viewer.
7. DOCX tables receive full-width, horizontally scrollable treatment to reduce overlap on narrow screens.

## Unchanged
- PDF/image/text browser viewing.
- Private Supabase signed-URL access.
- Excel/original Office files remain downloadable for actual work.
- This is a Batch 15 production defect correction, not Batch 16.
