# Archive of the old `zizocreates/zizocreates.github.io` repository

Made on 13 November 2026, right before the old repository was deleted, so nothing from it is lost.

- **`old-zizocreates.github.io-full-history.bundle`:** the entire old repository, all 42 commits, both branches.
  - **Branches:** `main-archive` is the old "coming soon" page. `portfolio-v1-archive` is the site at the moment it moved.
  - **Checked:** a test restore had all 42 commits, and the tip matched exactly.
  - **Also inside:** every earlier version of the site, including the retired all-in-one page and its generator, and the personal notes files that were taken off the public repository.
  - **To restore:** `git clone -b portfolio-v1-archive old-zizocreates.github.io-full-history.bundle restored-site`
- **`old-coming-soon-index.html`:** the "coming soon" page that used to be live at zizocreates.github.io, as a plain file.

**Checks before deleting:**
- **The site moved completely.** Every file in the old `portfolio-v1` exists in `zizocreates/portfolio`. That was checked twice: a file-by-file diff, then content hashes and byte checksums.
- **Nothing is missing.** 16 files are identical. 7 differ only by that day's intended edits: the new hosting notes, the share-preview links now pointing to zizocreates.pages.dev, and change-log entries.
