# Documents

## Lesko-Help-Brand-System-v0.1.pdf

The whole system as one document, 23 A4 pages, set in the brand's own fonts
(Anton + DM Sans, embedded from `fonts/`).

Sections: how to read it · the story · voice · vocabulary · the character ·
the wardrobe · colour · typography · objects · asset specs · status.

**Every section is marked settled or open.** Open sections are proposals, not
decisions — the colour pairings especially, which is the next thing to decide
because the rest of the visual system inherits it.

### Rebuilding

```bash
cd documents
python3 -c "from weasyprint import HTML; HTML('body.html').write_pdf('Lesko-Help-Brand-System-v0.1.pdf')"
```

Requires `weasyprint` (`pip install weasyprint`). Fonts are local in `fonts/`;
character images come from `../design/img/`.

## brand-system-page.html — readable in the browser

https://claude.ai/code/artifact/4fef338b-de8e-4110-b2b5-e78734b9264b

The same content as the PDF, as a page you can open without downloading. Set in the
brand's fonts from Google Fonts, character stills inlined as data URIs, sticky contents
index, light and dark themes.

Generated from `body.html` by the inline script in the commit that added it — rebuild by
re-running that transform, or edit `brand-system-page.html` directly and republish the
same file path to keep the URL.
