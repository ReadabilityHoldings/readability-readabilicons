# Readabilicons - An Icon Font for Readability

### Using SCSS? Sure you are. Here's a module
[_readabilicons.scss](https://github.com/arc90/readability-readabilicons/blob/master/webfont/css/_readabilicons.scss)

### Don't forget to…
Base64 encode the .woff and .ttf versions of the font and update the
SCSS module when you add new glyphs. Here's an encoder: [http://www.opinionatedgeek.com/dotnet/tools/base64encode/](http://www.opinionatedgeek.com/dotnet/tools/base64encode/)

Also, keep an eye on the id for the .svg. Fontsquirrel, generally keeps it the same
but It might be different.

### Read and reference this article
http://blog.fogcreek.com/trello-uses-an-icon-font-and-so-can-you/

### Adding a new Glyph
- You'll need
  - Adobe Illustrator CS6+
  - [Glyphs](http://glyphsapp.com/) or [Glyphs Mini](http://glyphsapp.com/glyphs-mini/)

1. In readabilicons.ai create the new icon on a new layer. The size of the icon
should be similar to all other icons. Be sure the new icon is on its own layer
with a unique name. When the icon is feeling good in vector form, it's time to take it to Glyphs.
2. Copy the icon from Illustrator.
3. In Glyphs create a new glyph with the plus button at the bottom of the window.
4. Rename the glyph by clicking in where it says "newGlyph".
5. Name the glyph "uniE***". The unicode number should follow the sequence of the
others. If you're curious about the naming, take a look at the Fog Creek article.
6. Double click the new glyph to edit it. Paste the vector icon.
7. Position the icon on the Y axis. You'll have to eyeball this. You can switch
back to the all glyphs view. You just want to be vertically positioned similarly
to the others.
8. When you're done creating glyphs it's time to export.
9. File > Export - The settings should be in place. Export it to readabilicons-Regular.otf
10. Convert the .otf to the other needed formats using the Fontsquirrel settings below.
11. Replace the existing fonts in `/webfont/fonts` with the newly generated fonts.
12. Add the new icon(s) to the demo html page and css.
13. Did you add the new icon(s) to the demo html page and css? Do it!

#### Fontsquirrel settings
http://www.fontsquirrel.com/tools/webfont-generator

- Expert...
- Font formats: TrueType, WOFF, EOT Compressed, SVG
- TrueType Hinting: Keep existing
- Rendering: None checked
- Fix Missing Glyphs: None checked
- X-height Matching: None
- Protection: None checked
- Subsetting: Custom Subsetting...
  - Character Encoding: None checked
  - Character Type: None checked
  - Language: None checked
  - Unicode Tables: None checked
  - Single Characters: Blank
  - Unicode Ranges: E000-F8FF
- CSS: Doesn't matter, we don't use this
- OpenType Options: None checked
- Advanced Options:
  - Remove "-webfont" from Font Name Suffix
  - Em Square Value: 1920 (This might not be needed)
- Shortcuts: Check Remember... (for your sanity)
