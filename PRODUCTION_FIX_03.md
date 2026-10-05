# Batch 15 Production Fix 03

The source DOCX is malformed enough that both normal browser DOCX renderers fail.

Fix 03 adds a third, independent Reading Mode fallback:
- unpacks the DOCX with JSZip;
- reads word/document.xml as plain text rather than parsing it as XML;
- reconstructs paragraphs and table rows/cells safely;
- preserves wide tables with horizontal scrolling;
- therefore avoids the invalid XML tagName failure entirely.

Normal DOCX rendering remains first choice. Reading Mode is used only when both
full-layout renderers reject the source document.

Back to Course, Download Original, Full Screen and exact course-position return remain.

This is a Batch 15 production correction, not Batch 16.
