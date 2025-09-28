# Peter Tinti Website

Personal portfolio website built with Jekyll and hosted on GitHub Pages.

---

## **Adding Photography Essays**

### Quick Steps:
1. **Create a folder** in `photography/` named after your essay  
   Example: `photography/desert-journey/`

2. **Add your photos** to that folder  
   Just drag and drop `.jpg`, `.JPG`, or `.png` files

3. **Create `index.md`** in that folder with:
   ```markdown
   ---
   layout: project
   title: "desert journey"
   essay_title: "desert journey"
   order: 5
   featured_image: "best-photo.jpg"
   ---
   
   Optional: Add text here describing the essay
   ```

### Settings Explained:
- **title**: Essay name (used for page title)
- **essay_title**: Essay name (shown on photography page)
- **order**: Display position (1 = first, 2 = second, etc.)
- **featured_image**: Thumbnail photo filename for main gallery

### Photo Tips:
- Photos automatically display in a 2-column grid
- Click any photo to open full-screen slideshow
- Use arrow keys or click to navigate between photos

---

## **Adding Blog Posts**

### Quick Steps:
1. **Create a file** in `_posts/` folder  
   Name format: `2024-01-15-my-post-title.md`

2. **Add this header** to your file:
   ```markdown
   ---
   layout: post
   title: "My Amazing Post Title"
   date: 2024-01-15
   author: Peter Tinti
   description: "A short summary of the post"
   tags: [photography, travel, nature]
   featured_image: "/photography/nature/sunset.jpg"
   ---
   
   Write your post content here...
   ```

3. **Write your content** using:
   - `**bold text**` for bold
   - `*italic text*` for italics  
   - `![Description](image-path)` for images
   - `> Quote text` for blockquotes

### Adding Images to Posts:

**Option 1: Use existing photos**
```markdown
![Desert sunset](/photography/desert-journey/sunset.jpg)
```

**Option 2: Add new blog images**
1. Save to `assets/images/blog/`
2. Reference as: `![Description](/assets/images/blog/image.jpg)`

### Image Features:
- Click any image to view full-screen
- Featured image appears at top of post
- Content images display at 60% width (90% on mobile)

---

## **Editing Main Pages**

| Page | File to Edit | Purpose |
|------|-------------|---------|
| Homepage | `index.markdown` | About text |
| Contact | `contact.markdown` | Email address |
| Photography | Don't edit | Auto-generated from essays |
| Blog | Don't edit | Auto-generated from posts |

---

## **Publishing Changes**

1. **Save your files** in the correct folders
2. **Commit changes** to GitHub
3. **Wait 2-3 minutes** for site to update
4. Visit `petertinti.github.io` to see changes

---

## **Folder Structure**

```
petertinti.github.io/
├── _posts/              ← Blog posts go here
├── photography/         ← Photo essays go here
│   ├── essay-name/
│   │   ├── index.md
│   │   └── photos.jpg
├── assets/
│   └── images/
│       └── blog/       ← Blog-specific images
├── index.markdown      ← Homepage content
└── contact.markdown    ← Contact info
```

---

## **Don't Edit These**

- `_config.yml` - Site settings
- `_layouts/` - Page templates
- `_includes/` - Site components  
- `assets/css/` - Styling
- `_site/` - Auto-generated files

---

## **Local Development**

To preview changes before publishing:
```bash
bundle exec jekyll serve --port 4000
```
Then visit: `http://localhost:4000`