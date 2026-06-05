# Images

Replace the `*-placeholder.svg` files here with your own images, then update the
paths in the relevant files.

| Placeholder                    | Used by                              | Replace with                         | Suggested size |
|--------------------------------|--------------------------------------|--------------------------------------|----------------|
| `profile-placeholder.svg`      | Home hero (`index.html`)             | your headshot                        | 600×600 (square) |
| `pub-placeholder.svg`          | `_data/publications.yml`             | a figure/teaser from each paper      | 1200×675 (16:9) |
| `book-cover-placeholder.svg`   | `_data/outreach.yml` (book)          | your book cover                      | 600×800 (3:4) |
| `talk-placeholder.svg`         | `_data/outreach.yml` (talk)          | video/talk thumbnail                 | 1200×675 (16:9) |
| `post-placeholder.svg`         | `_posts/*.md` front matter `image:`  | a header image per post              | 1200×675 (16:9) |

Tips
- Card thumbnails look best at a 16:9 ratio; book covers use a 3:4 ratio
  (the `.card-grid.covers` style handles that automatically).
- Keep files small (compress to < ~300 KB) so pages load fast.
- You can also point any `image:` field at a full URL instead of a local file.
