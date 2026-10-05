# Batch 15 Production Fix 02

## Reason
Production Fix 01 exposed an XML parser error when Mammoth attempted to render
TIB_SAP_Controls_Foundation_Manual_Part1.docx.

## Correction
- DOCX rendering now uses docx-preview as the primary browser renderer.
- Mammoth remains a secondary fallback.
- Raw XML/parser diagnostics are no longer shown as the normal trainee experience.
- Back to Course and Download Original remain available.
- The trainee remains at the same course stage after closing the viewer.

## Important
If both independent DOCX renderers reject a specific file, that indicates the source
DOCX contains XML/content that browser renderers cannot safely process. The UI then
gives a clean Download Original option rather than exposing a technical parser error.

This remains Batch 15 production defect correction; it is not Batch 16.
