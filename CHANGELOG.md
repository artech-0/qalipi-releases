# Changelog

## 0.0.3-alpha (2026-11-10)

Reading comfort, comics and search. Still an alpha with a debug key.

- Text settings (Aa in the book's top bar): font (Literata, Source Serif 4, Atkinson Hyperlegible, Inter, OpenDyslexic or the book's own), size, line height, margins, alignment, publisher styles, paged or scroll. "This book only" keeps a look for one book. Changes apply live.
- Page turns: a 3x3 tap grid (right side forward, left side back, middle menu), Volume Down for next and Volume Up for previous while the bar is hidden, and an end-of-book card that marks the book finished, with Undo.
- Settings (Library, More, Settings): Controls lets you set what each tap zone does for books and for PDFs and comics, pick a layout (Thirds, L-shape, Kindle, Edge) and set the volume keys. Display sets how long the screen stays on and the orientation.
- Reading comfort: drag along the left edge to change brightness (saved for each theme, with a button to go back to the system brightness), keep the screen on for 5 min, 15 min or always, and cycle Auto, Portrait and Landscape from the bar.
- Library search: find books by title, author or series as you type, ignoring case and accents.
- In-book search for EPUB: matches appear as they are found, with the chapter and the words around them. Tap one to see it marked in the page, then step through matches.
- Bookmarks for books, PDFs and comics: a ribbon marks the page, a Bookmarks tab lists them, swipe to delete (with Undo), long-press to rename.
- Comics: right-to-left reading for manga (set by ComicInfo, a default in Controls, or per comic), fit modes (screen, width, height, original), a page background (black, white, grey or auto from the page margins), a warm filter, and a page thumbnail grid.
- CBR (RAR 4 and 5) and CB7 comics open, as well as CBZ. Files are recognised by what is inside, not their name.
- CBZ comics from folders get their first-page cover again on phones where the 0.0.2-alpha scan failed with "Can't be opened".
- The database is now frozen: from this version on, updates keep your data.

Known limitations:

- Installing over 0.0.2-alpha needs the app's data cleared first (Android Settings, Apps, Qalipi, Storage, Clear data): the 0.0.2-alpha database cannot be upgraded.
- CBR and RAR5 comics, the end card, the Controls screen and the screen-on timer have only been tested by automated tests, not on a phone. Large PDFs (900 MB) were not timed.
- Password-protected PDFs and DRM-protected books cannot be opened.
- No highlights or notes, shelves, sync or backup yet. Buttons are text, not icons.
- This build is signed with a debug key.

Requires Android 8.0 (API 26) or newer.

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
