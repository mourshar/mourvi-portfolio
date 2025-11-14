# Portfolio Sync Documentation
Last Updated: November 13, 2024

## Project Overview
- **Live Site**: https://mourvi-portfolio.vercel.app
- **GitHub Repository**: https://github.com/mourshar/mourvi-portfolio
- **Local Path**: `/Users/mourvi/Desktop/portfolionew`
- **GitHub User**: mourshar

## Current Status
✅ Portfolio website successfully deployed on Vercel
✅ GitHub repository created and connected
✅ Automatic deployment enabled (pushes to GitHub trigger Vercel redeploy)

## Site Structure

### Main Landing Page (index.html)
- **Title**: Creative and AI Content Strategy Lead
- **Tagline**: Meta Superintelligence Labs
- **Styling**: Uses `styles-main.css` (from alt folder)
- **Profile Image**: `images/cover/26230184-10102295368335862-144264102828286482-n.jpg`
- **Features**:
  - Hero section with profile
  - About section with bio
  - Experience logos (Meta, Sesame, IBM, Byju's, Harvard)
  - Selected Work section with project cards
  - Contact section

### Project Pages
All project pages use `styles.css` for consistent styling:
- `meta.html` - Meta's AI Character Products
- `fairside-stories.html` - Fairside Stories
- `ibm-watson-sesame.html` - IBM Watson & Sesame Street
- `disney-imagicademy.html` - Disney Imagicademy
- `disney-byjus-early-learn.html` - Disney Byju's Early Learn
- `radiophone.html` - Sesame Street Radiophone
- `learn-to-read.html` - Learn to Read, Read to Learn
- `first8studios.html` - Early Math with Gracie & Friends
- `afterschool.html` - Sesame Street Afterschool STEM

### Important Folders
- `alt/` - Contains backup of original landing page
- `alt/Meta images/` - Meta project images (note: capital 'M' for case-sensitive servers)
- `images/` - All project images organized by project
- `images/logos/` - Company and university logos

## Key Technical Details

### Styling Setup
- **Main page**: `styles-main.css` (modern landing page design)
- **Project pages**: `styles.css` (original project page design)
- This separation ensures proper styling for both page types

### Image Path Considerations
- Folder "Meta images" has a space - URLs must be encoded as `Meta%20images`
- Case sensitivity matters on web servers (Meta not meta)
- All image paths are relative from root

### Navigation Structure
- All project pages link back to `index.html#work`
- Navigation includes: About, Work, Contact, LinkedIn, Blog (Medium)
- Anchor links: #about, #work, #contact

## Recent Changes (November 13, 2024)

1. **Structure Fix**:
   - Moved alt/index.html to root as main landing page
   - Separated styles for main vs project pages

2. **Content Updates**:
   - Title: "Creative and AI Content Strategy Lead"
   - Tagline: "Meta Superintelligence Labs"
   - Harvard logo scaled 15% larger
   - Removed em dashes, replaced with regular dashes

3. **Technical Fixes**:
   - URL-encoded spaces in "Meta images" folder paths
   - Fixed case sensitivity (meta → Meta)
   - Updated all navigation links to point to root

## Git Configuration
```bash
git config --global user.name "mourvi"
git config --global user.email "mourvi@gmail.com"
```

## Deployment Details
- **Platform**: Vercel
- **Auto-deploy**: Enabled (triggers on push to main branch)
- **Framework**: None (vanilla HTML/CSS)
- **Root Directory**: /
- **No build step required**

## Common Commands
```bash
# Check status
git status

# Add all changes
git add -A

# Commit with message
git commit -m "Your message"

# Push to GitHub (triggers Vercel deploy)
git push

# Open local preview
open file:///Users/mourvi/Desktop/portfolionew/index.html
```

## Files to Never Delete
- `.gitignore` - Prevents unnecessary files from being tracked
- `styles.css` - Required for project pages
- `styles-main.css` - Required for main landing page
- All images in `images/` folder

## Potential Future Tasks
- [ ] Add custom domain if available
- [ ] Optimize images for faster loading
- [ ] Add meta tags for SEO
- [ ] Consider adding favicon
- [ ] Add Google Analytics if needed

## Session Resume Checklist
When continuing work:
1. Navigate to: `cd /Users/mourvi/Desktop/portfolionew`
2. Check git status: `git status`
3. Pull latest changes: `git pull`
4. Make changes as needed
5. Test locally before pushing
6. Commit and push when ready

## Important Notes
- Always test locally before pushing
- Case sensitivity matters on web servers
- URL-encode spaces in folder/file names
- Vercel auto-deploys take ~1-2 minutes
- GitHub CLI is authenticated as 'mourshar'

## Support Links
- [Vercel Dashboard](https://vercel.com/dashboard)
- [GitHub Repository](https://github.com/mourshar/mourvi-portfolio)
- [Live Site](https://mourvi-portfolio.vercel.app)

---
*This document was created to maintain continuity across sessions. Update as needed.*