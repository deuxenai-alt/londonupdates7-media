# CLAUDE.md — London Updates Media Repository

## Project Overview

**London Updates** is a personal media content repository for scheduling and publishing social media posts about London lifestyle, facts, and culture. The repository contains a collection of curated slide-based posts featuring images and promotional content related to various London topics.

**Primary Use**: Personal social media publishing tool for the owner's own connected accounts (e.g., LinkedIn, social media platforms).

**Contact**: deuxen.ai@gmail.com

---

## Repository Structure

```
londonupdates7-media/
├── .git/                          # Git repository
├── CLAUDE.md                      # This file - AI assistant documentation
├── PRIVACY.md                     # Privacy policy for data handling
├── TERMS.md                       # Terms of service
└── posts/                         # Content posts directory (127 collections)
    ├── barbican1/
    ├── fact1002530julyretur/
    ├── fact101kitkatf1milkc/
    ├── ... (121 more post directories)
    └── [post-name]/
        ├── slide1.jpg
        ├── slide2.jpg
        ├── slide3.jpg
        └── slide4.jpg              # Typically 3-4 slides per post
```

### Directory Organization

- **`/posts`**: Contains all post collections, each in its own directory
  - **Directory Naming**: Post names are derived from content topics (e.g., `barbican1`, `fact101kitkatf1milkc`)
  - **Naming Convention**: Limited to ~30 characters to fit filesystem constraints; truncated descriptive names
  - **Content**: Each post directory contains 3-4 JPG slide images (96-500KB each)
  - **Total Posts**: 127 collections as of last update

---

## Key Information & Policies

### Privacy & Compliance

- **Data Collection**: None - this is a personal publishing tool only
- **Account Access**: Only authorized personal accounts via official platform APIs
- **Authorization Model**: Owner-only access; can be revoked from platform settings
- **Third-party Data**: No collection, storage, or sharing of third-party personal data
- **Tracking/Analytics**: None

See `PRIVACY.md` and `TERMS.md` for full legal documentation.

---

## Development Workflows

### Git Workflow

1. **Branches**:
   - `main`: Stable release branch
   - `claude/*`: Feature/documentation branches for AI-assisted changes

2. **Commit Messages**:
   - Format: `Add [post-name] post` or descriptive change summary
   - Example: `Add fact109mcguiganblack post`
   - Keep messages concise and descriptive

3. **Pushing Changes**:
   ```bash
   git add .
   git commit -m "Add [post-name] post"
   git push -u origin claude/claude-md-docs-xibcaz
   ```

### Adding New Posts

1. Create new directory under `/posts` with descriptive name (max ~30 chars)
2. Add slide images (JPG format, typically 3-4 per post)
3. Commit with message: `Add [post-name] post`
4. Push to branch and create/merge pull request

### Working with Large Repositories

- The repository contains 127+ posts with multiple image files per post
- Use targeted git commands rather than broad operations
- Example: `git log --oneline` for quick history review
- When exploring: use `find` and `ls` for directory inspection rather than full clones

---

## Common Tasks & Patterns

### For AI Assistants

#### Documentation Tasks
- **Updating CLAUDE.md**: Follow the structure and style of this file
- **Checking Repository State**: Use `git status` and `git log --oneline -10`
- **Validating Changes**: Run `git status` before committing to ensure expected files

#### Content Management
- **Listing Posts**: `find /home/user/londonupdates7-media/posts -mindepth 1 -maxdepth 1 -type d`
- **Counting Posts**: `find /home/user/londonupdates7-media/posts -mindepth 1 -maxdepth 1 -type d | wc -l`
- **Inspecting Post Content**: `ls -la /home/user/londonupdates7-media/posts/[post-name]/`

#### Quality Assurance
- Verify post directory structure (should contain JPG files)
- Check commit history for consistency: `git log --oneline | head -20`
- Validate no uncommitted changes before major operations: `git status`

---

## Technical Details

### File Format

