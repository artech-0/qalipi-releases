# Changelog

## 0.0.5-beta (2026-11-11)

First beta, and the first build signed with a real release key. The app now installs as `com.rouge.expero`.

**Read this before installing:** this build has a new package name, so Android treats it as a different app from 0.0.4-alpha and earlier. It installs next to the old one and does not update it. Your library, reading positions and bookmarks do not carry over: add your book folders again in Settings, Folders. When you are happy with it, uninstall the old "Qalipi" from Android Settings, Apps. Updates from this version on keep your data, because every release will be signed with the same key.

- Fix: typing a page number in the in-book search crashed the reader. It now offers "Go to page".
- Fix: a "Back to ..." button no longer appears every time a book opens or the screen rotates. It only appears after you jump somewhere (a link, a search result, Contents, Go to page, a bookmark, the slider).
- Page numbers are now one kind per book. A book shows the publisher's printed page numbers only when its page list covers almost all of the book; otherwise the whole book shows estimated pages. This fixes a bundle whose page list covered only its last part, where "Go to page 55" jumped to the end. The bar shows only the percent for a moment while the page numbers are worked out, then the page number appears.
- Settings, Display, "Page numbers in books" now has three choices: Printed (the default, with estimates where a book has no full page list), Estimated, and Off. If you had turned the old switch off, it stays off.

Known limitations:

- Tested on one phone, with EPUB and PDF: search, Go to page for EPUB and PDF, and landscape. Not tried on a phone: comics, the new page-number choices, the stray "Back to" fix on every book type, removal and Storage.
- Dark theme inverts the colours of PDFs, which makes colour comics saved as PDF look wrong. Turn off "PDF colours" in the reader bar, or use Basic theme.
- A printed page's place inside a chapter is worked out from the text, so it can be a little early or late.
- Password-protected PDFs and DRM-protected books cannot be opened.
- No highlights or notes, shelves, sync or backup yet. Buttons are mostly text, not icons.
- Not on Google Play. GitHub is the place to get Qalipi.

Requires Android 8.0 (API 26) or newer.

## 0.0.4-alpha (2026-11-11)

Storage, page numbers and fixes. Still an alpha with a debug key. Updating from 0.0.3-alpha keeps your data.

- Remove books: long-press a book in the library. "Remove from Qalipi" frees everything Qalipi stored for it: a book you opened from another app is deleted along with Qalipi's copy; a book from one of your folders is hidden and its temporary copies are cleared, and the file stays in the folder. Hidden books are listed in Settings, Folders, Hidden books, with Unhide. Opening the same file again also brings it back.
- "Remove and delete from device" for books in your folders deletes the file itself, after a second confirmation. The first time, Android asks you to pick the same folder again to allow changes to it. If a book has several copies and some cannot be deleted, the book is hidden and you are told how many remain.
- File sizes: the list view shows each book's size next to its author, and a new "Size, largest first" sort puts the heaviest books on top.
- Settings, Storage: what Qalipi keeps on your phone (books opened from other apps, and temporary copies), Clear cache, the ten largest books with Remove, and "Delete imported copies of finished books".
- Page numbers for EPUB: a book shows "p. 214 / 612 est. · 37 %", counted from the book's length (an estimate that does not change with text size). A book that carries the publisher's own page list shows the printed page instead, such as "p. 214" or "p. xiv". Settings, Display, "Page numbers in books" turns this off.
- Go to page: a bottom-bar button for EPUB, PDF and comics. Type a page number, or the printed page for books with a page list. Typing a page number in the in-book search also offers the jump. A "Back to" chip returns you.
- Bookmarks: each row has a small delete icon, and swiping toward it also deletes, both with Undo. Neither moves your place in the book.
- Fix: choosing landscape in the reader no longer turns back to portrait when the phone rotates. The same fix keeps a brightness you set.
- The reading bar scrolls sideways when its buttons do not fit.

Known limitations:

- Most of this release has only been tested by automated tests, not on a phone: removal and delete from device, the Storage screen, page numbers and printed pages (no real publisher EPUB with a page list was tried), Go to page, and the landscape fix.
- A printed page's place inside a chapter is worked out from the text, so it can be a little early or late.
- Password-protected PDFs and DRM-protected books cannot be opened.
- No highlights or notes, shelves, sync or backup yet. Buttons are mostly text, not icons.
- This build is signed with a debug key.

Requires Android 8.0 (API 26) or newer.

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
