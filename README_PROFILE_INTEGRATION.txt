TIB CONTROLS 360 — INTERVIEW PROFILE INTEGRATION
Implemented:
- Each completed gated interview is saved to interview_coaching_attempts.
- Full question-level score/answer/coaching note snapshot is retained in JSON.
- Average and READY / READY WITH COACHING / NOT YET READY are retained.
- Per-area averages are retained.
- Database trigger writes each tested area's rounded 0-4 result to the existing c360_scores table with source='interview_coaching'.
- Staff can review attempt history at interview-coaching-history.html.
- Existing separate coaching entitlement remains mandatory.

Acceptance:
1. Enroll test trainee in coaching.
2. Complete a 5-question interview.
3. Confirm result page says Saved.
4. Open history page as staff and confirm attempt appears.
5. Confirm Controls 360 Profile reflects new interview_coaching score source.
6. Repeat interview and confirm a second attempt is retained, not overwritten.
