# CLAUDE.md

## Project Overview
Merry Grantmas is a festive single-page static website that showcases the Grant family's holiday songs and playlists. The site features the latest song "Ting-a-ling" with an embedded audio player, links to streaming platforms, and a songbook of past holiday originals.

## Tech Stack
- **Pure HTML/CSS/JavaScript** - No frameworks or build tools
- **Static site** - Hosted with GitHub Pages (custom domain via CNAME)
- **Vanilla JavaScript** - Minimal JS for audio player controls
- **Google Analytics** - Event tracking for outbound link clicks

## Project Structure
```
/
├── index.html          # Single-page application with embedded styles and scripts
├── CNAME              # Custom domain configuration
├── assets/
│   ├── audio/         # Audio files (e.g., ting-a-ling.mp3)
│   └── img/           # Images (e.g., grantmas.jpg, favicon.svg)
├── README.md          # Public-facing documentation
└── CLAUDE.md          # This file - AI assistant context
```

## Key Features
1. **Featured Track Player**: Custom play/pause button for the current year's song
2. **Past Years Songbook**: Scrollable list of previous Grant family holiday tracks
3. **Playlist Links**: Quick access to Bandcamp, Apple Music, TIDAL, and Spotify
4. **Festive Design**: Decorative lights, snow effects, ribbons, and family photo
5. **Analytics**: Google Analytics tracking for outbound playlist/song clicks

## Development Guidelines

### Local Development
Since this is a static site, you can:
1. **Direct file access**: Open `index.html` in a browser
2. **Local server** (recommended for audio):
   ```bash
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

### Code Style
- The entire site is self-contained in `index.html`
- CSS is embedded in `<style>` tags
- JavaScript is embedded in `<script>` tags
- Keep the single-file architecture for simplicity

### Analytics
- Outbound links are tracked using Google Analytics events
- Track clicks with `ga()` function calls
- Event format: `ga('send', 'event', 'outbound', 'click', url)`

### Making Changes
Common tasks:
1. **Update featured song**: Modify the audio player section and update `src` attribute
2. **Add past songs**: Add new entries to the songbook list
3. **Update playlists**: Modify the playlist buttons' `href` attributes
4. **Change styling**: Edit CSS in the `<style>` section
5. **Update photo**: Replace `assets/img/grantmas.jpg`

### Deployment
- Hosted on GitHub Pages
- Custom domain configured via CNAME file
- Changes pushed to main branch auto-deploy
- No build process required

## Git Workflow
- Main branch for production
- Feature branches prefixed with `claude/` for AI-assisted development
- Commit messages should be descriptive and clear
- Always test audio playback before pushing

## Important Notes
- Keep the site lightweight (no frameworks needed)
- Maintain accessibility labels for audio controls
- Test across browsers (especially audio playback)
- Preserve festive theme and family-friendly content
- Respect copyright for all music links

## Testing Checklist
Before committing changes:
- [ ] Audio player plays/pauses correctly
- [ ] All outbound links work
- [ ] Festive decorations render properly
- [ ] Site is responsive on mobile
- [ ] Analytics events fire correctly
- [ ] No console errors

## Future Considerations
- Consider adding more songs as they're released
- May want to archive older years into separate pages if list grows
- Could add more interactive features (e.g., lyrics display)
- Mobile optimization for playlist buttons