- **Images**: JPG format (JPEG compression)
- **Typical Size**: 100-500KB per slide image
- **Typical Slides per Post**: 3-4 images
- **Total Repository Size**: ~400MB+ (primarily image data)

### Repository Metadata

- **Remote**: http://local_proxy@127.0.0.1:41729/git/deuxenai-alt/londonupdates7-media
- **Default Branch**: `main`
- **Working Branch**: `claude/claude-md-docs-xibcaz`

---

## Conventions for AI Assistants

### When Adding/Modifying Posts

1. **Preserve Structure**: Always maintain the `/posts/[name]/slideN.jpg` pattern
2. **Naming Consistency**: Use descriptive, filesystem-safe directory names
3. **Image Quality**: Maintain existing JPEG quality standards
4. **Metadata**: No separate metadata files needed; structure is self-documenting

### When Updating Documentation

1. **Keep This File Updated**: Reflect major repo changes in CLAUDE.md
2. **Follow Markdown Style**: Use heading hierarchy (H1→H2→H3) consistently
3. **Code Blocks**: Use triple backticks with `bash` language identifier
4. **Clarity**: Assume readers may be unfamiliar with this specific project

### Git Practices

1. **Atomic Commits**: One logical change per commit
2. **Always Verify**: Run `git status` before `git add` or `git commit`
3. **Branch Safety**: Never force-push; coordinate with team if rebasing needed
4. **Push Frequently**: Push to origin regularly to avoid work loss

---

## Common Scenarios

### Adding a New London Post

```bash
# 1. Create directory
mkdir /home/user/londonupdates7-media/posts/fact[number][topic]

# 2. Add slide images
# Copy slide1.jpg, slide2.jpg, slide3.jpg, slide4.jpg to the directory

# 3. Verify structure
ls -la /home/user/londonupdates7-media/posts/fact[number][topic]/

# 4. Commit and push
git add /home/user/londonupdates7-media/posts/fact[number][topic]/
git commit -m "Add fact[number][topic] post"
git push -u origin claude/claude-md-docs-xibcaz
```

### Reviewing Recent Changes

```bash
# See last 10 commits
git log --oneline -10

# See full diff of last commit
git show HEAD

# Check current status
git status
```

### Checking Repository Size

```bash
# Total repository size
du -sh /home/user/londonupdates7-media

# Largest posts by size
du -sh /home/user/londonupdates7-media/posts/*/ | sort -rh | head -10
```

---

## Integration & Publishing

This repository is designed to integrate with:

- **LinkedIn API**: For scheduling posts to company pages
- **Social Media Platforms**: Via official APIs with owner authorization
- **Content Management**: Personal publishing workflow

All API integrations are handled outside this repository (likely in a separate application).

---

## Support & Maintenance

### For Troubleshooting

- Check `/PRIVACY.md` and `/TERMS.md` for policy clarifications
- Review git log for recent changes: `git log --oneline -20`
- Validate image integrity after transfers: check file sizes match expected ranges

### Maintenance Notes

- Repository is primarily image-based; focus on structure maintenance
- No automated tests or CI/CD pipelines currently in place
- Manual review recommended for new posts before publishing
- Archive old/deprecated posts in separate directory if needed (not currently practiced)

---

## Last Updated

- **Date**: 2026-07-22
- **Branch**: `claude/claude-md-docs-xibcaz`
- **Total Posts**: 127 collections
- **Documentation Level**: Comprehensive

---

## Quick Reference

| Aspect | Details |
|--------|---------|
| **Owner** | Personal content creator (deuxen.ai@gmail.com) |
| **Primary Content** | London lifestyle facts and cultural posts |
| **Media Format** | JPEG slide images (3-4 per post) |
| **Repository Type** | Media asset storage + git-based versioning |
| **Access Level** | Personal/Private |
| **Update Frequency** | Regular (new posts added periodically) |
| **Branch for Development** | `claude/claude-md-docs-xibcaz` |
| **Merge Target** | `main` |

