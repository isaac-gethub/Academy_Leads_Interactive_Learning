# Corvane Project Reference Integration

This production correction integrates the Corvane Energy Controls Project Metadata & Training Reference into the existing TIB Academy Interactive Learning app.

- Adds a persistent **Corvane Project Reference** button in the app header.
- Opens the reference inside the existing full-screen Excel viewer.
- Provides worksheet tabs for all metadata categories and the end-to-end Relationship Map.
- Keeps the original XLSX available through **Download Original**.
- Does not create a separate app, course, enrollment, or Supabase schema change.
- Does not alter BUILD IT, LEAD IT, OWN IT, progress, submissions, assessment, or enrollment logic.

The reference workbook is packaged at the deployment root as:
`corvane-reference.xlsx`
