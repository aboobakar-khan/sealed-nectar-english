# Ar-Raheeq-Al-Makhtum — English export

Open **index.html** for the complete readable book with a clickable contents list.

- **book.txt**: the complete text, grouped by the app’s 48 chapters and 193 topics.
- **book.json**: nested chapter/topic data with exact raw HTML, app-normalized HTML, readable text, original IDs, reader titles, and TOC titles.
- **chapters/**: 48 numbered UTF-8 text files, one per chapter.
- **source.sqlite3**: byte-for-byte copy of the app’s bundled `assets/arm` book database.
- **manifest.json**: extraction source, hashes, validation, and file checksums.

## Fidelity and validation

The source is the English app `com.quranemajeedapp.org.seerah`, version 1.8 (version code 9), copied locally from the user-provided USB-connected phone on November 26, 2026. Its label is “Ar-Raheeq-Al-Makhtum”. No text from the earlier Urdu app was used.

SQLite integrity check: OK. Chapter IDs 1–48 and topic IDs 1–193 are complete. No blank topics, orphan topics, or missing topic headings were found. Every chapter’s stored topic count matches the exported count. The visible app chapter list was checked against the database.

Readable content follows the app’s verified `Topic.getContent()` preprocessing: remove the leading `<h3>` heading where the app removes it, replace backslash plus `&&` with an apostrophe, remove remaining backslashes, and render internal headings as bold text with line breaks. HTML lists and emphasis remain in the reading copy; plain text retains paragraph and list structure. Original raw content remains available separately.

Original wording and source defects are retained. Topic 25’s stored TOC title is truncated compared with its reader title; both fields are included in JSON. Chapter 21’s stored title is also truncated and is preserved exactly. Topic 126 refers to `images/seal.png`; that file is absent from the APK. The readable export preserves its alt text `[seal]` without inventing an image.

Completeness means all content contained in this installed app database, not an independent comparison with a publisher’s print edition. No outside edition was substituted, and no source spelling was silently corrected.

The export did not change the app’s database, settings, or original app package. The app was opened to verify its chapter display. Existing extraction files supplied by the user are handled separately and were not overwritten.
