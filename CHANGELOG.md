# Changelog

## 0.0.2-alpha (2026-11-10)

Folder library. Still an alpha with a debug key.

- Choose the folders your books live in, once. Qalipi finds EPUB, PDF and CBZ files in them, including subfolders, and the library fills in by itself. It rescans when the app starts (if the last scan is over 15 minutes old) and when you pull down to refresh. Your files are never changed.
- First launch shows a welcome screen that asks for a folder. A new Folders screen (Library, More, Folders) adds, re-grants and removes folders. Removing a folder hides its books but keeps your reading positions.
- Covers, titles, authors and series are read from the books themselves: EPUB metadata and cover, PDF title and first page, CBZ ComicInfo and first page. Books without a cover get a generated one.
- The library is now a cover grid, with a list view, filter chips (All, Reading, Unread, Finished, Comics, PDFs), six sort orders and a "Continue reading" row. Your choices are remembered.
- Big books open faster the second time. A book from a folder is copied into the app once, with a progress readout, and the last 5 (up to 3 GB) are kept for instant reopening.
- The scan reads files in place and never reads a file that has not changed, so rescanning a large library is quick.

Known limitations:

- Installing over 0.0.1-alpha needs the app's data cleared first: the database changed and there is no upgrade path yet. Reading positions and imported books from that build are lost.
- No library search screen, shelves, typography settings, tap-zone settings or manga right-to-left mode yet. CBR comics and TXT, FB2 and MOBI books are not supported.
- A folder you lose access to keeps its books visible; they fail to open with an error.
- CBR files are listed by file name only, with no cover, and cannot be opened yet.

Requires Android 8.0 (API 26) or newer.

## 0.0.1-alpha

First alpha. Expect rough edges.

- Read EPUB, PDF and CBZ (comic) files. Import from the file picker or with "Open with Qalipi".
- Reading position is saved and restored for every book.
- Tap the centre of a page for the reading bar: progress slider, Contents, and a "Back to" chip after a jump.
- Basic, Night (warm, low glare) and Dark themes. The button in the reading bar cycles them; with no choice the app follows the system light or dark setting.
- PDFs follow the theme too. For PDFs with photos, "PDF colours: Original" in the reading bar keeps the pages in their own colours.

Known limitations:

- Password-protected PDFs and DRM-protected books cannot be opened.
- CBR, CB7, image folders, manga right-to-left mode and a reading-settings screen are not available yet.
- The library is a plain list; there are no folders, shelves or search.
- Comics always use a black background.
- This build is signed with a debug key. It installs next to nothing else but cannot be updated by a differently signed build.

Requires Android 8.0 (API 26) or newer.
